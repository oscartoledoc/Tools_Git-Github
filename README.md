# Herramientas más importantes de Git y GitHub

# ¿Qué es Git?
Git es un sistema de control de versiones distribuido que te permite registrar los cambios que haces en tus archivos y volver a versiones anteriores si algo sale mal. Fue diseñado por Linus Torvalds para garantizar la eficiencia y confiabilidad del mantenimiento de versiones de aplicaciones que tienen un gran número de archivos de código fuente.\

# ¿Qué es Github?
GitHub es una plataforma que nos permite guardar repositorios de Git que podemos usar como servidores remotos y ejecutar algunos comandos de forma visual e interactiva (sin necesidad de la consola de comandos).\

- Instalación de Git: (para Windows, MAC y Linux)
https://git-scm.com/downloads

# Herramientas más importantes de Git y GitHub

# ¿Qué es Git?
Git es un sistema de control de versiones distribuido que te permite registrar los cambios que haces en tus archivos y volver a versiones anteriores si algo sale mal. Fue diseñado por Linus Torvalds para garantizar la eficiencia y confiabilidad del mantenimiento de versiones de aplicaciones que tienen un gran número de archivos de código fuente.\

# ¿Qué es Github?
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

### Sequence Diagram
                    
```seq
Directorio-->Staging: Git add 
Staging-->Repositorio: Git commit 
Directorio-->Staging: (Tracked) 
```
>[!NOTE]
>En el directorio, por defecto, los archivos están **Untracked**.

~~***Aquí poner imagen***~~

