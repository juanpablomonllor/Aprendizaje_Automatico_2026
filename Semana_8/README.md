<p align="center">
  <img src="assets/logo-pma.png" width="180" alt="Centro Politécnico Superior Malvinas Argentinas">
</p>

<h1 align="center">Aprendizaje Automático — Semana 8</h1>

<p align="center">
  <strong>Tecnicatura Superior en Ciencia de Datos e Inteligencia Artificial</strong><br>
  Centro Politécnico Superior Malvinas Argentinas
</p>

---

### Aprendizaje No Supervisado — Segmentación de clientes con K-Means

Actividad correspondiente a la **Semana 8** de la materia **Aprendizaje Automático**. Se aplica **K-Means** sobre un dataset de clientes para descubrir, sin etiquetas previas, cuántos grupos de clientes existen y qué perfil tiene cada uno.

## 📌 Objetivos

- Aplicar un algoritmo de agrupación sin etiquetas (clustering).
- Seleccionar las variables relevantes y escalarlas antes de agrupar.
- Elegir la cantidad de grupos con el método del codo.
- Interpretar los centroides para describir perfiles de clientes.

## 📊 Actividad realizada

### Segmentación de clientes de un comercio online

Se trabajó con el dataset **dataset_segmentacion_clientes.csv**, provisto en el campus. Contiene **700 clientes** y cinco variables de comportamiento:

- Frecuencia de compras por mes.
- Ticket promedio por compra (USD).
- Tiempo de permanencia en el sitio (minutos).
- Sensibilidad a descuentos (0 a 1).
- Tasa de devoluciones.

El desarrollo incluyó:

- Exploración del dataset: sin valores faltantes ni filas duplicadas.
- Descarte de las columnas `noise_gauss` y `noise_uniform`, que contienen ruido aleatorio y no describen al cliente.
- Escalado de las variables con **StandardScaler**, porque tienen escalas muy distintas.
- **Método del codo** probando k de 2 a 6: el codo aparece en **k = 3**.
- Entrenamiento de **K-Means con k = 3** e interpretación de los centroides en unidades originales.

### Resultados: tres perfiles de clientes

| Grupo | Clientes | Frecuencia | Ticket | Tiempo en sitio | Perfil |
|---|---:|---|---|---|---|
| 0 | 230 | Alta (12/mes) | Medio (180 USD) | Alto (35 min) | Frecuentes |
| 1 | 250 | Baja (2/mes) | Alto (450 USD) | Bajo (6 min) | Premium esporádicos |
| 2 | 220 | Media (4/mes) | Bajo (90 USD) | Bajo (10 min) | Ocasionales de ticket bajo |

La frecuencia, el ticket y el tiempo en el sitio son las variables que mejor separan a los grupos. La tasa de devoluciones resultó muy parecida en los tres grupos.

## 📁 Estructura de archivos

```text
Semana_8/
│
├── assets/
│   └── logo-pma.png
│
├── datasets/
│   └── dataset_segmentacion_clientes.csv
│
├── notebook/
│   └── Segmentacion_clientes_kmeans.ipynb
│
└── README.md
```

## 🗂️ Fuente de los datos

Dataset provisto por la cátedra en el campus virtual del Centro Politécnico Superior Malvinas Argentinas.

## 🛠️ Tecnologías utilizadas

`Python` · `Pandas` · `NumPy` · `Matplotlib` · `Scikit-learn` · `Jupyter Notebook`

---

<p align="center">
  <strong>Juan Pablo Monllor</strong><br>
  Tecnicatura Superior en Ciencia de Datos e Inteligencia Artificial<br>
  2026
</p>
