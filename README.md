# 📈 Análisis de Acciones e Ingresos: Tesla & GameStop
> **Proyecto Final: Python Project for Data Science | IBM Professional Certificate**

Este proyecto fue desarrollado como parte del curso de **IBM en Coursera**. El objetivo principal es demostrar habilidades de **Extracción, Transformación y Carga (ETL)** de datos financieros utilizando diversas fuentes y técnicas avanzadas de Python.

---

## 📝 Descripción del Proyecto
El proyecto analiza la correlación entre el precio de las acciones y los ingresos (*revenue*) de **Tesla** y **GameStop**. 
* **Precios:** Extraídos mediante APIs financieras.
* **Ingresos:** Obtenidos mediante Web Scraping.
* **Resultado:** Un panel interactivo que permite comparar visualmente el rendimiento bursátil frente al financiero.

---

## 🛠️ Tecnologías y Librerías
* ![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=flat&logo=python&logoColor=white) **Python:** Lenguaje base del análisis.
* ![Pandas](https://img.shields.io/badge/Pandas-2.0-150458?style=flat&logo=pandas&logoColor=white) **Pandas:** Estructuración y manipulación de DataFrames.
* **BeautifulSoup (bs4):** Extracción de datos de tablas HTML.
* **Requests:** Manejo de peticiones HTTP para Web Scraping.
* **yFinance:** Extracción de datos bursátiles de Yahoo Finance.
* **Matplotlib/Plotly:** Generación de visualizaciones dinámicas.

---

## 🚀 Flujo de Trabajo (Pipeline)

### 1. Extracción de Datos de Acciones
Se utilizó la librería `yfinance` para obtener el historial completo de precios de **Tesla (TSLA)** y **GameStop (GME)**, transformando la respuesta en objetos listos para análisis temporal.

### 2. Web Scraping de Ingresos (Revenue)
Dada la ausencia de ingresos históricos en algunas APIs, se implementó un script de scraping:
* Petición a URLs de almacenamiento de IBM.
* Parseo del HTML con `BeautifulSoup`.
* Extracción selectiva de tablas financieras.

### 3. Limpieza de Datos (Data Wrangling)
Se aplicaron procesos para asegurar la integridad de los datos:
* **Regex:** Eliminación de caracteres especiales (`$`, `,`) mediante expresiones regulares.
* **Manejo de Nulos:** Gestión de valores `NaN` y cadenas de texto vacías.
* **Casting:** Conversión de tipos de datos de *String* a *Float*.

### 4. Visualización de Resultados
Se implementó la función `make_graph` para generar un dashboard con:
1. **Gráfico de Precios de Cierre:** Evolución histórica del valor de mercado.
2. **Gráfico de Ingresos:** Crecimiento financiero reportado por la empresa.

---

## 📊 Conclusiones
Este proyecto permite visualizar cómo los eventos del mercado (como el *Short Squeeze* de GameStop o la expansión de gigafábricas de Tesla) afectan el precio de las acciones en comparación con el desempeño financiero real de las compañías.

---
**Autor:** Felipe Fernández Rodriguez
**Certificación:** IBM Data Science Professional Certificate | Coursera
