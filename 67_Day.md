10 Junio 2024

## Progreso de hoy:
- Inicio de curso con Node JS 
## Lo que aprendí 
- Creación de relaciones con Cypher y Neo4jGraph


Crear relaciones 
```
cypher = """
  MATCH (actor:Person)-[:ACTED_IN]->(movie:Movie) 
  RETURN actor.name, movie.title LIMIT 10
  """
kg.query(cypher)
```

Crear relaciones con condiciones 
```
cypher = """
  MATCH (nineties:Movie) 
  WHERE nineties.released >= 1990 
    AND nineties.released < 2000 
  RETURN nineties.title
  """
```

Consultar relaciones 
```
cypher = """
  MATCH (tom:Person {name:"Tom Hanks"})-[:ACTED_IN]->(m)<-[:ACTED_IN]-(coActors) 
  RETURN coActors.name, m.title
  """
kg.query(cypher)
```
Crear elemento 
```
cypher = """
	CREATE (pablo:Person {name:Pablo Sotres})
	RETURN pablo 
	"""
```

Borrar elemento
```
cypher = """
	MATCH(pablo: Person) {name:"Pablo Sotres}
	DELETE
	"""
```
## **Pensamientos**:
- Es interesante la creación de relaciones, aunque es complicado de visualizar. Quiero ver cómo se van a ver las relaciones en los Python Notebooks 
## Link to work: 
- Curso https://learn.deeplearning.ai/courses/knowledge-graphs-rag/lesson/3/querying-knowledge-graphs 
## Plan para mañana: 
- Continuar curso

