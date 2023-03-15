# Researcher Rising Stars

Un Rising Star es aquel investigador que ha demostrado un gran potencial para convertirse en investigador de alto impacto en los próximos años.

# Objetivos de investigación
* Generar un pronóstico del desempeño de un investigador
* Identificar el perfil de un investigador de alto rendimiento (Rising Star)

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

Comparación de score para cada modelo de h-index

Comparación de score para cada modelo de h-index ponderado

# Clasificación de Rising Stars

### Clustering
<iframe src="Figures/clustering.html" height="500" width="700"></iframe>

### Clustering con normalización de variables
<iframe src="Figures/clustering-std.html" height="500" width="700"></iframe>

Se prefiere el primer modelo porque tiene un cluster que encapsula la mayoria de las variables en su valores más altos

## Clasificación con kNN
