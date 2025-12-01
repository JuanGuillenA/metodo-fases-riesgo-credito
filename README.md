Proyecto de modelado de riesgo de crédito utilizando KNN, Random Forest y Redes Neuronales. Se sigue un proceso sistemático basado en CRISP-DM que incluye análisis exploratorio, PCA, validación cruzada y evaluación con F1_macro. El dataset utilizado es German Credit y se simulan nuevos perfiles de clientes para evaluar la capacidad del modelo final

# Método en Fases para la Predicción de Riesgo de Crédito

Este repositorio contiene un proyecto de modelado de **riesgo de crédito bancario** utilizando el dataset público *German Credit*.  
Se implementa un **método en fases** siguiendo la metodología CRISP-DM, incluyendo análisis exploratorio, preprocesamiento, reducción de dimensionalidad (**PCA**) y comparación de tres modelos de aprendizaje supervisado:

- K-Nearest Neighbors (KNN)  
- Random Forest  
- Red Neuronal Densa  

El cuaderno (`.ipynb`) desarrolla todo el proceso paso a paso, genera las figuras necesarias y reporta las métricas finales.

---

## Contenido del repositorio

- `notebook_credit_risk.ipynb` — Cuaderno principal con el análisis completo.  
- `Figuras/` — Carpeta donde se guardan automáticamente los gráficos generados (balance de clases, matriz de correlación, PCA, matrices de confusión, etc.).  
- `README.md` — Documentación del proyecto.

---

## Descripción del método

El cuaderno implementa tres fases principales:

### **1. Preparación de Datos**
- Análisis exploratorio del dataset.  
- Pipeline con estandarización (`StandardScaler`) y codificación (`OneHotEncoder`).  
- División estratificada train/test.  
- Aplicación de **PCA** para reducción de dimensionalidad y visualización.

### **2. Modelado y Optimización**
- Comparación de **KNN**, **Random Forest** y **Red Neuronal**.  
- Validación cruzada estratificada (**5-fold**).  
- Búsqueda de hiperparámetros básicos.  
- Métrica principal: **F1_macro** (adecuada para datos desbalanceados).

### **3. Evaluación y Nuevos Ejemplos**
- Tablas de métricas para cada modelo.  
- Matrices de confusión.  
- Selección del mejor modelo.  
- Predicción sobre dos clientes simulados: uno de bajo riesgo y otro de alto riesgo.

---

## Resultados principales

- El modelo con mejor desempeño general fue la **Red Neuronal**, logrando el mayor **F1_macro**.  
- Random Forest obtuvo resultados estables y competitivos.  
- KNN mostró alta sensibilidad a la métrica de distancia.  
- Los perfiles simulados fueron clasificados correctamente según su riesgo esperado.

---

## Ejecución

Puedes ejecutar el cuaderno en:

- **Google Colab**  
- **Jupyter Notebook**  
- **VS Code (Jupyter)**  

No requiere archivos adicionales más allá del dataset cargado desde UCI dentro del notebook.

---

## Autor

**Juan Alberto Guillén Albarracín y Ariel David Solano Rivera**  
Universidad Politécnica Salesiana – Cuenca, Ecuador  

