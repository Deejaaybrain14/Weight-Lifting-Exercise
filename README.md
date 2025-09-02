# Practical Machine Learning – Weight Lifting Exercise

**Objetivo.** Predecir `classe` (forma de ejecutar el ejercicio) a partir de mediciones de acelerómetros (cinturón, antebrazo, brazo, mancuerna).

**Datos.**
- Train: https://d396qusza40orc.cloudfront.net/predmachlearn/pml-training.csv
- Test (20 casos): https://d396qusza40orc.cloudfront.net/predmachlearn/pml-testing.csv  
Fuente descriptiva: (PUC-Rio, versión archivada) http://web.archive.org/web/20161224072740/http:/groupware.les.inf.puc-rio.br/har

**Metodología.**
1. Limpieza: retiro columnas con NA en train; excluyo identificadores/tiempos; `classe` como factor.
2. Partición 70/30 (validación), CV (5-fold) en entrenamiento.
3. Modelos: **Random Forest** (principal) y **GBM** (comparativo) con `caret`.
4. Métrica: exactitud; reporte de importancia de variables (1 figura).
5. Reentrenamiento final en todo el train y predicción de 20 casos.

**Resultados.**
- RF obtiene mayor exactitud en validación; GBM se mantiene como referencia.
- Error fuera de muestra estimado según validación (ver `index.html`).
- Se incluyen 20 archivos `problem_id_X.txt` en `predictions/`.

**Reproducibilidad.**
- `pml_project.Rmd` (este repo) → `index.html` (self-contained).
- Semilla fija y URLs oficiales del curso.
- Sesión R al final del Rmd.

**Predicciones (cuestionario).**
- Carpeta `predictions/` con 20 archivos de texto plano (una etiqueta por archivo).

Licencia/Datos: citar a los autores del conjunto de datos según la página del proyecto.
