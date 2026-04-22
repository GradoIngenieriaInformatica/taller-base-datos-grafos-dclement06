MATCH (p:Persona)
OPTIONAL MATCH (p)-[:PARTICIPA_EN]->(pr:Proyecto)
RETURN p.nombre AS Persona, count(pr) AS NumeroDeProyectos