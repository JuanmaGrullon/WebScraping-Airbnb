# Análisis del Mercado de Alquileres Vacacionales en República Dominicana mediante Web Scraping de Airbnb

## Descripción

Este proyecto tiene como objetivo explorar y analizar el mercado de alquileres vacacionales en la República Dominicana utilizando técnicas de web scraping para recopilar datos de Airbnb y visualizarlos en Power BI. Se enfoca en extraer información relevante de los listados de Airbnb como precios, número de huéspedes, características del alojamiento y políticas de reserva.

## Estructura del Proyecto

1. **Recopilación de Datos**
   - **Tecnologías Utilizadas:** Python, Selenium, BeautifulSoup, ChromeDriverManager.
   - **Proceso:** Extracción de datos de Airbnb mediante técnicas de web scraping, segmentando la búsqueda en áreas geográficas específicas.

2. **Limpieza y Organización de Datos**
   - **Pasos Clave:** 
     - Renombramiento y estandarización de variables.
     - Eliminación de datos innecesarios y limpieza de texto.
     - Mapeo de ubicaciones y tipos de alojamientos.
     - Imputación de valores nulos utilizando KNNImputer de scikit-learn.
     - Exportación de datos limpios en formato CSV.

3. **Visualización de Datos**
   - **Herramienta:** Power BI
   - **Visualizaciones:** Creación de dashboards interactivos para interpretar tendencias y patrones en el mercado de alquileres vacacionales.

## Resumen del repositorio

 ```bash
   - Notebooks
       - Imputacion de Valores No Encontrados - (3).ipynb
       - Limpieza de los datos - (2).ipynb
       - Reversion One Hot Encoding - (4).ipynb
       - Webscrap Airbnb V6 - (1).ipynb

   - PBI
       - Airbnb dashboard.pbix

   - Data_out
       - Hospedajes_RD - (1).xlsx
       - Hospedajes_RD- V PBI - (4).xlsx
       - Hospedajes_RD-CLEANED - (2).csv
       - Hospedajes_RD-IMPUTED V2 - (3).xlsx
 ```

## Cómo Empezar

1. **Requisitos Previos:**
   - Python 3
   - Selenium
   - BeautifulSoup
   - ChromeDriverManager
   - Power BI Desktop

2. **Instalación:**
   - Clonar el repositorio:
     ```bash
     git clone https://github.com/JuanmaGrullon/WebScraping-Airbnb.git
     ```
   - Instalar dependencias:
     ```bash
     pip install -r requirements.txt
     ```

3. **Ejecución del Web Scraping:**
   - Iniciar Jupyter Notebook:
     ```bash
     jupyter notebook
     ```
   - Abrir y ejecutar todas las celdas en `Webscrap Airbnb V6 - (1).ipynb`.

4. **Limpieza de Datos:**
   - Iniciar Jupyter Notebook:
     ```bash
     jupyter notebook
     ```
  - Abrir y ejecutar todas las celdas en `Limpieza de los datos - (2).ipynb`.

5. **Imputación de valores Nulos:**
   - Iniciar Jupyter Notebook:
     ```bash
     jupyter notebook
     ```
  - Abrir y ejecutar todas las celdas en `Imputacion de Valores No Encontrados - (3).ipynb`.

6. **Reversión del proceso de One Hot Encoding:**
   - Iniciar Jupyter Notebook:
     ```bash
     jupyter notebook
     ```
  - Abrir y ejecutar todas las celdas en `Reversion One Hot Encoding - (4).ipynb`.

7. **Visualización en Power BI:** 
 - Abrir `Airbnb dashboard.pbix` en Power BI Desktop.
   

# Resultados Y Análisis

## Dataframe

La siguiente imagen muestra la salida del comando .info() aplicado al DataFrame final, proporcionando información sobre el número de entradas no nulas y el tipo de datos de cada columna. El DataFrame resultante contiene 5038 filas y 22 columnas, indicando un conjunto de datos considerable que abarca una amplia gama de variables relevantes para el análisis de alojamientos en Airbnb.

