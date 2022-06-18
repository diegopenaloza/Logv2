- Archivos Locales
	- RAR
		- Extraer Archivos, en la carpeta donde se encuentre el archivo principal,  de un archivo comprimido RAR:
		  collapsed:: true
			- Primero instalamos la librería `patool`
			- ``` Python
			  pip install patool
			  ```
			- ``` Python
			  import patoolib
			  # Con `outdir` podemos especificar la dirección de la carpeta en la cual queremos 
			  # poner los archvos descomprimidos
			  patoolib.extract_archive("Test.rar", outdir="/some/dir")
			  ```
			- ref
			  collapsed:: true
				- https://stackoverflow.com/questions/43527641/extract-single-file-from-rar-archive-with-rarfile-in-python
	- Carpetas
	  collapsed:: true
		- Como mostrar archivos dentro de una carpeta
			- Esto muestra los archivos existentes dentro de la misma carpeta en la cual se encuentra el proyecto
			- ``` Python
			  import os
			  arr = os.listdir()
			  ```
			- Especificamos la dirección de la carpeta
			- ``` python
			  import os
			  arr = os.listdir('c:\\files')
			  ```
			- Ref
			  collapsed:: true
				- https://stackoverflow.com/questions/3207219/how-do-i-list-all-files-of-a-directory
-