# Temporal
This study aimed to investigate the temporal dynamics of microbial communities in the tomato rhizosphere. To this end, we designed an approach to assess changes in these communities through high-resolution sampling at short time intervals, allowing for detailed monitoring of the significant shifts occurring during the early stages of plant development.

<p align="center">
  <img src="/temporal_eng.svg" alt="temporal_eng">
</p>
 
## Pre-processing

The sequences from Illumina were pre-processed by removing the primers and then processed using the DADA2 pipeline ([DADA2_pipeline.Rmd](https://github.com/microenvgen/Temporal/blob/main/DADA2_pipeline.Rmd)). The resulting object from this processing step can be found in the [Releases](https://github.com/microenvgen/Temporal/releases/tag/temporal_data) section of this repository.

## Contents

- metadata_Temp: the excell file
- `Analysis.Rmd`:  the script containing the code used to perform the analyses in this chapter.
 
## Functions

### Análisis de diversidad y correlaciones

- Se representan los valores de las variables de trabajo (Carga, Peso, Riqueza, Homogeneidad y Diversidad) en función de Comunidad y Tiempo.
- Se analizan estadísticamente los efectos de Comunidad y Tiempo sobre las variables de trabajo.
- Se analizan estadísticamente los efectos de Riqueza y Diversidad sobre Carga y Peso.

### Análisis filogenético

- Se calculan las 10 familias más abundantes.
- Se analiza el efecto de Tiempo sobre la abundancia de los diferentes Filos y Familias.

### Análisis de la composición

- Representación de la composición microbiana mediante el método NMDS utilizando distancias Bray-Curtis, separando los datos por tipo de Comunidad y tiempo de muestreo, y agrupándolos visualmente según estas variables.
- Representación la composición microbiana, mediante el método NMDS utilizando distancias Bray-Curtis, separando los datos por cada tipo de Comunidad y agrupándolos según el tiempo de muestreo.
- Análisis de redundancia basado en distancias (dbRDA con Bray–Curtis) en su versión parcial, modelando la composición de las muestras en función de Tiempo mientras se controla el efecto de Comunidad y también modelando la composición de las muestras en función de Comunidad mientras se controla por Tiempo.
- Representación de la composición microbiana mediante el método NMDS utilizando distancias Unifrac, separando los datos por tipo de Comunidad y tiempo de muestreo, y agrupándolos visualmente según estas variables.
- Representación la composición microbiana, mediante el método NMDS utilizando distancias Unifrac, separando los datos por cada tipo de Comunidad y agrupándolos según el tiempo de muestreo.
- Análisis de redundancia basado en distancias (dbRDA con Unifrac) en su versión parcial, modelando la composición de las muestras en función de Tiempo mientras se controla el efecto de Comunidad y también modelando la composición de las muestras en función de Comunidad mientras se controla por Tiempo.
- Análisis de la dinámica temporal de la composición microbiana utilizando la matriz de distancias Bray-Curtis. Se calcula la distancia media dentro de cada comunidad por cada nivel de Tiempo y se estima la tendencia temporal para cada Comunidad. Después, se ponderan las pendientes para calcular un estadístico global y se evalúa su significancia estadística mediante un test de permutación restringida.
- Análisis de la dinámica temporal de la composición microbiana utilizando la matriz de distancias Unifrac. Se calcula la distancia media dentro de cada comunidad por cada nivel de Tiempo y se estima la tendencia temporal para cada Comunidad. Después, se ponderan las pendientes para calcular un estadístico global y se evalúa su significancia estadística mediante un test de permutación restringida.
