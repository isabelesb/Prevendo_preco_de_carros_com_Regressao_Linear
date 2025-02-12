# Regressão Linear - Preço de Carros

## Entendimento do Negócio:
Nosso objetivo é prever o preço de um carro, de acordo com suas características, utilizando uma Regressão Linear. Ou seja, dado um carro qualquer, iremos prever seu preço com uma boa aproximação.

## Bibliotecas:
* Pandas.
* Numpy.
* Seaborn.
* Statsmodels.
* Scikit-learn.

## Entendimento dos Dados:
Para este projeto, contaremos com uma tabela que contém 205 carros e suas características mais relevantes. Entre as características, podemos encontrar o número de portas, peso, potência, etc.

Com as análises iniciais, percebemos que:
* Os valores variam muito de uma coluna para outra (algumas têm como entrada valores menores que 10, enquanto outras têm valores maiores que 1.000). Isso significa que precisaremos normalizar a tabela pois, caso contrário, o modelo pode interpretar variáveis com valores maiores como mais importantes, mesmo que não seja o caso.
* Não há outliers.
* Não há valores nulos.
* Não há entradas duplicadas.
* Há várias variáveis categóricas, que precisaremos converter em numéricas para utilizar a regressão linear. (Uma vez que esse modelo se trata de uma equação matemática, ele não consegue lidar com dados que não sejam numéricos.)

## Tratamento dos Dados:
Utilizamos *LabelEncoder()* para tratar as variáveis categóricas. E, para normalizar os dados, o *MinMaxScaler()*.

## Modelagem:
1. Como há muitas caracteríscas listadas na tabela, iniciamos verificando a correlação entre elas, com o método *.corr()*. Aqui demos foco principalmente à coluna de preço.
2. Com o método *OLS* do Statsmodels, escolhemos as variáveis explicativas que serão utilizadas no modelo, nos baseando no *P-Value* (com o limite de 0.1) e através de tentativas e erros. As variáveis foram adicionadas seguindo a ordem decrescente do índice de correlação analisado anteriormente. Esse método tem por objetivo deixar o modelo mais leve, uma vez que utilizamos apenas as características mais importantes.
3. Criamos o medelo com a biblioteca Scikit-Learn, utilizando apenas 4 colunas da nossa tabela. E seu treinamento foi realizado com 80% dos dados.

## Avaliação:
Após testarmos o modelo, utilizamos as métricas *MAE - Erro Médio Absoluto*, *MSE - Erro Médio ao Quadrado* e *RMSE - Raís Quadrada do Erro Médio* para avaliá-lo. 
Como utilizamos apenas a Regressão Linear, a única comparação que realizada nessa etapa foi entre os dados de treino e teste. E com isso obtivemos um bom resultado, pois os valores de cada métrica foram bem semelhantes para os dois conjuntos de dados.

