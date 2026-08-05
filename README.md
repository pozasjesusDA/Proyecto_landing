# Proyecto: Experimento A/B en Página de Inicio (Landing Page)

## Objetivo del proyecto

El objetivo de este proyecto es analizar los resultados de un experimento A/B realizado sobre dos versiones de una página de inicio (Landing Page), con el propósito de determinar cuál genera un mejor desempeño en términos de conversión y valor económico para el negocio.

A partir del análisis estadístico y la visualización de datos, se comparan las versiones **A** y **B** de la página, evaluando el gasto promedio de los usuarios convertidos, la tasa de conversión y la influencia de variables como la fuente de tráfico y el tipo de usuario.

---

## Dataset utilizado

**landing_experiment.csv**

El conjunto de datos contiene información de **40,000 usuarios** que participaron en el experimento A/B e incluye las siguientes variables:

| Variable | Descripción |
|----------|-------------|
| user_id | Identificador único del usuario |
| date | Fecha de participación en el experimento |
| landing | Versión de la página (A o B) |
| region | Región del usuario |
| dispositivo | Dispositivo utilizado |
| traffic_source | Fuente de tráfico del usuario |
| user_type | Tipo de usuario (Nuevo o Recurrente) |
| converted | Indica si el usuario convirtió (0 = No, 1 = Sí) |
| gasto | Monto gastado por el usuario convertido |

---

## Etapas del análisis

### 1. Exploración y validación de datos

- Carga del dataset.
- Revisión de estructura y tipos de datos.
- Verificación de valores faltantes.
- Validación de usuarios únicos.
- Revisión del rango de fechas del experimento.
- Análisis descriptivo de la variable gasto.
- Validación de las categorías del experimento (Landing A y B).

---

### 2. Comparación del gasto promedio

Se comparó el gasto promedio de los usuarios que realizaron una conversión entre las versiones **A** y **B**.

Pruebas aplicadas:

- Prueba de Levene (homogeneidad de varianzas).
- Prueba t de Welch para muestras independientes.

---

### 3. Comparación de la tasa de conversión

Se comparó la proporción de usuarios convertidos entre ambas versiones de la página mediante:

- Prueba Z para diferencia de proporciones.

---

### 4. Asociación entre fuente de tráfico y conversión

Se analizó si la fuente de tráfico influye en la probabilidad de conversión utilizando:

- Tabla de contingencia.
- Prueba Chi-cuadrada de independencia.

---

### 5. Asociación entre tipo de usuario y conversión

Se evaluó la relación entre el tipo de usuario y la conversión mediante:

- Tabla de contingencia.
- Prueba Chi-cuadrada de independencia.

---

### 6. Visualización de resultados

Se elaboraron gráficos para respaldar los resultados estadísticos:

- Barras agrupadas de conversiones por fuente de tráfico.
- Barras apiladas con tasas de conversión por fuente de tráfico.
- Barras agrupadas de conversiones por tipo de usuario.
- Barras apiladas con tasas de conversión por tipo de usuario.

---

### 7. Insight Ejecutivo

Se sintetizaron los principales hallazgos del experimento para responder preguntas clave del negocio y generar recomendaciones basadas en evidencia estadística.

---

## Principales resultados

- La **versión B** presentó una tasa de conversión significativamente mayor que la versión A.
- Los usuarios que convirtieron mediante la **versión B** registraron un mayor gasto promedio.
- La **fuente de tráfico** mostró una asociación significativa con la conversión, siendo **Email** y **Ads** las fuentes con mayores tasas de conversión, mientras que **Organic** aportó el mayor volumen de conversiones.
- No se encontró evidencia de una relación significativa entre el **tipo de usuario** (Nuevo o Recurrente) y la conversión.

---

## Conclusión

Los resultados del experimento indican que la **versión B** supera a la versión A tanto en tasa de conversión como en gasto promedio por usuario convertido, por lo que representa la mejor alternativa para implementar en la página de inicio.

Asimismo, los hallazgos sugieren priorizar estrategias de adquisición enfocadas en los canales con mayores tasas de conversión y continuar optimizando la experiencia de la página para maximizar el rendimiento del negocio.

---

## Herramientas utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Statsmodels

---

## Pruebas estadísticas aplicadas

- Prueba de Levene
- Prueba t de Welch
- Prueba Z para diferencia de proporciones
- Prueba Chi-cuadrada de independencia

---

## Cómo ejecutar el proyecto

1. Abrir el notebook en Google Colab o Jupyter Notebook.
2. Instalar las librerías necesarias si no están disponibles.
3. Cargar el archivo `landing_experiment.csv` en la carpeta `/datasets/`.
4. Ejecutar las celdas en el orden establecido para reproducir el análisis y las visualizaciones.

---

## Autor

Proyecto desarrollado como práctica de análisis estadístico y experimentación A/B utilizando Python.