![imagen](https://github.com/user-attachments/assets/7642033a-6886-4a1c-902f-911a0fdcf8a4)

## Dashboard

La siguiente ilustración nos muestra una introducción a los datos de alojamientos en Airbnb. Donde lo primero que podemos notar es que tenemos una muestra de 4,831 alojamientos, lo que equivale a 11,277 habitaciones. 

![imagen](https://github.com/user-attachments/assets/b1e4cebd-9233-4a73-99ef-3ff7afda6095)


En el gráfico #3 se visualiza la segmentación de mercado basada en el tipo de alojamiento, mientras que en el grafico #4 se plasma el precio promedio por habitación según alojamiento. El análisis de estos gráficos nos aportaron bastante para las ideas de estrategias que se exponen en los párrafos siguientes.  
Los apartamentos y aparthoteles presentan una alta cantidad de ofertas (2,065 y 1,462 respectivamente) y precios promedio similares (alrededor de $220 USD por alojamiento y aproximadamente $83 USD por habitación). En este caso, se recomienda implementar una estrategia de precios competitivos, incluyendo descuentos para estancias prolongadas o promociones de última hora para aumentar la ocupación en periodos de baja demanda. Además, ofrecer servicios adicionales gratuitos o a bajo costo, como transporte al aeropuerto, desayuno incluido, o acceso a instalaciones recreativas, podría diferenciar a estos alojamientos en un mercado competitivo.
Las villas y hoteles tienen precios más altos ($264.55 USD y $228.33 USD por alojamiento; $79.65 USD y $83.97 USD por habitación respectivamente). Se recomienda diseñar campañas de marketing que resalten las experiencias premium, como el lujo y la exclusividad. Paquetes que combinen alojamiento con experiencias locales exclusivas (tours privados, cenas gourmet, servicios de spa) pueden justificar los precios más elevados. Además, es fundamental identificar y dirigirse a segmentos de mercado con mayor poder adquisitivo, como turistas internacionales o viajeros de negocios, utilizando canales de marketing especializados.
Los hostales y cabañas tienen precios más bajos ($107.12 USD y $145.63 USD por alojamiento; $91.63 USD y $68.21 USD por habitación respectivamente). Para atraer a viajeros con presupuesto limitado, se pueden ofrecer paquetes económicos que incluyan actividades locales gratuitas o a bajo costo. Promociones especiales dirigidas a grupos jóvenes o mochileros pueden incrementar la ocupación. 

*Gráfico 3. Precio promedio por tipo de alojamiento*

![imagen](https://github.com/user-attachments/assets/02ee21b9-ba10-41a7-abbf-795dba0577d4)

Los barcos presentan precios elevados ($291.33 USD por alojamiento y $61.96 USD por habitación). Estos tipos de alojamiento pueden capitalizar su exclusividad destacando las experiencias únicas que ofrecen. Los barcos, con un costo bajo por habitación, pueden ser promovidos como opciones únicas y asequibles. Enfocar las campañas en la experiencia singular de alojarse en un barco, combinado con el atractivo costo, puede atraer a turistas en busca de aventuras únicas.

*Gráfico 4. Precio promedio por habitación según alojamiento*
![imagen](https://github.com/user-attachments/assets/3e7d6623-8785-4854-8ee2-9d64f9180103)

El gráfico #5 muestra que el precio promedio de los alojamientos aumenta considerablemente a medida que se incrementa la capacidad de huéspedes, especialmente a partir de los ocho huéspedes. Esto sugiere una demanda significativa por alojamientos de mayor capacidad.
Para capitalizar esta tendencia, se propone aumentar el número de camas y, por ende, la capacidad de los alojamientos. Esta estrategia no solo permite captar una mayor cuota del mercado, sino también justificar precios más altos. La implementación de esta estrategia requiere optimizar el uso del espacio en los alojamientos. Esto podría incluir la reconfiguración de habitaciones para añadir más camas sin comprometer el confort, así como la adición de camas plegables o literas. También es fundamental asegurar que las áreas comunes sean adecuadas para un mayor número de huéspedes, manteniendo así una experiencia positiva para todos.

*Gráfico 5. Precio promedio por cantidad de huéspedes permitidos*
![imagen](https://github.com/user-attachments/assets/733b2d56-45d1-4470-ac1c-0c2ebf91ff71)

Los gráficos de dispersión presentados en el conjunto de Gráficos #6, junto con los niveles de correlación, indican una correlación positiva fuerte entre las calificaciones de los alojamientos y sus precios. Esta relación es particularmente evidente en las siguientes dimensiones: calificación general, calificación de limpieza, calificación de ubicación y calificación de comunicación.

*Ilustración 19. Niveles de correlación de las calificaciones y el precio*

![imagen](https://github.com/user-attachments/assets/5bb823f3-597b-4bc6-9410-52eaee5210c1)

Dada la fuerte correlación positiva entre las calificaciones y el precio, se recomienda enfocar los esfuerzos en mantener y mejorar constantemente estas calificaciones para maximizar los ingresos.

*Gráfico 6. Conjunto de gráficos de dispersión entre las calificaciones y el precio*

![imagen](https://github.com/user-attachments/assets/02afe329-4193-4f0c-b58e-af5f96f4d48b)


# Conclusiones

Este proyecto demuestra cómo la combinación de técnicas de web scraping y herramientas de visualización de datos puede transformar datos crudos en información significativa y accionable. Los insights obtenidos pueden ser utilizados por empresas del sector turístico, investigadores y profesionales del marketing para tomar decisiones informadas y estratégicas, mejorando así su oferta de servicios y adaptándose mejor a las necesidades del mercado.

# Agradecimientos

- A mi esposa Perla Hilario por su inquebrantable apoyo.
- A mi tutor el Dr. Deyslen Mariano Hernandez por su orientación.
- A Alvin Luperon por su apoyo en la creación del dashboard en Power BI.

# Autor
Juan Manuel Grullón Jiménez

