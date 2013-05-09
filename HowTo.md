Git / GitHub How
================

¿Cómo Crear un Repositorio Local?
=================================

- Crear una carpeta local:

<!-- language: lang-py -->
	
	$ mkdir <nombre_carpeta>
	$ cd <nombre_carpeta>

- Inicializar el repositorio:

<!-- language: lang-py -->
	
	$ git init

- Configuración:

<!-- language: lang-py -->

	$ git config --global user.name “Nombre Apellido”
	$ git config --global user.email “nombre@servidor.com”

¿Cómo Indicar a Git que debe dar seguimiento a archivos?
========================================================

<!-- language: lang-py -->

	$ git add .				# Todos los archivos.
	$ git add <nombre_archivo>		# Archivos específicos.

¿Cómo Preparar Archivos (Stage)?
================================

<!-- language: lang-py -->

	$ git add .				# Todos los archivos.
	$ git add <nombre_archivo>		# Archivos específicos.

¿Cómo Confirmar Archivos (Commit)?
==================================

<!-- language: lang-py -->

	$ git commit -m "mensaje de confirmación"

¿Cómo Crear Una Rama (Branch)?
==============================

<!-- language: lang-py -->

	$ git branch <nombre_rama>

¿Cómo Moverse a Otra Rama (Branch)?
===================================

<!-- language: lang-py -->

	$ git checkout <nombre_rama>

¿Cómo Mezclar Ramas (Merge)?
============================

<!-- language: lang-py -->

	$ git checkout master
	$ git merge <nombre_rama>





