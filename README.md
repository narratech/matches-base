# Matches Base

Asignatura: 
Grupo: 
Autores:
Nombre Alumno 1 (@usuario_github)
Nombre Alumno 2 (@usuario_github)

[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/narratech/matches-base/blob/main/notebooks/matches_base.ipynb)

Este repositorio contiene el punto de partida para las prácticas [Predicción de Resultados en League of Legends](https://narratech.com/es/aprendizaje-automatico-y-mineria-de-datos/aprendizaje-supervisado/prediccion-de-resultados-en-league-of-legends/) y [Análisis de Errores en la Predicción de Resultados en League of Legends](https://narratech.com/es/aprendizaje-automatico-y-mineria-de-datos/aprendizaje-no-supervisado/analisis-de-errores-en-la-prediccion-de-resultados-de-league-of-legends/) de la asignatura Aprendizaje Automático y Minería de Datos. 

## Instalación y uso
Para replicar el entorno de ejecución Python (con las versiones correctas de NumPy, Pandas, Matplotlib, Seaborne, etc.) se recomienda usar Conda 26.7.2 o superior junto al fichero de configuración proporcionado en este repositorio llamado *environment.yml*. Las instrucciones para crear el entorno correspondiente son estas:

```
conda env create -f environment.yml
conda activate aam 
```
Además si se utiliza Visual Studio Code se recomienda hacerlo con las extensiones mencionadas en *.vscode/extensions.json*.

## Objetivo de la práctica
Trabajar sobre un conjunto de datos que representa partidas competitivas de alto nivel en League of Legends tomadas a los 10 minutos de juego ([League of Legends Diamond Ranked Games (10 min)](https://www.kaggle.com/datasets/bobbyscience/league-of-legends-diamond-ranked-games-10-min), descargado de Kaggle el 15 de octubre de 2026), recorriendo las etapas de aprendizaje supervisado (clasificación del ganador mediante regresión logística, k-NN y árboles de decisión) y aprendizaje no supervisado (análisis de errores aplicando reducción de dimensionalidad con PCA y agrupamiento con k-Means).

## Estructura del repositorio

El repositorio sigue la siguiente arquitectura de archivos y carpetas estándar para proyectos de Ciencia de Datos:

```text
matches-base/
├── data/
│   ├── raw/          # Datasets brutos descargados automáticamente (ignorado por Git)
│   ├── processed/    # Datasets procesados (ignorado por Git)
│   └── sample/       # Muestras o datos auxiliares pequeños
├── notebooks/
│   └── matches_base.ipynb  # Cuaderno principal con la plantilla del análisis (Bloques A-E)
├── .gitignore        # Configuración de exclusiones de Git (evita subir datos pesados)
└── README.md         # Documentación general del repositorio
└── environment.yml   # Entorno de ejecución para Conda
```

Los archivos dentro de data/raw/ (como matches.csv) y data/processed no se almacenan en el control de versiones debido a su tamaño. El propio cuaderno interactivo se encarga de descargarlos e importarlos automáticamente desde la Release oficial de este mismo repositorio.

## Bloques del estudio

A. Descarga automatizada del dataset (matches.csv) desde la Release oficial del repositorio a data/raw/, análisis exploratorio (EDA), limpieza y escalado/estandarización de características clave para el modelo predictivo y algoritmos basados en distancias.

B. Entrenamiento, predicción y evaluación de un modelo de Regresión Logística como línea base (baseline). Evaluación mediante matriz de confusión, exactitud (accuracy) y puntuación F1.

C. Entrenamiento, ajuste de hiperparámetros y evaluación comparativa de al menos dos modelos adicionales (como k-NN y Árboles de Decisión). Selección de la mejor predicción y generación del fichero con los casos de fallo (matches-errors.csv).

D. Reducción de la dimensionalidad sobre el conjunto de datos de errores (matches-errors.csv) aplicando el algoritmo PCA hasta 2 dimensiones. Generación y discusión del diagrama de dispersión resultante.

E. Agrupamiento de los errores mediante el algoritmo k-Means en un espacio reducido bidimensional. Generación de la tabla de promedios/centroides por cluster e interpretación de los patrones del juego que explican los fallos en la predicción.

## Referencias
* Yi Lan Ma: [League of Legends Diamond Ranked Games (10 min)](https://www.kaggle.com/datasets/bobbyscience/league-of-legends-diamond-ranked-games-10-min) (Kaggle)
* [Riot Games](https://www.riotgames.com/es)
* [League of Legends Official Site](https://www.leagueoflegends.com/)


