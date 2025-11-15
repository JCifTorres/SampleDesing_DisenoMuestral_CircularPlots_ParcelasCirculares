Español
----------------------------------------

🛰️ Diseño de Muestreo Sistemático y Estratificado con ArcPy (ArcGIS Pro) para Parcelas Circulares

Este script automatiza un flujo de trabajo completo en ArcPy (ArcGIS Pro) para construir un diseño muestral sistemático, estratificado y aleatorio, aplicable a inventarios forestales, análisis de cobertura terrestre, estudios ambientales y monitoreos de campo.

El proceso combina métodos espaciales avanzados con reglas estadísticas, generando unidades muestrales precisas y distribuidas de manera uniforme y balanceada entre distintos estratos de uso/cobertura del suelo (LULC).

🔎 ¿Qué hace el script?

1. Genera una grilla sistemática (fishnet) sobre el área de estudio, creando unidades muestrales rectangulares (UM) de dimensiones (ajustables) aproximadas a 190 × 30 m.
2. Recorta y filtra las UM, conservando únicamente las que están completamente dentro del área válida y cuyo tamaño sea adecuado para el análisis.
3. Calcula el centroide de cada UM y crea puntos representativos que servirán como nodos de muestreo.
4. Determina el estrato o cobertura dominante de cada UM mediante intersecciones espaciales, asegurando que cada unidad esté correctamente categorizada.
5. Realiza un muestreo aleatorio estratificado, seleccionando de forma balanceada hasta 40 unidades (ajustable) por estrato (o todas las disponibles si un estrato o cobertura tiene menos).
6. Genera tres puntos por cada UM seleccionada: uno central, uno desplazado hacia el norte y otro hacia el sur.
7. Construye parcelas circulares de muestreo (15 m de radio) alrededor de cada punto, ideales para trabajos de campo.

📌 Resultado final

El script produce:

1. Un conjunto de unidades muestrales seleccionadas de forma sistemática, estratificada y aleatoria.
2. Puntos centrales y desplazados para cada UM.
3. Parcelas circulares listas para su uso en inventarios o estudios de campo.

Todo el proceso está diseñado para ser reproducible, transparente y robusto, utilizando exclusivamente herramientas de ArcPy (ArcGIS Pro) como CreateFishnet, Clip, Intersect, MinimumBoundingGeometry, SelectLayerByLocation, Buffer, entre otras.


English
----------------------------------------
🛰️ Systematic and Stratified Sampling Design with ArcPy (ArcGIS Pro) for Circular Plots

This script automates a complete workflow in ArcPy (ArcGIS Pro) to build a systematic, stratified and random sampling design, suitable for forest inventories, land-cover assessments, environmental studies, and field-monitoring programs.

The workflow integrates advanced spatial operations with statistical sampling rules, producing precise sampling units that are evenly distributed and balanced across land-use/land-cover (LULC) strata.

🔎 What does the script do?

1. Generates a systematic grid (fishnet) over the study area, creating rectangular sampling units (UMs) approximately 190 × 30 meters (adjustable) in size.
2. Clips and filters the UMs, retaining only those fully contained within the valid area and meeting minimum size criteria.
3. Calculates the centroid of each UM and produces representative sampling points.
4. Identifies the dominant LULC class within each UM using spatial intersections, ensuring proper stratification.
5. Performs a stratified random selection, choosing up to 40 UMs (adjustable) per stratum (or all available units when a stratum has fewer than 40).
6. Generates three points per selected UM: a central point, one shifted north, and one shifted south.
7. Creates circular sample plots (15-meter radius) around each point, ready for fieldwork.

📌 Final Outputs

The script produces:

1. A set of systematically,  stratified, and random selected sampling units.
2. Central and offset points for each UM.
3. Circular sampling plots prepared for on-site measurements or ecological surveys.

The workflow is fully reproducible, transparent, and robust, making use of core ArcPy (ArcGIS Pro) tools including CreateFishnet, Clip, Intersect, MinimumBoundingGeometry, SelectLayerByLocation, Buffer, and others.