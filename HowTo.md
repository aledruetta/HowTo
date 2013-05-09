Git / GitHub How To
===================

¿Cómo crear un repositorio local?
---------------------------------

- Crear una carpeta local:

<!-- language: lang-bash -->
	
	$ mkdir <directorio>
	$ cd <directorio>

- Inicializar el repositorio:

<!-- language: lang-bash -->
	
	$ git init

- Configuración:

<!-- language: lang-bash -->

	$ git config --global user.name “Nombre Apellido”
	$ git config --global user.email “nombre@servidor.com”

¿Cómo generar llaves SSH?
-------------------------

- Comprobar si existe alguna llave en el pc:

<!-- language: lang-bash -->

	$ cd ~/.ssh

- Generar una nueva llave SSH:

<!-- language: lang-bash -->

	$ ssh-keygen -t rsa -C "tu_email@ejemplo.com"

¿Cómo clonar un repositorio de GitHub?
--------------------------------------

<!-- language: lang-bash -->

	$ git clone [url]

- Ejemplo:

<!-- language: lang-bash -->

	$ git clone git://github.com/usuario/myCarpeta.git myCarpeta
	$ cd myCarpeta
	$ ls -a
	$ ls .git

¿Cómo ver el estado en que se encuentra el repositorio?
-------------------------------------------------------

<!-- language: lang-bash -->

	$ git status

¿Cómo Indicar a Git que debe dar seguimiento a archivos?
--------------------------------------------------------

- Todos los archivos:

<!-- language: lang-bash -->

	$ git add .

- Archivos específicos:

<!-- language: lang-bash -->

	$ git add <nombre_archivo>

- Tipos de archivos:

<!-- language: lang-bash -->

	$ git add *.py

¿Cómo preparar archivos (Stage)?
--------------------------------

- Todos los archivos:

<!-- language: lang-bash -->

	$ git add .

- Archivos específicos:

<!-- language: lang-bash -->

	$ git add <archivo1> <archivo2>

- Tipos de archivos:

<!-- language: lang-bash -->

	$ git add *.py

¿Cómo quitar archivos preparados (staged) erróneamente?
-------------------------------------------------------

<!-- language: lang-bash -->

	$ git reset HEAD

- Quitar sólo de Stage sólo uno o algunos archivos:

<!-- language: lang-bash -->

	$ git reset HEAD -- <archivo>

¿Cómo confirmar archivos (Commit)?
----------------------------------

<!-- language: lang-bash -->

	$ git commit -m "mensaje de confirmación"

- Para preparar (staged) y confirmar de una vez:

<!-- language: lang-bash -->

	$ git commit -a -m "mensaje de confirmación"

¿Cómo ver el historial de commits?
----------------------------------

<!-- language: lang-bash -->

	$ git log

¿Cómo ver los cambios desde el último Commit?
------------------------------------------------

- Para ver los cambios realizados que todavía no hemos preparado (unstaged).

<!-- language: lang-bash -->

	$ git diff

- Para ver los cambios que ya hemos preparado (staged).

<!-- language: lang-bash -->

	$ git diff --cached

- Para ver todos los cambios (staged and unstaged).

<!-- language: lang-bash -->

	$ git diff HEAD

- Para ver un resumen de los cambios realizados agregar la opción --stat a las
instrucciones anteriores.

Ejemplo:

<!-- language: lang-bash -->

	$ git diff HEAD --stat
	HowTo.md | 43 ++++++++++++++++++++++++++-----------------
 	1 file changed, 26 insertions(+), 17 deletions(-)

¿Cómo deshacer el último Commit y volver al último Stage?
---------------------------------------------------------

<!-- language: lang-bash -->

	$ git reset --soft HEAD~

¿Cómo eliminar archivos?
------------------------

<!-- language: lang-bash -->

	$ git rm <archivo>

¿Cómo renombrar archivos?
-------------------------

<!-- language: lang-bash -->

	$ git mv <archivo>

¿Cómo crear una rama (Branch)?
------------------------------

<!-- language: lang-bash -->

	$ git branch <nombre_rama>

¿Cómo moverse a otra rama (Branch)?
-----------------------------------

<!-- language: lang-bash -->

	$ git checkout <nombre_rama>

¿Cómo mezclar ramas (Merge)?
----------------------------

<!-- language: lang-bash -->

	$ git checkout master
	$ git merge <nombre_rama>





