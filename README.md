# Regressão Linear - Preço de Carros

Aqui, o objetivo é prever o preço de um carro, de acordo com suas características, utilizando uma Regressão Linear. Ou seja, com um tipo de equação matemática que envolve várias variáveis, iremos calcular os preços com uma boa aproximação.

## Bibliotecas:
* Pandas.
* Numpy.
* Seaborn.
* Statsmodels.
* Sklearn.

## Análise Descritiva:
* Os dados mostram valores discrepantes entre as colunas, então normalizaremos. Pois, caso contrário, o modelo pode interpretar variáveis com valores maiores como mais importantes, mesmo que não seja o caso.
* Não há outliers fora do esperado, nem dados nulos ou duplicados.
* Há várias variáveis categóricas, que precisaremos modificar para utilizar a regressão linear. Uma vez que se trata de uma equação matemática, ela não consegue lidar com dados que não sejam numéricos.

## Tratamento dos Dados:
* Utilizamos *LabelEncoder()* para tratar as variáveis categóricas e *MinMaxScaler()* para normalizar.

## Análise Exploratória:
* Verificamos a correlação entre as variáveis presentes no dataset.
* Em seguida, com o método *OLS* do Statsmodels escolhemos as variáveis explicativas que serão utilizadas no modelo, nos baseando no *P-Value* (com o limite de 0.1). As variáveis a serem adicionadas seguiram a ordem decrescente do índice de correlação, analisado anteriormente. Assim, não precisamos utilizar tantas colunas para a modelagem, somente as mais relevantes, e o modelo fica mais leve.

## Modelo:
Ao criarmos, treinarmos e testarmos o modelo, as métricas utilizadas foram *MAE*, *MSE* e *RMSE*, que se baseiam no erro das predições para avaliar o modelo. Como usamos apenas o modelo de Regressão Linear, não tivemos com o que compará-las, mas os resuldados para treino e teste foram próximos, o que é um bom sinal.
