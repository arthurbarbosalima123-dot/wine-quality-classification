# 🍷 Wine Quality Classification

Projeto desenvolvido como Tech Challenge da Fase 2 da Pós-Graduação em Data Analytics - FIAP (PosTech).

## 📋 Descrição

Este projeto tem como objetivo desenvolver um modelo de Machine Learning capaz de prever a qualidade de vinhos tintos com base em suas características físico-químicas. O problema foi tratado como uma classificação binária:

- **Alta Qualidade:** nota ≥ 7 (1)
- **Baixa/Média Qualidade:** nota < 7 (0)

## 📁 Estrutura do Projeto

wine-quality-classification/
│
├── data/               # Base de dados utilizada
├── notebooks/          # Notebook com a análise e modelagem
├── src/                # Scripts auxiliares
├── results/            # Gráficos e métricas dos modelos
├── requirements.txt    # Bibliotecas utilizadas
└── README.md           # Descrição do projeto
## 📊 Dataset

- **Fonte:** Wine Quality Dataset - Kaggle
- **Total de amostras:** 1.143 vinhos tintos
- **Variáveis:** 12 características físico-químicas + variável alvo
- **Desbalanceamento:** 84% baixa/média qualidade vs 16% alta qualidade

## 🔍 Etapas do Projeto

1. **Análise Exploratória (EDA)**
   - Distribuição das variáveis
   - Análise de correlação
   - Identificação de outliers
   - Análise do desbalanceamento das classes

2. **Pré-processamento**
   - Criação da variável alvo binária
   - Divisão treino/teste com stratify
   - Padronização com StandardScaler

3. **Modelos Treinados**
   - Regressão Logística
   - Random Forest Classifier

4. **Avaliação**
   - Acurácia, Precision, Recall e F1-Score
   - Matriz de Confusão
   - Importância das variáveis

## 📈 Resultados

| Modelo | Acurácia | F1-Score (Alta Qualidade) |
|---|---|---|
| Regressão Logística | 81% | 0.51 |
| Random Forest | 91% | 0.60 |

O **Random Forest** apresentou desempenho superior em todas as métricas avaliadas.

## 🔑 Principais Insights

- Vinhos com **maior teor alcoólico** tendem a ser de maior qualidade
- **Acidez volátil** tem relação inversa com a qualidade — quanto maior, pior o vinho
- **Sulfatos** mais altos estão associados a vinhos de melhor qualidade

## 📖 Storytelling da Análise

A indústria vitivinícola tradicionalmente depende de especialistas humanos para avaliar a qualidade dos vinhos — um processo caro, subjetivo e demorado.

Este projeto demonstra que é possível substituir parte desse processo por um modelo preditivo baseado em dados físico-químicos, atingindo **91% de acurácia** com o Random Forest.

### A jornada dos dados

**1. O problema**
Dos 1.143 vinhos analisados, apenas 159 (14%) foram classificados como alta qualidade. Esse desbalanceamento reflete a realidade do mercado — vinhos verdadeiramente bons são minoria.

**2. O que os dados revelaram**
Durante a análise exploratória, três variáveis se destacaram como as mais relevantes para a qualidade:
- 🍷 **Teor alcoólico** — vinhos bons têm mais álcool
- ⚗️ **Acidez volátil** — vinhos ruins têm mais acidez
- 🧪 **Sulfatos** — vinhos bons têm mais sulfatos

**3. O modelo**
Após testar dois algoritmos, o Random Forest se mostrou superior, errando muito menos e identificando melhor os vinhos de alta qualidade.

**4. O impacto para o negócio**
Com esse modelo, produtores podem prever a qualidade do vinho ainda durante o processo de produção, permitindo ajustes antes que o produto chegue ao consumidor final — reduzindo custos e aumentando a padronização da qualidade.

## 🚀 Como Rodar

1. Clone o repositório
```bash
git clone https://github.com/seu-usuario/wine-quality-classification.git
```

2. Instale as dependências
```bash
pip install -r requirements.txt
```

3. Abra o notebook
```bash
jupyter notebook notebooks/wine_quality.ipynb
```

## 🛠️ Tecnologias Utilizadas

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn

## 👤 Autores

Arthur Lima, Bruna Rodrigues, Keisy Magalhães, Luiz Cesar dos Santos, Renato Naddeo

Pós-Graduação em Data Analytics - FIAP PosTech
