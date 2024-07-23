# Projeto de Portfólio: Análise de Dados com SQL

Este projeto foi desenvolvido com base nos estudos do curso "[SQL para Análise de Dados: Do básico ao avançado](https://www.udemy.com/course/sql-para-analise-de-dados/?couponCode=24T7MT72224)", ministrado por [Midori Toyota](https://www.linkedin.com/in/midoritoyota/). O curso foi conduzido em um cenário fictício de e-commerce, simulando uma plataforma onde várias lojas vendem seus carros. Utilizando dados fictícios gerados para representar interações de clientes com o site da empresa, o objetivo foi criar um sistema realista e analisar as informações obtidas. Como resultado final, o projeto apresenta análises detalhadas e relatórios que evidenciam a aplicação prática dos conhecimentos adquiridos ao longo do curso. Essas análises fornecem insights valiosos sobre o comportamento dos clientes e ajudam a entender melhor o desempenho das vendas, demonstrando a eficácia das técnicas de SQL no contexto de negócios.


## Estrutura do banco de dados
O projeto utiliza um banco de dados relacional dividido em dois schemas distintos, conforme ilustrado na imagem abaixo. Essa divisão permite uma organização mais clara e eficiente dos dados, facilitando a realização de análises complexas.

O primeiro schema, denominado **sales**, contém a maior parte dos dados gerados pelo sistema fictício de e-commerce. Este schema inclui informações cruciais sobre interações dos clientes, detalhes dos produtos, dados das lojas e registros das vendas. Essa estruturação permite uma visão abrangente e detalhada das operações de vendas e do comportamento dos clientes no site.

O segundo schema, chamado **temp_tables**, é dedicado a tabelas auxiliares que dão suporte a diversas análises. Essas tabelas são utilizadas para armazenar dados temporários, resultados intermediários de consultas e outras informações auxiliares que facilitam a execução de análises detalhadas e a geração de relatórios. A utilização deste schema separado ajuda a manter o schema principal mais organizado e focado nas transações essenciais.

![](/Imagens/Estrutura_Banco.PNG) 


<div align="center">
<img src = "https://github.com/user-attachments/assets/4474d9b0-37d8-4bab-9068-97e56ab17a58" width="3000px" />
</div>

### Tabelas no Schema sales:
* **funnel**:  Esta é a tabela principal que registra todas as interações dos clientes com o site. Ela captura cada etapa do funil de vendas, desde a visita inicial ao site até qualquer ação subsequente, incluindo visualizações de produtos, adições ao carrinho e compras. Também inclui interações onde o cliente não realizou uma compra, fornecendo uma visão completa do comportamento dos usuários no site.
* **customers**: Armazena informações detalhadas sobre os clientes, como nome, e-mail, e outras características relevantes que ajudam a identificar e analisar o comportamento dos usuários.
* **stores**: Fornece informações sobre as lojas que estão oferecendo produtos aos clientes. Inclui dados como nome da loja e outras características da loja.
* **products**: Contém dados sobre os produtos que os clientes estão procurando. Inclui informações como nome do marca, modelo, preço e outras especificações relevantes.

## Dados

Os dados para este projeto podem ser obtidos utilizando o arquivo `Query_Criar_Banco_Dados.txt`, que está presente neste diretório. Este arquivo é responsável por criar e popular as tabelas mencionadas na seção [Estrutura do banco de dados](#estrutura-do-banco-de-dados).

Devido ao grande número de linhas, o conteúdo do arquivo não é exibido diretamente no GitHub. Para acessá-lo, siga os passos abaixo:

1. Clique no botão `View raw` para visualizar o arquivo em sua forma bruta.
2. Após o código aparecer, pressione `Ctrl + A` para selecionar todas as linhas.
3. Copie o conteúdo selecionado (`Ctrl + C`).
4. Cole o conteúdo no seu editor de query preferido e execute para criar e popular as tabelas necessárias.

Essa abordagem garantirá que todas as tabelas sejam corretamente criadas e populadas, permitindo que você reproduza as análises e relatórios do projeto.

## Dashboard de acompanhamento de vendas

O objetivo do projeto, conforme proposto por [Midori Toyota](https://www.linkedin.com/in/midoritoyota/), foi desenvolver um dashboard de vendas que destaca os principais indicadores de desempenho e os drivers dos resultados para o mês de agosto de 2021. O dashboard foi projetado para fornecer uma visão clara e compreensiva do desempenho de vendas da empresa durante esse período.

### Indicadores e Análises

O dashboard inclui os seguintes indicadores principais:

* **Receita e Ticket Médio**: Observamos que a receita da empresa apresentou crescimento contínuo, enquanto o ticket médio permaneceu relativamente constante. Isso sugere que o aumento na receita é resultado de um maior volume de vendas, e não necessariamente de um aumento no valor médio de cada venda.
  
* **Leads e Taxa de Conversão**: O segundo gráfico do dashboard ilustra a relação entre o número de leads gerados (interações no site) e a taxa de conversão desses leads. Notamos que, com o tempo, a taxa de conversão aumentou, assim como o número de leads. Isso corrobora a ideia de que o crescimento da receita pode ser atribuído ao aumento no número de vendas, enquanto o ticket médio permaneceu estável.
  
* **Detalhes do Mês de Agosto de 2021**: O dashboard também inclui gráficos detalhados sobre:
  * Marcas mais vendidas durante o mês.
  * Lojas com maiores volumes de vendas.
  * Regiões com melhor desempenho em vendas.
  * Distribuição das visitas ao site por dia da semana.

Essas visualizações foram criadas utilizando o Excel para proporcionar uma análise detalhada e acessível dos dados. As queries SQL utilizadas para gerar essas visões podem ser encontradas no arquivo `queries_dash_vendas` presente nesse diretório na pasta `Queries`. As consultas foram realizadas utilizando **PostgreSQL** no software **PgAdmin 4**.

O dashboard completo pode ser visualizado na imagem abaixo:

![](/Imagens/Dash_vendas.png) 
