---
title: "Comandos útiles"
weight: 4
---
# Comandos útiles
Como ya se menciono previamente la terminal es la principal forma de interacción con los sistema tipo Unix, por esta razón se han desarrollado una gran cantidad de herramientas para diferentes propósitos que funcionan completamente dentro de una terminal, estas herramientas incluyen reproductores de música, navegadores web, etc.

En esta sección se presentan algunas de las herramientas de uso mas común en la terminal. 

## Fecha del sistema
Para poder ver la fecha y hora del sistema tenemos el comando `date`, para ver la hora y fecha actuales solo hace falta ejecutar el comando sin ninguna opción.

```bash
$ date
```

>[!note] Nota
>
>Este comando no solo muestra la hora y fecha, también se puede usar para cambiar esta información. 
>
>Este comando da la salida en el formato que se le solicite.

## Calendario
El comando del calendario es `cal`, este comando nos puede mostrar cualquier año, una cantidad variable de meses, entre otras opciones.
```bash
$ cal
```

Para mas información consultar el manual de cal.

## Calculadora
Siempre es útil tener una calculadora a la mano. `bc` es una calculadora muy potente que nos permite realizar las operaciones matemáticas elementales así como definir variables y funciones, también cuenta con las funciones matemáticas mas comunes.

```bash
$ bc -l
```

## Buscador de archivos
Buscar archivos es una tarea muy común, el comando que realiza esto es `find`,
este comando no solo nos permite filtrar nuestra búsqueda por el nombre del archivo.

También nos permite definir una acción a realizar para cada uno de los archivos que coinciden con nuestros criterios de búsqueda.

```bash
$ find <opción>... <directorio> <expresión>
```

En este comando `<expresión>` define los criterios de búsqueda y las acciones que se realizaran sobre los archivos filtrados.


## Buscador de texto
Debido a que en Unix manejamos una gran cantidad de archivos de texto es necesario tener una herramienta que nos permita buscar texto de forma eficiente, para esto existe `grep`, con este comando podemos buscar tanto texto explicito como patrones de texto.

Esta herramienta solo nos mostrara las lineas del archivo que coinciden con nuestros criterios de búsqueda.

```bash
$ grep <opción>... -F -e <texto>... <archivo>...
$ grep <opción>... -e <patrón>... <archivo>...
```