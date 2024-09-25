# Web application using Streamlit and Render for a given dataset 

# Descripción del proyecto

En este proyecto, me proporcionaron un conjunto de datos de anuncios de venta de coches. Sin embargo, en este proyecto, el enfoque no se centrará en el conjunto de datos ni en el análisis, por lo que se es libre de elegir cualquier dataset que desees.

Se va a construir y desplegar un panel de control de una aplicación web en un servicio en la nube. Las tareas incluyen la creación y gestión de entornos virtuales de Python, el desarrollo de una aplicación web y su despliegue en un servicio en la nube que la hará accesible al público.

Para la realización de este proyecto se utlizó GitHub y **Render** el framework para este proyecto fue **Streamlit**.

Este proyecto implica realizar un análisis exploratorio de datos, se necesitará el paquete **streamlit** para desarrollar una aplicación web y el despliegue de la versión final de la aplicación en **Render**.

Aqui puedes ver el resultado final del proyecto, esta es la URL de la aplicación en Render: https://projects5.onrender.com/


# DATASETS

- **vehicles_us.csv**

# Instrucciones

**Paso 1. Configuración**

Asegúrate de haber instalado al menos los siguientes paquetes en el entorno: **pandas**, **streamlit** y **plotly-express**.

Además, necesitarás instalar una librería adicional (**nbformat**) para habilitar plotly express. Instálala mediante: 

```bash
conda install -n myenv nbformat
```

**Paso 2. Descarga del archivo de datos**

Coloca el conjunto de datos en el directorio del proyecto.

**Paso 3. Análisis exploratorio de datos**

Como construir un histograma mediante **plotly-express**:

```bash
import pandas as pd
import plotly.express as px

car_data = pd.read_csv('vehicles_us.csv') # leer los datos
fig = px.histogram(car_data, x="odometer") # crear un histograma
fig.show() # crear gráfico de dispersión
```

Cómo construir un gráfico de dispersión en esta librería:

```bash
import pandas as pd
import plotly.express as px

car_data = pd.read_csv('vehicles_us.csv') # leer los datos
fig = px.scatter(car_data, x="odometer", y="price") # crear un gráfico de dispersión
fig.show() # crear gráfico de dispersión
```

**Paso 4. Desarrollo del cuadro de mandos de la aplicación web**

Este es un ejemplo de cómo puedes hacerlo:

```bash
import pandas as pd
import plotly.express as px
import streamlit as st
        
car_data = pd.read_csv('vehicles_us.csv') # leer los datos
hist_button = st.button('Construir histograma') # crear un botón
        
if hist_button: # al hacer clic en el botón
    # escribir un mensaje
    st.write('Creación de un histograma para el conjunto de datos de anuncios de venta de coches')
            
    # crear un histograma
    fig = px.histogram(car_data, x="odometer")
        
    # mostrar un gráfico Plotly interactivo
    st.plotly_chart(fig, use_container_width=True)
```

Este es un ejemplo simple de cómo funcionan las casillas de verificación en streamlit:

```bash
import streamlit as st

# crear una casilla de verificación
build_histogram = st.checkbox('Construir un histograma')

if build_histogram: # si la casilla de verificación está seleccionada
    st.write('Construir un histograma para la columna odómetro')
    ...
```

**Paso 5. Despliegue de la versión final de la aplicación en Render**

Configura el nuevo servicio web Render añadiendo un **Build Command** que instale todo lo necesario para iniciar tu app, incluyendo streamlit y todos los paquetes de requirements.txt. Utiliza el siguiente comando:

```bash
pip install --upgrade pip & pip install -r requirements.txt
```

Añade a tu **Start Command**: 

```bash
streamlit run app.py
```

Despliega en Render y espera a que el build se ejecute con éxito.

Comprueba que tu aplicación sea accesible a través de la siguiente URL: https://<APP_NAME>.onrender.com/.

Si actualizas tu repositorio de GitHub, para implementar la versión más reciente en Render, haz clic en "Manual Deploy" → "Latest Commit" (Implementación manual → Última confirmación).

## 🛠 Skills

![Visual Studio Code](https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white)

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)

![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)

![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)

![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)

![Plotly](https://img.shields.io/badge/Plotly-%233F4F75.svg?style=for-the-badge&logo=plotly&logoColor=white)

![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)

![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)

![Render](https://img.shields.io/badge/Render-%46E3B7.svg?style=for-the-badge&logo=render&logoColor=white)

**Streamlit** 

## Lessons Learned

Aprendí a crear entornos virtuales en Python. Pude implementar una página web en Render usando el framework Streamlit. Aprendí a crear algunas herramientas y visualizaciones usando Streamlit y bibliotecas de Python. Git y GitHub son herramientas muy utiles a la hora de crear directorio de proyectos y trabajos colaborativos.

