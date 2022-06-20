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
	- Convertir archivos
	  collapsed:: true
		- De Stata(.dta) a Python
		- ``` Python
		  df = pd.read_stata('animals.dta')
		  ```
		- ref
		  collapsed:: true
			- https://pandas.pydata.org/docs/reference/api/pandas.read_stata.html
	- Filtrar Base de Datos
		- Usando Condicionales
			- ``` python
			  
			  ```
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
	- [[Plotly]]
		- Histograma Simple con Una variable - Grafico de Barras simple con una Variable
		  collapsed:: true
			- ``` python
			  import plotly.graph_objects as go
			  
			  import numpy as np
			  np.random.seed(1)
			  
			  x = np.random.randn(500)
			  
			  fig = go.Figure(data=[go.Histogram(x=x)])
			  fig.show()
			  ```
			- ![image.png](../assets/image_1655650481523_0.png)
			- ref
			  collapsed:: true
				- https://plotly.com/python/histograms/
		- Ajustes
			- Ajustar Axix. Ajustar Ejex
				- ``` python
				  
				  ```
				- Ref
					- https://plotly.com/python/axes/
			- Rellenar area cp color -Fill Area
			  collapsed:: true
				- ``` python
				  
				  ```
				- ref
					- https://plotly.com/python/filled-area-plots/
			- Cambiar Color y Transparencia de Area de Color - Fill Area
			  collapsed:: true
				- ``` python
				  fillcolor='rgba(255, 0, 0, 0.1)',
				  ```
				- ref
					- https://community.plotly.com/t/plotly-python-fill-control-opacity-of-filled-area/18445
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
- IDES
  collapsed:: true
	- [[Jupyter Notebook]]
		- {{embed ((62af393f-3e18-4210-ab57-6f60968563b7))}}
	- [[Jupyter Lab]]
		- Cambiar Ancho de celdas o bloques de codigo
		- id:: 62af393f-3e18-4210-ab57-6f60968563b7
		  ``` python
		  from IPython.core.display import display, HTML
		  display(HTML("<style>.container { width:100% !important; }</style>"))
		  ```
		- ref
			- https://www.codegrepper.com/code-examples/python/expand+jupyter+notebook+width
- Bases de Datos
	- Pandas
		- Importar base de Datos [[Stata]] (.dta) a Pandas
			- ``` python
			  df = pd.read_stata('animals.dta')  
			  ```
			- ref
				- https://pandas.pydata.org/docs/reference/api/pandas.read_stata.html