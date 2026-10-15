# Market Base

Asignatura: 
Grupo: 
Autores:
Nombre Alumno 1 (@usuario_github)
Nombre Alumno 2 (@usuario_github)

[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/narratech/market-base/blob/main/notebooks/market_base.ipynb)

Este repositorio contiene el punto de partida para la práctica [Estudio del Mercado de Steam](https://narratech.com/es/aprendizaje-automatico-y-mineria-de-datos/mineria-de-datos/estudio-del-mercado-de-steam/) de la asignatura Aprendizaje Automático y Minería de Datos. 

## Instalación y uso
Para replicar el entorno de ejecución Python (con las versiones correctas de NumPy, Pandas, Matplotlib, Seaborne, etc.) se recomienda usar Conda 26.7.2 o superior junto al fichero de configuración proporcionado en este repositorio llamado *environment.yml*. Las instrucciones para crear el entorno correspondiente son estas:

```
conda env create -f environment.yml
conda activate aam 
```
Además si se utiliza Visual Studio Code se recomienda hacerlo con las extensiones mencionadas en *.vscode/extensions.json*.

## Objetivo de la práctica
Trabajar sobre un conjunto de datos que representa el catálogo de videojuegos en la tienda Steam (Steam Games Dataset, descargado de Kaggle el 17 de septiembre de 2026), recorriendo las etapas de adquisición, limpieza, transformación, visualización y extracción de conocimiento para la toma de decisiones en el sector del videojuego.

## Estructura del repositorio

El repositorio sigue la siguiente arquitectura de archivos y carpetas estándar para proyectos de Ciencia de Datos:

```text
market-base/
├── data/
│   ├── raw/          # Datasets brutos descargados automáticamente (ignorado por Git)
│   ├── processed/    # Datasets procesados (ignorado por Git)
│   └── sample/       # Muestras o datos auxiliares pequeños
├── notebooks/
│   └── market_base.ipynb  # Cuaderno principal con la plantilla del análisis (Bloques A-E)
├── .gitignore        # Configuración de exclusiones de Git (evita subir datos pesados)
└── README.md         # Documentación general del repositorio
└── environment.yml   # Entorno de ejecución para Conda
```

Los archivos dentro de data/raw/ (como games.csv) y data/processed no se almacenan en el control de versiones debido a su tamaño. El propio cuaderno interactivo se encarga de descargarlos e importarlos automáticamente desde la Release oficial de este mismo repositorio.

## Requisitos e instalación

Para ejecutar y reproducir el análisis en un entorno local (como **Visual Studio Code** con la extensión de Python y Jupyter), se requieren las siguientes dependencias de Python (3.9+):

Asegúrate de tener instalados los paquetes principales ejecutando en tu entorno virtual o Anaconda Prompt:

## Bloques del estudio

A. Descarga automatizada del dataset desde la Release oficial del repositorio a data/raw/ y verificación de la estructura de datos sin desfasajes de cabecera.

B. Tratamiento de valores ausentes, transformación de cadenas de géneros/tags a listas iterables y cálculo de la métrica de tasa de positividad (filtrando juegos con más de 50 reseñas totales para evitar sesgos).

C. Análisis de frecuencia del Top 10 de géneros frente a su popularidad real y estudio estadístico de la distribución de precios en la plataforma.

D. Correlaciones y análisis temporal: Evaluación de la relación entre el precio, el volumen de reseñas y la recepción del público, sumado al estudio de la evolución histórica de lanzamientos por año.

E. Nichos de Oportunidad: Identificación de combinaciones de géneros o etiquetas poco saturadas con alta valoración media y redacción del informe de conclusiones generales de mercado.

## Referencias
* [Bustos, M.: Steam Games Dataset (Kaggle)](https://www.kaggle.com/datasets/fronkongames/steam-games-dataset)
* [SteamSpy API & Analytics](https://steamspy.com/)
* [Valve Corporation: Steam Store](https://store.steampowered.com/)
