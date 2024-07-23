# Projeto de Portfólio: Análise de Dados com SQL

Este projeto de portfólio é o resultado dos estudos realizados no curso "[SQL para Análise de Dados: Do básico ao avançado](https://www.udemy.com/course/sql-para-analise-de-dados/?couponCode=24T7MT72224)", ministrado por [Midori Toyota](https://www.linkedin.com/in/midoritoyota/). O curso foi estruturado em torno de um cenário fictício de e-commerce, simulando uma plataforma onde diversas lojas vendem carros. Utilizando dados fictícios gerados para representar as interações dos clientes com o site da empresa, o objetivo foi construir um sistema realista e analisar as informações obtidas para obter insights valiosos.

O projeto apresenta análises detalhadas e relatórios que demonstram a aplicação prática dos conceitos aprendidos durante o curso. As análises fornecem uma compreensão aprofundada sobre o comportamento dos clientes e o desempenho das vendas, destacando a eficácia das técnicas de SQL em um contexto empresarial. Através desse projeto, foi possível evidenciar como a utilização de SQL pode revelar padrões e informações cruciais para a tomada de decisões estratégicas.

## Índice

- [Estrutura do Banco de Dados](#estrutura-do-banco-de-dados)
- [Tabelas no Schema sales](#tabelas-no-schema-sales)
- [Dados](#dados)
- [Dashboard de Acompanhamento de Vendas](#dashboard-de-acompanhamento-de-vendas)
  - [Indicadores e Análises](#indicadores-e-análises)
- [Dashboard de Análise do Cliente](#dashboard-de-análise-do-cliente)
  - [Estrutura do Dashboard](#estrutura-do-dashboard)
- [Agradecimentos](#agradecimentos)

## Estrutura do Banco de Dados
O projeto utiliza um banco de dados relacional dividido em dois schemas distintos, conforme ilustrado na imagem abaixo. Essa divisão permite uma organização mais clara e eficiente dos dados, facilitando a realização de análises complexas.

O primeiro schema, denominado **sales**, contém a maior parte dos dados gerados pelo sistema fictício de e-commerce. Este schema inclui informações cruciais sobre interações dos clientes, detalhes dos produtos, dados das lojas e registros das vendas. Essa estruturação permite uma visão abrangente e detalhada das operações de vendas e do comportamento dos clientes no site.

O segundo schema, chamado **temp_tables**, é dedicado a tabelas auxiliares que dão suporte a diversas análises. Essas tabelas são utilizadas para armazenar dados temporários, resultados intermediários de consultas e outras informações auxiliares que facilitam a execução de análises detalhadas e a geração de relatórios. A utilização deste schema separado ajuda a manter o schema principal mais organizado e focado nas transações essenciais.

![](/Imagens/Estrutura_Banco.PNG) 

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

## Dashboard de Acompanhamento de Vendas

O objetivo do primeiro projeto, conforme proposto por [Midori Toyota](https://www.linkedin.com/in/midoritoyota/), foi desenvolver um dashboard de vendas que destaca os principais indicadores de desempenho e os drivers dos resultados para o mês de agosto de 2021. O dashboard foi projetado para fornecer uma visão clara e compreensiva do desempenho de vendas da empresa durante esse período.

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

## Dashboard Análise do Cliente

O objetivo do segundo projeto foi criar um dashboard para analisar as principais características dos leads que visitam a página do e-commerce. A intenção era gerar insights sobre o perfil de cliente ideal (ICP) para o e-commerce, ajudando a entender melhor quem são os visitantes e como direcionar estratégias de marketing e vendas.

### Estrutura dashboard

O dashboard é dividido em duas partes principais:

1. **Análise dos Clientes**:

  * **Características Demográficas**: Inclui gráficos que mostram a distribuição dos clientes por gênero, status profissional, faixa salarial e faixa etária. Por exemplo, observamos que cerca de 67% dos clientes recebem entre R$ 0 a R$ 10.000 por mês e quase 49% estão na faixa etária de 20 a 40 anos.

2. **Análise dos Produtos**:

  * **Preferências e Classificações**: Apresenta dados sobre os produtos mais procurados, classificando-os como novos ou seminovos (com base na regra de que veículos com mais de 2 anos são considerados seminovos e os demais são novos). O dashboard também analisa a faixa etária dos carros e a quantidade de procura. Constatamos que mais de 90% das pesquisas são por carros seminovos.

  * **Marcas Mais Procuradas**: Identifica as marcas mais buscadas, com Fiat, Volkswagen e Chevrolet liderando a lista. Isso pode estar relacionado ao fato de que essas marcas oferecem modelos mais acessíveis, que são frequentemente procurados por clientes na faixa etária e faixa salarial mencionadas.

Essa análise permite compreender melhor o perfil dos clientes e suas preferências, facilitando a adaptação das ofertas e estratégias de marketing para atender às necessidades e expectativas do público-alvo.

O dashboard completo pode ser visualizado na imagem abaixo:

![](/Imagens/Dash_clientes.png)

## Agradecimentos

Gostaria de expressar minha sincera gratidão a [Midori Toyota](https://www.linkedin.com/in/midoritoyota/) pelos conhecimentos valiosos compartilhados no curso "[SQL para Análise de Dados: Do básico ao avançado](https://www.udemy.com/course/sql-para-analise-de-dados/?couponCode=24T7MT72224)". Os ensinamentos fornecidos foram fundamentais para a realização desses projetos e para o aprimoramento das minhas habilidades em SQL.

O curso se destacou pela sua abordagem clara e acessível, e a didática da Midori é excepcional. Recomendo fortemente este curso para qualquer pessoa que deseje aprofundar seus conhecimentos em SQL, pois ele combina teoria e prática de maneira eficaz, tornando o aprendizado leve e envolvente.

Obrigado, Midori, por contribuir significativamente para o meu desenvolvimento profissional!
