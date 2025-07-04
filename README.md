# global-cancer-patients-ml

# 🧬 Global Cancer Risk Prediction

Este repositório apresenta uma análise preditiva utilizando algoritmos de Machine Learning para investigar os principais fatores associados ao risco de câncer. Utilizamos o dataset **Global Cancer Patients 2015-2024** disponível no [Kaggle](https://www.kaggle.com/datasets/zahidmughal2343/global-cancer-patients-2015-2024).

## 📊 Objetivo

Identificar os fatores mais condicionantes para o diagnóstico de câncer com base em dados clínicos, demográficos e regionais por meio de modelos supervisionados de regressão.

## 🗂️ Dataset

- **Fonte**: Kaggle
- **Nome**: Global Cancer Patients 2015–2024
- **Tamanho**: ~55 mil registros
- **Features principais**:
  - Idade, Gênero, País, Tipo e Estágio do câncer
  - Tempo de tratamento, Custo, Tipo de tratamento
  - Diagnóstico e variáveis regionais

## ⚙️ Pré-processamento

- Separação entre variáveis **numéricas** e **categóricas**
- Transformações aplicadas:
  - `StandardScaler`
  - `MinMaxScaler`
  - `OneHotEncoder` (com `handle_unknown='ignore'`)
- Pipeline de pré-processamento usando `ColumnTransformer`

## 🤖 Modelos treinados

| Modelo              | Descrição                             |
|---------------------|---------------------------------------|
| Decision Tree       | Árvore de decisão para regressão      |
| Random Forest       | Conjunto de árvores com bagging       |
| Support Vector Regressor (SVR) | Regressão com margem máxima |
| MLP Regressor       | Perceptron Multi-Camadas              |

## 🔁 Validação cruzada

Foram testadas múltiplas `random_state` (seeds) para garantir estabilidade dos resultados e reduzir viés na divisão dos dados.

## 📈 Métricas de Avaliação

- **MSE** (Erro Quadrático Médio)  
- **MAE** (Erro Absoluto Médio)  
- **R² Score** (Coeficiente de Determinação)  

As métricas foram calculadas para cada modelo e comparadas entre diferentes técnicas de pré-processamento.

## 🧠 Feature Importance

- Avaliação da importância das variáveis nos modelos baseados em árvore
- Comparação das top-5 variáveis mais influentes no risco de câncer

## 🧪 Tecnologias Utilizadas

- `Python 3.11+`
- `scikit-learn`
- `pandas`
- `matplotlib` / `seaborn` (para visualizações)
- `Jupyter Notebook`

