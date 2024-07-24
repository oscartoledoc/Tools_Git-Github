# Herramientas más importantes de Git y GitHub

## ¿Qué es Git?
Git es un sistema de control de versiones distribuido que te permite registrar los cambios que haces en tus archivos y volver a versiones anteriores si algo sale mal. Fue diseñado por Linus Torvalds para garantizar la eficiencia y confiabilidad del mantenimiento de versiones de aplicaciones que tienen un gran número de archivos de código fuente.

## ¿Qué es Github?
GitHub es una plataforma que nos permite guardar repositorios de Git que podemos usar como servidores remotos y ejecutar algunos comandos de forma visual e interactiva (sin necesidad de la consola de comandos).\

- Instalación de Git: (para Windows, MAC y Linux)
https://git-scm.com/downloads


## Comandos para iniciar tu repositorio con Git
**Directorio**: una ubicación de almacenamiento en tu sistema de archivos \
**Repositorio**: es una colección organizada de archivos y recursos relacionados

>[!IMPORTANT]
> **RECUERDA**: Desde el 1 de octubre de 2020 GitHub cambió el nombre de la rama principal: ya no es **'master'** , ahora se llama **'main'**.

| Comando  | Instrucción  |
| ------------ | ------------ |
|  **git init** | para inicializar el repositorio git y el staged   |
| **git add nombre_del_archivo.txt**  | enviar el archivo al staged  |
| **git status**  | ver el estado, si se requiere agregar al starget o si se requiere commit  |
|  **git conf** | para ver las posibles configuraciones  |
|  **git conf --list** | para ver las posibles configuraciones  |
| **git conf --list --show-origin**  | para mostrar las configuraciones y sus rutas  |
| **git rm --cached nombre_del_archivo.txt**  | para eliminar el archivo del staged(ram)  |
| **git rm nombre_del_archivo.txt**  | para eliminar del repositorio |


## Estructura básica de archivos Github
1. **Staging**: la memoria RAM. Estado temporal de archivos que voy agregando, ahí voy poniendo la modificaciones antes del commit. Va entre directorio y repositorio.
2. **Untracked**: no mapeado (sin el git add)
3. **Tracked**: mapeado (con git add)

### Diagrama de secuencia
![Sequence Diagrama](https://i.imgur.com/IRUmDNc.jpg)

>[!NOTE]
>En el directorio, por defecto, los archivos están **Untracked**.

### Paso a paso para hacer tu 1er commit:

- ```git init``` : iniciar el seguimiento del directorio local. Ejecutar dentro del directorio que quieres hacer seguimiento.
- ```git add [nombre del archivo]``` : preparar o mover al área de preparación (staging) los archivos modificados.
- ```git add .``` : preparar TODOS los archivos a la vez al staging.
- ```git commit -m [nombrar el commit]``` : luego del git add, ya puedes nombrar el commit o versión de tu archivo cambiado.

>[!NOTE]
>```git commit --amend -m "nombre nuevo"``` : Esto es para cambiar el nombre del último commit hecho por si nos equivocamos.\
>```Git mv [file name] [new file name]``` : Esto es para cambiar el nombre del último commit hecho por si nos equivocamos.


# Ramas (branches) y cómo funcionan
Branch (rama): Son líneas que se usan para hacer experimentos, cambios, solucionar conflictos o arreglar bugs.\
En algún punto del branch, uno lo puede unir o fusionar (merch) para recuperar los mejor de ambas versiones.\

## Los pasos para crear un rama:
1) Abre tu terminal o línea de comandos: Abre la terminal en tu computadora.

2) Navega hasta el directorio de tu repositorio Git: Utiliza el comando cd para cambiar al directorio donde está tu repositorio Git.

3) Crea la rama: Utiliza el comando git branch seguido del nombre que desees para tu nueva rama. Por ejemplo, si quieres crear una rama llamada "nueva-funcionalidad", escribe:
   
```git
git branch nueva-funcionalidad
```

4) Cambia a la nueva rama: Si deseas trabajar en la nueva rama de inmediato, puedes cambiar a ella utilizando el comando git checkout:
   
```git
git checkout -b nueva-funcionalidad
```

> [!IMPORTANT]
> Líneas arriba te había mencionado que ya no se usa _**master**_ como rama por defecto, sino se usa _**main**_. Para hacer este cambio debes escribir este comando:
> ```git
>   git branch -m main
> ```

Si quieres hacer experimentos con ramas:
- **Branch Development:** Cuando decides hacer experimentos, puedes generar ramas experimentales (usualmente llamadas development), que están basadas en alguna rama main, pero sobre las cuales puedes hacer cambios a tu gusto sin necesidad de afectar directamente al código principal.


- **Branch Hotfix:** En otros casos, si encuentras un bug o error de código en la rama Main (que afecta al proyecto en producción), tendrás que crear una nueva rama (que usualmente se llaman bug fixing o hot fix) para hacer los arreglos necesarios. Cuando los cambios estén listos, los tendrás que fusionar con la rama Main para que los cambios sean aplicados mediante un comando llamado Merge, que mezcla los cambios de la rama que originaste a la rama Main. _(esto será mostrado más adelante)_

# Git checkout y git reset (volviendo al pasado)

## Git checkout:
El comando ```git checkout + ID del commit``` nos permite viajar en el tiempo. Solo para chequear cómo era mi documento antes, pero si le hago un commit puede quedarse ahí como está. [*cuidado*]

**Si quieres regresar a tu versión original:**
```git checkout master [file name]```: esto es para regresar a su estado original luego de hacerle el checkout de tipo anterior.

## Git reset:
Se utiliza para deshacer cambios en el repositorio local. Es una herramienta poderosa que permite ajustar el historial de commits y el estado del área de preparación (index) y el árbol de trabajo (working directory). O sea lo que hace es deshacer commits definitiva o temporalmente.

Opciones de ```git reset```:
- ```git reset [código del commit] --soft``` : desahace el commit, pero los cambios permanecen en el área de staging.
- ```git reset [código del commit] --hard``` : desahace el commit definitivamente sin dejar histórico ni en el área de staging

![Sequence Diagrama](https://i.imgur.com/MHelk9e.jpg)

>[!NOTE]
>Para ver el [código del commit] puedo usar ```git log```:

El código tiene la forma: **43ca82e36870b9d529b216d78974f0ff9a799389**




**Link de referencias para hacer este Readme:**
> - [This was done with Markdown Code](https://docs.github.com/es/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
> - [Markdown for code](https://docs.github.com/es/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks)