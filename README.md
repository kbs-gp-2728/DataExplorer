# Data Explorer

Desarrollar una aplicación web para cargar conjuntos de datos en formato CSV o Excel y obtener un diagnóstico exploratorio inicial. La aplicación permitirá examinar la estructura del archivo, los tipos de variables, los valores faltantes, los registros duplicados, las estadísticas descriptivas y las visualizaciones. Está dirigida a investigadores y estudiantes que necesitan conocer rápidamente las características de un dataset sin programar cada análisis desde cero.

## Herramientas identificadas

Esta sección es para la especificación de las herramientas que se van a utilizar en el desarrollo del proyecto, en base a un full stack de Python y con ayuda de varias librerías del mismo entorno.

--- 
### Librerías utilizadas:

| Librería | Función principal | Capa del sistema |
|---|---|---|
| numpy | Cálculo numérico vectorizado sobre arreglos `ndarray` | Núcleo numérico |
| pandas | Manipulación y análisis de datos tabulares (`DataFrame`, `Series`) | Procesamiento |
| scipy | Estadística, optimización, álgebra lineal y procesamiento de señales | Cálculo científico |
| openpyxl | Lectura y escritura de archivos `.xlsx` (Office Open XML) | Entrada/salida |
| plotly | Gráficos interactivos basados en especificaciones JSON renderizadas con plotly.js | Visualización |
| streamlit | Construcción de aplicaciones web de datos en Python puro | Presentación |
| pytest | Framework de pruebas unitarias e integración | Verificación |
---
