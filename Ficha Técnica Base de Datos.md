# Ficha Técnica de la Base de Datos

## Características de los Datos

- **Nombre de la Base de Datos**: Base de datos númerica
- **Formato**: CSV 
- **Periodo de Tiempo**: 2023
- **Cobertura**: Chile
- **Fuente de Datos**: Página ANFP

## Variables Incorporadas

| Varible                                    | Descripción                                                                 |
|--------------------------------------------|-----------------------------------------------------------------------------|
| Nombres de las jugadoras                   | Edad de las jugadoras                                                       |
                          


## Comentarios sobre la Base de Datos

La base de datos utilizada incluye registros sobre las jugadoras de fútbol femenino de la selección chilena que participaron en los Juegos Panamericanos 2023. Cada registro proporciona información sobre el nombre de la jugadora, el equipo al que pertenece y su edad. La selección de estas variables se basó en su relevancia para analizar la distribución de edades de las jugadoras y el contexto de sus equipos de origen. Esta información es crucial para entender la composición del equipo y destacar tanto la experiencia como la juventud presentes en la selección, permitiendo así una narrativa más completa sobre el desarrollo del fútbol femenino en Chile.

## Procesamiento de la Base de Datos 

Carga Inicial: Los datos se cargaron en un DataFrame utilizando pandas.
Limpieza y Transformación: Se renombraron las columnas para una mejor comprensión y se aseguró que la columna de edad fuera de tipo numérico, utilizando la función pd.to_numeric con el parámetro errors='coerce' para manejar posibles errores de conversión.
Preparación para la Visualización: Los datos procesados se utilizaron directamente para generar un gráfico de barras que muestra la distribución de edades de las jugadoras de fútbol femenino chileno en los Juegos Panamericanos 2023.

## Selección de la Base de Datoa

Esta base de datos fue seleccionada debido a su relevancia en el contexto de los Juegos Panamericanos 2023 y la información detallada que proporciona sobre las jugadoras de la selección chilena. La inclusión de variables como el nombre de la jugadora, el equipo al que pertenece y su edad permite un análisis comprensivo de la composición del equipo. Esta información es crucial para evaluar la distribución de edades y el balance entre experiencia y juventud dentro del equipo, aspectos fundamentales para comprender el desarrollo y el potencial del fútbol femenino en Chile.

## Herramientas

- Python 3.x
- pandas
- matplotlib
- mpld3
