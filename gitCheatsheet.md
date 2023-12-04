# git cheatsheet

`Ctrl + shift + R`: Fuerza el refrescar de página para ver los binarios modificados.

`gitk`: Abre una ventana con una interfaz gráfica para ver las ramas de manera gráfica.

`git add file`: Añade un archivo al stage, se hace después de hacer modificaciones, antes del commit.<br>
`git add .`: Añade todos los archivos de la carpeta.

`git blame "archivo"`: Ver quien ha cambiado las líneas de un archivo.<br>
`git blame "-c archivo"`: Ver una mejor identación.<br>
`git blame "archivo" -l renglón,renglón`: Ver quien modificó los renglones de un archivo.

`git branch`: Revisar que ramas existen y cual es la actual.<br>
`git branch nombre`: Crear rama.<br>
`git branch -a`: Ver todas las ramas.<br>
`git branch -D nombre`: Borrar rama.<br>
`git branch -r`: Ver ramas remotas.<br>
`git branch nombre -c`: copia la rama.

`git checkout hash file`: Podremos ver el archivo en la versión del indicador.<br>
`git checkout master file`: Podremos ver el archivo en la versión del master.<br>
`git checkout "rama"`: Cambiar de rama.<br>
`git checkout -b " nueva rama"`: copia la presente rama en una nueva.

`git cherry-pick hash`: Trae un commit cualquiera de otra rama y lo une automáticamente.

`git clean --dry-run`: Simular lo que se va a borrar, sin borrar.<br>
`git clean -f`: borra los archivos, menos las carpetas y gitignore.

`git clone URL`: Clona el repositorio remoto.

`git commit -m "mensaje"`: Mandar al repositorio, junto con un mensaje.<br>
`git commit -am "mensaje"`: Mandar al repositorio sin hacer add, junto con un mensaje.<br>
`git commit --amend`: Agrega los cambios al último commit (hay que hacer un add a los archivos modificados primero).

`git config`: Ver la lista de las configuraciones de git.<br>
`git config --global user.name "nombre"`: Cambiar la configuración sobre tu nombre.<br>
`git config --global user.email "correo"`: Cambiar la configuración sobre tu correo.<br>
`git config --global init.defaultBranch main`: Cambiar rama principal a main por defecto.<br>
`git config --global alias.abreviación "instrucción"`: Hacer una nueva instrucción abreviada permanente.

`git diff`: Ver diferencias actuales.<br>
`git diff hash hash`: Ver diferencias entre diferentes versiones.

`git fetch`: Actualiza el registro de GitHub en las ramas locales sin hacer cambio a los archivos.

`git grep palabra`: Muestra cuantas veces aparece una palabra y en donde.<br>
`git grep -n palabra`: Muestra el renglón en el que aparece la palabra.<br>
`git grep -c palabra`: Muestra el numero de apariciones de la palabra en cada archivo.<br>
`git grep -c "<p>"`: Muestra el número de apariciones de la etiqueta 	&lt;p&gt;.
  
`git init`: Prepara la carpeta para git.

`git --list`: La configuración del git.<br>
`git --list --show-origin`: Mostrar donde estan las configuraciones guardadas.

`git log`: Ver el historial de cambios.<br>
`git log file`: Ver el historial de cambios de un archivo.<br>
`git log file --stat`: Ver los cambios específicos en los archivos.<br>
`git log --all`: Ver todo el historial de cambios.<br>
`git log --all --graph`: Ver todo el historial de cambios graficado con ramas.<br>
`git log --all --graph --decorate --oneline`: Ver todo el historial de cambios graficado con ramas en una sola linea.<br>
`git log -S "palabra"`: Muestra todas las veces que aparece una palabra en un commit.

`git merge "rama"`: mezcla los cambios de la rama escrita a la actual.

`git pull "remoto" "rama"`: sintaxis.<br>
`git pull origin main`: Traer el repositorio remoto.<br>
`git pull origin main --allow-unrelated-histories`: Trae el repositorio remoto aunque haya historias no relacionadas (archivos sobrantes).

