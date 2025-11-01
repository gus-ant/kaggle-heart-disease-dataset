# 🫀 Previsão de Doença Cardíaca (98.5% de Acurácia)

Este projeto de Machine Learning visa desenvolver um modelo de classificação robusto capaz de prever a presença de doença cardíaca em pacientes com base em dados clínicos e demográficos, alcançando uma acurácia de **98.5%** no conjunto de testes.

Os dados são desse Dataset no Kaggle: https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset 

Meu Dataset no Kaggle com a explicação completa: https://www.kaggle.com/code/gustavrod/heart-disease-98-5-accuracy 

## Gráficos gerados

### Feature Importances

Esta visualização mostra quais atributos do paciente tiveram maior peso na decisão do modelo. É essencial para entender a relevância clínica de cada variável para a previsão de doença cardíaca.

![feature importance](https://github.com/gus-ant/kaggle-heart-disease-dataset/blob/main/feat_importance.png)

### Correlation Matrix

A matriz de correlação ilustra as relações lineares entre todas as variáveis. Esta análise foi crucial para identificar possíveis problemas de multicolinearidade e entender como as características se agrupam.

![correlation matrix](https://github.com/gus-ant/kaggle-heart-disease-dataset/blob/main/correlation_mat.png)

### Confusion Matrix

A matriz de confusão valida o desempenho do modelo no conjunto de testes, mostrando a contagem de previsões corretas (Verdadeiros Positivos e Verdadeiros Negativos) e incorretas. Ela é a base para o cálculo da acurácia de 98.5%.

![confusion matrix](https://github.com/gus-ant/kaggle-heart-disease-dataset/blob/main/conf_matrix.png)

##  Objetivo

O objetivo principal é construir um sistema de suporte à decisão clínica que possa identificar pacientes com alto risco de doença cardíaca, utilizando um pipeline de Ciência de Dados que inclui Análise Exploratória de Dados (EDA), pré-processamento, seleção de características e treinamento de modelos de classificação avançados.

##  Conjunto de Dados

O projeto utiliza o amplamente reconhecido **Heart Disease Dataset** da UCI, que contém 13 atributos clínicos chave por paciente.

### Atributos Chave:

| Atributo | Descrição |
| :--- | :--- |
| **age** | Idade em anos. |
| **sex** | Gênero (1 = masculino; 0 = feminino). |
| **cp** | Tipo de dor no peito (4 valores). |
| **trestbps** | Pressão arterial de repouso (mm Hg). |
| **chol** | Colesterol sérico (mg/dl). |
| **fbs** | Açúcar no sangue em jejum (> 120 mg/dl). |
| **thalach** | Frequência cardíaca máxima atingida. |
| **exang** | Angina induzida por exercício (1 = sim; 0 = não). |
| **oldpeak** | Depressão do segmento ST induzida por exercício em relação ao repouso. |
| **target** | **Variável de Saída:** Presença de doença cardíaca (1 = sim; 0 = não). |

## 💻 Tecnologias e Bibliotecas

O projeto foi desenvolvido em Python e utiliza as seguintes bibliotecas principais:

* **Python** (3.x)
* **Jupyter Notebook** (ou ambiente de desenvolvimento compatível)
* **Pandas** e **NumPy** para manipulação de dados.
* **Matplotlib** e **Seaborn** para Análise Exploratória de Dados (EDA) e visualizações.
* **Scikit-learn** para pré-processamento de dados (Scaling, Encoding), divisão de treino/teste e avaliação de modelos.
* **Modelo de Classificação Avançado** (Sugestão: Random Forest, XGBoost ou Stacking Classifier).

##  Metodologia

O pipeline de Machine Learning seguiu as seguintes etapas:

1.  **Análise Exploratória de Dados (EDA):** Verificação de valores ausentes, análise de distribuição de variáveis e identificação de correlações com a variável `target`.
2.  **Pré-processamento de Dados:** Tratamento de *outliers*, normalização/padronização de variáveis numéricas e codificação (One-Hot Encoding) de variáveis categóricas.
3.  **Balanceamento de Classes:** (Se aplicável) Técnicas como SMOTE ou ajuste de pesos para lidar com o desbalanceamento das classes.
4.  **Treinamento do Modelo:** Treinamento do classificador e otimização de hiperparâmetros (via GridSearchCV ou Random Search) para maximizar a acurácia e o F1-Score.
5.  **Avaliação:** Avaliação do desempenho do modelo utilizando métricas como Acurácia, Precisão, Recall, F1-Score e Curva ROC.

##  Resultado Principal

O modelo final atingiu o seguinte desempenho no conjunto de testes:

| Métrica | Valor |
| :--- | :--- |
| **Acurácia** | **98.5%** |

O alto nível de acurácia demonstra a eficácia da combinação de engenharia de recursos e otimização do modelo para esta tarefa de classificação.

##  Como Executar o Projeto

Para replicar este projeto localmente, siga os passos abaixo:

1.  **Clone o repositório:**
    ```bash
    git clone https://github.com/gus-ant/kaggle-heart-disease-dataset
    cd kaggle-heart-disease-dataset
    ```
2.  **Crie e ative o ambiente virtual (opcional, mas recomendado):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # Linux/macOS
    # .\venv\Scripts\activate # Windows
    ```
3.  **Instale as dependências:**
    ```bash
    pip install pandas numpy scikit-learn matplotlib seaborn 
    ```
4.  **Execute o Notebook:**
    Abra o arquivo `.ipynb` no Jupyter Notebook ou Jupyter Lab para visualizar e rodar o código passo a passo.
    ```bash
    jupyter notebook
    ```
