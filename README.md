# ELASTICIDADE DE PREÇO 


![image](https://github.com/GuiGrecov/ElasticityPrice/assets/94385953/0d4d1e32-9766-4a7a-a02d-6e9c93b40835)


## PROBLEMA DE NEGÓCIO 
Uma empresa pretende alterar os preços dos produtos vendidos, mas tem receio dessa alteração impactar na demanda desses produtos e por consequência no faturamento. Essa demanda foi submetida para você e como Cientista de dados precisa determinar a elasticidade dos preços usando a metodologia científica embasado nos dados dos preços dos produtos vendidos pela empresa.

## 1. BREVE EXPLICAÇÃO SOBRE ELASTICIDADE DE PREÇO

A elasticidade de preço é uma medida que indica a sensibilidade da demanda de um produto em relação às mudanças no seu preço. Ela é calculada dividindo-se a variação percentual na quantidade demandada pelo produto pela variação percentual no preço do produto.

O conceito de elasticidade de preços visa medir se, por exemplo, o aumento de preços impacta significativamente ou não na demanda do produto

EXEMPLOS DE ELASTICIDADE 
- 1. ELASTICA: uma pequena variação no preço de um produto pode causar uma grande mudança na quantidade demandada. Quando o valor de elasticidade é maior que 1.
- 2. INELASTICA: inelástica é uma medida que indica que a demanda de um produto é pouco sensível às mudanças no seu preço. Ela é calculada quando o valor da elasticidade é menor do que 1.
- 3. PREÇO UNITÁRIO: A elasticidade de preço unitária é uma medida que indica que a demanda de um produto é proporcional às mudanças no seu preço. Ela é calculada quando o valor da elasticidade é exatamente igual a 1.

Também temos os conceitos referente a Elasticidade Cruzada, quando dois produtos podem existir elasticidade entre eles. Nesses caso a literatura coloca 3 tipos de elasticidade cruzada: 
- **1. Elasticidade de preço cruzada positiva**: Isso ocorre quando a **quantidade demandada de um produto aumenta em resposta a um aumento no preço de um produto relacionado**. Indica que os **dois produtos são substitutos**, e um aumento no preço de um produto leva os consumidores a buscar o produto alternativo, aumentando sua demanda.

- **2. Elasticidade de preço cruzada negativa**: Isso ocorre quando a **quantidade demandada de um produto diminui em resposta a um aumento no preço de um produto relacionado**. Indica que **os dois produtos são complementares**, e um aumento no preço de um produto reduz a demanda pelo outro produto.

- **3. Elasticidade de preço cruzada nula (ou próxima de zero)**: Isso ocorre quando **não há uma relação significativa entre a variação no preço de um produto e a quantidade demandada do outro produto**. Indica que não há substitutos ou complementares próximos entre os dois produtos


## 2. PRINCIPAIS INSIGHTS DA SOLUÇÃO DO PROBLEMA 

A base que recebemos temos a vendas por algumas lojas (e-commerces) e também temos a venda de vários segmentos de produtos diferentes. No caso, limitamos o estudo apenas para estudar a BestBuy e os produtos de Laptop e Computer - principal produto vendido no e-commerce

![image](https://github.com/GuiGrecov/ElasticityPrice/assets/94385953/afaaaf60-c054-4688-87c4-47e7e9cd6359)

Mês que aconteceu o maior número de vendas 

![image](https://github.com/GuiGrecov/ElasticityPrice/assets/94385953/6437ac06-d078-444f-a067-4e06e5b041b2)

Somente na BestBuy o mês mais forte de vendas foi Agosto isso mostra alguma presença de ums super promoção ou algo relacionado a queima de estoque. 

## 3. Business Performance 

Aplicamos uma regressão linear por meio do método dos mínimos quadrados por meio da biblioteca statsmodel.api

Para fins de generalização da equação eu preferi seguir uma recomendação do professor Maciel 

![image](https://github.com/GuiGrecov/ElasticityPrice/assets/94385953/dfaa74f5-d79a-4423-9de8-a24d88b80924)

O correto é mesclarmos o indicador R² e P-valor porque dessa forma vamos conseguir ter um modelos que explica as variações dos dados e é o melhor cenário. Com um p-valor baixo (margem de erro) menor que 0,05 e um R² otimizado


Aplicando os conceitos acimas de uma lista com mais de 25 produtos conseguimos somente 7 produtos os quais aplicando desconto podemos afirmar estatisticamente que vai ocorrer um ganho de valor porque nesses casos tem uma proporção de quando mais eu diminuo o preço maior é a probabilidade de ocorrer mais vendas. 


![image](https://github.com/GuiGrecov/ElasticityPrice/assets/94385953/618d80b8-c61a-4f3c-ae39-8342f71bf000)

**CENÁRIO SUPONDO DESCONTO DE 10%**

![image](https://github.com/GuiGrecov/ElasticityPrice/assets/94385953/756648cb-9381-4a5f-8761-6f3ff5296a45)

Vamos lucrar com o novo faturamente: R$ 121.304 quando comparamos o cenário antigo (sem desconto) com o cenário novo (com desconto). Isso acontece porque a adesão de vendas será superior no cenário com desconto.











