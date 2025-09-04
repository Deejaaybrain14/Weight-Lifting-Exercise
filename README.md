# Practical Machine Learning - Proyecto Final

Este repositorio contiene mi entrega para el **proyecto final** del curso [Practical Machine Learning (Coursera)](https://www.coursera.org/learn/practical-machine-learning).

## 📂 Contenido
- **PML-Proyecto.Rmd** → documento R Markdown con el análisis completo.
- **PML-Proyecto.html** → versión compilada en HTML del informe (listo para revisión por pares).
- **problem_id_#.txt** → archivos de predicción (20 casos de prueba), generados automáticamente.

## 🎯 Objetivo
Predecir la variable `classe` (forma en que se realizó el ejercicio) a partir de datos de sensores de acelerómetros en diferentes posiciones corporales. 

## 🛠️ Metodología
1. **Descarga y limpieza de datos**: se eliminaron columnas irrelevantes, con demasiados valores NA y de varianza-cero.
2. **Partición train/valid**: 70% entrenamiento, 30% validación.
3. **Modelado**: se compararon **Random Forest (RF)** y **Gradient Boosting (GBM)** con validación cruzada de 5 folds.
4. **Selección del mejor modelo**: se escogió el de mayor *Accuracy* en validación.
5. **Predicciones finales**: se aplicó el modelo ganador sobre los 20 casos de `pml-testing.csv`.

## 📊 Resultados
- El modelo ganador alcanzó una **alta exactitud** (> 99%) en el conjunto de validación.
- Se generaron los 20 archivos de predicción en el formato requerido.

## ▶️ Link 
- [Ver informe HTML en GitHub Pages](https://deejaaybrain14.github.io/Weight-Lifting-Exercise/)

## 🔗 Revisión por pares
Para la evaluación:
- Suba este repositorio a GitHub.
- Active GitHub Pages con `PML-Proyecto.html` como página principal (`/docs` o rama `gh-pages`).
- Entregue el enlace al repositorio y/o a la página publicada.

## ▶️ Reproducibilidad
- El documento fija la semilla (`set.seed`) y muestra `sessionInfo()` al final.
- El HTML está configurado como **self-contained**.

## 📚 Referencias
- [PUC-Rio HAR dataset (archivado)](http://web.archive.org/web/20161224072740/http:/groupware.les.inf.puc-rio.br/har)
- Curso *Practical Machine Learning* (Coursera)
