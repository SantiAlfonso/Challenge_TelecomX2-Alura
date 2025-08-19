# 📊 Predicción de Cancelación de Clientes

Este proyecto aplica técnicas de **Machine Learning** para predecir la cancelación de clientes, utilizando distintos modelos y comparando su rendimiento.  

---

## 🚀 Objetivo
Identificar los principales factores que influyen en la cancelación de clientes y evaluar diferentes modelos de clasificación con el fin de proponer estrategias de retención más efectivas.  

---

## 🛠️ Tecnologías Utilizadas
- Python 3.x  
- Pandas  
- NumPy  
- Scikit-learn  
- Matplotlib / Seaborn  

---

## 📂 Estructura del Proyecto
├── data/ # Dataset utilizado
├── notebooks/ # Experimentos en Google Colab / Jupyter
├── src/ # Código fuente (modelos, preprocesamiento, métricas)
├── results/ # Resultados, gráficos y salidas de los modelos
└── README.md # Documentación principal


---

## 📊 Modelos Evaluados
Se implementaron y compararon los siguientes modelos:  

- 🔹 **Regresión Logística**  
- 🔹 **Random Forest**  

> Nota: El proyecto puede extenderse a otros modelos como **KNN, SVM o XGBoost** para mejorar resultados.

---

## 📈 Resultados Principales

### ✔ Regresión Logística
- **Accuracy**: 0.798  
- **Precision (Yes)**: 0.66  
- **Recall (Yes)**: 0.50  
- **F1-score (Yes)**: 0.57  

Matriz de confusión:  
[[1416 136] → Predicción: "No"
[ 279 282]] → Predicción: "Yes"


---

### ✔ Random Forest
- **Accuracy**: 0.789  
- **Precision (Yes)**: 0.63  
- **Recall (Yes)**: 0.50  
- **F1-score (Yes)**: 0.56  

Matriz de confusión:  
[[1378 174] → Predicción: "No"
[ 280 281]] → Predicción: "Yes"


---

## 🔎 Análisis Crítico
- Ambos modelos tienen un desempeño similar (~79%).  
- **Regresión Logística** presenta un ligero mejor resultado global.  
- Problema común: bajo **Recall en la clase "Yes"**, es decir, muchos clientes que cancelan no son detectados.  
- Ningún modelo mostró sobreajuste (*overfitting*). Sin embargo, la regresión logística puede estar subajustando (*underfitting*).  

---

## ✅ Conclusiones
- Los factores más influyentes en la cancelación se relacionan con las variables seleccionadas en el preprocesamiento y evaluadas mediante coeficientes e importancia de variables.  
- La **Regresión Logística** ofrece un desempeño más estable y comprensible para la interpretación de resultados.  
- Se recomienda:  
  - Ajustar umbrales de decisión.  
  - Aplicar **GridSearchCV** para optimización de hiperparámetros.  
  - Explorar modelos más avanzados como **XGBoost o SVM**.  
  - Implementar técnicas de **balanceo de clases**.  
