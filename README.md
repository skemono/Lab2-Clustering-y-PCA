# Laboratorio 2: Aprendizaje No Supervisado

Clustering, Reglas de Asociacion, PCA y t-SNE sobre el dataset The Movie DB.

## Descripcion

Proyecto del curso de Mineria de Datos que aplica tecnicas de aprendizaje no supervisado para descubrir patrones y segmentos en el mercado cinematografico, generando recomendaciones estrategicas para CineVision Studios.

**Dataset:** `movies_2026.csv` — 19,883 peliculas con 13 variables numericas retenidas.

## Contenido del Notebook

El analisis se encuentra en `ClusteringPCA.ipynb` y sigue el siguiente pipeline:

1. **Configuracion y carga de datos** — Instalacion de dependencias, carga del CSV, exploracion inicial, analisis de valores faltantes y estadisticas descriptivas.
2. **Preprocesamiento** — Seleccion de variables numericas, imputacion de nulos con mediana, recorte de outliers (percentil 5-95) y escalamiento estandar.
3. **Clustering** — Validacion de tendencia al agrupamiento (Hopkins, VAT), seleccion de k optimo (metodo del codo + silueta), K-Means y Clustering Jerarquico Aglomerativo con k=3.
4. **Reglas de Asociacion** — Discretizacion de variables numericas, codificacion one-hot y algoritmo Apriori con multiples combinaciones de soporte y confianza.
5. **PCA** — Pruebas de factibilidad (Bartlett, KMO), determinacion de componentes principales y visualizacion de cargas factoriales.
6. **t-SNE** — Visualizacion 2D de los clusters en el espacio original de alta dimension.

## Requisitos

```
pandas
numpy
matplotlib
seaborn
scikit-learn
mlxtend
factor_analyzer
pingouin
scipy
pyclustertend
```

## Ejecucion

```bash
pip install pandas numpy matplotlib seaborn scikit-learn mlxtend factor_analyzer pingouin scipy pyclustertend
jupyter notebook ClusteringPCA.ipynb
```

El notebook esta disenado para ejecutarse de forma secuencial de arriba hacia abajo. La primera celda tambien instala las dependencias automaticamente.
