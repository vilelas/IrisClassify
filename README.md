## [IrisClassify](https://github.com/vilelas/IrisClassify/blob/main/Iris/Conjunto%20de%20dados%20flor%20Iris.ipynb)
Este projeto utiliza o conjunto de dados "Iris" para criar uma rede neural simples de classificação de espécies de plantas Iris usando a biblioteca Keras. O objetivo deste projeto é demonstrar a utilização do Keras em um problema de classificação de múltiplas classes.

## Conjunto de dados
O conjunto de dados Iris consiste em 150 amostras de plantas Iris, cada uma com quatro atributos: largura e comprimento da sépala e da pétala. As amostras são rotuladas com a espécie de planta correspondente: Iris setosa, Iris versicolor ou Iris virginica.

## Pré-processamento dos dados
Primeiramente, importei os dados do conjunto Iris usando a biblioteca pandas e removemos a coluna "Id", que não é necessária para a classificação das espécies. Em seguida, verifiquei se há valores duplicados e ausentes nas amostras.

Também criei gráficos para visualizar a contagem de espécies e a correlação entre os atributos.

## Criação do modelo de rede neural
O modelo de rede neural consiste em uma camada de entrada com 4 neurônios, uma camada oculta com 8 neurônios e uma camada de saída com 3 neurônios correspondentes às três espécies de plantas Iris. Além disso, adicionei uma camada de ``dropout`` para evitar overfitting.

O modelo foi compilado com a função de perda ``categorical_crossentropy``, o otimizador ``adam`` e a métrica de avaliação ``accuracy``.

## Validação cruzada
Utilizei a validação cruzada com a biblioteca ``scikeras.wrappers`` para avaliar a performance do modelo. Dividi o conjunto de dados em 10 partes e treinei o modelo em 9 partes, testando-o na parte restante. O processo foi repetido 10 vezes, alternando as partes de treinamento e teste.

Os valores de média e desvio padrão foram calculados a partir dos resultados obtidos nas repetições da validação cruzada.

## Resultados
O modelo obteve um desempenho médio de 96% com desvio padrão de 0.044, indicando uma boa performance na classificação das espécies de plantas Iris.

## Conclusão
Este projeto demonstrou a utilização da biblioteca Keras em um problema de classificação de múltiplas classes e o uso da validação cruzada para avaliar o desempenho do modelo. O modelo criado obteve uma boa performance na classificação das espécies de plantas Iris.