<h1 align="center"> &#128202; Dashboard de Análise e Suporte de Vendas </h1>

<p align="center">Este repositório contém o dashboard referente ao primeiro estudo de caso do curso <strong>Microsoft Power BI para Data Science</strong> da Data Science Academy.<p>
<p align="center">



<p align="center">
    <a href="##Tecnologias">Tecnologias</a> |
    <a href="##Dados">Dados</a> |
    <a href="##Objetivos do relatório">Objetivos do relatório</a> |
    <a href="##Dashboard e Resultados">Dashboard e Resultados</a> 
</p>



## Tecnologias

<p style='margin: 16px 4px 32px;'>
    <a href="https://powerbi.microsoft.com/pt-br/" target="_blank" rel="noreferrer">
        <img src="https://github.com/Vinicius999/Dashboard-de-Vendas/blob/main/images/Power-BI.png" alt="Power BI" width="40" height="40" />
    </a>



## Dados

| Coluna      | Descrição                                |
| ----------- | ---------------------------------------- |
| ID-Produto  | Identificar número de cada produto       |
| Produto     | Nome do produto                          |
| Categoria   | Categoria do produto                     |
| Segmento    | Segmento do produto                      |
| Fabricante  | Fabricante de produto                    |
| Loja        | Loja onde foi efetuada a venda           |
| Cidade      | Cidade da loja onde foi efetuada a venda |
| Estado      | Estado da loja onde foi efetuada a venda |
| Vendedor    | Nome do vendedor                         |
| ID-Vendedor | ID-Vendedor                              |
| DataVenda   | Data da venda                            |
| ValorVenda  | Valor da venda                           |



## Modelo de Organização dos Dados

### Porque é necessário um modelo de organização dos dados?

- **Posso levar os dados para o Power BI da forma que estão?**

  Precisamos organizar os dados e pensar na solução do problema pensando sempre em como entregar o resultado para o gestor da melhor maneira possível.

- **Quais são os requerimentos de organização dos dados?**

  Preciso se comunicar com área de negócio e compreender o problema para poder desenvolver a solução.

- **Como mantér os dados em formato de atualização sob demanda?**

  Os dados estão em constante atualização e mutação. Dessa forma, a partir do Modelo de Organização dos Dados será possível manter a atualização dos dados sob demanda.

- **Como visualizar dados por diferentes visões e ângulos?** 

  Para poder entregar visualizações em ângulos diferentes, será necessário organizar melhor os dados, ao invés de um única planilha.


### Definindo Modelo de Organização dos Dados

- **Processo de Negócio**
Exemplo: Vendas de Produtos Eletrônicos

- **Definimos o Nível de Detalhamento (Granularidade)**
Exemplo: Total de Produtos Mais Vendidos Por Dia

- **Identificar as Dimensões Necessárias**
Exemplo: Fabricante, Produto, Loja, Tempo

- **Criamos o Schema**
Modelo criado no Data Warehouse ou no Power BI (mais simples)


### Modelo de Organização dos Dados

- **Modelo Star Schema**
	
	<p>
		<img src="https://github.com/Vinicius999/Dashboard-Suporte-de-Vendas/blob/main/images/modelo-star-schema.png" alt="modelo-star-schema" />
	</p>
	
	
	- **Tabelas DIM** são as dimensões que representam as entidades em nosso
	problema de negócio e que classificam os dados;
	- **Tabela FATO** representa um fato, um detalhe, por exemplo, uma venda.
	Cada detalhe das dimensões;
	- **PK** é a Chave Primária (Primary Key) da tabela em questão;
	- **FK** é a Chave Estrangeira (Foreign Key) que referencia a Chave Primária
	de outra tabela;
	
- **Criando Modelo**
  Após carregar e realizar os tratamentos iniciais nos dados, criamos as tabelas DIM
  e tabela FATO, tomando o cuidado de remover registros duplicados (PK).

  <p>
  	<img src="https://github.com/Vinicius999/Dashboard-Suporte-de-Vendas/blob/main/images/tabelas-DIM-tabela-FATO.png" alt="tabelas-DIM-tabela-FATO"/>
  </p>

  Após a criação das tabelas, gerenciamos os relacionamentos entre as mesmas. Por 
  se tratar de um modelo Star Schema, todas as tabelas DIM se relacionama diretamente
  com a tabela FATO que se posiciona ao centro.

  <p>
  	<img src="https://github.com/Vinicius999/Dashboard-Suporte-de-Vendas/blob/main/images/criando-relacionamentos.png" alt="criando-relacionamentos" />
  </p>



## Objetivos do Relatório

1. Qual dos fabricantes dos produtos vendidos, apresenta melhor desempenho nas vendas?
2. Qual o total de vendas por estado e por categoria?
3. Qual o total de vendas por segmento? 
4. Qual segmento tem maior influência no valor médio de venda? 



## Dashboard e Resultados

#### 1 - Fabricante com melhor desempenho nas vendas

<p>
	<img src="https://github.com/Vinicius999/Dashboard-Suporte-de-Vendas/blob/main/images/01-total-vendas-por-fabricante.png" alt="total-vendas-por-fabricante"  width="611px" height="275px"/>
</p>




#### 2 - Total de vendas por estado e por categoria

<p>
	<img src="https://github.com/Vinicius999/Dashboard-Suporte-de-Vendas/blob/main/images/02-total-vendas-por-categoria-nos-estados.png" alt="total-vendas-por-categoria-nos-estados" width="612" height="275" />
</p>




#### 3 - Total de vendas por segmento

<p>
	<img src="https://github.com/Vinicius999/Dashboard-Suporte-de-Vendas/blob/main/images/03-total-vendas-por-segmento.png" alt="total-vendas-por-segmento" width="612" height="275" />
</p>




#### 4 - Segmento com maior influência no valor médio de venda

<p>
	<img src="https://github.com/Vinicius999/Dashboard-Suporte-de-Vendas/blob/main/images/04-maior-influencia-valor-medio-de-vendas.png" alt="maior-influencia-valor-medio-de-vendas" width="611" height="274" />
</p>






#### 5 - Dashboard de Suporte de Vendas

<p style="margin: 0px 0px;">
    <img src="https://github.com/Vinicius999/Dashboard-Suporte-de-Vendas/blob/main/images/00-Dashoard.png" alt="Dashoard"/>
    </a>
</p>
