---
title: "Comandos para archivos"
weight: 3
---
# Comandos para archivos
En Unix el concepto de archivo es muy importante, pero ¿Cómo trabajamos con archivos?

Las acciones comunes que se pueden realizar con archivos son:
* [[docs/comandos_archivos/_index#Crear archivos|Crearlos]]
* [[docs/comandos_archivos/_index#Borrar archivos|Borrarlos]]
* [[docs/comandos_archivos/_index#Copiar archivos|Copiarlos]]
* [[docs/comandos_archivos/_index#Organizar archivos|Organizarlos]]
* [[/docs/comandos_archivos/_index#Mover archivos|Moverlos]]

Para cada una de estas tareas tenemos comandos que nos ayudan.

## Crear archivos 
Para crear archivos tenemos el comando `touch`, este comando crea un archivo vació con el nombre indicado.

``` bash
$ touch <opción>... <archivo>...
```

>[!note] Nota
>
>El propósito original de este comando es modificar la fecha de acceso y modificación del archivo, pero si el archivo no existe un efecto secundario es que lo crea.

>[!example] Ejercicio
>
>Crea los archivos `gato_1` ... `gato_10` usando el comando `touch`
## Borrar archivos
Cuando queremos borrar archivos usamos el comando `rm` (Remove), este comando acepta una lista de archivos que serán borrados.
```bash
$ rm <opción>... <archivo>... 
```
>[!note] Nota
>
>`rm` también puede borrar un directorio junto con todo su contenido.

>[!example] Ejercicio
>
>Elimina los archivos que creaste en el ejercicio anterior.
## Copiar archivos
Copiar archivos es una tarea muy común, para esto existe el comando `cp` (Copy) , la formas formas de usar este comando son
```bash
$ cp <opción>... <origen> <destino>
$ cp <opción>... <origen>... <directorio>
```

>[!note] Nota 
>
>Al igual que `rm` este comando también puede actuar sobre un directorio y todo su contenido.

>[!example] Ejercicio.
>
>1. Crea los archivos `perro_1` ... `perro_10`
>1. Copia estos archivos a los archivos `oso_1` ... `oso_10`.
## Organizar archivos
Los archivos se organizan en directorios. Los directorios se pueden crear y eliminar.
### Crear directorios
Para crear directorios se usa el comando `mkdir` (Make Directory). 
```bash
$ mkdir <opción>... <directorio>...
```

>[!example] Ejercicio.
>
>1. Crea los directorios `perros` y `osos`
>1. Copia los archivos que creaste en el ejercicio anterior al lugar adecuado 
>1. Elimina los archivos originales.

### Borrar directorios
Para borrar directorios podemos usar `rmdir` (Remove Directory)

```bash
$ rmdir <opción>... <directorio>...
```

>[!note] Nota
>
>Este comando solo borra directorios vacíos, por lo tanto se debe borrar el contenido antes de eliminar el directorio.

>[!example] Ejercicio
>
>Elimina el directorio `osos` junto con su contenido.
## Mover archivos
En ejercicios anteriores se movieron archivos copiandolos y eliminando los originales, pero esto se puede hacer con un solo comando. El comando es `mv` (Move)

```bash
$ mv <opción>... <origen> <destino>
$ mv <opción>... <origen>... <directorio>
```

>[!note] Nota
>
>Este comando tambien puede ser usado para cambiar el nombre a un archivo o directorio.

>[!example] Ejercicio
>1. Crea el directorio `animales` 
>1. Mueve el directorio `perros` junto con todo su contenido dentro del directorio `animales` 