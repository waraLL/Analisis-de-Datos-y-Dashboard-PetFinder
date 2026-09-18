# Análisis de Datos y Dashboard — PetFinder

Proyecto de **limpieza, preparación, análisis exploratorio y visualización de datos de gatos**, desarrollado a partir del dataset de la competencia **PetFinder.my Adoption Prediction**.

El proyecto tiene como objetivo transformar un conjunto de datos original en información estructurada y visualmente útil para analizar las características de los gatos y su relación con la **velocidad de adopción**.

<img width="1431" height="808" alt="home" src="https://github.com/user-attachments/assets/2ebf7822-f8d9-4c34-8820-131f49cabc96" />

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

### Notebook 01 — Limpieza y preparación de datos

En este notebook se realiza la revisión inicial del conjunto de datos y se aplican las transformaciones necesarias para obtener un dataset limpio y listo para el análisis.

#### Principales actividades

* Revisión de la estructura del conjunto de datos
* Identificación y ajuste de tipos de datos
* Revisión de valores nulos
* Revisión de categorías de las variables
* Revisión de rangos de las variables numéricas
* Detección de posibles valores inconsistentes
* Filtrado de registros correspondientes únicamente a gatos
* Eliminación de variables que no son necesarias para el análisis
* Renombrado de variables al español para mejorar la interpretación
* Conversión de variables categóricas al tipo `category`
* Limpieza y estandarización de las variables **Nombre** y **Descripción**
* Validación del conjunto de datos después de las transformaciones.
* Generación del conjunto de datos limpio (`dataset_gatos_limpio.csv`).

Como resultado de esta etapa se obtiene un conjunto de datos consistente y preparado para la incorporación de información adicional y el análisis exploratorio.

---

### Notebook 02 — Preparación e integración de diccionarios

El conjunto de datos de PetFinder utiliza identificadores numéricos para representar razas, colores y estados. En esta etapa se incorporan los archivos de referencia proporcionados por PetFinder para enriquecer la información del dataset, conservando también los identificadores originales.

#### Diccionarios incorporados

| Diccionario        | Información incorporada                            |
| ------------------ | -------------------------------------------------- |
| `breed_labels.csv` | Identificación y nombre de las razas.              |
| `color_labels.csv` | Identificación y nombre de los colores.            |
| `state_labels.csv` | Identificación y nombre de los estados de Malasia. |

#### Principales actividades

* Carga de los archivos de referencia
* Limpieza y preparación de los diccionarios
* Filtrado de razas correspondientes únicamente a gatos
* Integración de los nombres de raza principal y secundaria
* Integración de los nombres de los colores
* Integración de los nombres de los estados
* Conservación de los códigos originales junto con sus nombres descriptivos
* Generación del conjunto de datos preparado (`dataset_gatos_preparado.csv`)

Esta etapa transforma variables codificadas en categorías interpretables, facilitando el análisis y las visualizaciones posteriores.

---

### Notebook 03 — Análisis Exploratorio de Datos (EDA)

En este notebook se desarrolla un análisis exploratorio utilizando estadísticas descriptivas y visualizaciones para conocer mejor el comportamiento de las variables más importantes del conjunto de datos.

#### Análisis realizado

* Estadística descriptiva del conjunto de datos
* Distribución de edades de los gatos
* Distribución por género
* Distribución por tamaño y longitud del pelaje
* Análisis de las principales razas
* Análisis de colores principales 
* Distribución geográfica por estados de Malasia
* Variables relacionadas con salud y cuidados
* Cantidad de fotografías por publicación
* Análisis de la velocidad de adopción
* Comparación de la velocidad de adopción entre distintas categorías
* Visualizaciones para identificar patrones y tendencias

#### Variable de interés: Velocidad de adopción

La **velocidad de adopción** representa el tiempo relativo en que una mascota fue adoptada. Durante la preparación del conjunto de datos se incorporó una etiqueta descriptiva para cada categoría, permitiendo utilizar tanto el código numérico como el nombre de la categoría en los análisis y visualizaciones.

---

### Dashboard interactivo 

Este dashboard fue desarrollado en **Power BI** como la etapa final del proyecto de análisis de adopción de gatos de **PetFinder Malaysia**. Su propósito es explorar de forma interactiva las características de los gatos publicados en adopción y analizar los factores asociados con la velocidad de adopción.

El dashboard permite navegar entre diferentes páginas temáticas, aplicar filtros dinámicos y descubrir patrones relacionados con la edad, raza, salud, fotografías y ubicación de los gatos.

### ¿Qué incluye el dashboard?

* **Inicio:** página de navegación con acceso a todas las secciones del dashboard
* **Perfil Gatuno:** distribución por edad, género, raza, color, tamaño y longitud del pelaje
* **Salud y Cuidado:** análisis del estado de salud, vacunación, esterilización y desparasitación de los gatos
* **Publicación y Visibilidad:** relación entre la cantidad de fotografías, la edad y la visibilidad de las publicaciones por estado
* **Adopción:** análisis de la velocidad de adopción y comparación entre razas, edades y características de los gatos

### Características interactivas

* Segmentadores para filtrar por estado, género, tamaño 
* Tarjetas dinámicas con indicadores principales
* Gráficos de barras, treemap, mapa, matriz con formato condicional y gráficos de dispersión
* Navegación entre páginas mediante botones interactivos

### Objetivo del análisis

El dashboard responde preguntas como:

* ¿Qué características son más comunes en los gatos publicados en adopción?
* ¿Cómo varía la velocidad de adopción según la edad, la raza o el estado?
* ¿Existe una relación entre la cantidad de fotografías publicadas y la velocidad de adopción?
* ¿Cómo se distribuyen los cuidados (vacunación, esterilización y desparasitación) entre los gatos disponibles?

---

### Revisiones finales y documentación

**Estado:** 🚧 Pendiente

La etapa final estará dedicada a consolidar el proyecto y preparar la versión definitiva para el portafolio.

#### Actividades previstas

* Revisión final del conjunto de datos.
* Verificación de consistencia entre notebooks.
* Revisión y mejora del dashboard.
* Documentación del proyecto.
* Organización del repositorio para GitHub.
* Preparación de imágenes y recursos del dashboard.
* Redacción de conclusiones y resultados principales.

---

## Tecnologías utilizadas

* **Python**

  * Pandas
  * NumPy
  * Matplotlib
  * Seaborn
  * Power BI
  * Jupyter Notebook

---

# Resultado esperado

El resultado final será un proyecto de análisis de datos que integre **Python + Power BI**, mostrando el proceso completo desde los datos originales hasta una herramienta de visualización interactiva.

El proyecto busca demostrar no solamente la capacidad de generar gráficos, sino también el proceso previo de **comprender, limpiar, transformar, analizar y preparar los datos** para obtener información útil.

---

## Autora

**Wara López**

Ingeniera Electrónica

Interés en análisis de datos, preparación de datos, visualización y herramientas de Business Intelligence.




