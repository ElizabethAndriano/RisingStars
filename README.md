# Researcher Rising Stars

Un Rising Star es aquel investigador que ha demostrado un gran potencial para convertirse en investigador de alto impacto en los próximos años.

# Objetivos de investigación
* Generar un pronóstico del desempeño de un investigador
* Identificar el perfil de un investigador de alto rendimiento (Rising Star)

# Métricas relevantes
* CITE SCORE: Promedio anual de citas de los artículos publicados
* SNIP: Impacto de las citas ponderando en un área determinada.
* H-INDEX: Productividad académica y el impacto de la investigación de un autor o científico

# Preprocesamiento de datos
Este proceso se puede encontrar en `merge_db.ipynb`. Después de unificar las bases de datos presentadas en un solo archivo y limpiar los autores, se tiene registro de 136,109 investigadores únicos.

# Pronóstico de desempeño
## Correlación entre predictores

<iframe src="Figures/heatmap.html" height="500" width="700"></iframe>

## Modelos de regresión
Se realizaron 6 modelos con las siguientes características para predecir el h-index y el h-index ponderado

* Regresión lineal Ordinary Least Squares (OLS)
* Regresión lineal con sklearn
* Regresión polinomial con OLS
* Regresión polinomial con kNN
* Regresión con Árbol de decisión
* Regresión con Random Forest

### Mejores modelos para h-index

|                | Adjusted $R^2$ | Score Train | Score Test |
| -------------- | -------------- | ----------- | ---------- | 
| Polinomial OLS | 0.910          | -           | -          | 
| kNN            | -              | 0.961       | 0.928      |
| Random Forest  | -              | 0.940       | 0.923      |

### Mejores modelos para h-index ponderado

|                | Adjusted $R^2$ | Score Train | Score Test |
| -------------- | -------------- | ----------- | ---------- | 
| Polinomial OLS | 0.719          | -           | -          | 
| kNN            | -              | 0.924       | 0.874      |
| Random Forest  | -              | 0.900       | 0.890      |

# Clasificación de Rising Stars

### Clustering
<iframe src="Figures/clustering.html" height="500" width="700"></iframe>

| Cluster Index | Clasificación        |
| ------------- | -------------------- |
| 0             | Not Rising Star      |
| 1             | Rising Star          |
| 2             | Not Rising Star      |
| 3             | Not Rising Star      |
| 4             | Possible Rising Star |

Los grupos quedan conformados de la siguiente forma:
* **Rising Star**: 0.1%
* **Possible Rising Star**: 2%
* **Not Rising Star**: 97.9%

## Clasificación con kNN

<iframe src="Figures/cm3.html" height="500" width="700"></iframe>
<iframe src="Figures/cm5.html" height="500" width="700"></iframe>
<iframe src="Figures/cm7.html" height="500" width="700"></iframe>
