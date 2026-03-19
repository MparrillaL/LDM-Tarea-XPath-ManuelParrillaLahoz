# LDM-Tarea-XPath-ManuelParrillaLahoz

Práctica de consultas XPath sobre un catálogo técnico en XML.

Estructura del repositorio
xml/recursos.xml: archivo de datos (30 recursos).
xml/recursos.xsd: esquema de validación.
consultas_xpath.xbook: notebook con enunciado, consulta y resultado de cada reto.
README.md: documentación de la práctica.
Retos resueltos
Reto 1. Filtrado por contenido y estado
Obtener los títulos de los recursos con categoría CSS y disponibles.

XPath:
//bibliotecaTecnica/recurso[categoria='CSS' and disponible='true']/titulo/text()

Reto 2. Atributos y negaciones
Obtener los ID de los recursos cuyo formato no sea PDF.

XPath:
//recurso[@formato!='PDF']/@id

Reto 3. Manejo de múltiples nodos (Autores)
Obtener solo el primer autor del primer recurso publicado después de 2015.

XPath:
//bibliotecaTecnica/recurso[anio > 2015][1]/autor[1]/text()

Reto 4. Nivel y categoría
Obtener los títulos de los recursos de categoría XPath o XSLT con nivel 5.

XPath:
//bibliotecaTecnica/recurso[(categoria='XPath' or categoria='XSLT') and nivel=5]/titulo/text()

Notas técnicas
En este XML, formato es un atributo del recurso, por eso se usa @formato.
El campo correcto para la dificultad es nivel.
Para mostrar el contenido textual del nodo se usa text().
Autor
Alumno: Manuel Parrilla Lahoz
Módulo: LDM
Fecha: 19/03/2026
