title: Introdução ao NoSQL e MongoDB
date: 2016-02-13 21:23
tags: nosql, mongodb
slug: intro-nosql-mongo
author: Antonio Alves Lima
email: antonio.malves.lima@gmail.com
summary: Apresentação do NoSQL e uma Introdução ao MongoDB. Isso é um resumo do que foi apresentado na primeira aula do workshop de Be MEAN.

### NoSQL

Devido ao grande crescimento de aplicações web e a cada vez ser mais comum a grande quantidade de informações,
criou-se um problema: Como lidar com isso de maneira eficaz?

O NoSQL surgiu da necessidade de uma melhor performance e escalabilidade, pois os bancos relacionais são muito restritos a isso.
Quanto mais dados no banco, torna-se necessário mais máquinas e mais memória. O movimento NoSQL não tem como objetivo substituir
 o modelo relacional mas sim o fim do modelo relacional como a única solução correta ou válida.

### As principais diferenças entre o modelo relacional e o não relacional são:

* Os bancos de dados não relacionais não suportam operações de junções de tabela.
* Não existe normalização, isto é, são shemaless, diferentemente de bancos relacionais.
    * Utilizar schemaless, significa não se preocupar com os tipos de dados, nomes de colunas, nome de tabelas e seus relacionamentos. Não há necessidade de realizar normalização.
* Os bancos de dados relacionais são verticalmente escaláveis enquanto os NoSQL's são horizontalmente escaláveis.

#### Tipos de bancos NoSQL

Como os bancos NoSQL não usam o modelo relacional irei apresentar quais os modelos disponíveis no NoSQL:

* Chave-Valor
    * É armazenado uma chave e um valor, esse valor pode ser qualquer informação, suporte a maior carga de dados.
    * Exemplo: Memcache, SimpleDB.
* Documento
    * Armazena documento, sem a necessidade de definir sua estrutura. Os documentos são armazenados
 em conjunto mesmo que não tenham nada em comum. Uma outra característica importante desse modelo é a tendência
 de desnormalização dos dados, deixando em um só documento todas as informações relacionadas desejadas.
	* Exemplo: CouchDB, MongoDB
* Grafo
    * > "Grafo é uma estrutura de dados que conecta um conjunto de vértices através de um conjunto de arestas.
Os bancos de dados de grafo modernos suportam estruturas de grafo multi-relacionais, onde existem tipos diferentes
de vértices (representando pessoas, lugares, itens) e diferentes tipos de arestas (como por exemplo amigo de,
 mora em, comprado por)[...].” - Marko Rodriguez (arquiteto de sistemas de grafo da AT&T Interactive)
    * Exemplo: Neo4j, monetdb, ArangoDB
* Mistos
    * São os bancos que possuem dois ou mais tipos de modelos. Como exemplo existe o [ArangoDB](https://www.arangodb.com/) que utiliza o modelo de Documento e Grafo.


### MongoDB

O [MongoDB](https://www.mongodb.org/) é derivado da palavra humongous em inglês, que quer dizer gigantesco. Ele é um banco que utiliza o conceito de modelo de Documentos.

Foi criado com o objetivo de trabalhar com o modelo de documentos em vez de linhas, extremamente rápido, amplamente escalável e fácil de usar. Para isso foi deixado algumas funcionalidades de lado, o que o torna não recomendável para determinadas situações, como por exemplo não deve ser usado para um sistema de contabilidade, pois o MongoDB não possui suporte a transações.

Armazena os seus documentos na coleção em formato BSON - que é a abreviatura de binary JSON (JSON binário) - desenvolvido pela equipe do MongoDB. No entanto a manipulação dos dados, tanto para escrita como para consulta dos dados, é feita usando o formato JSON


#### Alguns serviços do MongoDB

* mongod
    * inicia o servidor do MongoDB.
* mongo
    * inicia o cliente do Mongo.
* mongoimport
    * serviço utilizado para importação dos dados em formato JSON ou CSV para uma coleção no BD.
    * `mongoimport --db nome_do_banco --collection nome_da_colecao --drop --file data.json`
* mongoexport
    * serviço utilizado para exportação dos dados de uma coleção para o formato JSON.
    * `mongoexport --db nome_do_banco --collection nome_da_colecao --out minha_colecao.json` 


### Últimas considerações

Esta é a primeira parte do artigo no qual resolvi compartilhar meu conhecimento e o que estou aprendendo no workshop do Be MEAN. 
Logo irei colocar o link para os outros post que publicarei no blog.

