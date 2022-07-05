# knn
Implementation of the knn algorithm using the "breast cancer data"

Ricco Vasconcellos Constante Soares
00307968

## Observe o intervalo em que varia cada atributo no dado de treinamento: há uma grande diferença entre os valores máximo e mínimo de cada atributo?

A diferença entre os valores máximo e mínimo de cada atributo variam muito consideravelmente, com atributos que apresentam variação da ordem de grandeza de 10^(-2), enquanto outros, da ordem de 10^3.

## Discuta brevemente sobre a distribuição de valores e como isto pode impactar no processo de tomada de decisão do modelo

A presença de descrepâncias nas variações de cada atributo do conjunto de dados tende a produzir piores resultados na classificação, uma vez que faz com que os atributos que apresentam maior variação dos valores adiquiram maior peso. É justamente por isso que é ideal realizar a normalização dos dados antes da aplicação do algoritmo de KNN.

## Faça uma avaliação do resultado, brevemente discutindo os achados e se existe alguma tendência ou associação entre desempenho e valor de k.

O valor de k decresce de forma praticamente constante conforme o valor de k cresce para valores de k maiores que 10. Para valores muito altos, é esperado que a classificação piore consideravelmente, uma vez que o classificador passa a classificar a maior parte das instâncias como pertencentes à classe majoritária.

## Analise e comente se houveram ou não diferenças em relação à taxa de acerto do algoritmo treinado e testado com dados não normalizados. A normalização impactou? De que forma: melhorando ou piorando o desempenho? Esta tendência foi observada para todos os valores de k?

A diferença de desempenho entre os resultados obtidos com e sem normalização é nítida. Para os melhores resultados, observa-se uma melhoria de cerca de 5,56% com a utilização da normalização. O decaimento de acurácia com o crescimento do valor de k teve um comportamento semelhante nos dois casos, mas a acurácia diminuiu até valores proporcionalmente menores no caso em que os dados não foram normalizados.
