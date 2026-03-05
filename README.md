![Nomadismo digital](./src/img/ML%20nomadismo.jpg)

## Proyecto de Machine Learning: nomadismo digital y coste de vida global


### Descripción del proyecto:

Este proyecto analiza el atractivo de ciudades y países para nómadas digitales a partir de variables relacionadas con coste de vida, conectividad, bienestar y capacidad adquisitiva.

El objetivo es construir una base analítica que permita:

segmentar ciudades en distintos perfiles de destino para nómadas digitales, identificar los factores más relevantes en la elección de destino y sentar las bases para predecir el digital_nomad_score de un país mediante técnicas de aprendizaje automático.

El proyecto parte de un trabajo previo de análisis exploratorio (EDA) y extiende ese enfoque hacia una estrategia de Machine Learning.

---

### Problema de negocio:

El nomadismo digital es una tendencia creciente: cada vez más profesionales trabajan en remoto desde distintos lugares del mundo. Sin embargo, elegir un destino no depende de una sola variable, sino de la interacción entre múltiples factores como:

coste de vida, velocidad de internet, vivienda, seguridad, bienestar social y facilidad de integración o movilidad.

#### Este proyecto busca responder principalmente a dos preguntas:

¿Qué factores determinan el atractivo de un destino para nómadas digitales?

¿Es posible segmentar ciudades según perfiles nómadas y, a partir de ello, predecir el score de un país?

---

## Objetivos:

- Analizar variables clave asociadas al coste de vida y calidad de vida.

- Preparar un conjunto de variables útiles para clustering de ciudades.

- Explorar la variable objetivo digital_nomad_score.

- Evaluar relaciones entre variables numéricas y su posible utilidad predictiva.

- Definir una base reproducible para futuras fases de modelado supervisado y no supervisado.

---

## Enfoque metodológico: 

El notebook plantea un pipeline híbrido en tres fases:

### *Fase 1 — Clustering*

Segmentación de 4,742 ciudades en perfiles nómadas usando variables agregadas de coste de vida.

### *Fase 2 — Regresión*

Predicción del digital_nomad_score de 81 países a partir de variables de coste, conectividad, bienestar y los perfiles derivados del clustering.

### *Fase 3 — Iteración futura*

Posible incorporación de nuevas variables temporales como:

- Inflación, ingresos por turismo, precio de la vivienda, clima, para evaluar cómo cambia la capacidad predictiva del modelo.

---

### Datasets utilizados: 


| Dataset | Registros | Variables | Fuente |
|---------|-----------|-----------|--------|
| Cost of Living | 4.742 ciudades | 65 variables | [Numbeo/Kaggle](https://www.kaggle.com/datasets/mvieira101/global-cost-of-living/data) |
| Circleloop Index | 85 países | 10 variables | [Circleloop](https://www.circleloop.com/nomadindex/) |
| Movingto Index | 40 países | 10 variables | [Movingto](https://www.movingto.com/digital-nomad-index) |


---


*Variables principales*
*Variables para clustering de ciudades*

El notebook define estas variables como base del análisis de clustering:

-`monthly_nomad_cost:` coste mensual total estimado para nómada

-`nomad_housing_cost`: coste medio del alquiler de un piso de 1 habitación

-`basic_basket_index`: cesta básica de la compra en supermercados

-`daily_meal_cost`: coste diario de comidas fuera de casa

-`local_purchasing_power`: poder adquisitivo local

-`housing_salary_ratio`: % salario destinado a vivienda

-`cappuccino_index`

*Variable objetivo para regresión*

- `digital_nomad_score`

---


## Hallazgos previos del EDA que motivan el proyecto:

El notebook recoge varios hallazgos del análisis exploratorio previo, entre ellos:

- La conectividad aparece como el predictor más fuerte del score nómada, el bienestar social también muestra una correlación alta, los destinos mejor valorados tienden a ser más caros, la seguridad no muestra una correlación fuerte y existen posibles outliers de “value for money” (bajo coste y alto score).

### Análisis exploratorio incluido en este notebook:

En este notebook se realiza una preparación inicial orientada a Machine Learning:

- Carga de datasets limpios.
- Inspección de estructura y tipos de datos.
- Verificación de nulos.
- Análisis descriptivo de variables agregadas.
- Visualización de distribuciones.
- Análisis de correlación entre variables para clustering.
- Análisis de distribución del target.
- Y correlaciones de variables numéricas con digital_nomad_score.

---

### Tecnologías y librerías

Principales herramientas utilizadas:

- Python
- Pandas
- Numpy
- Matplotlib
- Seaborn
- Scipy
- Scikit-learn
- Joblib

---

### Estructura del trabajo:

1.- Carga y revisión de datos.

2.- Análisis descriptivo de los datasets.

3.- Selección de variables clave.

4.- Mini-EDA para clustering.

5.- Mini-EDA para regresión.

6.- Preparación para futuras fases de modelado.


---

## Estado actual del proyecto:

*El notebook compartido muestra principalmente la fase de preparación y exploración de datos para el proyecto de Machine Learning. En el contenido visible se define claramente la estrategia analítica y las variables, pero no se observan aún resultados finales de entrenamiento, métricas comparativas ni modelos persistidos dentro de esta parte del notebook*.


---

### Autores del proyecto

| Autor | LinkedIn | GitHub |
|-------|----------|--------|
| **Daniela Aguirre** | [LinkedIn](https://www.linkedin.com/in/alicia-aguirre-5b5a57188/) | - |
| **Agustin Arganin Castillo** | [LinkedIn] | - |
| **Juan F. Cía** | [LinkedIn](https://www.linkedin.com/in/juanfcia/) | [GitHub](https://github.com/juanfcia) |

---

#### Proyecto base relacionado

- Este trabajo se apoya en el análisis exploratorio previo:

*EDA Nomadismo Digital*