`git push "remoto" "rama"`: sintaxis.<br>
`git push origin main`: Enviar al repositorio remoto los cambios.<br>
`git push origin --tags`: Enviar al repositorio remoto los tags.<br>
`git push origin :refs/tags/nombre`: Comando interno de github que borra el tag.

`git rebase "rama"`: reescribe la historia (primero desde la rama experimental y al final desde main).

`git reflog`: lista TODO, incluso lo borrado.

`git remote add origin dirección`: Enlazar un repositorio remoto.<br>
`git remote`: revisar repositorios remotos.<br>
`git remote -v`: revisar repositorios remotos de manera verbal.<br>
`git remote set-head origin "rama"`: cambiar la dirección por defecto de la rama remota.

`git reset hash --hard`: TODO vuelve a una versión anterior. (Ver nota).<br>
`git reset hash --soft`: El directorio de trabajo vuelve a la versión anterior pero el staging sigue intacto.

`git restore "archivo"`: Restaura el archivo a la versión anterior.

`git rm file`: Nada si el archivo esta en el stage. (Ver nota).<br>
`git rm --cached file`: Borrar el archivo de la memoria RAM, del stage.

`git shortlog`: Muestra los commits de cada persona.<br>
`git shortlog -sn`: Sólo muestra las personas que han hecho commits y el número de los que han hecho.<br>
`git shortlog -sn -all`: Muestra todos los commits, incluso los borrados.<br>
`git shortlog -sn -all --no-merges`: Muestra todos los commits sin tomar en cuenta los merges.

`git stash`: guardar cambios temporales no listos para un commit, dejando todo como estaba en el ultimo commit.<br>
`git stash list`: Ver lo guardado en un stash.<br>
`git stash pop`: Regresar a los cambios hechos en el stash.<br>
`git stash "nueva rama"`: Mover las modificaciones al stash de otra rama.<br>
`git stash drop`: borrar los cambios en el stash.

`git status`: Ver el estado del proyecto.

`git show`: Mostrar el ultimo cambio.<br>
`git show file`: Mostrar los cambios.<br>
`git show-ref --tags`: Mostrar los hashes junto a los tags.<br>
`git show-branch`: Ver ramas existentes y su historia.<br>
`git show-branch -all`: Ver ramas existentes con un poco más de datos.

`git tag`: Ver tags existentes.<br>
`git tag -a v0.1 -m "mensaje" hash`: Colocar una nueva etiqueta (-add).<br>
`git tag -d nombre`: Borrar tag (-delete).


## SSH

Generar una llave **SSH**:

`ssh-keygen -t`:(t, especificar algoritmo 'rsa'; b, complejidad de la llave; C, correo).<br>
Ejemplo: `ssh-keygen -t rsa -b 4096 -C "ejemplo@correo.com"`

`eval $(ssh-agent -s)`: evaluar que el comando se dispare, comprobar el funcionamiento.

`ssh-copy-id correo`: copiar la clave pública.

`git remote set-url origin enlace de repositorio`: Cambiar la url/

## Nota git rm, git reset

`git rm` y `git reset` son comandos con utilidades muy diferentes, pero aún así se confunden muy fácilmente.

### git rm

Este comando nos ayuda a eliminar archivos de Git sin eliminar su historial del sistema de versiones. Esto quiere decir que si necesitamos recuperar el archivo solo debemos “viajar en el tiempo” y recuperar el último commit antes de borrar el archivo en cuestión.

Recuerda que `git rm` no puede usarse así nomás. Debemos usar uno de los flags para indicarle a git como eliminar los archivos que ya no necesitamos en la última versión del proyecto:

`git rm --cached`: Elimina los archivos del área del staging y del próximo commit pero los mantiene en nuestro disco duro.<br>
`git rm --force`: Elimina los archivos de git y del disco duro. git siempre guarda todo, por lo que podemos acceder al registro de la existencia de los archivos, de modo que podremos recuperarlos si es necesario (pero debemos usar comandos más avanzados).

### git reset

