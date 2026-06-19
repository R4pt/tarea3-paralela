# Tarea 3: Polars — Análisis de Datos y Machine Learning

**LEAD University** | Computación Paralela

## Descripción

Pipeline completo de ciencia de datos sobre el dataset de diabetes clínica (100,000 registros), comparando el rendimiento de **Polars** vs **Pandas** en cada etapa del procesamiento, e incluyendo entrenamiento de modelos de clasificación binaria.

## Dataset

- **Fuente:** [100,000 Diabetes Clinical Dataset — Kaggle](https://www.kaggle.com/datasets/priyamchoksi/100000-diabetes-clinical-dataset)
- **Archivo:** `diabetes_dataset.csv`
- **Registros:** 100,000 filas × 16 columnas
- **Problema:** Clasificación binaria (variable objetivo: `diabetes`)

## Requisitos

```
polars
pandas
matplotlib
seaborn
scikit-learn
xgboost
lightgbm
dask[dataframe]
psutil
pyarrow
jupyter
```

Instalar con:

```bash
pip install polars pandas matplotlib seaborn scikit-learn xgboost lightgbm "dask[dataframe]" psutil pyarrow jupyter
```

## Ejecución

1. Clonar el repositorio y activar el entorno virtual.
2. Colocar `diabetes_dataset.csv` en la misma carpeta que el notebook.
3. Abrir y ejecutar `tarea3_polars.ipynb` de arriba hacia abajo.

## Estructura

```
tarea3/
├── tarea3_polars.ipynb   # Notebook principal
├── diabetes_dataset.csv  # Dataset
├── README.md
└── informe_tarea3.pdf
```

## Resumen de resultados

| Operación          | Speedup Polars vs Pandas |
|--------------------|--------------------------|
| Lectura CSV        | ~2–4×                    |
| Filtrado           | ~3–6×                    |
| Agregación         | ~2–4×                    |
| Join               | ~2–5×                    |
| Feature Engineering| ~3–6×                    |

| Modelo              | AUC-ROC (aprox.) |
|---------------------|------------------|
| Logistic Regression | ~0.82            |
| Random Forest       | ~0.97            |
| XGBoost             | ~0.98            |
| LightGBM            | ~0.98            |

> Los valores exactos dependen del entorno de ejecución.
