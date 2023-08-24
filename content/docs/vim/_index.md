---
title: "Vim"
weight: 5
draft: true
---
# Vim (VI IMproved)

![logo vim](/docs/vim/images/vimlogo.png)

## Lo más básico de lo básico
### Piedra roseta

|                            |                     |
| ----------:                | :---------------    |
| **Crear un archivo nuevo** | $ vim nuevo_archivo |
| **Insertar texto**         | i   (Insert)        |
| Seleccionar (modo visual)  | v   (Visual)        |
| Copiar                     | y   (Yank)          |
| Pegar                      | p   (Paste)         |
| Guardar                    | :w   (Write)        |
| Salir                      | :q   (Quit)         |
| Forzar salida              | :q!   (Quit!)       |
| **Guardar y Salir**        | :wq   (WriteQuit)   |

## Los modos de vim
### Modos principales

|                      |            |
| ------:              | :------    |
| **Editar (default)** | \<esc\>    |
| Insertar             | i          |
| Visual               | v          |
| Visual de bloque     | \<CTRL\> v |
| **Comando**              | :     |

## Modo editar

> **El modo estrella de Vim**


> [!info]- Vim habla...
>
> En inglés

> Es como crear "oraciones"

## ¿Cómo hablar con vim?


| Verbos              |          | Sustantivos/Movimientos     |        |
| -----:              | :------- | -------:                    | :----- |
| **Yank (copiar)**   | y        | **Word (palabra)**          | w      |
| **Delete (borrar)** | d        | **Back (palabra anterior)** | b      |
| Cambiar             | c        | 'til (hasta)                | t      |
| Indentar            | <        | Find (encontrar)            | f      |
|                     |          | Parrafo                     | p      |
|                     |          | Principo de linea           | 0      |
|                     |          | Final de linea              | $      |

> [!tip] tip
>
>  [verbo] [número] [sustantivo]

## Otras palabras
| Adjetivos         |        | Especiales      |            |
| ------:           | :----- | ------:         | :-----     |
| **Número**        | \#     | Borrar linea    | dd         |
| Inner (dentro de) | i      | Copiar linea    | yy         |
|                   |        | Idem, Lo mismo  | .          |
|                   |        | Undo (Deshacer) | u          |
|                   |        | Redo (Rehacer)  | \<CTRL\> r |

## Modo comando

> [!info] info
> 
> **Se accede con  ':'**

Para usar comandos de vim:

- Guardar (w)
- Salir (q)
- set [opción]
- read [file]
- read !
- split y vsplit
- Sustitución (s///)(sed)

## Encontrar y Reemplazar

La sintaxis:

```
: [Rango]s/{patron}/{reemplazo}/{opciones}
```
'''

Rango:
- lin,lfin : Sección
- % : todo el documento
-   : la linea actual

opciones:
- g : global, todas las ocurrencias por linea
- c : preguntar confirmación
- I : sensibilidad a las mayusculas

## Ejemplos

    : s/conejitos esponjosos/angeles descarnados de la noche/g

    : 15,23s/guerra/amor/g

    : %s/Shakespeare/Marlowe/gcI

## Recomendaciones
Para ampliar el conocimiento y aprovechar el insomnio
sugiero:

- El comando en linux **vimtutor**
- El comando :help dentro de vim
- El libro **Pro Vim** de Mark McDonnell
- El link [your problem with vim is that you don't grok vi](https://gist.github.com/nifl/1178878)
## Extras
- macros
- incrementos
- cambiar a mayúsculas
- Ejecutar un comando de bash
- Modo block visual

# Bram Moolenaar

![moolenar|500](/docs/vim/images/moolenaar.jpg)

> 1961 - 3 agosto de 2023
> 
> Ingeniero de sotware y activista holandés.  
> Creador, responsable y benevolente dictador de por vida de VIm.

