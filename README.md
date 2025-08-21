# 📉 Predicción de Cancelación de Clientes - Interconnect

## 📌 Descripción del Proyecto
El operador de telecomunicaciones **Interconnect** busca predecir la **tasa de cancelación de clientes (churn)** con el objetivo de implementar estrategias de retención.  
Si se detecta que un cliente planea cancelar, se le podrán ofrecer **códigos promocionales y planes especiales**.  

Este proyecto utiliza datos de contratos, información personal, servicios de Internet y telefonía para construir un modelo de **machine learning** que prediga la cancelación.

---

## 📂 Servicios de Interconnect
Los servicios ofrecidos incluyen:  
- 📞 Teléfono fijo (con múltiples líneas).  
- 🌐 Internet (DSL o fibra óptica).  
- 🔒 Seguridad en Internet: *Protección de Dispositivo* y *Seguridad en Línea*.  
- 🛠️ Soporte técnico dedicado.  
- ☁️ Almacenamiento en la nube y backup online.  
- 📺 Streaming de TV y directorio de películas.  

Los contratos pueden ser **mensuales** o de **1 a 2 años**, con diversos métodos de pago y facturación electrónica.

---

## 📊 Descripción de los Datos
Archivos disponibles en `/datasets/final_provider/` y en [final_provider.zip](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/94210e31-fd3d-451b-a350-4a8476756413/final_provider.zip):

- `contract.csv` → Información de contratos.  
- `personal.csv` → Datos personales de clientes.  
- `internet.csv` → Servicios de Internet contratados.  
- `phone.csv` → Servicios de telefonía.  

🔑 **Variable objetivo:**  
- `EndDate` → Clientes con `'No'` siguen activos, de lo contrario han cancelado.  

---

## 🎯 Objetivo
Desarrollar un modelo de **machine learning** que prediga la probabilidad de cancelación de clientes.  

**Métrica principal:**  
- AUC-ROC  

**Métrica adicional:**  
- Exactitud (Accuracy)  

---

## 🧠 Metodología
1. **Análisis exploratorio de datos (EDA):** Integración de archivos, limpieza y visualización.  
2. **Preprocesamiento:** Codificación de variables categóricas, manejo de valores faltantes, escalado.  
3. **Balanceo de clases:** Estrategias para manejar el desbalance entre clientes activos y cancelados.  
4. **Modelado:** Pruebas con varios algoritmos de clasificación:  
   - Regresión Logística  
   - Random Forest  
   - Gradient Boosting (XGBoost, LightGBM, CatBoost)  
5. **Evaluación:** Comparación de modelos con base en AUC-ROC y Accuracy.  
6. **Selección del mejor modelo:** Optimización de hiperparámetros y validación final.  

---

## 📈 Resultados Esperados
La evaluación del modelo se basa en los siguientes criterios:  

- AUC-ROC < 0.75 → ❌ Rechazado  
- 0.75 ≤ AUC-ROC < 0.81 → ⭐ Aceptable  
- 0.81 ≤ AUC-ROC < 0.85 → ⭐⭐ Bueno  
- 0.85 ≤ AUC-ROC < 0.87 → ⭐⭐⭐ Muy Bueno  
- 0.87 ≤ AUC-ROC < 0.88 → ⭐⭐⭐⭐ Excelente  
- AUC-ROC ≥ 0.88 → 🏆 Sobresaliente  

---

## 🛠️ Tecnologías Utilizadas
- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Scikit-learn  
- LightGBM, CatBoost, XGBoost  
- Jupyter Notebook  

---

## 📦 Requisitos
Instalar dependencias con:  

```bash
pip install -r requirements.txt
