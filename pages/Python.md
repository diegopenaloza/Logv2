- Archivos Locales
  collapsed:: true
	- RAR
	  collapsed:: true
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
- Pandas
  collapsed:: true
	- Convertir archivos
		- De Stata(.dta) a Python
		- ``` Python
		  df = pd.read_stata('animals.dta')
		  ```
		- ref
		  collapsed:: true
			- https://pandas.pydata.org/docs/reference/api/pandas.read_stata.html
- Listas (arrays)
  collapsed:: true
	- Selecionar
		- Desde el Segundo Valor y sin Incluir el Ultimo
		- ``` python
		  my_list = my_list[1:-1]
		  ```
		- ref
		  collapsed:: true
			- https://stackoverflow.com/questions/11338143/how-to-remove-the-first-and-last-item-in-a-list
- Gráficos
	- Histograma
	- ``` python
	  import plotly.graph_objects as go
	  
	  import numpy as np
	  np.random.seed(1)
	  
	  x = np.random.randn(500)
	  
	  fig = go.Figure(data=[go.Histogram(x=x)])
	  fig.show()
	  ```
- Factor de Expansión en Python
  collapsed:: true
	- ``` python
	  import pandas as pd
	  from pandas_weighting import weight
	  
	  pd.Series.weight = weight
	  pd.DataFrame.weight = weight
	  
	  df = pd.DataFrame({
	      'val': [1, 2, 3, 4, 5, 6],
	      'weights': [3, 2, 1, 1, 0, None],
	  })
	  
	  # mean 3.5 =(1+2+3+4+5+6)/6
	  df.val.mean()
	  
	  # weighted mean 2.0 =(3*1+2*2+1*3+1*4)/(3+2+1+1)
	  df.val.weight(df.weights).mean()
	  ```
	- ref
		- https://pypi.org/project/pandas-weighting/#:~:text=pandas%2Dweighting%20enables%20general%20level,defined%20in%20'weight'%20column.
		- https://datagy.io/pandas-weighted-average/