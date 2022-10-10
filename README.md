# House Rocket Project

![House_Rocket_Logo](https://user-images.githubusercontent.com/68931118/194935369-bed73ceb-a037-4ecf-8d2d-4e3b5a722b78.png)

A House Rocket é uma empresa fictícia do ramo imobiliário que lucra a partir da compra e venda de imóveis, tendo como principal estratégia a compra de casas em boas condições por um baixo preço, as vendendo por um valor superior. Visando maximizar a eficiência na busca das melhores oportunidades de mercado e obter uma maior noção de qual preço aplicar em cima dos imóveis comprados, a empresa solicitou este projeto utilizando ferramentas de Ciência de Dados para gerar insights através da manipulação dos dados e consequentemente auxiliar as melhores decisões da equipe de negócios.

# Questões de Negócio

1. Quais são os imóveis que a House Rocket deveria comprar e por qual preço?
2. Uma vez a casa comprada, qual o melhor momento para vendê-las e por qual preço?

# Atributos

Os dados usados na elaboração desse projeto podem ser encontrados em: https://www.kaggle.com/harlfoxem/housesalesprediction/discussion/207885. 

Abaixo segue a definição para cada um dos 21 atributos:
![Dicionario_Colunas](https://user-images.githubusercontent.com/68931118/194935580-43318e09-df49-4c8c-b010-96ec0625e499.png)

# Premissas de Negócio

Para o desenvolvimento desse projeto, foram determinadas as seguintes premissas:

1. Na coluna "yr_renovated", valores iguais a zero correspondem a imóveis que nunca passaram por reforma.
2. Na coluna "waterfront", valores iguais a um correspondem a imóveis com vista para o mar, já valores iguais a zero correspondem a imóveis sem vista para o mar.
3. A partir das análises, o imóvel com valor da coluna "bathroom" igual a 33 foi considerado como erro de digitação e em seguida removido.
4. Para valores com ID duplicados, apenas o mais recente foi utilizado.

# Planejamento da solução

Cronograma de estratégias para resolução do projeto:

1. Entendimento de Negócio
2. Definição das ferramentas e produto final
3. Coleta de dados via Kaggle
4. Limpeza dos dados
5. Análise dos dados
6. Criação de hipóteses
7. Manipulação dos dados para testar hipóteses e gerar insights
8. Resolver os problemas de negócio
9. Desenvolver um Dashboard com os resultados obtidos
10. Alocar esse produto final em um ambiente em nuvem

# Ferramentas

Python 3.8.10

Vscode

Streamlit

Amazon EC2

Manipulação de dados: pandas, numpy
Visualização de dados: seaborn, plotly, folium

# Principais insights

Durante o projeto, foram pensadas diversas hipóteses, algumas delas gerando interessantes insights de negócios, como:

Hipótese 1: Imóveis que possuem vista para água, são pelo menos 30% mais caros, na média.
- Hipótese confirmada. Em média, o valor dos imóveis com vista para o mar são mais que 3x maiores aos imóveis sem esse privilégio.

Hipótese 2: Imóveis com data de construção menor que 1955, são 50% mais baratos, na média.
- Hipótese falsa. A partir da invalidação dessa hipótese, deu pra chegar a conclusão que o preço médio das casas antigas é pouca coisa inferior ao preço médio das casas mais atuais.
 
Hipótese 7: Imóveis variam pelo menos 30% de média de preço por condição.
- Hipótese falsa. Entretanto, foi possível constatar um aumento de 15% da média do preço da condição 4 para 5.

Hipótese 9: Imóveis com mais de 2 quartos são 70% mais caros que os que possuem apenas 1
- Hipótese falsa. Além de identificar a magnitude da diferença do preço entre imóveis com 1 quarto para os demais, também se tornou possível perceber que a partir 9 quartos, existe uma queda significativa do preço médio.

Hipótese 10: Imóveis variam 4% ou mais o preço por nota de design, em média.
- Hipótese verdadeira. Em média, imóveis variam 4% ou mais o preço por nota de design.

# Conclusão

Imóveis foram agrupados por região e foi calculada a mediana do preço dos imóveis dentro de cada estação do ano dentro de cada região. Todos os imóveis com o valor inferior a maior mediana de preço da sua região e com distancia de pelo menos 5% a ela foram indicados para compra. Para cada um desses imóveis selecionados foi sugerido o valor e melhor momento de venda, variando de acordo com sua região, condição e melhor mediana de preço por estação da sua região.

Caso a empresa consiga comprar e revender todos os imóveis pelos valores de compra e venda estipulados, a mesma terá um lucro de ~$287.879.849 (Sem levar em conta outros gastos da empresa durante esse período). 
