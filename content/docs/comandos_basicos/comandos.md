---
title: "Comandos basicos para el sistema de archivos"
weight: 2
---

## Comandos imprescindibles
Primero revisaremos algunos comando básicos que son de mucha utilidad cuando empiezas a usar una terminal de comandos.

### ¿Como obtener ayuda sobre la utilización de algún comando?
En Linux la mayoría de los comandos que tiene disponible sistema tienen información que nos ayuda a entender como se pueden usar.

Para poder conocer esta información tenemos algunas opciones diferentes.
* Leer el manual del comando.
* Leer la ayuda del comando.
* Usar el comando `info`

#### El manual
Para leer el manual de algún comando lo único que tenemos que hacer es ejecutar el comando 
``` bash
$ man <comando>  
```
donde `<comando>` es el comando del que queremos información.

*¿Como podemos leer el manual del comando `man`?*
{{<details "Respuesta">}}
```bash
$ man man
```
{{</details>}}
>[!note] Nota
>
>El uso básico de `info` es igual al de `man`, con la diferencia que `info` puede tener mas información.

#### La ayuda
Para el la ayuda de un comando el comando que necesitamos es:
```shell
$ <comando> --help
```

La mayoría de los comando siguen esta convención, aunque depende de los desarrolladores.

*¿Como podemos leer la ayuda del comando `man`?*
{{<details "Respuesta">}}
```bash
$ man --help
```
{{</details>}}

### ¿Como muestro un mensaje en la terminal?
Siempre es útil poder mostrar mensajes en la terminal, para esta tarea tenemos `echo`, su uso es 
``` bash
$ echo "<mensaje>"
```
>[!note] Opciones
>
 >Para mas opciones revisar el manual o la ayuda del comando.

## Comandos para el sistema de archivos

Como ya se menciono previamente, al estar en una terminal es importante saber usar el sistema de archivos. En esta sección se mostrar como realizar algunas de las tareas mas comunes relacionadas con el sistema de archivos.

### ¿Como saber en donde estoy?
La terminal siempre trabaja desde un directorio del sistema de archivos (Working Directory), esto afecta el comportamiento de algunos comandos y a las rutas relativas.

Para saber cual es el directorio actual en el que nos encontramos se usa el comando `pwd` (Print Working Directory).

### ¿Como se que es lo que hay en algún directorio?
Si queremos mostrar el contenido de algún directorio usamos `ls` (List) de la siguiente forma:
``` bash
$ ls <ruta>
```
donde `<ruta>` es una ruta absoluta o relativa al directorio.

>[!note] Nota
>
>Si usamos `ls` sin algún argumento nos mostrara el contenido del directorio de trabajo actual.

*¿Como muestro el contenido oculto del directorio de trabajo?*
{{<details "Respuesta">}}
```bash
$ ls -a 
```
{{</details>}}

### ¿Como me muevo a otro directorio?
Es muy común cambiar de directorio de trabajo mientras usamos la terminal, esto se logra con el comando `cd` (Change Directory)

```bash
$ cd <ruta>
```
`<ruta>` es la ruta al nuevo directorio de trabajo.

*¿Cuales son los pasos para cambiar al directorio `/home` y listar su contenido?*
{{<details "Respuesta">}}
```bash
$ cd /home
$ ls
```
{{</details>}}