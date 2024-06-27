Visualización de datos "Guerreras de la Roja"

Este repositorio contiene un script de Python para mostrar las juegadoras de la selección que representaron a Chile en los Juegos Panamericanos. 

Link video Youtube: https://youtu.be/uYhmkzovdR4

#Descripción#

La seleccion chilena femenina es un equipo que ha ganado espacio poco a poco. En ella hemos visto una diversidad de jugadoras en edad, pero cada una con un talento invaluable. 

#Paso 1: Selección de Datos#

Para esta visualización, seleccionamos datos de la cantidad de jugadoras y su edad en los Juegos Panamericanos 2023. Estos datos son muy importantes, ya que acá se evidencia quienes representaron y más adelante evienciaremos cuantos años llevan en la selección.

Base de datos utilizada: 
- Nombre: Base de datos
- Formato: CSV
- Contenido: Cantidad de jugadoras en los Juegos Panamericanos 2023.


#Paso 2: Procesamiento de Datos#
Para este caso se uso google colab, google colab usa el phyton. Se cargaron los datos en el mismo google colab.
El archivo cvs contenia el nombre de las jugadoras y su edad, renombramos las columnas como edad que se uso en este caso. nos aseguramos que la columna edad sea de tipo numerico.

#paso 3:
Se uso matplotlib para crear el grafico de barras, en donde se muestras la edad de las jugadoras.El grafico cuenta con un titulo y nombre a los 2 ejes.

"PREGUNTAS QUE PUEDE RESPONDER LA VISUALIZACIÓN"

- ¿Qué edad predomina en las jugadoras de la selección femenina?
  Esta pregunta se puede analizar viendo los gráficos.

- ¿Qué edad tienen las jugadoras de la Roja?
 Esta pregunta se puede observar al ver el nombre de cada jugadora. 

- ¿La edad de las jugadoras tiene un patrón o es diversa?
  Esta pregunta se responde viendo los gráficos y el eje vertical.

  #CÓDIGO UTILIZADO"
!pip install mpld3
import pandas as pd
import matplotlib.pyplot as plt
import mpld3

# Leer el archivo CSV
file_path = '/content/Adri.csv'  # Asegúrate de que el archivo esté en esta ruta en Colab
data = pd.read_csv(file_path)

# Renombrar las columnas
data.columns = ['Nombre Jugadora', 'Equipo', 'Edad']

# Verificar que la columna Edad sea de tipo numerico:
data['Edad'] = pd.to_numeric(data['Edad'], errors='coerce')
print(data.head())

# Crear y guardar el gráfico de barras
plt.figure(figsize=(10, 6))
plt.bar(data['Nombre Jugadora'], data['Edad'], color='skyblue')
plt.xlabel('Jugadora')
plt.ylabel('Edad')
plt.title('Distribución de Edades de las Jugadoras de Fútbol Femenino Chileno en los Juegos Panamericanos 2023')
plt.xticks(rotation=90)

# Guardar como imagen
plt.savefig('/content/distribucion_edades.jpg')

# Mostrar el gráfico
plt.show()


html_fig = mpld3.fig_to_html(fig)
with open('/content/distribucion_edades.html', 'w') as f:
    f.write(html_fig)
