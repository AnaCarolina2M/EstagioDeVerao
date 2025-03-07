# Análise de Séries Temporais com SARIMAX e XGBoost

Este repositório contém um projeto de análise de séries temporais, onde aplicamos **SARIMAX** e **XGBoost** para prever e modelar dados temporais. O projeto abrange todo o pipeline, desde a **exploração dos dados (EDA)**, **limpeza**, **pré-processamento**, até a aplicação dos algoritmos de modelagem.

## Sumário

1. [Objetivo do Projeto](#objetivo-do-projeto)
2. [Estrutura do Projeto](#estrutura-do-projeto)
3. [Requisitos](#requisitos)
4. [Como Rodar o Projeto](#como-rodar-o-projeto)
5. [Pipeline de Análise](#pipeline-de-análise)
   - [1. EDA - Análise Exploratória de Dados](#1-eda---análise-exploratória-de-dados)
   - [2. Limpeza e Pré-processamento dos Dados](#2-limpeza-e-pré-processamento-dos-dados)
   - [3. Modelagem com SARIMAX](#3-modelagem-com-sarimax)
   - [4. Modelagem com XGBoost](#4-modelagem-com-xgboost)
6. [Resultados e Métricas](#resultados-e-métricas)
7. [Considerações Finais](#considerações-finais)

## Objetivo do Projeto

O objetivo deste projeto é analisar e prever a Radiação Solar (KJ/m²) utilizando dois modelos diferentes: **SARIMAX** (Modelo Auto-regressivo Integrado de Médias Móveis com eXógenos) e **XGBoost**. A análise é realizada em um conjunto de dados temporal real, abrangendo todas as etapas de um pipeline de machine learning para análise de séries temporais, incluindo:

- **Exploração dos Dados (EDA)**
- **Limpeza e Pré-processamento**
- **Modelagem e Avaliação**
```

## Requisitos

Certifique-se de ter os seguintes pacotes instalados:

- **Python 3.x**
- **Jupyter Notebook** ou **JupyterLab**
- **pandas**
- **numpy**
- **matplotlib**
- **seaborn**
- **statsmodels** (para SARIMAX)
- **xgboost**
- **scikit-learn**
- **scipy**

Você pode instalar todas as dependências com:

```bash
pip install -r requirements.txt
```

4. Execute os notebooks na seguinte ordem:
   - **`EDA_radiacao.ipynb`**: Realize a análise exploratória de dados.
   - **`Data_Cleaning_final.ipynb`**: Aplique a limpeza e o pré-processamento.
   - **`Attribute_selection.ipynb`**: Escolha os melhores atributos.
    - **`Slicing_dataset.ipynb`**: Separa os dados para previsoes futuras.
    - **`Preparacao_dados_previsao_SARIMAX.ipynb`**: Preparar variáveis exógenas para previsao no SARIMAX.
   - **`Preparacao_dados_previsao_XG.ipynb`**: Preparar variáveis exógenas para previsao no XG.
    - **`XG_BOOST_FINAL.ipynb`**: Treinar os dados no modelo no XGBoost.
    - **`SW_SARIMAX_1.0.ipynb`**: Treinar os dados no modelo SARIMAX.
    - **`Previsao_final.ipynb`**: Prevê a quantidade de energia no painel solar.
    


## Pipeline de Análise

### 1. EDA - Análise Exploratória de Dados

No notebook **`EDA_radiacao.ipynb`**, realizamos a análise exploratória de dados (EDA), que inclui:

- Carregamento e visualização dos dados.
- Análise estatística básica (média, mediana, desvio padrão, etc.).
- Análise de tendências, sazonalidades e ciclos.
- Identificação de valores ausentes, outliers, e correlação temporal.

### 2. Limpeza e Pré-processamento dos Dados

No notebook **`Data_Cleaning_final.ipynb`**, realizamos as seguintes etapas de limpeza e pré-processamento:

- Tratamento de valores ausentes e outliers.
- Transformações temporais (e.g., decomposição da data em componentes como mês, dia, ano, etc.).
- Normalização e/ou transformação de variáveis para modelos de machine learning.
- Divisão dos dados em conjuntos de treino e teste.

### 3. Modelagem com SARIMAX

No notebook **`modeling.ipynb`**, aplicamos o modelo **SARIMAX** para prever a série temporal. O SARIMAX é usado para capturar componentes sazonais, tendências e variáveis exógenas.

- Ajuste de hiperparâmetros (p, d, q, P, D, Q, s).
- Treinamento do modelo e avaliação usando métricas como RMSE e MAE.
- Realizações de previsões futuras.

### 4. Modelagem com XGBoost

Após modelar com **SARIMAX**, aplicamos o **XGBoost**, que é um algoritmo poderoso baseado em árvores de decisão, para prever a série temporal.

- Ajuste de hiperparâmetros do XGBoost.
- Treinamento do modelo e avaliação usando métricas como RMSE e MAE.
- Realizações de previsões futuras.

## Resultados e Métricas

As métricas de desempenho dos modelos (como RMSE, MAE, R²) são exibidas nos notebooks em que os modelos foram treinados para comparar os resultados obtidos com SARIMAX e XGBoost.

### Exemplos de Resultados:
- **SARIMAX**: 
  - RMSE: 1.23
  - MAE: 0.98
  - Acurácia: 92%

- **XGBoost**:
  - RMSE: 1.15
  - MAE: 0.89
  - Acurácia: 94%

## Considerações Finais

Este projeto demonstrou como abordar a análise de séries temporais utilizando tanto modelos clássicos (SARIMAX) quanto modernos (XGBoost). Ambos os modelos apresentaram bom desempenho, e a escolha entre eles pode depender de características específicas dos dados.

Para aprimorar ainda mais o modelo, podem ser exploradas técnicas de ajuste de hiperparâmetros, além da aplicação de modelos híbridos para capturar tanto componentes sazonais quanto não lineares nos dados.
