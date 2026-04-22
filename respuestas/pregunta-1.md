MATCH (p:Persona)-[:TRABAJA_EN]->(e:Empresa)
RETURN p.nombre AS Persona, e.nombre AS Empresass