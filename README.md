# Analizador Estadístico Profesional de Quini 6 Argentina

Este proyecto consiste en un software de analítica avanzada desarrollado en **Python** y optimizado para ejecutarse en entornos de **Google Colab** o Jupyter Notebooks. Su objetivo es procesar el histórico de sorteos de la popular lotería argentina "Quini 6" para identificar patrones, frecuencias, combinaciones consecutivas y paridades numéricas, transformando datos crudos en reglas de juego inteligentes basadas en evidencia estadística.

## Estructura del Proyecto y Objetivos

El cuaderno de análisis está diseñado de forma modular y profesional, dividiéndose en las siguientes etapas consecutivas:

1. **Importación de Librerías y Configuración del Entorno:** Preparación de herramientas esenciales de ciencia de datos (`pandas`, `numpy`, `matplotlib`, `seaborn`).
2. **Carga e Ingesta de Datos Inteligente:** Algoritmo robusto de lectura de archivos CSV locales que limpia formatos de texto y resuelve conflictos de parsing de fechas (`NaT`), ordenando el historial de forma cronológica descendente.
3. **Matriz Global de Combinaciones Repetidas:** Motor combinatorio que ordena horizontalmente las bolillas ganadoras de cada sorteo histórico para agrupar, consolidar y verificar si combinaciones exactas de 6 números ya han resultado ganadoras en el pasado, permitiendo filtrar por múltiples modalidades en simultáneo.
4. **Buscador de Combinaciones Personalizadas:** Panel interactivo donde el usuario ingresa sus 6 números de la suerte. El sistema valida las reglas del juego y realiza una búsqueda de conjuntos para identificar aciertos históricos perfectos (6 aciertos) o aproximaciones de alto valor (5 y 4 aciertos) que hubieran generado premios secundarios.
5. **Análisis de Frecuencia Individual:** Generación de reportes tabulares y gráficos de barras interactivos que mapean la cantidad de apariciones de cada número (del 00 al 45) según la modalidad seleccionada (*Tradicional, La Segunda, Revancha, Siempre Sale*).
6. **Análisis Avanzado de Paridad (Pares vs. Impares):** Evaluación distributiva de la estructura interna de los sorteos para comprobar de forma estadística los patrones mixtos más comunes.
7. **Análisis de Números Consecutivos:** Algoritmo de detección de rachas numéricas contiguas dentro de un mismo sorteo para medir la tendencia natural del azar a agrupar bolillas.
8. **Informe Ejecutivo de Conclusiones:** Resumen técnico de los sesgos populares derribados mediante el análisis masivo de datos.

## Arquitectura del Repositorio

* `quini6_analisis.ipynb`: Notebook principal con el código fuente estructurado en celdas de texto explicativas (Markdown) y bloques de código Python limpios de advertencias.
* `quini6_ejemplo.csv`: Dataset acotado de muestra que contiene los sorteos del rango 3387 al 3405, permitiendo a cualquier usuario clonar el repositorio y probar la ejecución completa del entorno.
* `.gitignore`: Archivo de seguridad fundamental que protege tu base de datos real completa (`quini6_historico.csv`) para evitar que se suba a servidores públicos.

## Buenas Prácticas y Seguridad de Datos

Siguiendo los estándares de la industria en desarrollo de software, este proyecto implementa una estrategia de **exclusión de datos sensibles**:
* El archivo con el histórico masivo real que costó recolectar (`quini6_historico.csv`) está declarado explícitamente en el archivo `.gitignore`.
* Git omitirá este archivo en cada proceso de subida, manteniéndolo seguro de forma local en tu computadora.
* Se provee la plantilla de muestra `quini6_ejemplo.csv` con la estructura de columnas exacta (`numero_sorteo`, `fecha`, `modalidad`, `bolilla_1`... `bolilla_6`) para resguardar la funcionalidad del código.

## Tecnologías Utilizadas

* **Python 3.13**
* **Pandas** (Estructuras de datos y agregaciones avanzadas)
* **NumPy** (Procesamiento de matrices y álgebra numérica lineal)
* **Matplotlib & Seaborn** (Visualizaciones y gráficos estadísticos estilizados)

---
*Desarrollado con fines analíticos y científicos aplicando ingeniería de datos.*
