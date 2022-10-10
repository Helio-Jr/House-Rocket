# House Rocket Project

![House_Rocket_Logo](https://user-images.githubusercontent.com/68931118/194935369-bed73ceb-a037-4ecf-8d2d-4e3b5a722b78.png)

A House Rocket é uma empresa fictícia do ramo imobiliário que lucra a partir da compra e venda de imóveis, tendo como principal estratégia a compra de casas em boas condições por um baixo preço, as vendendo por um valor superior. Visando maximizar a eficiência na busca das melhores oportunidades de mercado e obter uma maior noção de qual preço aplicar em cima dos imóveis comprados, a empresa solicitou este projeto utilizando ferramentas de Ciência de Dados para gerar insights através da manipulação dos dados e consequentemente auxiliar as melhores decisões da equipe de negócios.

# Questões de Negócio

1. Quais são os imóveis que a House Rocket deveria comprar e por qual preço?
2. Uma vez a casa comprada, qual o melhor momento para vendê-las e por qual preço?

# Atributos

![Dicionario_Colunas](https://user-images.githubusercontent.com/68931118/194935580-43318e09-df49-4c8c-b010-96ec0625e499.png)
div align="center"
img src="[https://desblogada.files.wordpress.co...](https://user-images.githubusercontent.com/68931118/194935580-43318e09-df49-4c8c-b010-96ec0625e499.png)" width="400px" /
/div

# Premissas de Negócio

Para o desenvolvimento desse projeto, foram determinadas as seguintes premissas:

1. Na coluna "yr_renovated", valores iguais a zero correspondem a imóveis que nunca passaram por reforma.
2. Na coluna "waterfront", valores iguais a um correspondem a imóveis com vista para o mar, já valores iguais a zero correspondem a imóveis sem vista para o mar.
3. A partir das análises, o imóvel com valor da coluna "bathroom" igual a 33 foi considerado como erro de digitação e em seguida removido.
4. Para valores com ID duplicados, apenas o mais recente foi utilizado.
