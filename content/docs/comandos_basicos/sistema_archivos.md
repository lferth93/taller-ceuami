---
title: "Sistema de archivos en Linux"
weight: 1
---

## ¿Que es un sistema de archivos?
En general, el propósito básico de un sistema de archivos es representar y organizar los recursos de almacenamiento
del sistema.

¿Cuáles de las siguientes cosas esperarías encontrar en un sistema de archivos?
* Procesos
* Dispositivos de audio
* Parámetros del Kernel
* canales de comunicación entre procesos

{{< details "Respuesta">}}
Si el sistema es tipo UNIX *¡Todas las de arriba y más!*

{{< details >}}
Y sí, también algunos archivos regulares.

{{< details >}}
En un sistema tipo UNIX *Todo es un archivo*

{{</ details >}}
{{</ details >}}
{{</ details >}}

* Ventajas de este tipo de sistemas de archivos
	* Mismo conjunto de comandos para programar e interactuar.
	* Fácil acceso desde la terminal
* Desventajas de este tipo de sistemas de archivos
	* Es una especie de monstruo de Frankenstein
 
## Principales componentes del sistema de archivos

* Namespace - Una forma de nombrar las cosas y organizarlas de forma jerárquica
* API - un conjunto de llamadas al sistema para navegación y manipulación de objetos
* Modelo de seguridad - Un modelo para proteger, esconder y compartir cosas
* Implementación - software para unir el modelo al hardware

En otras palabras

* Árbol de archivos y pathname
* comandos de navegación y manipulación de archivos
* esquema de permisos
* drivers o módulos del kernel

## Pathnames

Los archivos en un sistema tipo Unix están organizados en una *única* estructura jerárquica de varios niveles conocida como árbol de directorios.

En la parte superior del sistema de archivos hay un directorio
llamado "raíz" que se representa con "/". Todos los demás archivos son "descendientes" de la raíz.

![Ejemplo de Pathname](/docs/comandos_basicos/images/pathname.png)

La lista de directorios que se deben recorrer para localizar un archivo en particular más el nombre de ese archivo forman un pathname o ruta.

Los nombres de directorios y de archivos van separados por
una `/` (barra oblicua) en las rutas.

### Ruta absoluta

Una ruta absoluta se basa en la raíz del árbol de Linux. Toda ruta absoluta empieza, por `/`.

*¿Cuál es la ruta absoluta del archivo `glop`?*
{{<details "Respuesta">}}
`/tmp/glop`
{{</details>}}

*¿Cuál es la ruta absoluta del archivo `notas`?*
{{<details "Respuesta">}}
`/home/willy/notas`
{{</details>}}

*¿Cuál es la ruta absoluta del archivo `triángulo`?*

*¿Cuál es la ruta absoluta del archivo `.bashrc?`*

### Ruta relativa

Las rutas relativas dependen del directorio actual en el que se encuentra el usuario. Para definir una ruta, se usan los símbolos:

| Símbolo | Descripción|
|:--------:|-------------|
| `/`    | Hace referencia al directorio raíz y a la separación entre directorios|
| `.`  | Hace referencia al directorio actual|
| `..` | Hace referencia al directorio padre del directorio actual

*¿Cuál es la ruta relativa del archivo `glop`, si estoy en el directorio `/`?*
{{<details "Respuesta">}}
`tmp/glop`
{{</details>}}

*¿Cuál es la ruta relativa del archivo `archivo1`, si estoy en el directorio `colores`?* 
{{<details "Respuesta">}}
`../../gerardo/archivo1`
{{</details>}}

## Árbol de archivos
![Jerarquia de archivos](/docs/comandos_basicos/images/arbol.png)

|Directorio |Descripción|
|:---:|---|
| */* | El carácter de barra inclinada / por sí solo denota la raíz del árbol del sistema de archivos.
| */bin* | Significa "binarios" y contiene comandos importantes, como ls o cp, que generalmente necesitan todos los usuarios.
| /boot| Contiene todos los archivos necesarios para un proceso de arranque exitoso.
| /dev | Significa "dispositivos". Contiene representaciones de archivos de dispositivos periféricos y pseudodispositivos.
| */home*| contiene los directorios de inicio de los usuarios.
| /lib| contiene bibliotecas del sistema y algunos archivos críticos, como módulos del kernel o controladores de dispositivos.
| /media | punto de montaje predeterminado para dispositivos extraíbles, como memorias USB, reproductores multimedia, etc.
| /mnt| significa "montar". Contiene puntos de montaje del sistema de archivos.
| /proc| sistema de archivos virtual que muestra información sobre los procesos como archivos.
| */root*| el directorio de inicio del superusuario "root", es decir, el administrador del sistema.
| */sbin* | Comandos importantes para la administración del sistema.
| /tmp | Un lugar para archivos temporales.
| /usr| contiene ejecutables, bibliotecas y recursos compartidos que no son críticos para el sistema.
| /usr/bin| este directorio almacena todos los programas binarios distribuidos con el sistema operativo que no residen en /bini o /sbin.
| /usr/lib| almacena las bibliotecas y los archivos de datos necesarios para los programas almacenados en /usr o en otro lugar.
| /var| una abreviatura de "variable". Un lugar para archivos que pueden cambiar con frecuencia, especialmente en tamaño. (logs por ejemplo)
>[!note] Nota
>
>Esta información está disponible mediante el comando `$ man hier`

## Tipos de archivos

El sistema de archivos UNIX contiene varios tipos diferentes de archivos:

* *Archivos ordinarios*: Series de bytes, Pueden contener datos, texto o instrucciones de programa.
* *Directorios*: Contienen referencias a otros archivos (nombres de archivos)
* *Enlace simbólico*: Distintas rutas para un mismo archivo de forma relativa.
* Enlace duro: Distintas rutas para un mismo archivo de forma absoluta.
* Dispositivos de bloque y caracter: Representan un dispositivo físico real, como una impresora
* Pipes (Tuberías): para vincular comandos. La tubería actúa como un archivo temporal que solo existe para contener datos de un comando hasta que los lea otro.
* Sockets: permite una comunicación limpia entre procesos, incluso procesos ejecutándose en otras computadoras.
