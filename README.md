# LDM · Tarea XPath · Manuel Parrilla Lahoz

Práctica de consultas XPath sobre un catálogo de recursos técnicos en XML.

## Objetivo
Resolver 4 retos aplicando filtros, atributos, negaciones y selección de nodos en XPath.

## Estructura del repositorio

```text
/xml/recursos.xml
/xml/recursos.xsd
consultas_xpath.xbook
README.md
```

## Retos resueltos

### 1) Filtrado por contenido y estado
**Enunciado:** obtener los títulos de los recursos con categoría `CSS` y disponibles.

```xpath
//bibliotecaTecnica/recurso[categoria='CSS' and disponible='true']/titulo/string()
```

### 2) Atributos y negaciones
**Enunciado:** obtener los ID de los recursos cuyo formato no sea `PDF`.

```xpath
//recurso[@formato!='PDF']/@id
```

### 3) Múltiples nodos (autores)
**Enunciado:** obtener solo el primer autor del primer recurso publicado después de 2015.

```xpath
//bibliotecaTecnica/recurso[anio > 2015][1]/autor[1]/string()
```

### 4) Nivel y categoría
**Enunciado:** obtener los títulos de recursos de categoría `XPath` o `XSLT` con nivel `5`.

```xpath
//bibliotecaTecnica/recurso[(categoria='XPath' or categoria='XSLT') and nivel=5]/titulo/string()
```



## Autor
- Alumno/a: **Manuel Parrilla Lahoz**
- Módulo: **LDM**
- Fecha: **19/03/2026**