Este comando nos ayuda a volver en el tiempo. Pero no como git checkout que nos deja ir, mirar, pasear y volver. Con git reset volvemos al pasado sin la posibilidad de volver al futuro. Borramos la historia y la debemos sobreescribir. No hay vuelta atrás.

Este comando es muy peligroso y debemos usarlo solo en caso de emergencia. Recuerda que debemos usar alguna de estas dos opciones:

Hay dos formas de usar `git reset`: con el argumento `--hard`, borrando toda la información que tengamos en el área de staging (y perdiendo todo para siempre). O, un poco más seguro, con el argumento `--soft`, que mantiene allí los archivos del área de staging para que podamos aplicar nuestros últimos cambios pero desde un commit anterior.

`git reset --soft`: Borramos todo el historial y los registros de git pero guardamos los cambios que tengamos en staging, así podemos aplicar las últimas actualizaciones a un nuevo commit.

`git reset --hard`: Borra todo. Todo todito, absolutamente todo. Toda la información de los commits y del área de staging se borra del historial.

¡Pero todavía falta algo!

`git reset HEAD`: Este es el comando para sacar archivos del área de staging. No para borrarlos ni nada de eso, solo para que los últimos cambios de estos archivos no se envíen al último commit, a menos que cambiemos de opinión y los incluyamos de nuevo en staging con `git add`, por supuesto.

¿Por qué esto es importante?

Imagina el siguiente caso:

Hacemos cambios en los archivos de un proyecto para una nueva actualización. Todos los archivos con cambios se mueven al área de staging con el comando `git add`. Pero te das cuenta de que uno de esos archivos no está listo todavía. Actualizaste el archivo pero ese cambio no debe ir en el próximo commit por ahora.

¿Qué podemos hacer?

Bueno, todos los cambios están en el área de staging, incluido el archivo con los cambios que no están listos. Esto significa que debemos sacar ese archivo de staging para poder hacer commit de todos los demás.

¡Al usar `git rm` lo que haremos será eliminar este archivo completamente de git! Todavía tendremos el historial de cambios de este archivo, con la eliminación del archivo como su última actualización. Recuerda que en este caso no buscábamos eliminar un archivo, solo dejarlo como estaba y actualizarlo después, no en este commit.

En cambio, si usamos `git reset HEAD`, lo único que haremos será mover estos cambios de staging a unstaged. Seguiremos teniendo los últimos cambios del archivo, el repositorio mantendrá el archivo (no con sus últimos cambios pero sí con los últimos en los que hicimos commit) y no habremos perdido nada.

**Conclusión**: Lo mejor que puedes hacer para salvar tu puesto y evitar un incendio en tu trabajo es conocer muy bien la diferencia y los riesgos de todos los comandos de git.

## Protocolo de mensajes

**sintaxis de mensaje**:

&lt;tipo&gt;[alcance opcional]: *emoji* &lt;descripción(iniciar con verbo en minúscula)&gt;

[cuerpo opcional]

[pie(s) de página opcional(es)]

| tipo | significado |
| --- | --- |
| Add | Crear una capacidad, p.ej. característica, prueba, dependencia. |
| Cut | Eliminar una capacidad, p.ej. característica, prueba, dependencia. |
| Fix | Arreglar un problema, p.ej. error, error tipográfico, accidente, declaración errónea. |
| Bump | Aumentar la versión de algo, p.ej. dependencia. |
| Make | Cambie el proceso de construcción, las herramientas o la infraestructura. |
| Start | Empezar a hacer algo; p.ej. crear una bandera característica. |
| Stop | Terminar de hacer algo; p.ej. eliminar un indicador de característica. |
| Refactor | Un cambio de código que DEBE ser solo una refactorización. |
| Reformat | Refactorizar el formateo, p.ej. omitir espacios en blanco. |
| Optimize | Refactorizar el rendimiento, p.ej. acelerar el código. |
| Document | Refactorizar la documentación, p.ej. archivos de ayuda. |

Lista completa de *emojis* [aquí](https://gist.github.com/rxaviers/7360908).
