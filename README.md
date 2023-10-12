# Proyecto Machine Learning

## Introduccion 
Este proyecto nacio en necesidad de experimentar en propia mano un analisis de datos real como resultado de los modulos y sesiones en BEDU

Nuestro Dataset esta basado en informacion disponible en kaggle y cuenta con informacion del clima en la ciudad de Seattle divido en 

- Fechas de registro
- Precipitacion
- Temperatura maxima
- Temperatura minima
- Velocidad del viento
- Tipo de clima

### Objetivos 

- Realizar un análisis exploratorio de dato con el fin de obtener estadísticas sobre los datos obtenidos.
- Conectar la base de datos con Python usando GOOGLE COLAB para realizar labores de predicción, clasificación, entre otras posibles
- Con base  a la informacion, determinar el tipo de clima en la ciudad de Seatlle, evaluando los distintos tipos de modelos usados para encontrar la mejor posible prediccion para eventos futuros 

## Analisis exploratorio de datos 
El analisis inicial en nuestro Dataset consinte en dos partes

**1.** Comprender el conjunto de datos en la informacion predicha por el Dataset
 
**2.** Comprender visualmente la relacion que se tiene entre cada variable independiente dividiendo la informacion en las variables dependientes 
[Notebook](https://github.com/jnkrd27/ProyectoMachineLearn/blob/main/Analisis_Exploratorio.ipynb)

Al finalizar este analisis se opto por eliminar la columna "date", ya que esta solo tenia informacion que no tenia mayor relevancia para nuestros modelos de prediccion

## Clasificacion de datos 
En nuestro entrenamiento de datos se baso en.
1.  Se dividio el Data set en  X y Y, Siendo X nuestras variables independientes (precipitacion, temperatura maxima, tamperatura minima y velocidad de viento) y y la variable dependiente (tipo de clima)
2. Al querer iniciar nuestro modelo de prediccion con un aregresion lineal se opto por una manipulacion de datos, en nuestra variable y, transformando las 5 variables en numeros asignados a cada 
3. Con los datos transformados, se inicio la separacion de los datos  con un tamaño de entrenamiento de 70% y de prueba 30% [Notebook](https://github.com/jnkrd27/ProyectoMachineLearn/blob/main/Clasificacion.ipynb)
## Regresion linear 

Al querer hacer un modelo de prediccion se opto por una regresion linear como primer acercamiento, teniendo transformada nuestra variable en Y asi como el modelo clasificado en prueba y entrenamiento, se continuo entrenando los datos con el modelo de regresion linear y este al finalizar se evaluo el rendimiento del modelo con el coeficiente de determinacion (r2) y su error cuadrado medio (MSE),
Sin embargo, al desarrollar una validacion cruzada para evaluar el desempeño, los resultados no eran los esperados, ya que estos nos mostraban un redimiento deficiente [Notebook](https://github.com/jnkrd27/ProyectoMachineLearn/blob/main/Regresion_Linear_.ipynb)

Por lo que se opto por modificar el tipo de modelo a uno de clasificacion
## Modelos de clasificacion
### Regresion logistica
Haciendo un cambio en el modelo, de prediccion a clasificacion, el modelo de regresion logistica nos muestra mucho mejores resultados con un valor mayor al 85% [Notebook](https://github.com/jnkrd27/ProyectoMachineLearn/blob/main/Regresion_Logistica.ipynb)

### Arbol de decision
En un modelo de Arbol de decision el accurracy nos mostro un 79% en exactitud  [Notebook](https://github.com/jnkrd27/ProyectoMachineLearn/blob/main/Arbol_de_decision.ipynb)

## Conclusiones
- No es posibleusar el Dataset para la clasificacion en cuanto a las variables de brisa y nieve, puesto que estos son datos minimos en comparacion a las otras variables, se recomienda para trabajos futuros contar con un numero igual de datos entre variables, asi tener una mejor y mas equilibrada informacion
- La eleccion de cambiar modelo de prediccion a una clasificacion fue acertada pues, los valores de evaluacion mejoraron enormemente, siendo estos cerca del 80% entre ambos modelos 

