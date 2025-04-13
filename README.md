# Predicción de Delitos Violentos: Integración de Datos de la ENDES y Denuncias Nacionales | 2019 - 2023

Este proyecto consiste en la integración y análisis de datos provenientes de distintas fuentes para alimentar un modelo predictivo de delitos violentos. Se trabajó con información de la Encuesta Nacional de Salud y Demografía (ENDES) de 5 años consecutivos y denuncias realizadas en el país, complementados con datos externos del INEI (población total por departamento) y geogpsperu.

## Índice

- [Descripción del Proyecto](#descripción-del-proyecto)
- [Fuentes de Datos](#fuentes-de-datos)
- [Metodología](#metodología)
  - [Preparación e Integración de Datos](#preparación-e-integración-de-datos)
  - [Modelos de Imputación](#modelos-de-imputación)
  - [Análisis Estadístico](#análisis-estadístico)
  - [Generación del Dataset Final](#generación-del-dataset-final)
- [Resultados y Conclusiones](#resultados-y-conclusiones)
- [Uso del Dataset y Modelo Predictivo](#uso-del-dataset-y-modelo-predictivo)
- [Autor](#autor)

## Descripción del Proyecto

El objetivo del proyecto es integrar y transformar datos de diversas fuentes para construir un dataset final que alimente un modelo predictivo de delitos violentos. Entre los análisis realizados, se encuentran la imputación de variables, el cálculo de indicadores de salud (IMC, medidas de presión arterial y PHQ9), así como la realización de pruebas estadísticas como ANOVA, análisis de correlaciones, incidencia y prevalencia.

## Fuentes de Datos

- **ENDES:**  
  Datos de 5 años consecutivos que suman un total de 187,872 filas.  
- **Denuncias Nacionales:**  
  Datos de denuncias realizadas en el país, con un total de 48,444 filas.
- **Datos Externos:**  
  - INEI: Población total por departamento.  
  - geogpsperu: Información geográfica para la ubicación de los datos.

## Metodología

### Preparación e Integración de Datos

- Se trabajó en la limpieza y consolidación de la data de la ENDES y denuncias nacionales.
- Se integraron datos externos para enriquecer la información, asignando población por departamento y ubicaciones geográficas.

### Modelos de Imputación

- Se aplicaron modelos de imputación para completar variables faltantes en la data de la ENDES:
  - **Regresión Múltiple:** Utilizada para variables con relación lineal.
  - **Random Forest:** Utilizada para variables con relaciones no lineales o más complejas.

### Análisis Estadístico

Se realizaron diversas pruebas estadísticas para entender la relación entre variables:
- **ANOVA:** Para determinar diferencias significativas entre grupos.
- **Correlaciones:** Análisis de relaciones entre variables imputadas y originales.
- **Incidencia y Prevalencia:** Para evaluar la frecuencia y distribución de los eventos (delitos y problemas de salud).

### Generación del Dataset Final

- Luego de integrar y depurar los datos, se generó un DataFrame final de **140,831 registros**.
- El dataset incluye:
  - Información de la ENDES categorizada por indicadores de salud:
    - **IMC:** Para identificar pacientes con obesidad.
    - **Presión Arterial:** Medidas sistólica y diastólica para detectar hipertensión.
    - **PHQ9:** Cálculo del cuestionario de salud mental para determinar el nivel de depresión.
  - Datos de denuncias nacionales vinculadas a la incidencia de delitos violentos.

## Resultados y Conclusiones

- El análisis permitió identificar patrones y prevalencia entre variables de salud y la incidencia de delitos violentos.
- La integración de datos externos mejoró la capacidad predictiva del modelo al contextualizar la información con datos demográficos y geográficos.
- La aplicación de métodos de imputación (Regresión Múltiple y Random Forest) aseguró la consistencia y completitud del dataset.

## Uso del Dataset y Modelo Predictivo

El dataset final, con 140,831 registros, está diseñado para alimentar modelos predictivos de delitos violentos. Se pueden implementar técnicas de machine learning que permitan:
- Predecir la ocurrencia de delitos violentos en base a variables socioeconómicas, de salud y denuncias históricas.
- Realizar análisis de riesgo y definir estrategias para la prevención de delitos.

## Autor

**Arelly Fernanda Vega Peche**  
Responsable de la integración y análisis de datos en este proyecto.


*Este proyecto se realizó con fines de análisis y modelado predictivo, integrando diversas fuentes de datos para generar conocimiento y apoyar estrategias de prevención de delitos violentos.*
