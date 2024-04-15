<div style="text-align: center;">
  <h2>PROYECTO INTEGRADOR 1 (Data Engineer y Machine Learning)</h2>
</div>

![Portada](https://github.com/pablongrs/MLOps_Steam/blob/master/img/portada_steam.jpg)

### Descripción del Proyecto
En este proyecto se trabaja sobre la plataforma de juegos Steam. El objetivo es desarrollar un Producto minimo viable, que incluye una API y la implementacion de un sistema de recomendacion de juegos a usuarios.

Para realizar este proyecto se dispone de 3 dataset, estos son:

• steam_games.json.gz: Conjunto de datos que contiene nombre de los juegos, genero, id , precios y características.

• users_items.json.gz: Conjunto de datos con información de los juegos, y el tiempo de juego por cada usuario.

• user_reviews.json.gz: Conjunto de datos que contiene el id de usuarios, id del juego,reseñas de los juegos y recomendación o no de cada usuario.

[Consigna](https://github.com/soyHenry/PI_ML_OPS/tree/FT)

En base a estos conjuntos de datos se realizan las siguientes tareas.

- **ETL**
Durante esta etapa se empezo extrayendo los 3 conjuntos de datos los cuales estaban en formato json.  Luego se procedio a realizar el proceso de limpieza y normalizacion de los datos, donde se eliminaron valores nulos, duplicados y columnas innecesarias, se rellenaron filas vacias y se modificaron algunos tipos de datos.
- **Analisis exploratorio de datos**
En esta etapa se llevo a cabo el analisis de cada conjunto de datos, con el objetivo de comprender mejor los datos. Analizando medidas estadisticas, valores atipicos y realizando distintas visualizaciones.
- **Desarrollo de API**
El desarrollo de la API se realizo utilizando FastAPI. Se crearon 5 funciones de obtencion de datos, cada una con el objetivo de mostrar cierta informacion.
- **Implementacion de modelo de ML**
Se procedio a realizar una optimizacion sobre el conjunto de datos, resultando en un dataset mas compacto, luego se creo una funcion que  en base a un id pasado como argumento retornara una lista de juego similares. Por ultimo se procedio a entrenar el modelo utilizando los datos optimizados.
- **Despliegue de API**
Por ultimo se procedio a deployar el sistema de recomendacion y los endpoints en Render, para que cualquier persona tenga acceso a el sistema de recomendación de videojuegos y los endpoints.

### Endpoints

El codigo se puede encontrar en el siguiente link: [Endpoints](https://github.com/pablongrs/MLOps_Steam/blob/master/main.py)

• `developer( desarrollador : str )`: Retorna la cantidad de items y porcentaje de contenido Free por año según empresa desarrolladora

• `userdata( User_id : str )`: Retorna la cantidad de dinero gastado por el usuario, el porcentaje   de recomendación en base a reviews.recommend y cantidad de items.

• `UserForGenre( genero : str )`: Retorna el usuario que acumula más horas jugadas para el género dado y una lista de la acumulación de horas jugadas por año de lanzamiento.

• `best_developer_year( año : int )`: Retorna el top 3 de desarrolladores con juegos MÁS recomendados por usuarios para el año dado

• `developer_reviews_analysis( desarrolladora : str )`: Retorna un diccionario con el nombre del desarrollador como llave y una lista con la cantidad total de registros de reseñas de usuarios que se encuentren categorizados con un análisis de sentimiento como valor positivo o negativo.

Luego se realizo la implementacion del modelo de recomendacion de videojuegos. Para esto se utilizó la similitud del coseno, que determina cuán similares son dos conjuntos de datos.

• `def recomendacion_juego( id de producto )`: Ingresando el id de producto, recibimos una lista con 5 juegos recomendados similares al ingresado.

Notebook [Modelo_ML](https://github.com/pablongrs/MLOps_Steam/blob/master/Modelamiento.ipynb)

### Deploy Render

Se decidió utilizar Render para el despliegue de la API. Render ofrece un servicio gratuito que, aunque proporciona una cantidad limitada de memoria, destaca por su simplicidad de despliegue.

[Render](https://mlops-steam-9iga.onrender.com/docs)









