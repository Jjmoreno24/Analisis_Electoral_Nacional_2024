# Análisis Electoral Nacional 2024 - Panamá con Power BI

![PowerBI](https://img.shields.io/badge/Power%20BI-Business%20Intelligence-yellow?style=for-the-badge&logo=powerbi) ![DAX](https://img.shields.io/badge/DAX-Medidas%20%26%20Columnas-blue?style=for-the-badge) ![Excel](https://img.shields.io/badge/Excel-Dataset-green?style=for-the-badge&logo=microsoftexcel)

## Descripción

Este proyecto consiste en el desarrollo de un análisis de inteligencia de negocios sobre los resultados de las **Elecciones Generales 2024 de Panamá**, enfocado en los comicios para **alcaldes a nivel nacional**. Utilizando **Power BI**, se construyeron dos tableros interactivos que permiten explorar los resultados electorales por partido político, distrito y provincia, aplicando conceptos de modelado de datos, relaciones entre tablas, columnas calculadas y medidas DAX.

El objetivo fue demostrar cómo Power BI permite conectar, transformar, modelar y visualizar información electoral bruta para convertirla en conocimiento accionable, mediante el uso de mapas, gráficas interactivas, segmentaciones de datos y tarjetas dinámicas.

## Desarrollo

### Herramientas y Tecnologías Utilizadas

- **Herramienta principal:** Microsoft Power BI Desktop
- **Fuente de datos:** Excel adaptado a partir de los resultados oficiales del Tribunal Electoral
- **Modelado de datos:** relaciones entre tablas y columnas calculadas
- **Lenguaje de análisis:** DAX (medidas y columnas calculadas)
- **Visualizaciones:** mapa de burbujas, segmentación de datos, tarjeta, gráfico de columnas apiladas al 100%, TreeMap, tabla

### Dataset

Los datos parten de la información pública que publica el Tribunal Electoral de Panamá para la elección de alcaldes a nivel nacional. A partir de esos resultados oficiales se hizo un proceso de limpieza y adaptación: se extrajeron únicamente los campos necesarios para este análisis y se eliminaron los que no aportaban al modelo, dejando un archivo Excel (incluido en este repositorio) organizado en cuatro tablas relacionadas entre sí:

- **Distritos** — listado de distritos, con un ID propio y el ID de la provincia a la que pertenecen.
- **Provincia** — listado de provincias del país, cada una con su ID.
- **Mesas** — cantidad de mesas por distrito, mesas escrutadas, votos nulos y votos en blanco.
- **Votos** — cantidad de votos obtenidos por cada partido político en cada distrito.

Para que el modelo funcione correctamente es necesario validar que las relaciones entre estas cuatro tablas queden bien establecidas al cargar la información, respetando la carga por tablas (y no por hojas completas del libro), ya que dentro del archivo cada hoja tiene definido el rango exacto de filas y columnas correspondiente a los datos a utilizar.

> **Nota:** en el documento original del Tribunal Electoral se usa la nomenclatura "N/P" para los distritos donde no hubo representante de un partido político. En el dataset adaptado esos espacios se dejaron en blanco por simplicidad, sin que esto afecte los resultados reales.

El archivo adaptado (`DatosVotacionAlcalde2024`) se encuentra en este repositorio. Los datos oficiales originales, sin procesar, pueden consultarse en el conjunto de datos del Tribunal Electoral para la elección de alcaldes 2024, dentro del portal de Datos Abiertos de Panamá: https://www.datosabiertos.gob.pa/dataset/te-elecciones-generales-alcaldes-2024

## Implementación

### Tablero 1 — Distribución Geográfica de Votos por Partido

Este tablero muestra la distribución de los votos por partido político ubicados geográficamente en un mapa de Panamá. Es interactivo: al seleccionar un partido desde la segmentación de datos, el mapa actualiza las burbujas mostrando la cantidad de votos obtenidos por ese partido en cada distrito disponible, mientras que una tarjeta muestra en tiempo real el total de votos obtenidos por ese partido a nivel nacional.

**Elementos visuales utilizados:** Tarjeta, Segmentación de Datos, Mapa (burbujas por distrito)

Para este tablero también se trabajó con una **columna calculada** y una **medida** en DAX, necesarias para el cálculo y despliegue de los totales de votos por partido.

### Tablero 2 — Comparativa de Votos por Provincia

Este tablero compara los votos obtenidos por cada partido político a nivel de provincia. Se usa una gráfica de columnas apiladas al 100% para representar la proporción de votos de cada partido dentro de cada provincia, acompañada de una tabla numérica que se actualiza al seleccionar una provincia o un partido en la gráfica. Se incorporó además un TreeMap que representa visualmente el peso de los votos por partido.

**Elementos visuales utilizados:** Gráfico de Columnas Apiladas en Porcentaje (100%), TreeMap, Tabla

Al igual que en el primer tablero, se implementó una **medida** en DAX para soportar los cálculos dinámicos que exige la interactividad entre los visuales.

## 🔭 Vista - Tableros

<!-- Capturas o enlace de los tableros -->

<div align="center">
<h3 align="center">Contacto 😋</h3>
</div>
<p align="center">
<a href="https://www.linkedin.com/in/TU-USUARIO" target="blank">
<img align="center" width="30px" alt="LinkedIn" src="https://www.vectorlogo.zone/logos/linkedin/linkedin-icon.svg"/></a> &nbsp; &nbsp;
<a href="https://twitter.com" target="blank">
<img align="center" width="30px" alt="Twitter" src="https://www.vectorlogo.zone/logos/twitter/twitter-official.svg"/></a> &nbsp; &nbsp;
<a href="https://github.com/TU-USUARIO" target="blank">
<img align="center" width="30px" alt="GitHub" src="https://www.vectorlogo.zone/logos/github/github-icon.svg"/></a> &nbsp; &nbsp;
</p>
