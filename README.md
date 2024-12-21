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
- Implantar o modelo para prever encargos em tempo real.
