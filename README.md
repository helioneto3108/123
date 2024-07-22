# Projeto de Portfólio: Análise de Dados com SQL

Este projeto foi desenvolvido com base nos estudos do curso "[SQL para Análise de Dados: Do básico ao avançado](https://www.udemy.com/course/sql-para-analise-de-dados/?couponCode=24T7MT72224)", ministrado por [Midori Toyota](https://www.linkedin.com/in/midoritoyota/). O curso foi conduzido em um cenário fictício de e-commerce, simulando uma empresa que vende carros. Utilizando dados fictícios gerados para representar interações de clientes com o site da empresa, o objetivo foi criar um sistema realista e analisar as informações obtidas. Como resultado final, o projeto apresenta análises detalhadas e relatórios que evidenciam a aplicação prática dos conhecimentos adquiridos ao longo do curso. Essas análises fornecem insights valiosos sobre o comportamento dos clientes e ajudam a entender melhor o desempenho das vendas, demonstrando a eficácia das técnicas de SQL no contexto de negócios.


## Estrutura do banco de dados
O projeto utiliza um banco de dados relacional dividido em dois schemas, conforme ilustrado na imagem abaixo. O primeiro schema, **sales**, contém a maior parte dos dados gerados pelo sistema fictício de e-commerce. Já o segundo schema, **temp_tables**, abriga tabelas auxiliares que suportam diversas análises.

![](https://github.com/helioneto3108/Analise_Dados_PostgreSQL/blob/main/Imagens/Estrutura_Banco.PNG) 


<div align="center">
<img src = "https://github.com/user-attachments/assets/4474d9b0-37d8-4bab-9068-97e56ab17a58" width="3000px" />
</div>

### Tabelas no Schema sales:
* **funnel**:  Esta é a tabela principal que registra todas as interações dos clientes com o site. Ela captura cada etapa do funil de vendas, desde a visita inicial ao site até qualquer ação subsequente, incluindo visualizações de produtos, adições ao carrinho e compras. Também inclui interações onde o cliente não realizou uma compra, fornecendo uma visão completa do comportamento dos usuários no site.
* **customers**: Armazena informações detalhadas sobre os clientes, como nome, e-mail, e outras características relevantes que ajudam a identificar e analisar o comportamento dos usuários.
* **stores**: Fornece informações sobre as lojas que estão oferecendo produtos aos clientes. Inclui dados como nome da loja e outras características da loja.
* **products**: Contém dados sobre os produtos que os clientes estão procurando. Inclui informações como nome do marca, modelo, preço e outras especificações relevantes.
