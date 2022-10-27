# TÍTULO DO DASHBORAD

resumo

menu

## Tecnologias


## Dados



## Modelo de Organização dos Dados

### Porque é necessário um modelo de organização dos dados?

- Posso levar os dados para o Power BI da forma que estão?
Precisamos organizar os dados e pensar na solução do problema pensando sempre em como
entregar o resultado para o gestor da melhor maneira possível.

- Quais são os requerimentos de organização dos dados?
Preciso se comunicar com área de negócio e compreender o problema para poder
desenvolver a solução.

- Como mantér os dados em formato de atualização sob demanda?
Os dados estão em constante atualização e mutação. Dessa forma, a partir do **Modelo
de Organização dos Dados** será possível manter a atualização dos dados sob demanda.

- Como visualizar dados por diferentes visões e ângulos?
Para poder entregar visualizações em ângulos diferentes, será necessário organizar
melhor os dados, ao invés de um única planilha.


### Definindo Modelo de Organização dos Dados

- Processo de Negócio
Exemplo: Vendas de Produtos Eletrônicos

- Definimos o Nível de Detalhamento (Granularidade)
Exemplo: Total de Produtos Mais Vendidos Por Dia

- Identificar as Dimensões Necessárias
Exemplo: Fabricante, Produto, Loja, Tempo

- Criamos o Schema
Modelo criado no Data Warehouse ou no Power BI (mais simples)


### Modelo de Organização dos Dados

- Modelo Star Schema
	- **Tabelas DIM** são as dimensões que representam as entidades em nosso
	problema de negócio e que classificam os dados;
	- **Tabela FATO** representa um fato, um detalhe, por exemplo, uma venda.
	Cada detalhe das dimensões;
	- **PK** é a Chave Primária (Primary Key) da tabela em questão;
	- **FK** é a Chave Estrangeira (Foreign Key) que referencia a Chave Primária
	de outra tabela;

- Criando Modelo
Após carregar e realizar os tratamentos iniciais nos dados, criamos as tabelas DIM
e tabela FATO, tomando o cuidado de remover registros duplicados (PK).
<imagem aqui>

Após a criação das tabelas, gerenciamos os relacionamentos entre as mesmas. Por 
se tratar de um modelo Star Schema, todas as tabelas DIM se relacionama diretamente
com a tabela FATO que se posiciona ao centro.
<imagem aqui>


## Objetivos do Relatório
1- Qual dos fabricantes dos produtos vendidos, apresenta melhor desempenho nas vendas? (já resolvido)
2- Qual o total de vendas por estado e por categoria? Use um mapa.
3- Qual o total de vendas por segmento? 
4- Qual segmento tem maior influência no valor médio de venda? 


## Dashboard

