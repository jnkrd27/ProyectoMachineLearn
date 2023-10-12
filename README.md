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
Nuestro modelo de clasifiacion en modelo regresion logistica inicia muy parecido a una regresion linear, con la excepcion de no transformar la variable Y, y clasificando los datos con un porcentaje de 25% en prueba y 75% para entrenamiento
Posteriormente se entre el modelo de regresion logistica y se evalua el rendimiento en este modelo, dandonos un promedio con mucho mejores resultados a diferencia de una regresion lineal 
Por ultimo se opto por evaluar el modelo desde una matriz de confusion, sin embargo al ser un una clasificacion multiclase se utilizo un variable del codigo, permitiendo evaluar la precision, la sensibilidad, F1 y exactitud del modelo
Al evaluar estos, se presenta una precision y sensibilidad de 0 para 2 de las 5 variables, esto en consecuencia de la falta de datos para estas variables [Notebook](https://github.com/jnkrd27/ProyectoMachineLearn/blob/main/Regresion_Logistica.ipynb)
