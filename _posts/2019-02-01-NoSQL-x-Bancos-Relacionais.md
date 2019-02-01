---
layout: post
title:  "NoSQL x Bancos Relacionais"
date:   2019-02-01
desc: "Conceitos teoricos"
keywords: "Life,Tese,Monografia,blog,easy"
categories: [Database]
tags: [SQL,Bancos Relacionais,NoSQL]
icon: fa-database
---

## **NoSQL x Bancos Relacionais**
-

## **1 Introdução**

Neste capitulo serão apresentados os principais conceitos, definições e temas que são abordados posteriormente na condução da monografia.

## **2 Bancos de dados**

Bancos de dados são definidos como coleções organizadas de dados (BEYNON-DAVIES, 2004). Apesar de comumente denominarmos como banco de dados todo o sistema gerenciador de bancos de dados ele se refere somente a coleção e aos dados. O sistema que manipula os dados, transações, problemas e outros aspectos é o Sistema de Gerenciamento de Banco de Dados (SGBD) (HADJIGEORGIOU, 2013).

Designs e implementações mais antigas de bancos de dados eram baseadas no uso de listas ligadas para criar relações entre os dados e para encontrar dados. Esse modelo não era padronizado e um treinamento intensivo, era requerido para que se conseguisse utilizar este modelo com eficiência (HADJIGEORGIOU, 2013).

Abaixo são apresentados alguns importantes tipos de Sistemas de gerenciamento de banco de dados.

## **3 Bancos de dados relacionais**

Bancos de dados relacionais usam a convenção de bases de dados que contem tabelas, onde cada coluna representa um campo e cada linha representa um registro. Tabelas podem ser relacionadas ou ligadas umas com as outras, com o uso do conceito de chaves estrangerias ou colunas em comum. Em um nível mais abstrato tabelas representam entidades, como usuários, produtos, empresas, entre outras. Esta abstração é muito útil para se desenhar o esquema do banco de dados onde objetos do mundo real precisam ser mapeados para a base de dados (HADJIGEORGIOU, 2013).

Um exemplo de design do esquema de uma base de dados pode ser visualizado na Figura 1.

