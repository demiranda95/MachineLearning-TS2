# 📊 Machine Learning – Trabajo Sumativo Unidad 2

## 📌 Descripción del Proyecto
Este repositorio contiene el desarrollo del **Trabajo Sumativo Unidad 2** de la asignatura *Machine Learning*, el cual da continuidad al análisis realizado en la Unidad 1 sobre el caso **Walmart Sales Forecasting**.

En esta etapa, el enfoque se centra en el **modelamiento supervisado**, reformulando el problema original de regresión a un problema de **clasificación binaria**, con el objetivo de identificar semanas de ventas altas y bajas.

---

## 🎯 Objetivo
Evaluar y comparar distintos modelos de Machine Learning para predecir la variable **High_Sales**, definida como:

- `1` → Semana con ventas sobre la mediana  
- `0` → Semana con ventas bajo la mediana  

El objetivo es:
- Comparar desempeño de modelos
- Justificar métricas utilizadas
- Seleccionar el mejor modelo para el problema

---

## 🧠 Modelos Implementados
Se entrenaron y compararon los siguientes modelos:

- 🔹 **Regresión Logística Penalizada**
  - Lasso (L1)
  - Ridge (L2)

- 🌲 **Random Forest**
- ⚡ **XGBoost**
- 🧩 **Red Neuronal (MLPClassifier)**

---

## 📊 Métricas de Evaluación
Se utilizaron métricas de clasificación sobre el conjunto de validación:

- Accuracy
- Precision
- Recall
- F1-Score ⭐ (métrica principal)
- AUC

---

## 🧪 Resultados Principales
- **Random Forest** obtuvo el mejor desempeño en F1-score (~0.95)
- **XGBoost** alcanzó el mejor AUC (~0.986)
- Modelos lineales (Lasso y Ridge) mostraron bajo desempeño (~0.62 F1)
- La red neuronal tuvo rendimiento intermedio

👉 Conclusión:  
El problema presenta **relaciones no lineales complejas**, mejor capturadas por modelos basados en árboles.

---

## ⚙️ Optimización de Hiperparámetros
Se aplicó:

- **RandomizedSearchCV**
- Validación cruzada (cv = 3)
- Métrica objetivo: F1-score

🔎 Resultado:
- La optimización **no mejoró** el desempeño del modelo base
- Sirvió como validación metodológica del proceso

---

## 🗂️ Estructura del Proyecto
```
📁 MachineLearning-TS2
│
├── Trabajo_Sumativo_2_Machine_Learning.ipynb
├── train_prepared_ts2.csv
├── val_prepared_ts2.csv
├── test_prepared_ts2.csv
└── README.md
```

---

## 🔁 Pipeline del Notebook
El flujo desarrollado incluye:

1. Carga de datos (train, validation, test)
2. Conversión de variables (Date)
3. Creación de variable objetivo `High_Sales`
4. Selección de variables explicativas
5. Entrenamiento de modelos
6. Evaluación con métricas
7. Comparación de resultados
8. Optimización de hiperparámetros
9. Evaluación final en test

---

## 📌 Consideraciones Metodológicas
- Se utilizó **partición temporal** (heredada de Unidad 1)
- Dataset balanceado (mediana como umbral)
- Escalamiento aplicado para red neuronal
- Modelos comparados bajo mismo set de variables

---

## 👨‍💻 Integrantes
- Diego Miranda  
- Arturo Irribarra  
- Ignacio Gutiérrez  
- Sebastián Martínez  
- Cristian Vergara  

---

## 📎 Repositorio
👉 [https://github.com/demiranda95/MachineLearning-TS2](https://github.com/demiranda95/MachineLearning-TS2)

---

## 📚 Contexto
Este trabajo corresponde a la continuación del pipeline desarrollado en la **Unidad 1**, donde se abordaron:

- Exploración de datos
- Limpieza
- Feature engineering
- Separación temporal

---

