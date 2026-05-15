# Detecção de Fraudes com Machine Learning

![Python](https://img.shields.io/badge/Python-3.11-blue)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange)
![Status](https://img.shields.io/badge/status-finalizado-green)

---

# Visão Geral

Este projeto aplica técnicas de Machine Learning para detecção de fraudes em transações financeiras utilizando modelos de classificação supervisionada em um dataset altamente desbalanceado.

O principal objetivo é identificar transações fraudulentas com alta taxa de recall, reduzindo falsos negativos e melhorando a capacidade de prevenção de perdas financeiras.

O projeto foi desenvolvido com foco em:

- Pré-processamento de dados
- Tratamento de classes desbalanceadas
- Engenharia de atributos
- Comparação de modelos de Machine Learning
- Avaliação utilizando métricas apropriadas para fraude
- Explicabilidade do modelo

---

# Problema de Negócio

Fraudes financeiras representam um dos maiores desafios para instituições bancárias e sistemas de pagamento.

O principal desafio técnico deste problema é o forte desbalanceamento entre transações legítimas e fraudulentas, exigindo técnicas específicas para evitar que o modelo aprenda apenas a classe majoritária.

---

# Tecnologias Utilizadas

- Python
- Pandas
- NumPy
- Scikit-Learn
- XGBoost
- Matplotlib
- SHAP
- Imbalanced-Learn (SMOTE)

---

# Dataset

O dataset contém transações financeiras anonimizadas classificadas como fraudulentas ou legítimas.

Principais características:

- Classes altamente desbalanceadas
- Variáveis numéricas transformadas
- Cenário real de detecção de fraudes

---

# Pipeline do Projeto

## 1. Coleta de Dados

O dataset foi carregado a partir de uma fonte pública contendo transações financeiras anonimizadas.

---

## 2. Análise Exploratória de Dados (EDA)

Foi realizada análise exploratória para compreender:

- Distribuição das classes
- Nível de desbalanceamento
- Comportamento das variáveis
- Distribuição dos valores de transações

### Principais observações

- Forte predominância da classe não fraudulenta
- Necessidade de balanceamento
- Alta dispersão na variável `Amount`

---

# Engenharia de Features

## Transformação Logarítmica

Aplicada na variável `Amount` para reduzir assimetria e melhorar a distribuição dos dados.

## Padronização

Foi utilizado `StandardScaler` para normalização das variáveis numéricas.

---

# Divisão dos Dados

Os dados foram divididos em:

- Treino
- Teste

Utilizando `train_test_split`.

---

# Modelos de Machine Learning

## Logistic Regression

Modelo baseline utilizado para comparação inicial.

### Vantagens

- Simples
- Rápido
- Interpretável

---

## Random Forest

Modelo baseado em ensemble de árvores de decisão.

### Benefícios

- Melhor capacidade de generalização
- Redução de overfitting
- Melhor desempenho em dados complexos

---

## XGBoost

Modelo avançado baseado em Gradient Boosting.

### Destaques

- Alta performance em datasets tabulares
- Excelente desempenho em classificação desbalanceada
- Amplamente utilizado no mercado e em competições Kaggle

---

# Tratamento de Desbalanceamento

## Undersampling

Redução da classe majoritária.

## SMOTE (Synthetic Minority Oversampling Technique)

Geração sintética de exemplos da classe minoritária.

### Objetivo

Melhorar a capacidade do modelo em detectar fraudes.

---

# Métricas Utilizadas

## Classification Report

Avaliação baseada em:

- Precision
- Recall
- F1-Score

## ROC Curve

Utilizada para avaliar a capacidade de separação entre classes.

## Precision-Recall Curve

Especialmente relevante para datasets altamente desbalanceados.

---

# Ajuste de Threshold

Foi realizado ajuste manual do threshold de classificação para aumentar o recall do modelo.

Exemplo:

```python
threshold = 0.3
```

Essa abordagem aumenta a detecção de fraudes, mesmo ao custo de mais falsos positivos.

---

# Otimização de Hiperparâmetros

Foi utilizado `GridSearchCV` para busca das melhores combinações de parâmetros.

### Objetivos

- Melhorar desempenho
- Reduzir overfitting
- Otimizar configuração do modelo

---

# Explicabilidade do Modelo

A biblioteca SHAP foi utilizada para interpretar o impacto das variáveis nas previsões.

## Benefícios

- Transparência
- Interpretabilidade
- Apoio à tomada de decisão

---

# Resultados

## Principais ganhos obtidos

- Melhor capacidade de detecção de fraudes
- Comparação entre múltiplos modelos
- Uso de técnicas modernas de balanceamento
- Pipeline reproduzível
- Machine Learning explicável

---

# Melhorias Futuras

Possíveis evoluções do projeto:

- Deploy com FastAPI
- Dashboard com Streamlit
- Monitoramento de modelos
- Detecção de drift
- Integração com banco de dados
- Deploy em nuvem
- Pipeline MLOps

---

# Estrutura do Projeto

```text
Projeto_Deteccao_fraudes_transacoes.ipynb/
│
├── data/
│   └── creditcard.csv
│
├── notebooks/
│   └── DIO_Projeto_Deteccao_Fraudes_Transacoes.ipynb
│
├── models/
│   └── xgboost_model.pkl
│
├── images/
│   ├── roc_curve.png
│   ├── precision_recall.png
│   └── feature_importance.png
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

# Como Executar o Projeto

## Clonar o repositório

```bash
git clone https://github.com/tarsoa/Projeto_Deteccao_fraudes_transacoes.ipynb.git
```

---

## Criar ambiente virtual

```bash
python -m venv venv
```

---

## Ativar ambiente virtual

### Windows

```bash
venv\Scripts\activate
```

### Linux / Mac

```bash
source venv/bin/activate
```

---

## Instalar dependências

```bash
pip install -r requirements.txt
```

---

## Executar notebook

```bash
jupyter notebook
```

---

# Diferenciais Técnicos

- Uso de múltiplos modelos de Machine Learning
- Tratamento de datasets desbalanceados
- Engenharia de atributos
- Explicabilidade com SHAP
- Ajuste de threshold
- Otimização de hiperparâmetros
- Pipeline próximo de cenários reais de Data Science

---

# Repositório

GitHub:
https://github.com/tarsoa/Projeto_Deteccao_fraudes_transacoes.ipynb

---

# Descrição para LinkedIn

Projeto de Machine Learning voltado para detecção de fraudes financeiras utilizando técnicas de classificação supervisionada, balanceamento de dados com SMOTE, ajuste de threshold, otimização de hiperparâmetros e explicabilidade com SHAP. O projeto compara modelos como Logistic Regression, Random Forest e XGBoost utilizando métricas adequadas para datasets desbalanceados.

---

# Autor

Tarso de Azevedo

Formado em Administração de Empresas e Análise e Desenvolvimento de Sistemas em transição para Data Science e Machine Learning.

GitHub:
https://github.com/tarsoa/Projeto_Deteccao_fraudes_transacoes.ipynb