<span style="display:block;text-align:center">![](https://media.licdn.com/dms/image/C4D12AQGBF_7nWbFgHg/article-inline_image-shrink_1000_1488/0?e=1554336000&v=beta&t=s4IJoUwBQfB1dnCXn_wu98MBwdRhLxroitXxUPvPlw4)</span>

Figura 1. Um exemplo de esquema de dados (Hadjigeorgiou, 2013).

Um importante aspecto do design dos bancos de dados relacionais se refere a sua normalização.

A normalização de um banco de dados é dividida em três formas idealizadas por Codd, E.F em 1970 em seu livro "A Relational Model of Data for Large Shared Data Banks", abaixo segue um breve resumo de cada forma:

-   Primeira Forma Normal (ou 1FN) A normalização para a primeira forma normal elimina grupos repetidos, pondo-os cada um em uma tabela separada, conectando-os com uma chave primária ou estrangeira.
-   Segunda Forma Normal (ou 2FN) requer que não haja dependência funcional não trivial de um atributo que não seja a chave, em parte da chave candidata.
-   Terceira Forma Normal (ou 3FN) requer não haver dependências funcionais não triviais de atributos que não sejam chave, em qualquer coisa exceto um super-conjunto de uma chave candidata.

## **4 Bancos de dados NoSQL**

Apesar de bancos de dados relacionais ainda serem ótimos para alguns tipos de aplicações, por terem se aperfeiçoado por seu prolongado tempo de existência e sua ampla adoção em inúmeros casos, infelizmente para a maioria das arquiteturas de software modernas os bancos relacionais começam a demostrar sinais de envelhecimento, não entregando o desempenho esperado, especialmente quando é necessário lidar com grandes conjuntos de dados (bilhões) e esquemas dinâmicos (KAUR, RANI, 2013). Cada vez mais aceitamos que vivemos em um mundo onde o modelo de domínio das soluções é constantemente alterado, a tal ponto de metodologias de desenvolvimento que aceitam tais mudanças constantes se tornem cada vez mais populares. Tais fatos descritos acima neste capitulo junto com diversos outros levaram a criação, maior interesse e crescente adoção dos bancos de dados não relacionais (KAUR, RANI, 2013).

O Termo NoSQL é um acrônimo para “Not Only SQL” que foi primeiramente introduzido por Carlo Strozzi em 1998 e foi o nome de seu banco de dados relacional _opensource_ que não oferecia uma interface SQL (STROZZI, 2013). O termo foi reintroduzido em Outubro de 2009 por Eric Evans em um evento denominado no:sql(east), organizado para a discussão de bancos de dados open source distribuídos (EVANS, 2009). O termo foi uma tentativa de descrever o aumento do uso de bancos de dados não relacionais, na segunda metade da década dos anos 2000, onde um número cada vez maior de usuários da chamada Web 2.0 começou a reconhecer a ineficiência de bancos de dados relacionais, para lidar com um grande volume de dados gerados por essas novas aplicações (KAUR, RANI, 2013).

O termo NoSQL, talvez não fosse o melhor para definir estes tipos de bancos, pois seu principal diferencial não esta na forma como são feitas as _“querys”_ nos bancos de dados, momento este em que realmente é utilizado o SQL, mas sim na forma como armazenamos as informações, porém o termo se espalhou rapidamente e se tornou um sinônimo destes novos tipos de banco para a comunidade (KAUR, RANI, 2013). O Google foi à primeira empresa a organizar e liderar o movimento a favor de bancos de dados NoSQL com a introdução de seu banco de dados BigTable (CHANG et al., 2006) em 2006 seguido pela Amazon e seu bancos de dados Dynamo (HASTORUN et al., 2007) em 2007.

## **5 Bancos relacionais X Bancos NoSQL**

Há basicamente quatro fatores que distinguem os bancos de dados relacionais tradicionais dos bancos NoSQL são eles: variedade, estrutura, escalabilidade e foco (HOBERMAN, 2014). Abaixo uma comparação entre esses fatores.

Tabela 1. Comparação Bancos relacionais x Bancos NoSQL

<span style="display:block;text-align:center">![](https://media.licdn.com/dms/image/C4D12AQEExD5rdT649Q/article-inline_image-shrink_1500_2232/0?e=1554336000&v=beta&t=jzvqfgKNN1BfybXt7sjj7i5K6R9yeW8n6nj9asfcaA0)</span>

### 5.1 Variedade

Bancos de dados relacionais possuem apenas uma estrutura, a relacional onde campos são armazenados em linhas de uma tabela, cada coluna possui um pedaço especifico do dado daquela linha. Quando precisamos de dados de mais de uma tabela, elas são “unidas”, por exemplo, os pedidos podem estar em uma tabela e clientes em outra, quando precisamos saber quais pedidos um determinado cliente efetuou, nos unimos à tabela de pedidos a tabela de clientes para obter essa informação.

<span style="display:block;text-align:center">![](https://media.licdn.com/dms/image/C4D12AQHahYFzmkg72g/article-inline_image-shrink_1000_1488/0?e=1554336000&v=beta&t=F7GENW_pYC0s0WfifIWhs-MgO3YdmnQY8p4OnxbTdA8)</span>

Figura 2. Variedade de bancos de dados NoSQL (Hoberman, 2014).

Bancos NoSQL possuem quatro grandes variedades, as quais iremos abordar com mais detalhes nos próximos capítulos, são ela s; orientados a documentos, orientados a colunas, “key-value” e orientados a grafos. Cada uma destas variedades possui a sua própria maneira de armazenar os dados, os bancos relacionais têm sido escolhidos para todos os tipos de soluções e cenários analíticos, porém bancos NoSQL possuem diversas vantagens em vários cenários específicos, por exemplo, um banco orientado a grafos normalmente seria usado em um cenário onde um banco orientado a documentos não apresentaria o desempenho ou modelo apropriado (HOBERMAN, 2014).

### 5.2 Estrutura

Bancos de dados relacionais possuem uma estrutura predefinida, sendo assim caso seja necessário adicionar uma nova coluna em uma tabela, devemos primeiramente alterar a estrutura da tabela, o que implicitamente adicionará uma nova coluna a cada registro já existente na tabela, antes de podemos preencher este novo campo com uma informação relevante, já bancos de dados NoSQL normalmente possuem estruturas de dados dinâmicas, sendo assim novos tipos de informação podem ser adicionadas sem a necessidade de recarregar ou reconstruir a estrutura do banco de dados. (HOBERMAN, 2014)

### 5.3 Escalabilidade

Inicialmente bancos relacionais não foram concebidos para armazenar informações dispersas e serem facilmente escaláveis, seu modelo de dados é baseado em uma arquitetura que contem uma única máquina, sendo assim se queríamos melhorar o desempenho do banco deveríamos adicionar recursos a esta máquina ou migrar o banco para uma máquina que possua mais recursos, porém nos dias atuais desenvolvedores normalmente estão esperando trabalhar com uma grande quantidade de registros (milhões), cenário este que não era a realidade quando o conceito dos bancos relacionais foi concebido por volta dos anos 70.

Escalabilidade é um dos assuntos mais discutidos nos dias atuais, pois aplicações web tem recebido uma enorme atenção (KAUR, RANI, 2013), escalabilidade pode ser alcançada de duas formas tradicionalmente verticalmente ou horizontalmente. Escalabilidade vertical normalmente é mais fácil de ser alcançada, pois envolve apenas o aumento de recursos físicos da máquina em questão sejam eles de memoria, processador, disco, entre outros. Escalabilidade horizontal por outro lado prove uma maior flexibilidade, pois apenas adiciona mais um nó ao sistema podendo este nó ser apenas mais uma instancia de uma máquina virtual ou mais uma máquina adicionada fisicamente ao cluster de máquinas.

Bancos de dados tradicionais normalmente somente podem ser escalados verticalmente enquanto bancos de dados NoSQL normalmente podem ser escalados verticalmente, horizontalmente ou em ambos os modelos, porém a estratégia mais adotada é a escalada horizontal.

### 5.4 Foco

Um aspecto importante dos bancos de dados relacionais que garantem a confiabilidade das transações é a aderência das propriedades **ACID:** **A**tomicity (Atômicas), **C**onsistency (Consistência), **I**solation (Isoladas), **D**urability (Durabilidade) [1], estas propriedades são descritas abaixo dentro do contexto de banco de dados.

-   **Atomicidade**: Todas as atualizações feitas por uma transação são efetivadas no BD ou nenhuma delas (tudo ou nada);
-   **Consistência**: A execução de uma transação deve garantir que o BD passe de um estado consistente para outro;
-   **Isolamento**: Eventos dentro de uma transação devem ser transparentes para outras transações executando concorrentemente (sincronização de transações);
-   **Durabilidade**: Sempre que uma transação é executada com sucesso, o SGDB deve garantir que o seu resultado sobreviva a qualquer falha subsequente.

Já bases NoSQL possuem um foco menor na integridade dos dados e um foco maior no desempenho e na disponibilidade seguindo o acrônimo BASE **B**asically Available (Basicamente Disponível), “**S**oft-state”, **E**ventual consistency (Consistente eventualmente) (HOBERMAN, 2014).

-   **Basicamente Disponível:** Há uma resposta para cada query realizada, porém esta resposta pode informar que ocorreu um erro na execução da query ou ate mesmo que a informação retornada pode estar defasada, pois ainda está passando por uma mudança de estado. Um exemplo deste cenário: um vendedor de livros que ao consultar o inventário da livraria obtém a informação de quantos livros ela possui, porém também recebe um alerta informando que a informação não foi totalmente atualizada nas ultimas 24 horas podendo assim estar defasada.
-   **“Soft-state”:** significa que os bancos de dados NoSQL trabalham atualizando continuamente os dados com cada atualização realizada, o que tornaria a informação de nosso exemplo anterior em momentaneamente inconsistente, pois já pode ter ocorrido uma venda de um livro que não foi completamente atualizada em todo o banco.
-   **Eventualmente consistente:** Consistência significa que o dado atual reflete qualquer mudança que possa ter ocorrido ate aquele momento no tempo. Bases NoSQL eventualmente se tornam consistentes, porém somente quando param de receber novos dados para inserção ou atualização. Em nosso exemplo os dados do inventário podem estar consistentes minutos ou horas após a compra de um livro.

## **Referências Bibliográficas**

(BEYNON-DAVIES, 2004) BEYNON-DAVIES P. **Database Systems**. Palgrave Macmillan, 3rd edition. . 2004, p. 6

(HADJIGEORGIOU, 2013) HADJIGEORGIOU, Christoforos. **RDBMS vs NoSQL: Performance and Scaling Comparison.** 2013. Tese (MSc in High Performance Computing) - The University of Edinburgh, 2013

(KAUR, RANI, 2013) KAUR, Karamjit; RANI, Rinkle. **Modeling and Querying Data in NoSQL Databases** In: IEEE International Conference on Big Data, 6-9 Outubro 2013, Silicon Valley, CA, USA Anais eletrônicos disponivel em: [http://ieeexplore.ieee.org/xpl/articleDetails.jsp?tp=&arnumber=6691765](http://ieeexplore.ieee.org/xpl/articleDetails.jsp?tp=&arnumber=6691765) Acesso em: 20 Abril 2015.

(STROZZI, 2013) STROZZI, Carlo. (2013) **NoSQL: A non-sql relational database management system.** [Online]. Disponível em: [http://www.strozzi.it/cgi-bin/CSA/tw7/I/en US/nosql/Home-Page](http://www.strozzi.it/cgi-bin/CSA/tw7/I/en%20US/nosql/Home-Page), Acesso em: 05 Maio 2015.

(EVANS, 2009) EVANS, Eric 2009, **NoSQL conference**. [Online]. Disponível em: [https://nosqleast.com/2009/](https://nosqleast.com/2009/) Acesso em: 05 Maio 2015.

(CHANG et al., 2006) CHANG, Fay, et al., **“Bigtable: a distributed storage system for structured data,”** em “Proceedings of the 7th USENIX Symposium on Operating Systems Design and Implementation - Volume 7” Berkeley, CA, USA: USENIX Association, 2006, pp. 15–15. [Online]. Disponível em: [http://dl.acm.org/citation.cfm?id=1267308.1267323](http://dl.acm.org/citation.cfm?id=1267308.1267323) Acesso em: 05 Maio 2015.

(HASTORUN et al., 2007) D. Hastorun; M. Jampani; G. Kakulapati; A. Pilchin; S. Sivasubramanian, P. Vosshall, and W. Vogels, **“Dynamo: amazons highly available key-value store,”** In Proc. SOSP , 2007, pp. 205–220.

> Written with [StackEdit](https://stackedit.io/).