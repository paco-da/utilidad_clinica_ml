# utilidad_clinica_ml

Mi nombre es Francisco Delgado Ayala. He realizado el siguiente Notebook de Jupyter utilizando Python 3, y las librerías incluidas en Anaconda, procurando facilitar la lectura y comprensión del código a través de comentarios explicativos en cada paso.

Espero que el uso de Python facilite la enseñanza de la estadística, la metodología de la investigación y la ciencia de datos en áreas donde será de gran utilidad, tanto para el crecimiento del conocimiento como para el desarrollo de los médicos en formación. Es importante recalcar que algunos términos utilizados en este archivo son empleados por "convención" en cuanto al código, y otros para facilitar la descripción.

## Breviario breve

### Definiciones

- **Marco de datos** (Dataframe): En el contexto de programación y ciencia de datos, un Dataframe es una estructura bidimensional de datos, similar a una tabla de base de datos, una hoja de cálculo de Excel o una tabla de datos en estadísticas. Está organizado en columnas que pueden contener datos de diferentes tipos (como números, cadenas, entre otros) y permite realizar operaciones como filtrado, agrupación y agregación de datos. Las librerías de Python, como pandas, ofrecen herramientas para manipular Dataframes de manera efectiva.
- **Librería**: En programación, es una colección de funciones y procedimientos que facilita realizar tareas específicas sin redactar código desde cero. (Nota: Aunque en algunos contextos hispanohablantes "librería" se relaciona con libros, en programación se emplea para describir esta colección de herramientas).

### Pruebas estadísticas

Estos términos son ampliamente usados en estadística y en la evaluación de modelos de clasificación. A continuación, te describiré cómo se calcula cada uno, basándome en una matriz de confusión que tiene cuatro componentes: Verdaderos Positivos (VP, o TP en inglés por "True Positives"), Verdaderos Negativos (VN, o TN en inglés por "True Negatives"), Falsos Positivos (FP), y Falsos Negativos (FN).

1. **Exactitud (Accuracy)**: 
    - `(VP+VN) / (VP+VN+FP+FN)`

2. **Precisión o Valor Predictivo Positivo (VPP)**:
    - `(VP) / (VP+FP)`

3. **Sensibilidad (Recall)**:
    - `(VP) / (VP+FN)`
    - Es la proporción de positivos reales que fueron identificados correctamente.

4. **F1-Score**:
    - `2 * (Precisión * Sensibilidad) / (Precisión + Sensibilidad)`
    - Es la media armónica entre precisión y sensibilidad.

5. **Especificidad**:
    - `(VN) / (VN + FP)`
    - Es la proporción de negativos reales que fueron identificados correctamente.

6. **Valor Predictivo Negativo (VPN)**:
    - `(VN) / (VN + FN)`

Estos cálculos asumen que tienes acceso a la matriz de confusión de tu modelo o método de clasificación. La matriz de confusión es una herramienta esencial para evaluar la calidad de un clasificador, especialmente en contextos donde las clases no están equilibradas.

## Descripción

Comparamos tres algoritmos de Aprendizaje Automático (árbol de decisión, bosque aleatorio y KNN) para la predicción de factores de riesgo cardiovascular, utilizando Python como herramienta analítica. Debemos recalcar que un modelo altamente preciso no es sinónimo de perfección y que el sobreajuste del modelo lleva a estimación de datos erróneos. La estandarización de los valores y la exploración en la predicción de variables numéricas es lo que contrasta con la gran mayoría de los artículos científicos actuales, y dota de originalidad a nuestro estudio donde se compara la capacidad predictiva del Machine Learning en medicina.

El aprendizaje automático (Machine Learning) se emplea actualmente como herramienta en múltiples áreas, tales como finanzas, física, biología, videojuegos o en nuestra vida diaria, especialmente cuando utilizamos a ChatGPT como “multiusos”; y la medicina no debería ser una excepción. No obstante, existen diferentes obstáculos que deben ser superados para adoptar estas tecnologías con el objetivo de mejorar la salud de nuestros pacientes. La creación y publicación de este tipo de trabajos representa la superación de uno de esos obstáculos.

## Contenido

- **Limpieza de Datos**: Se realizaron cambios en el conjunto de datos de la población original para proteger la privacidad y se eliminaron participantes duplicados. También se descartaron variables no esenciales para la calidad del estudio. De 872 participantes iniciales, se obtuvieron datos de 641 con 16 variables, sumando 7,064 registros. El porcentaje de datos faltantes fue diferente según la variable (turno laboral 0.78%, tensión arterial sistólica 0.62%, tensión arterial diastólica 0.62%, circunferencia de cintura 13.88% y perímetro de pantorrilla 82.06%).
Se utilizó el lenguaje Python y sus principales bibliotecas (pandas, numpy, matplotlib.pyplot, seaborn, ydata_profiling, scipy, sklearn) para la manipulación y limpieza de datos, análisis exploratorio, análisis estadístico y desarrollo de modelos predictivos. Para asegurar la reproducibilidad y minimizar el sobreajuste, se emplearon tres divisiones aleatorias del conjunto de datos, distribuyendo los datos en grupos de entrenamiento y prueba en una proporción de 70% y 30%, respectivamente, mediante la función train_test_split de sklearn.

- **Métodos de Predicción**: Bosque Aleatorio exhibió el mejor desempeño global, debido a que superó en todas las predicciones de variables numéricas y fue ligeramente inferior que KNN para variables categóricas. En variables categóricas (Tabla 1), logró una exactitud y sensibilidad de 0.61; superó al Árbol de Decisión y KNN en valor predictivo positivo -o precisión- con 0.57, presentó un F1 de 0.55 y tuvo un ROC/AUC de 0.77. Bosque aleatorio fue el mejor en todas las variables numéricas (Tabla 2). En la predicción de tensión sistólica, BA obtuvo un RMSE de 0.80, MAE 0.63, R2 de 0.22 y un MSE de 0.65, indicando una menor variabilidad y refleja una menor dispersión de los errores. En
tensión diastólica, BA obtuvo el mejor RMSE, MAE, R2 y MSE (0.64, 0.46, 0.62 y 0.41 respectivamente). Las predicciones en circunferencia de cintura (RMSE 0.59, MAE 0.46, R2 0.66 y MSE 0.35) y perímetro de pantorrilla (RMSE 0.76, MAE 0.63, R2 0.34 y MSE 0.57) también fueron las mejores.

## Contacto

Si tienes alguna duda o sugerencia, por favor enviame un correo a [dr.fco.da@outlook.com](mailto:dr.fco.da@outlook.com), o tambien en Git Hub [GitHub Francisco DA](https://github.com/paco-da)