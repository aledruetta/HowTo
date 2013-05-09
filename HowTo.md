Git / GitHub How
================

¿Cómo Crear un Repositorio Local?
=================================

- Crear una carpeta local:

<!-- language: lang-bash -->
	
	$ mkdir <nombre_carpeta>
	$ cd <nombre_carpeta>

- Inicializar el repositorio:

<!-- language: lang-bash -->
	
	$ git init

- Configuración:

<!-- language: lang-bash -->

	$ git config --global user.name “Nombre Apellido”
	$ git config --global user.email “nombre@servidor.com”

¿Cómo clonar un repositorio de GitHub?
======================================

<!-- language: lang-bash -->

	$ git clone <path/a/GitHub> <nombre_carpeta>

- Ejemplo:

<!-- language: lang-bash -->

	$ git clone git://github.com/usuario/myCarpeta.git myCarpeta
	$ cd myCarpeta
	$ ls -a
	$ ls .git

¿Cómo ver el estado en que se encuentra el repositorio?
=======================================================

<!-- language: lang-bash -->

	$ git status

¿Cómo Indicar a Git que debe dar seguimiento a archivos?
========================================================

- Todos los archivos:

<!-- language: lang-bash -->

	$ git add .

- Archivos específicos:

<!-- language: lang-bash -->

	$ git add <nombre_archivo>

- Tipos de archivos:

<!-- language: lang-bash -->

	$ git add *.py

¿Cómo Preparar Archivos (Stage)?
================================

- Todos los archivos:

<!-- language: lang-bash -->

	$ git add .

- Archivos específicos:

<!-- language: lang-bash -->

	$ git add <nombre_archivo>

- Tipos de archivos:

<!-- language: lang-bash -->

	$ git add *.py

¿Cómo Confirmar Archivos (Commit)?
==================================

<!-- language: lang-bash -->

	$ git commit -m "mensaje de confirmación"

¿Cómo ver el historial de commits?
==================================

<!-- language: lang-bash -->

	$ git log

¿Cómo ver los cambios realizados a los archivos?
================================================

- Para ver los cambios realizados pero no preparados (unstaged).

<!-- language: lang-bash -->

	$ git diff

- Para ver los cambios preparados (staged).

<!-- language: lang-bash -->

	$ git diff --cached

- Para ver todos los cambios (staged and unstaged).

<!-- language: lang-bash -->

	$ git diff HEAD

¿Cómo eliminar archivos?
========================

<!-- language: lang-bash -->

	$ git rm <nombre_archivo>

¿Cómo renombrar archivos?
=========================

<!-- language: lang-bash -->

	$ git mv <nombre_archivo>

¿Cómo Crear Una Rama (Branch)?
==============================

<!-- language: lang-bash -->

	$ git branch <nombre_rama>

¿Cómo Moverse a Otra Rama (Branch)?
===================================

<!-- language: lang-bash -->

	$ git checkout <nombre_rama>

¿Cómo Mezclar Ramas (Merge)?
============================

<!-- language: lang-bash -->

	$ git checkout master
	$ git merge <nombre_rama>





