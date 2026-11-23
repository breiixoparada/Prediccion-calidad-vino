# Predicción de la calidad del vino

Proyecto de machine learning que estima si un vino es "bueno" o "malo" a partir de sus propiedades fisicoquímicas.

## Autores

- Breixo Parada López
- Marco Somoza López

## Descripción

El objetivo es clasificar vinos como buenos o malos a partir de 11 variables fisicoquímicas (acidez fija, acidez volátil, ácido cítrico, azúcar residual, cloruros, dióxido de azufre libre y total, densidad, pH, sulfatos y alcohol). La calidad original se valora de 3 a 8 y se agrupa en dos clases: "malo" (3-6) y "bueno" (7-8).

## Metodología

1. Análisis exploratorio y limpieza de datos (eliminación de 240 duplicados).
2. Procesado: escalado con `StandardScaler` y reducción de dimensionalidad con PCA (de 11 a 4 componentes).
3. Comparación de cuatro modelos: regresión logística, SVM lineal, SVM con kernel RBF y bosque aleatorio.

## Resultados

| Modelo              | Accuracy | Precision | Recall | F1    |
|---------------------|----------|-----------|--------|-------|
| Regresión logística | 0,871    | 0,619     | 0,325  | 0,426 |
| SVM lineal          | 0,853    | 0,000     | 0,000  | 0,000 |
| SVM RBF             | 0,871    | 0,692     | 0,225  | 0,340 |
| Bosque aleatorio    | 0,868    | 0,583     | 0,350  | 0,438 |

El bosque aleatorio obtiene el mejor F1. Ningún modelo detecta bien los vinos buenos, que son minoría en el dataset.

## Requisitos

- Python 3
- numpy, pandas, matplotlib, seaborn, scikit-learn

## Ejecución

1. Clona el repositorio o descarga los archivos.
2. Asegúrate de que `calidadvino.csv` está en la misma carpeta que el notebook.
3. Abre `prediccion_calidad_vino.ipynb` con Jupyter Notebook o VS Code y ejecuta las celdas en orden.

## Datos

El dataset procede de [Wine Quality Prediction]([enlace-al-repositorio-de-github](https://github.com/shsarv/Machine-Learning-Projects))
