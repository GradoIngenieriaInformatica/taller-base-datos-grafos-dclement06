MATCH (p1:Persona)-[:USA_TECNOLOGIA]->(t:Tecnologia)
WITH p1, collect(id(t)) AS techsP1
MATCH (p2:Persona)-[:USA_TECNOLOGIA]->(t2:Tecnologia)
WHERE p1 <> p2
WITH p1, techsP1, p2, collect(id(t2)) AS techsP2
WHERE all(x IN techsP1 WHERE x IN techsP2)
RETURN DISTINCT p1.nombre AS Persona