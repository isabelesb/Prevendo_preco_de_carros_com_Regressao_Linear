# Regressão Linear - Preço de Carros
Aqui, o objetivo é prever o preço de um carro utilizando Regressão Linear.

Começamos analisando os dados, e observa-se que:
* Os dados mostram discrepâncias entre as colunas, então precisaremos normalizar.
* Não há outliers fora do esperado.
* Não há dados nulos.
* Há várias variáveis categóricas, que precisaremos modificar para utilizar a regressão linear.
* Não há variáveis duplicadas.

Após os devidos tratamentos, verifica-se a correlação entre as variáveis presentes no dataset. Em seguida, com o método **OLS** do Statsmodels escolhemos as variáveis explicativas que serão utilizadas no modelo, nos baseando no **P-Value** (com o limite de 0.1). As variáveis a serem adicionadas seguiram a ordem decrescente do índice de correlação, analisado anteriormente.

Por fim, ao criarmos, treinarmos e testarmos o modelo, as métricas utilizadas foram **MAE**, **MSE** e **RMSE**.

**Bibliotecas:**
- Pandas;
- Numpy;
- Seaborn;
- Scikit-Learn.
