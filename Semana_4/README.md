<p align="center">
  <img src="assets/logo-pma.png" width="180" alt="Centro Politécnico Superior Malvinas Argentinas">
</p>

<h1 align="center">Aprendizaje Automático — Semana 4</h1>

<p align="center">
  <strong>Tecnicatura Superior en Ciencia de Datos e Inteligencia Artificial</strong><br>
  Centro Politécnico Superior Malvinas Argentinas
</p>

---

### Aprendizaje Supervisado — Regresión y Clasificación

Actividad correspondiente a la **Semana 4** de la materia **Aprendizaje Automático**, orientada a la aplicación de técnicas de **aprendizaje supervisado** mediante modelos de **regresión lineal** y **regresión logística** utilizando Python y Scikit-learn.

## 📌 Objetivos

- Comprender los fundamentos del **aprendizaje supervisado**.
- Diferenciar problemas de **regresión** y **clasificación**.
- Preparar y explorar datasets antes del entrenamiento de modelos.
- Dividir los datos en conjuntos de **entrenamiento y prueba**.
- Aplicar modelos de **regresión lineal** y **regresión logística**.
- Evaluar e interpretar el desempeño de los modelos mediante diferentes métricas.

## 📊 Actividades realizadas

### Actividad 1 — Regresión lineal

Se trabajó con un dataset real de **demanda de electricidad mensual en Argentina**, con el objetivo de estimar la **potencia máxima mensual** a partir de diferentes variables relacionadas con el consumo eléctrico y la temperatura.

Se utilizaron como variables predictoras:

- Demanda residencial.
- Demanda de comercio e industria.
- Demanda de grandes usuarios.
- Temperatura promedio.

El desarrollo incluyó:

- Inspección y preparación del dataset.
- Análisis exploratorio de los datos.
- Selección de variables predictoras y variable objetivo.
- División temporal de los datos en entrenamiento y prueba.
- Entrenamiento de un modelo de **regresión lineal múltiple**.
- Evaluación mediante **MAE, RMSE, R² y varianza explicada**.
- Análisis gráfico de valores reales, estimados y residuos.

El modelo obtuvo un **R² de 0,759** sobre el conjunto de prueba y un **MAE de 1.141,10 MW**, permitiendo analizar tanto su capacidad predictiva como sus principales limitaciones.

---

### Actividad 2 — Regresión logística

Se utilizó el dataset `usuarios_win_mac_lin.csv` para desarrollar un modelo de **clasificación** capaz de predecir el sistema operativo utilizado por un usuario de un sitio web a partir de sus características de navegación.

Las variables predictoras utilizadas fueron:

- Duración de la visita.
- Cantidad de páginas vistas.
- Cantidad de acciones realizadas.
- Valor de las acciones.

La variable objetivo contiene tres clases:

- **0 — Windows**
- **1 — Macintosh**
- **2 — Linux**

El desarrollo incluyó:

- Inspección y análisis exploratorio del dataset.
- Análisis de la distribución de las clases.
- Separación de variables predictoras y variable objetivo.
- División estratificada de los datos en **80 % entrenamiento y 20 % prueba**.
- Entrenamiento de un modelo de **regresión logística**.
- Evaluación mediante **accuracy, matriz de confusión, precision, recall y F1-score**.
- Predicción del sistema operativo para un nuevo usuario.

El modelo alcanzó una **exactitud del 73,53 %**, clasificando correctamente **25 de los 34 usuarios** del conjunto de prueba.

La evaluación permitió observar un mejor desempeño en la identificación de usuarios **Linux**, mientras que la principal dificultad del modelo se presentó en la diferenciación entre algunos usuarios de **Windows y Macintosh**.

## 📁 Estructura de archivos

```text
Semana_4/
│
├── actividad_1/
│   ├── datasets/
│   │   └── demanda-de-electricidad-datos-mensuales.csv
│   └── notebook/
│       └── Regresion_lineal_electricidad.ipynb
│
├── actividad_2/
│   ├── datasets/
│   │   └── usuarios_win_mac_lin.csv
│   └── notebook/
│       └── Regresion_logistica.ipynb
│
├── assets/
│   └── logo-pma.png
│
└── README.md
```

## 🛠️ Tecnologías utilizadas

`Python` · `Pandas` · `NumPy` · `Matplotlib` · `Scikit-learn` · `Jupyter Notebook`

---

<p align="center">
  <strong>Juan Pablo Monllor</strong><br>
  Tecnicatura Superior en Ciencia de Datos e Inteligencia Artificial<br>
  2026
</p>