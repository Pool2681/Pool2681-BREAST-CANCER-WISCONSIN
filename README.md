# Proyecto Final-BREAST-CANCER-WISCONSIN

Para este proyecto final de seleccionar el modelo para el conjunto de datos de cáncer de mama, primero empezamos importando las librerías que vamos a requerir para este ejercicio.

Descargamos el dataset para comenzar con la exploración y análisis de los datos.

Contamos las filas y columnas de nuestro dataset.

Posteriormente leemos 10 registros de nuestro dataset. 

Borramos la columna Id que es irrelevante para nuestro estudio.

Dividimos el conjunto de datos en conjuntos de datos independientes y dependientes para una exploración más optimizada.

Utilizamos las gráficas de violin ya que son una gran herramienta para representar distribuciones de datos numéricos. Combinan características de diagrama de caja y diagramas de densidad de núcleo. Aquí, usaremos gráficos de violín para comparar las distribuciones de variables en condiciones benignas y malignas.

Las gráficas anteriores nos muestran qué variables tienen distribuciones distintas bajo condiciones M y B, por lo que podemos confiar en tales variables para la clasificación. Por ejemplo, radius_se.

Podemos ver claramente que varias columnas están muy altamente correlacionadas, causando multicolinealidad entre variables independientes, por lo que necesitamos eliminar las características altamente correlacionadas en los pasos de preprocesamiento.

### PREPROCESAMIENTO DE DATOS

Para que un algoritmo de aprendizaje automático funcione con sus datos, es importante que todos los valores estén entrerd en forma numérica. Primero necesitamos explorar los tipos de datos presentes en nuestro conjunto de datos. Un codificador de etiquetas convierte las etiquetas legibles por humanos en numéricas. En nuestro caso, las entradas 'M' y 'B' se convertirían en 1 y 0 respectivamente.

A continuación, eliminamos características altamente correlacionadas.

Dividimos los datos preprocesados en variables independientes y dependientes para su posterior procesamiento.

Eliminamos características altamente correlacionadas.

Como siguiente paso a nuestro estudio,eliminamos los valores nulos restantes.

### CONJUNTO DE DATOS DIVIDIDO

Dividimos el conjunto de datos en entrenamiento (75%) y pruebas (25%).

Necesitamos llevar nuestros valores de características dentro de un rango comparable, manteniendo al mismo tiempo su independencia. Para ello utilizaremos el método fit_transform en el conjunto de datos de entrenamiento. Este método aprende sobre nuestros datos (media y varianza) y luego utiliza esta información para transformar los datos en un rango de varianza unitaria de media cero.

Escalamos los datos para que estén dentro de un cierto rango.

Construimos un clasificador de regresión logística.

Como siguiente paso, elegimos un modelo de aprendizaje automático.

Elegimos el modelo de aprendizaje automático de acuerdo con el problema que estamos tratando de resolver. Dado que nuestros datos ya están etiquetados (malignos / benignos), utilizaremos el enfoque de aprendizaje supervisado. Dos tipos diferentes de problemas en el aprendizaje supervisado son la clasificación y la regresión. Dado que nuestro objetivo es categorizar los datos en malignos o benignos, estamos tratando con un problema de clasificación. Aquí, utilizaremos un modelo de regresión logística.

## LOGISTIC REGRESSION

Procederemos a construir el modelo de regresión logística.

Realizamos la matriz de confusión y calculamos la puntuación de precisión

## KNN

Procederemos a construir el modelo de KNN.

Encontramos el número óptimo de vecinos.

Realizamos el entrenamiento del clasificador K del vecino más cercano en el conjunto de entrenamiento.

Realizamos la matriz de confusión y calculamos la puntuación de precisión.

## RANDOM FOREST CLASSIFCATION

Procederemos a construir el modelo de ramdom forest classification.

Encontramos el número óptimo de n_estimators.

Entrenamiento del clasificador RandomForest en el conjunto de entrenamiento.

Predicción de los resultados del conjunto de pruebas.

Hacemos la matriz de confusión y calculamos la puntuación de precisión.

## DECISIONTREECLASSIFIER

Procederemos a construir el modelo de DecisionTreeClassifier.

Encontramos el número óptimo de max_leaf_nodes.

Entrenamiento del clasificador del árbol de decisión en el conjunto de entrenamiento.

Predicción de los resultados del conjunto de pruebas.

Realizamos la matriz de confusión y calculamos la puntuación de precisión.

## Support Vector Machines

Procederemos a construir el modelo de support vector machines.

Entrenamiento del clasificador de vectores de soporte en el conjunto de entrenamiento.

Predicción de los resultados del conjunto de pruebas.

Realizamos la matriz de confusión y calculamos la puntuación de precisión.

**Y finalmente mostramos el siguiente cuadro con los Modelos que realizamos con su correspondiente puntuación**

**Y un cuadro del % de precisión vs los modelos clasificadores**

**Partiendo de los datos obtendos, podemos observar que el mejor modelo por el que podemos decidirnos, es el de Regresión Logística, ya que tiene el porcentaje más alto de precisión y el modelo de Decisión Tree, tiene el porcentaje más bajo de precisión.**










