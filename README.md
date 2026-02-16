[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](
[https://colab.research.google.com/github/AlejaCruzR/Telecom_X_2/blob/main/TelecomX_LATAM_.ipynb]
)

# 📊 Telecom X – Predicción de Evasión de Clientes (Churn)

**Challenge:** Telecom X Parte 2 – Alura (Data Science / Machine Learning)

---

## 🧠 Introducción

Este proyecto corresponde a la **Parte 2 del Challenge Telecom X**, en la cual se desarrolla un **modelo predictivo de Machine Learning** para anticipar la evasión de clientes (*churn*) en Telecom X.

A partir del conjunto de datos previamente analizado y tratado en la Parte 1, el objetivo de este trabajo es construir un pipeline de modelado que permita identificar clientes con mayor probabilidad de cancelar el servicio, facilitando la toma de decisiones estratégicas orientadas a la retención.

El enfoque combina preparación de datos, entrenamiento de modelos de clasificación, evaluación con métricas adecuadas e interpretación de resultados con una perspectiva de negocio.

---

## 🎯 Objetivos del proyecto

- Preparar los datos para su uso en modelos de Machine Learning.
- Analizar el balance de clases y su impacto en el modelado.
- Entrenar y comparar distintos modelos de clasificación.
- Evaluar el desempeño mediante métricas apropiadas para problemas de churn.
- Interpretar la importancia de las variables más relevantes.
- Generar conclusiones y recomendaciones estratégicas basadas en los resultados.

---

## 🧹 Preparación y preprocesamiento de datos

En esta etapa se realizaron las siguientes tareas:

- Carga del archivo tratado en la Parte 1 del proyecto.
- Eliminación de columnas irrelevantes para el modelado (identificadores).
- Codificación de variables categóricas mediante **One-Hot Encoding**.
- Separación de variables numéricas y categóricas utilizando `ColumnTransformer`.
- Análisis de la proporción de churn para detectar desbalance de clases.
- Normalización aplicada únicamente a los modelos sensibles a la escala.

---

## 🤖 Modelado y evaluación

Se entrenaron y evaluaron los siguientes modelos:

- **Baseline (DummyClassifier):** utilizado como referencia para evaluar el valor agregado de los modelos predictivos.
- **Árbol de Decisión:** modelo no sensible a la escala, con buena interpretabilidad.
- **Regresión Logística:** modelo sensible a la escala, seleccionado como modelo final por su desempeño y capacidad explicativa.

La evaluación se realizó utilizando:

- Accuracy
- Precision
- Recall
- F1-score
- Matrices de confusión (valores absolutos y normalizados)

Se priorizaron métricas como **Recall** y **F1-score**, considerando el desbalance moderado de clases y la importancia de detectar clientes con riesgo de evasión.

---

## 📈 Importancia de las variables

A partir del modelo seleccionado (Regresión Logística), se analizó la contribución de las variables al proceso de predicción.

Los resultados indican que la evasión de clientes está principalmente asociada a:

- Baja antigüedad del cliente.
- Contratos de corto plazo.
- Determinadas configuraciones de servicios y cargos.

Por el contrario, una mayor permanencia y contratos de mayor duración actúan como factores protectores frente al churn.

---

## 📌 Conclusiones

El modelo de **Regresión Logística** presentó el mejor desempeño general, logrando un equilibrio adecuado entre precisión y capacidad de detección de clientes que cancelan.

El análisis confirma que la evasión de clientes no depende de un único factor, sino de la combinación de variables contractuales, económicas y de relación con el servicio. La utilización de modelos predictivos permite anticipar comportamientos de riesgo y orientar acciones preventivas basadas en datos.

---

## 💡 Recomendaciones estratégicas

- Implementar estrategias de retención temprana para clientes con baja antigüedad.
- Incentivar la migración hacia contratos de mayor duración.
- Priorizar acciones comerciales sobre clientes identificados como de alto riesgo.
- Integrar el modelo predictivo como sistema de alerta temprana dentro del negocio.

---

## 🛠️ Tecnologías utilizadas

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Matplotlib  
- Seaborn  
- Google Colab  

---

## 📘 Nota final

Este proyecto forma parte del **Challenge Telecom X Parte 2 del programa de formación de Alura** y fue desarrollado con fines educativos y analíticos, aplicando técnicas de Data Science y Machine Learning a un caso de negocio realista.
