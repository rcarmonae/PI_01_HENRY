# PI_01_HENRY
El Proyecto Individual 1 HENRY: Machine Learning Operations consiste en un proyecto de práctica cuyo propósito es aplicar métodos y técnicas de Data Engineering y Machine Learning a una base de datos cinematográfica como parte de la carrera de Ciencia de Datos de HENRY. El proyecto se organiza en dos fases: 1. Procesamiento de los datos y creación de una API y 2) Análisis Exploratorio de Datos (EDA) y 3) Creación de un modelo Machine Learning para hacer recomendaciones. 

A continuación, se describen los procesos y archivos correspondientes a cada fase, los cuales se encuentran en este repositorio:

## 1) Procesamiento de los datos y creación de una API
Consistió en la extracción y transformación de las base de datos originales provistas por HENRY. A partir de estas bases de datos se extrae información de diccionarios y listas de diccionarios (sin desanidar) para generar nuevos archivos CSV que se utilizan posteriormente en el EDA y Sistema de Recomendación. Durante esta etapa también se construyó una aplicación utilizando las herramientas FastAPI y Render. La liga de acceso a la aplicación es la siguiente: https://proyecto-individual-1-rosa-carmona.onrender.com/docs
   
### Archivos:
- ETL_RMCE.ipynb - Se presentan y comentan paso a paso todos los procedimientos aplicados a los datasets. Se incluyen las ligas al repositorio de Google Drive donde se almacena la base de datos proporcionadas por HENRY (movies y credits    datasets).
- main.py - Contiene las funciones para realizar las consultas a través de la API en Render.

### 2) Análisis Exploratorio de Datos (EDA)
Se realizó una exploración y breve análisis a partir de la frecuencia de los valores de las variables con potencial para entrenar un sistema de recomendación de películas.

### Archivos:
- EDA_RMCE.ipynb - Se presentan análisis de frecuencias de los valores de los distintos campos de los datasets, susceptibles a formar parte del sistema de recomendación. Se incluyen diferentes tipos de figuras que ilustran la descripción de las variables.
- sis_rec_RMCE.csv - Base de datos procesada y filtrada, contiene información únicamente de las variables susceptibles a formar parte del sistema de recomendación.
  
## 3) Creación de un modelo Machine Learning para hacer recomendaciones
Se eligió el modelo Nearest Neighbour para determinar la similitud de las películas a partir de sus valores de género, director, casa productora, país de origen y de ser el caso, colección a la que pertenece. Los archivos CSV que se enlistan en esta sección son los que alimentan a las funciones que se pueden consultar mediante la API en render.

### Archivos:
- movies_dataset_filtrado_RMCE.csv - datos procesados y filtrados del dataset original "movies". 
- movies_cast_actor_RMCE.csv - relación de los datasets movies y credits (procesados y filtrados) con información referente a los actores de las películas.
- movies_crew_director.csv - relación de los datasets movies y credits (procesados y filtrados) con información referente a los directores de las películas.
- sis_rec_RMCE_reduced.csv - contiene únicamente el título de las películas y las variables que se usaron para entrenar el sistema de recomendación. 
