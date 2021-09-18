# Laboratório 05 - Marcadores e Taxonomia em Cypher

Estrutura de pastas:

├── README.md  <- arquivo apresentando a tarefa  

# Aluno
* Nome: Bruno Henrique Emidio Leite RA: 214017

## Tarefa de Cypher sobre Marcadores e Taxonomia
## Tarefa 1

Escreva em Cypher uma consulta que retorne os marcadores da categoria Serviços, sem considerar as categorias subordinadas

## Resolução

  MATCH (m1:Marcador) MATCH (c1:Categoria {id:"Serviços"}) WHERE (m1)-[:Pertence]->(c1) RETURN m1
  
## Tarefa 2

Escreva em Cypher uma consulta que retorne os marcadores da categoria Serviços, considerando as categorias subordinadas.

MATCH (m1:Marcador) MATCH (c1:Categoria) MATCH (c2:Categoria {id:"Serviços"}) WHERE (c1)-[:Superior]->(c2) AND  (m1)-[:Pertence]->(c1) OR (m1)-[:Pertence]->(c2) RETURN m1
