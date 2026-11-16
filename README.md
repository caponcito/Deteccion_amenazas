# Detección de amenazas en tráfico de red mediante Machine Learning

<!-- Banner: reemplazar por la imagen definitiva de 800 x 300 -->
![Banner del proyecto](banner.png)

**Autores:** [Nombre del autor 1], [Nombre del autor 2], [Nombre del autor 3]

**Objetivo:** Detectar y clasificar tráfico de red benigno y malicioso, así como estimar la duración de los flujos, mediante modelos de Machine Learning entrenados sobre CIC-IDS2017.

## Dataset

**CIC-IDS2017** (Canadian Institute for Cybersecurity). Contiene 8 archivos CSV con tráfico de red capturado durante una semana, procesado con CICFlowMeter. Cada fila representa un flujo de red con ~78 características estadísticas y una etiqueta (`Label`) de tráfico benigno o tipo de ataque.

- **Descarga (Kaggle):** [CIC-IDS2017 — chethuhn/network-intrusion-dataset](https://www.kaggle.com/datasets/chethuhn/network-intrusion-dataset)
- **Fuente original:** [CIC-IDS2017 — University of New Brunswick](https://www.unb.ca/cic/datasets/ids-2017.html)
- **Descarga desde el código:** `kagglehub.dataset_download("chethuhn/network-intrusion-dataset")`

Las 15 etiquetas originales se agrupan en 8 familias: `BENIGN`, `DoS`, `DDoS`, `PortScan`, `Brute Force`, `Web Attack`, `Bot` y `Raras` (Infiltration, Heartbleed).

## Modelos

- Clasificación binaria y multiclase
- Regresión
- Decision Tree
- Random Forest
- SVM (kernel RBF)
- Gaussian Naive Bayes
- Ridge Regression
- Decision Tree Regressor
- Random Forest Regressor
- GridSearchCV
- RandomizedSearchCV
- Validación cruzada estratificada
- F1 macro
- Selección de características por correlación
- Transformación logarítmica con signo (`log1p`)
- StandardScaler
- `class_weight='balanced'`
- Estudio de ablación
- Matrices de confusión normalizadas
- Importancia de características

## Código

| Notebook | Contenido |
|---|---|
| [`proyectoML.ipynb`](proyectoML.ipynb) | Análisis exploratorio, limpieza, preprocesamiento y modelos base |
| [`proyectoML_corregido_ablation.ipynb`](proyectoML_corregido_ablation.ipynb) | Pipeline corregido, búsqueda de hiperparámetros, modelos finales y ablation study |
| [`proyectoML_ablation_rapido.ipynb`](proyectoML_ablation_rapido.ipynb) | Versión rápida del ablation study |
| [`proyectoML_regresion.ipynb`](proyectoML_regresion.ipynb) | Regresión sobre la duración de los flujos |

## Enlaces

- **Código:** [Notebooks del repositorio](.)
- **Video:** pendiente de agregar.
- **Repositorio:** [Agregar URL del repositorio]

## Ejecución

```bash
pip install -r requirements.txt
jupyter notebook
```

> El dataset se descarga automáticamente con `kagglehub` al ejecutar los notebooks.
