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

En base a estos conjuntos de datos se realizan las siguientes tareas.

- **Extraccion, Transformacion y Carga de datos**
- **Analisis exploratorio de datos**
- **Desarrollo de API**
- **Implementacion de modelo de ML**
- **Despliegue de API**

### Endpoints

El desarrollo de la API se realizo utilizando FastAPI. Se realizaron 5 funciones de obtencion de datos, cada una con un objetivo.
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

####  Documentación

[link](https://github.com/soyHenry/PI_ML_OPS/tree/FT)







