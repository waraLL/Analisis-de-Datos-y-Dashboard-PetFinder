# Análisis de Datos y Dashboard — PetFinder

Proyecto de **limpieza, preparación, análisis exploratorio y visualización de datos de gatos**, desarrollado a partir del dataset de la competencia **PetFinder.my Adoption Prediction**.

El proyecto tiene como objetivo transformar un conjunto de datos original en información estructurada y visualmente útil para analizar las características de los gatos y su relación con la **velocidad de adopción**.

---

## Objetivo del proyecto

Realizar un flujo completo de análisis de datos utilizando **Python y Power BI**, comenzando desde la revisión y limpieza del dataset hasta la construcción de un dashboard interactivo.

El proyecto busca aplicar de forma práctica conceptos de:

* Limpieza y preparación de datos
* Tratamiento de valores nulos y datos inconsistentes
* Revisión y normalización de categorías
* Integración de diccionarios de datos
* Análisis exploratorio de datos (EDA)
* Estadística descriptiva
* Visualización de datos
* Preparación de información para herramientas de Business Intelligence
* Construcción de un dashboard interactivo en Power BI

---

## Dataset

El proyecto utiliza información proveniente de **PetFinder.my Adoption Prediction**, un dataset orientado al análisis de adopciones de mascotas.

El conjunto original contiene información sobre perros y gatos. Para este proyecto se realizó un **filtrado específico para trabajar únicamente con gatos**.

### Datos utilizados

El dataset original fue complementado con los siguientes diccionarios:

* `breed_labels.csv` → información de razas
* `color_labels.csv` → información de colores
* `state_labels.csv` → información de estados/localizaciones

Después del proceso de filtrado y preparación se obtuvo un dataset de aproximadamente:

**6.861 registros × 30 variables**

---

# Flujo del proyecto

```text
Dataset PetFinder
       │
       ▼
Revisión inicial
       │
       ▼
Limpieza y preparación
       │
       ▼
Filtrado de gatos
       │
       ▼
Integración de diccionarios
       │
       ▼
Análisis exploratorio (EDA)
       │
       ▼
Preparación de dataset final
       │
       ▼
Power BI
       │
       ▼
Dashboard interactivo
```

---

# Estructura del proyecto

```text
Dashboard-PetFinder/
│
├── data/
│   ├── dataset_gatos_limpio.csv
│   ├── dataset_gatos.csv
│   ├──dataset_gatos_preparado.csv
│   ├── breed_labels.csv
│   ├── color_labels.csv
│   └── state_labels.csv
│
├── notebooks/
│   ├── 01_Limpieza_datos_gatos.ipynb
│   ├── 02_Diccionario_datos_gatos.ipynb
│   └── 03_EDA_gatos.ipynb
│
├── dashboard/
│   └── Dashboard_adopcion_cat.pbix
│
├── README.md
└── Requerimientos.txt
```

> La estructura puede ajustarse posteriormente según la organización definitiva del repositorio.

---

# 01 — Limpieza y preparación de datos

En el primer notebook se realizó la revisión y preparación del dataset.

### Principales actividades

* Revisión de la estructura del dataset
* Identificación de tipos de datos
* Revisión de valores nulos
* Revisión de categorías
* Revisión de rangos de las variables
* Detección de posibles valores inconsistentes
* Filtrado de registros correspondientes a gatos
* Renombrado de variables al español
* Tratamiento de variables categóricas
* Revisión de las variables `Nombre` y `Descripcion`
* Generación del dataset limpio

El resultado de este proceso permitió disponer de un conjunto de datos más consistente y preparado para las siguientes etapas.

---

# 02 — Incorporación de diccionarios

El segundo notebook está orientado a complementar la información del dataset mediante los archivos de referencia proporcionados por PetFinder.

Se incorporaron los diccionarios correspondientes a:

| Diccionario    | Información                              |
| -------------- | ---------------------------------------- |
| `breed_labels` | Identificación y nombre de las razas     |
| `color_labels` | Identificación de los colores            |
| `state_labels` | Identificación de estados/localizaciones |

Esto permite pasar de identificadores numéricos a categorías interpretables, facilitando tanto el análisis como la visualización posterior.

---

# 03 — Análisis Exploratorio de Datos (EDA)

En el tercer notebook se realizó el análisis exploratorio del dataset limpio.

El objetivo es comprender la distribución de las principales variables y encontrar patrones que puedan ser relevantes para el proceso de adopción.

### Análisis realizado

* Estadística descriptiva
* Distribución de edades
* Distribución por género
* Análisis de razas
* Análisis de colores
* Tamaño y características de los gatos
* Distribución geográfica
* Variables relacionadas con la adopción
* Análisis de la **velocidad de adopción**
* Comparación entre categorías
* Visualizaciones para identificar patrones y tendencias

### Velocidad de adopción

Una de las variables de interés del dataset es la **velocidad de adopción**, que representa el tiempo relativo en que una mascota fue adoptada.

Para facilitar su interpretación, durante la preparación del dataset se busca complementar el valor numérico con una **etiqueta descriptiva de la categoría**, permitiendo utilizar tanto el código como el nombre de la categoría en los análisis y visualizaciones.

---

# 04 — Dashboard en Power BI

### Estado: 🚧 Pendiente

La siguiente etapa consiste en llevar el dataset final a **Power BI** y desarrollar un dashboard interactivo.

El dashboard tendrá como objetivo presentar los principales resultados del análisis de manera clara y accesible.

Entre las visualizaciones previstas se encuentran:

* Total de gatos analizados
* Distribución por género
* Distribución por edad
* Principales razas
* Distribución de colores.
* Ubicación de los registros
* Velocidad de adopción
* Comparaciones entre características y velocidad de adopción
* Indicadores generales del dataset

Se buscará que el dashboard permita explorar los datos mediante filtros y segmentaciones.

---

# 05 — Revisiones finales

### Estado: 🚧 Pendiente

Antes de considerar finalizado el proyecto se realizará una última revisión de:

---

# Tecnologías utilizadas

### Lenguaje y análisis

* **Python**
* **Pandas**
* **NumPy**

### Visualización

* **Matplotlib**
* **Seaborn**
* **Plotly**

### Entorno de trabajo

* **Jupyter Notebook**
* **Google Colab**

### Business Intelligence

* **Microsoft Power BI**

### Control de versiones

* **GitHub**

---

# Resultado esperado

El resultado final será un proyecto de análisis de datos que integre **Python + Power BI**, mostrando el proceso completo desde los datos originales hasta una herramienta de visualización interactiva.

El proyecto busca demostrar no solamente la capacidad de generar gráficos, sino también el proceso previo de **comprender, limpiar, transformar, analizar y preparar los datos** para obtener información útil.

---

## Autora

**Wara López**

Ingeniera Electrónica

Interés en análisis de datos, preparación de datos, visualización y herramientas de Business Intelligence.




