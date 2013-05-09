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

¿Cómo ver el estado en que se encuentra el repositorio?
=======================================================

<!-- language: lang-bash -->

	$ git status

¿Cómo Indicar a Git que debe dar seguimiento a archivos?
========================================================

<!-- language: lang-bash -->

	$ git add .					# Todos los archivos.
	$ git add <nombre_archivo>			# Archivos específicos.
	$ git add *.py					# Tipos de archivos.

¿Cómo Preparar Archivos (Stage)?
================================

<!-- language: lang-bash -->

	$ git add .					# Todos los archivos.
	$ git add <nombre_archivo>			# Archivos específicos.
	$ git add *.py					# Tipos de archivos.

¿Cómo Confirmar Archivos (Commit)?
==================================

<!-- language: lang-bash -->

	$ git commit -m "mensaje de confirmación"

¿Cómo ver el historial de commits?
==================================

<!-- language: lang-bash -->

	$ git log

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





