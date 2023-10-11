# crispy-invention_metodos

{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# Bienvenida\n",
    "\n",
    "Mi nombre es Francisco Delgado Ayala. He realizado el siguiente Notebook de Jupyter utilizando Python 3, y las librerías incluidas en Anaconda, procurando facilitar la lectura y comprensión del código a través de comentarios explicativos en cada paso.\n",
    "\n",
    "Espero que el uso de Python facilite la enseñanza de la estadística, la metodología de la investigación y la ciencia de datos en áreas donde será de gran utilidad, tanto para el crecimiento del conocimiento como para el desarrollo de los médicos en formación. Es importante recalcar que algunos términos utilizados en este archivo son empleados por \"convención\" en cuanto al código, y otros para facilitar la descripción.\n",
    "\n",
    "## Definiciones\n",
    "\n",
    "- **Marco de datos** (Dataframe): En el contexto de programación y ciencia de datos, un Dataframe es una estructura bidimensional de datos, similar a una tabla de base de datos, una hoja de cálculo de Excel o una tabla de datos en estadísticas. Está organizado en columnas que pueden contener datos de diferentes tipos (como números, cadenas, entre otros) y permite realizar operaciones como filtrado, agrupación y agregación de datos. Las librerías de Python, como pandas, ofrecen herramientas para manipular Dataframes de manera efectiva.\n",
    "- **Librería**: En programación, es una colección de funciones y procedimientos que facilita realizar tareas específicas sin redactar código desde cero. (Nota: Aunque en algunos contextos hispanohablantes \"librería\" se relaciona con libros, en programación se emplea para describir esta colección de herramientas)."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Pruebas estadísticas\n",
    "\n",
    "Estos términos son ampliamente usados en estadística y en la evaluación de modelos de clasificación. A continuación, te describiré cómo se calcula cada uno, basándome en una matriz de confusión que tiene cuatro componentes: Verdaderos Positivos (VP, o TP en inglés por \"True Positives\"), Verdaderos Negativos (VN, o TN en inglés por \"True Negatives\"), Falsos Positivos (FP), y Falsos Negativos (FN).\n",
    "\n",
    "1. **Exactitud (Accuracy)**: \n",
    "    - `(VP+VN) / (VP+VN+FP+FN)`\n",
    "\n",
    "2. **Precisión o Valor Predictivo Positivo (VPP)**:\n",
    "    - `(VP) / (VP+FP)`\n",
    "\n",
    "3. **Sensibilidad (Recall)**:\n",
    "    - `(VP) / (VP+FN)`\n",
    "    - Es la proporción de positivos reales que fueron identificados correctamente.\n",
    "\n",
    "4. **F1-Score**:\n",
    "    - `2 * (Precisión * Sensibilidad) / (Precisión + Sensibilidad)`\n",
    "    - Es la media armónica entre precisión y sensibilidad.\n",
    "\n",
    "5. **Especificidad**:\n",
    "    - `(VN) / (VN + FP)`\n",
    "    - Es la proporción de negativos reales que fueron identificados correctamente.\n",
    "\n",
    "6. **Valor Predictivo Negativo (VPN)**:\n",
    "    - `(VN) / (VN + FN)`\n",
    "\n",
    "Estos cálculos asumen que tienes acceso a la matriz de confusión de tu modelo o método de clasificación. La matriz de confusión es una herramienta esencial para evaluar la calidad de un clasificador, especialmente en contextos donde las clases no están equilibradas.\n"
   ]
  },
