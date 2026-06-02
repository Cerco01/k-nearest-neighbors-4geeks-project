# Clasificador de calidad de vino con KNN

## Contexto

¿Puede la IA clasificar la calidad de un vino tinto usando solo su composición química? En este proyecto entreno un modelo **K-Vecinos más Cercanos (KNN)** sobre el dataset de vinos tintos del UCI ML Repository para predecir si un vino es de **baja**, **media** o **alta** calidad a partir de 11 features químicas.

## Variables del dataset

| Variable | Descripción | Tipo |
|----------|-------------|------|
| `fixed acidity` | Acidez fija | Numérico |
| `volatile acidity` | Acidez volátil | Numérico |
| `citric acid` | Ácido cítrico | Numérico |
| `residual sugar` | Azúcar residual | Numérico |
| `chlorides` | Cloruros | Numérico |
| `free sulfur dioxide` | Dióxido de azufre libre | Numérico |
| `total sulfur dioxide` | Dióxido de azufre total | Numérico |
| `density` | Densidad | Numérico |
| `pH` | pH | Numérico |
| `sulphates` | Sulfatos | Numérico |
| `alcohol` | Alcohol | Numérico |
| `label` | Calidad (`0` baja, `1` media, `2` alta) | Categórico |

## Cómo usar este proyecto

1. Clonar el repositorio.
2. Instalar dependencias: `pip install -r requirements.txt`
3. Abrir el notebook `src/explore.ipynb` y ejecutar las celdas en orden.
4. El dataset ya está en `data/raw/winequality-red.csv`.

## Qué incluye el proyecto

- Carga y exploración del dataset de vinos.
- Mapeo de `quality` (3-8) a `label` (0-2).
- Split train/test 80/20 con `StandardScaler`.
- Entrenamiento de `KNeighborsClassifier` base.
- Barrido de `k` de 1 a 20 y gráfico accuracy vs k.
- Función `predict_wine_quality([...])` para predecir un vino nuevo.

## Archivos principales

- `src/explore.ipynb`: notebook principal.
- `data/raw/winequality-red.csv`: dataset original.
- `data/processed/`: datasets procesados (si se guardan).
- `models/`: modelos entrenados (si se guardan).

## Créditos

Proyecto realizado como parte del [Bootcamp de Data Science y Machine Learning](https://4geeksacademy.com/us/coding-bootcamps/datascience-machine-learning) de 4Geeks Academy. Dataset: [UCI Wine Quality](https://archive.ics.uci.edu/dataset/186/wine+quality).
