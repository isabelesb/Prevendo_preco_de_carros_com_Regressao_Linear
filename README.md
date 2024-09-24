# Regressão Linear - Preço de Carros

Aqui, o objetivo é prever o preço de um carro utilizando Regressão Linear.

## Bibliotecas:
1. Pandas.
2. Numpy.
3. Seaborn.
4. Statsmodels.
5. Sklearn.

## Análise Descritiva:
* Os dados mostram valores discrepantes entre as colunas, então normalizaremos.
* Não há outliers fora do esperado.
* Não há dados nulos.
* Há várias variáveis categóricas, que precisaremos modificar para utilizar a regressão linear.
* Não há variáveis duplicadas.

## Tratamento dos Dados:
* Utilizamos *LabelEncoder()* para tratar as variáveis categóricas e *MinMaxScaler()* para normalizar.

## Análise Exploratória:
* Verificamos a correlação entre as variáveis presentes no dataset.
* Em seguida, com o método *OLS* do Statsmodels escolhemos as variáveis explicativas que serão utilizadas no modelo, nos baseando no *P-Value* (com o limite de 0.1). As variáveis a serem adicionadas seguiram a ordem decrescente do índice de correlação, analisado anteriormente.

## Modelo:
Ao criarmos, treinarmos e testarmos o modelo, as métricas utilizadas foram *MAE*, *MSE* e *RMSE*. Como usamos apenas um tipo de modelo, não tivemos como compará-las, mas os resuldados de treino e teste foram próximos, o que é um bom sinal.
