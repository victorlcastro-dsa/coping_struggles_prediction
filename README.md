
---

# Coping Struggles Prediction

Este projeto tem como objetivo prever dificuldades de enfrentamento com base em dados de saúde mental. Utilizamos um conjunto de dados coletados através de um formulário e aplicamos técnicas de aprendizado de máquina para criar um modelo preditivo.

Link para o notebook: [Coping Struggles Prediction](notebook/Coping_Struggles_ML.ipynb)

## Estrutura do Projeto

- `data/`: Contém os dados utilizados no projeto.
  - `img/`: Contém imagens relacionadas ao projeto.
  - `Mental Health Dataset.csv`: Conjunto de dados principal.
  - `Respostas ao formulário.csv`: Respostas coletadas do formulário.
- `notebook/`: Contém notebooks Jupyter para análise e modelagem.
  - `Coping_Struggles_ML.ipynb`: Notebook principal com a análise e modelagem.
  - `final_model.joblib`: Modelo final treinado.
  - `requirements.txt`: Dependências do projeto.

## Pré-requisitos

Certifique-se de ter o Python 3.11.9 instalado. Você pode especificar a versão do Python usando o arquivo `.python-version`.

## Instalação

1. Clone o repositório:
    ```sh
    git clone https://github.com/victorlcastro-dsa/coping_struggles_prediction.git
    cd coping_struggles_prediction
    ```

2. Crie um ambiente virtual e ative-o:
    ```sh
    python -m venv venv
    source venv/bin/activate  # No Windows use `venv\Scripts\activate`
    ```

3. Instale as dependências:
    ```sh
    pip install -r notebook/requirements.txt
    ```

## Uso

1. Navegue até o diretório `notebook` e inicie o Jupyter Notebook:
    ```sh
    cd notebook
    jupyter notebook
    ```

2. Abra o notebook `Coping_Struggles_ML.ipynb` e execute as células para reproduzir a análise e a modelagem.

## Análise e Modelagem

### Importação das Bibliotecas
As bibliotecas necessárias incluem:
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `plotly`
- `scikit-learn`

### Carregamento dos Dados
Os dados são carregados do arquivo `Mental Health Dataset.csv` e armazenados em um DataFrame do pandas.

### Estudo dos Atributos
Análise dos atributos do dataset para entender suas características e identificar potenciais preditores.

### Visualização dos Dados
Gráficos de barras e mapas de calor são utilizados para visualizar a distribuição dos dados e correlações entre variáveis.

### Engenharia de Atributos
Transformações como One-Hot Encoding e Label Encoding são realizadas para preparar os dados para a modelagem.

### Seleção de Atributos
Técnicas de seleção de features são usadas para escolher os atributos mais relevantes.

### Experimentação Inicial de Modelos
Testes com diferentes modelos de aprendizado de máquina, incluindo:
- Regressão Logística
- K-Nearest Neighbors
- Random Forest
- Gradient Boosting

### Ajuste Fino dos Hiperparâmetros
GridSearchCV é utilizado para ajustar os hiperparâmetros do modelo Random Forest.

### Métodos de Ensemble
Combinação de modelos utilizando Voting Classifier para criar um modelo mais robusto.

### Avaliação do Modelo
Desempenho do modelo final avaliado com métricas como precisão, recall, F1-score e acurácia.

## Resultados
O modelo final, um Voting Classifier combinando Random Forest e AdaBoost, alcançou uma acurácia de 86.58% no conjunto de testes.

## Contribuição
Contribuições são bem-vindas! Abra issues e pull requests para colaborar.
