# Análise de Dados de Seguro de Saúde

## Descrição

Este notebook realiza uma análise exploratória de dados e modelagem preditiva em um conjunto de dados de seguro de saúde. O objetivo é entender os fatores que influenciam os custos do seguro e desenvolver um modelo para prever os encargos com base nas características do indivíduo.

## Passo a Passo

1. **Importação de bibliotecas:** Importa as bibliotecas necessárias, como pandas, matplotlib, seaborn e scikit-learn.
2. **Carregamento dos dados:** Carrega o conjunto de dados de seguro de saúde de um arquivo CSV.
3. **Limpeza e preparação dos dados:**
    - Lidar com valores ausentes substituindo-os pela média ou pelo valor mais frequente.
    - Atualizar os tipos de dados das colunas.
    - Arredondar os valores na coluna 'charges' para duas casas decimais.
4. **Análise exploratória de dados (EDA):**
    - Criar gráficos de dispersão e boxplots para visualizar a relação entre as variáveis.
    - Calcular a matriz de correlação para identificar relações lineares entre as variáveis.
5. **Desenvolvimento do modelo:**
    - Ajustar um modelo de regressão linear simples usando apenas o atributo 'smoker' para prever os encargos.
    - Ajustar um modelo de regressão linear múltipla usando todos os atributos para prever os encargos.
    - Criar um pipeline de treinamento que inclui StandardScaler, PolynomialFeatures e LinearRegression para melhorar o desempenho do modelo.
6. **Refinamento do modelo:**
    - Dividir os dados em conjuntos de treinamento e teste.
    - Inicializar e ajustar um modelo RidgeRegressor com um hiperparâmetro alfa de 0.1.
    - Avaliar o desempenho do modelo usando o R-quadrado.
    - Aplicar transformação polinomial aos dados de treinamento e ajustar o modelo novamente.
    - Avaliar o desempenho do modelo com os dados transformados.

## Pontos chave

- O conjunto de dados contém informações sobre indivíduos, incluindo idade, sexo, IMC, número de filhos, status de fumante, região e encargos com seguro.
- A EDA revela insights sobre as relações entre as variáveis e os encargos com seguro.
- Vários modelos de regressão são ajustados e avaliados para prever os encargos.
- O refinamento do modelo inclui o uso de regularização e transformação polinomial para melhorar o desempenho.
- O R-quadrado é usado como uma métrica para avaliar a qualidade dos modelos.

## Conclusões

Este notebook demonstra o processo de análise de dados e modelagem preditiva em um conjunto de dados de seguro de saúde. Os insights obtidos da EDA e os modelos desenvolvidos podem ser usados para entender os fatores que influenciam os custos do seguro e prever encargos futuros.

## Próximos passos

- Explorar diferentes técnicas de modelagem, como regressão polinomial ou árvores de decisão.
- Ajustar os hiperparâmetros dos modelos para otimizar o desempenho.
- Implantar o modelo para prever encargos em tempo real.# Medical Insurance Cost Prediction

# Medical Insurance Cost Prediction - English (EN)

This project analyzes a medical insurance dataset and builds a model to predict insurance charges based on various factors.

## Dataset Overview

The dataset used in this project contains the following parameters:

| Parameter | Description | Content type |
|---|---|---|
| age | Age in years | integer |
| gender | Male or Female | integer (1 or 2) |
| bmi | Body mass index | float |
| no_of_children | Number of children | integer |
| smoker | Whether smoker or not | integer (0 or 1) |
| region | Which US region - NW, NE, SW, SE | integer (1, 2, 3, or 4 respectively) |
| charges | Annual Insurance charges in USD | float |

## Project Steps

1. **Data Wrangling:**
    - **Handling Missing Data:** Missing values in the dataset are identified and addressed. For continuous attributes like 'age', missing values are replaced with the mean. For categorical attributes like 'smoker', missing values are replaced with the most frequent value. This ensures data completeness for analysis.
    - **Data Type Conversion:** The data types of certain columns are updated to ensure consistency and compatibility with analysis techniques. For instance, the 'age' and 'smoker' columns are converted to integer types, and the 'charges' column is rounded to two decimal places.

2. **Exploratory Data Analysis (EDA):**
    - **Regression Analysis:** The relationship between insurance charges ('charges') and body mass index ('bmi') is explored using regression plots. This helps visualize the correlation and potential impact of 'bmi' on insurance costs.
    - **Box Plot Analysis:** Box plots are used to compare the distribution of insurance charges ('charges') across different categories of smokers ('smoker'). This provides insights into how smoking status influences insurance costs.
    - **Correlation Analysis:** The correlation matrix for the dataset is calculated to identify relationships between all variables. This helps understand the overall interdependencies within the data.

3. **Model Development:**
    - **Baseline Model:** A basic linear regression model is built using only the 'smoker' attribute to predict insurance charges. This serves as a baseline for evaluating more complex models.
    - **Multiple Linear Regression:** A comprehensive linear regression model is built using all relevant attributes (age, gender, bmi, no_of_children, smoker, and region) to predict insurance charges. This aims to capture the combined influence of these factors on costs.
    - **Pipeline with Feature Engineering:** A machine learning pipeline is implemented, incorporating feature scaling (StandardScaler), polynomial feature transformation (PolynomialFeatures), and linear regression. This pipeline aims to improve model performance by enhancing data representation and capturing non-linear relationships.

4. **Model Refinement:**
    - **Data Splitting:** The dataset is split into training and testing subsets (80% training, 20% testing) to evaluate model performance on unseen data.
    - **Ridge Regression:** A Ridge regression model is employed with a regularization parameter (alpha) to address potential overfitting and improve generalization.
    - **Polynomial Transformation with Ridge Regression:** Polynomial feature transformation is applied to the data before fitting a Ridge regression model. This aims to further capture non-linear relationships and enhance model accuracy.
    - **Model Evaluation:** The performance of different models is evaluated using the R-squared score, a measure of how well the model fits the data and explains the variation in insurance charges.

## Libraries Used

- pandas
- matplotlib
- numpy
- seaborn
- scikit-learn

## Usage

1. Clone the repository.
2. Open the Jupyter notebook in Google Colab or a local Jupyter environment.
3. Run the notebook cells to execute the code and view the results.

## Results

The project demonstrates the use of various machine learning techniques to predict medical insurance costs. The results show that the model's performance improves with feature engineering and the use of regularization techniques.

## Conclusion

This project provides a comprehensive analysis of a medical insurance dataset and builds a predictive model for insurance charges. The findings can be used to gain insights into the factors that influence insurance costs and to develop strategies for cost optimization.
