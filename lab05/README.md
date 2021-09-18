# Laboratório 05 - Marcadores e Taxonomia em Cypher

# Aluno
* Nome: Bruno Henrique Emidio Leite RA: 214017

## Tarefa de Cypher sobre Marcadores e Taxonomia
## Tarefa 1

Escreva em Cypher uma consulta que retorne os marcadores da categoria Serviços, sem considerar as categorias subordinadas.
## Resolução

  MATCH (m1:Marcador) MATCH (c1:Categoria {id:"Serviços"}) WHERE (m1)-[:Pertence]->(c1) RETURN m1
