# Comparación de Modelos de Inteligencia Artificial para Mantenimiento Predictivo

## Implementación y evaluación de modelos utilizando AI4I 2020 Predictive Maintenance

---

## Maestría en Inteligencia Artificial

**Módulo 2 – Selección de Modelos Preentrenados y Prototipado Rápido**

**Alumno:** Jonathan Daniel Bernal Sánchez

**Profesor:** Luis Ariel Vázquez Piña

**Fecha:** Julio 2026

---

# Descripción del proyecto

El presente proyecto tiene como objetivo implementar y comparar diferentes modelos de aprendizaje automático aplicados a un caso de **mantenimiento predictivo industrial**, utilizando el dataset **AI4I 2020 Predictive Maintenance**.

Se desarrollaron tres experimentos independientes empleando exactamente el mismo conjunto de datos, el mismo proceso de preparación, las mismas variables de entrada y las mismas métricas de evaluación. De esta manera, las diferencias observadas en los resultados corresponden únicamente al comportamiento de cada algoritmo.

Los modelos implementados son:

- Regresión Logística
- Random Forest
- XGBoost

Cada experimento fue desarrollado de forma independiente en Google Colab y documentado siguiendo la misma estructura metodológica para facilitar su comparación.

---

# Objetivo general

Comparar el desempeño de tres modelos de clasificación para seleccionar la alternativa más adecuada para la detección temprana de fallas en maquinaria industrial, considerando tanto la precisión de las predicciones como la eficiencia computacional.

---

# Caso de uso

Las fallas inesperadas en maquinaria industrial representan pérdidas económicas importantes debido a tiempos muertos, costos de reparación y disminución de la productividad.

El propósito del proyecto consiste en desarrollar un modelo capaz de estimar si una máquina presentará una falla a partir de variables relacionadas con sus condiciones de operación, apoyando así estrategias de mantenimiento predictivo.

---

# Dataset

**Nombre:**

AI4I 2020 Predictive Maintenance Dataset

**Origen:**

Hugging Face Datasets

El conjunto de datos contiene aproximadamente 10,000 registros sintéticos que representan diferentes condiciones de operación industrial.

## Variable objetivo

Machine Failure

- 0 = Operación normal
- 1 = Falla de máquina

## Variables utilizadas

- Type
- Air temperature [K]
- Process temperature [K]
- Rotational speed [rpm]
- Torque [Nm]
- Tool wear [min]

Las columnas identificadoras y las variables que describen directamente el tipo de falla fueron eliminadas para evitar fuga de información.

---

# Modelos implementados

## Experimento 1

### Regresión Logística

Modelo lineal utilizado como línea base del proyecto.

Características principales:

- Alta interpretabilidad.
- Bajo costo computacional.
- Entrenamiento rápido.
- Excelente punto de comparación.

---

## Experimento 2

### Random Forest

Modelo basado en múltiples árboles de decisión.

Características principales:

- Modela relaciones no lineales.
- Reduce el sobreajuste.
- Buen desempeño con datos tabulares.
- Permite estimar la importancia de las variables.

---

## Experimento 3

### XGBoost

Modelo basado en Gradient Boosting.

Características principales:

- Alta capacidad predictiva.
- Excelente desempeño en datos tabulares.
- Incluye mecanismos de regularización.
- Muy utilizado en aplicaciones industriales y competencias de Machine Learning.

---

# Tecnologías utilizadas

- Python
- Google Colab
- Hugging Face Datasets
- Hugging Face Hub
- Pandas
- NumPy
- Scikit-Learn
- XGBoost
- Matplotlib
- ipywidgets



---

# Flujo de trabajo

Cada notebook sigue exactamente el mismo procedimiento:

1. Configuración del entorno.
2. Verificación de GPU.
3. Instalación de dependencias.
4. Autenticación en Hugging Face.
5. Carga del dataset.
6. Exploración del conjunto de datos.
7. Validación de calidad.
8. Selección de variables.
9. División entrenamiento/prueba.
10. Preprocesamiento.
11. Entrenamiento del modelo.
12. Pipeline de inferencia.
13. Medición de latencia.
14. Evaluación mediante métricas.
15. Matriz de confusión.
16. Curva ROC.
17. Curva Precision-Recall.
18. Visualización de resultados.
19. Evaluación de umbrales.
20. Resumen del experimento.
21. Conclusiones.
22. Simulador interactivo.

---

# Métricas evaluadas

Para los tres experimentos se calcularon las siguientes métricas:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Tiempo de entrenamiento
- Tiempo de inferencia
- Latencia promedio

Estas métricas permiten comparar objetivamente el desempeño de cada modelo.

---

# Comparación de resultados

Una vez ejecutados los tres notebooks, la siguiente tabla puede utilizarse para resumir los resultados obtenidos.

| Modelo | Accuracy | Precision | Recall | F1-score | ROC-AUC | Latencia |
|---------|----------|-----------|--------|----------|----------|-----------|
| XGBoost |0.988 |0.907 |0.72 |0.803 |0.969 |0.045 |
| Random Forest |0.975 |0.655 |0.588 |0.62 |0.966 |0.063 |
| Regresión Logística  |0.824 |0.141 |0.823 |0.241 |0.906 |0.013 |

---

# Modelo recomendado

La selección final del modelo deberá realizarse considerando los resultados obtenidos durante la ejecución de los tres experimentos.

La recomendación deberá tomar en cuenta:

- Desempeño general.
- Capacidad para detectar fallas.
- Equilibrio entre Precision y Recall.
- F1-score.
- Tiempo de inferencia.
- Complejidad computacional.

---

# Condiciones de ejecución

- Entorno: Google Colab
- Acelerador recomendado: GPU T4
- Lenguaje: Python 3
- División entrenamiento/prueba: 80% / 20%
- Semilla aleatoria: 42
- Dataset: AI4I 2020 Predictive Maintenance

---

# Uso de la Inteligencia Artificial

Para el desarrollo de este proyecto se utilizó **ChatGPT** como herramienta de apoyo para estructurar la documentación, organizar el flujo de trabajo y generar un primer borrador del código necesario para implementar los modelos de aprendizaje automático.

Posteriormente, el código fue revisado, ajustado y validado manualmente durante su ejecución en Google Colab, verificando el correcto funcionamiento de cada algoritmo, la interpretación de las métricas obtenidas y la coherencia de los resultados con el objetivo del proyecto.

Asimismo, se empleó **Hugging Face** para la obtención del dataset y Google Colab como entorno de desarrollo para la implementación, entrenamiento y evaluación de los modelos de inteligencia artificial.

---

# Conclusiones generales

Los tres modelos fueron implementados bajo las mismas condiciones experimentales, permitiendo realizar una comparación objetiva de su desempeño para un problema de mantenimiento predictivo.

La metodología utilizada garantiza que las diferencias observadas entre los resultados corresponden únicamente al comportamiento de cada algoritmo y no a cambios en el conjunto de datos o en el proceso de entrenamiento.

La selección final del modelo recomendado dependerá del análisis conjunto de las métricas obtenidas durante la ejecución de los tres experimentos.

---

# Autor

**Alumno:** Jonathan Daniel Bernal Sánchez

**Profesor:** Luis Ariel Vázquez Piña

**Programa académico:** Maestría en Inteligencia Artificial

**Proyecto:** Comparación de modelos de inteligencia artificial para mantenimiento predictivo utilizando el dataset AI4I 2020 Predictive Maintenance.

**Versión:** 1.0
