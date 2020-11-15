# MySql Clase 2

## Titulo pendiente

> Describir los pasos del ciclo de vida de una base de datos

## Varios caminos, mismo resultado

### Desde CLI

#### Visualizacion de Estructura

Para ver todas las bases de datos

``` mysql
SHOW DATABASES;
```

Para crear una base de datos
```mysql
CREATE DATABASE <nombre de la base de datos>
```

Para seleccionar/trabajar sobre una base de datos.

``` mysql
# Sintaxis: USE <tu_base_de_datos>
USE dsajhda;
```

Para listar tablas

``` bash
# SHOW tables: SHOW TABLES;
```

``` mysql

```

Para crear una tabla

``` mysql
# sintaxis:
# CREATE TABLE <nombre_de_tu_tabla> (
#    <nombre de la columna> <tipo de dato> <extras>,
#    <nombre de la columna> <tipo de dato> <extras>
# );

CREATE TABLE users(
    id INT NOT NULL AUTO INCREMENT, 
    name VARCHAR(50), 
    tinder_url VARCHAR(50)
);
```

Describir datos de la tabla
```mysql
#sintaxis:
#DESCRIBE <nombre_de_tu_tabla>;
```

Insertar datos a la tabla (2 formas)

1. FACIL y BONITO

```mysql
#Sintaxis:
#INSERT INTO <nomre_de_tu_tabla>
#(NOMBRE, ) #<PASAR CUALES CAMPOS QUIERO INSERTAR> 
#("CAMPOS",) #<LOS CAMPOS TIENEN QUE SEGUIR LA ESTRUCTURA>
INSERT INTO users
        (nombre, tinder_url)
    VALUES
        ("willy", "papa Willy.com"),
        ("Sole", "404.com");

# Si, se puede insertar vacio
INSERT INTO users () VALUES ();
INSERT INTO users VALUES (5, "beatriz", "larioz@ipn.mx")
```

2. Se puede hacer (No recomendable)
```mysql
#Sintaxis:
INSERT INTO users VALUES (5, "beatriz", "larioz@ipn.mx")
```

Para borrar en tabla

> Sintaxis:
> DELETE FROM <tu_tabla> WHERE [<condiciones de borrado>](8)

``` mysql
#Especificar para que no borre todo
```

Update 

> Sintaxis
> UPDATE <tu_tabla> SET <clave = valor nuevo, valor = nuevo>

```
UPDATE USERS
    SET
        nombre = "nuevonombre",
        tinder_url = "holaTinder.com"
    WHERE
        nombre = "nasho";
```

Que es lo que hay dentro?

```mysql
SELECT * FROM table_name; 
```

#### Visualizacion de datos



### Trucos de la CLI

Puedes usar comandos del sistema dentro de la terminal de MySQL usando `"\!"`

``` bash
# Ejemplo
\! clear
```