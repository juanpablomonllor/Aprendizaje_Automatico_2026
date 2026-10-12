<p align="center">
  <img src="assets/logo-pma.png" width="180" alt="Centro Politécnico Superior Malvinas Argentinas">
</p>

<h1 align="center">Aprendizaje Automático — Semana 6</h1>

<p align="center">
  <strong>Tecnicatura Superior en Ciencia de Datos e Inteligencia Artificial</strong><br>
  Centro Politécnico Superior Malvinas Argentinas
</p>

---

### Aprendizaje Supervisado — Comparación de dos modelos de clasificación

Actividad correspondiente a la **Semana 6** de la materia **Aprendizaje Automático**. Se aplican dos modelos de clasificación vistos en el bloque, **regresión logística** y **SVM (Support Vector Machine)**, sobre un mismo dataset, para comparar cómo resuelve el problema cada uno y decidir cuál lo aborda mejor.

## 📌 Objetivos

- Aplicar dos modelos de clasificación distintos al mismo problema.
- Preparar un dataset con variables numéricas y categóricas.
- Trabajar con clases desbalanceadas y ajustar los modelos con un conjunto de validación.
- Evaluar los modelos mediante matriz de confusión, precisión, recall y F1.
- Comparar los resultados y justificar la elección de un modelo.

## 📊 Actividad realizada

### Predicción de fallas en máquinas industriales

Se trabajó con el dataset **AI4I 2020 Predictive Maintenance Dataset** (UCI Machine Learning Repository, licencia CC BY 4.0), un dataset sintético que imita datos reales de mantenimiento predictivo. Contiene **10.000 registros**, de los cuales solo el **3,39 %** corresponde a fallas.

El objetivo es predecir si una máquina va a fallar (**clasificación binaria**) a partir de seis variables predictoras:

- Tipo de producto (categórica: L, M, H).
- Temperatura del aire.
- Temperatura del proceso.
- Velocidad de giro.
- Torque.
- Desgaste de la herramienta.

El desarrollo incluyó:

- Inspección del dataset y selección de variables, excluyendo las columnas que producirían fuga de datos.
- Análisis exploratorio y revisión del desbalance de clases.
- Codificación de la variable categórica y escalado de las numéricas, ajustado solo con entrenamiento.
- División estratificada de los datos en **60 % entrenamiento, 20 % validación y 20 % prueba**.
- Entrenamiento de una **regresión logística** y de un **SVM con kernel RBF**.
- Ajuste con el conjunto de validación: **umbral de decisión** de la regresión logística (elegido: 0,2) y parámetro **C** de SVM (elegido: 100, con gamma por defecto).
- Evaluación de los dos modelos sobre los mismos datos de prueba.
- Interpretación de los coeficientes de la regresión logística y de los vectores de soporte de SVM.

### Resultados sobre los datos de prueba (68 fallas reales)

| | Regresión logística | SVM (kernel RBF) |
|---|---:|---:|
| Fallas detectadas | 34 de 68 | 43 de 68 |
| Recall de "Falla" | 0,50 | 0,63 |
| Falsas alarmas | 42 | 18 |
| Precisión de "Falla" | 0,45 | 0,70 |
| F1 de "Falla" | 0,47 | 0,67 |
| Exactitud | 0,96 | 0,98 |

**SVM** fue el modelo que mejor abordó el problema: detectó más fallas y generó menos de la mitad de las falsas alarmas. La **regresión logística** resultó más fácil de interpretar, porque sus coeficientes muestran el peso de cada variable.

## 📁 Estructura de archivos

```text
Semana_6/
│
├── assets/
│   └── logo-pma.png
│
├── datasets/
│   └── ai4i2020.csv
│
├── notebook/
│   └── Comparacion_logistica_svm.ipynb
│
└── README.md
```

## 🗂️ Fuente de los datos

AI4I 2020 Predictive Maintenance Dataset. UCI Machine Learning Repository, 2020.
https://archive.ics.uci.edu/dataset/601/ai4i+2020+predictive+maintenance+dataset

## 🛠️ Tecnologías utilizadas

`Python` · `Pandas` · `NumPy` · `Matplotlib` · `Scikit-learn` · `Jupyter Notebook`

---

<p align="center">
  <strong>Juan Pablo Monllor</strong><br>
  Tecnicatura Superior en Ciencia de Datos e Inteligencia Artificial<br>
  2026
</p>
