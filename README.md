# Detección de Fraude en Transacciones con Tarjeta de Crédito 💳

Este proyecto tiene como objetivo identificar transacciones fraudulentas a partir de un dataset real de tarjetas de crédito utilizando técnicas de análisis de datos y modelos de machine learning. Es un proyecto realizado para el curso de IA de IBM.

## 📁 Dataset

El dataset contiene 284,807 transacciones realizadas por titulares europeos en septiembre de 2013. Solamente 492 transacciones (0.172%) fueron fraudulentas.

- Cada fila representa una transacción.
- Las características `V1` a `V28` provienen de una transformación PCA por motivos de privacidad.
- Las columnas `Time` y `Amount` no fueron transformadas.
- La columna `Class` es la variable objetivo: 
  - `1` = transacción fraudulenta  
  - `0` = transacción legítima

## 🧪 Proceso

### 1. Carga y limpieza de datos
- Eliminación de duplicados
- Verificación de valores nulos

### 2. Análisis exploratorio
- Porcentaje de fraude (~0.17%)
- Importe medio de fraude (~123.87 €)
- Visualización con histogramas y gráficos de barras

### 3. Preprocesamiento
- División en conjuntos de entrenamiento y prueba (80% - 20%)
- Estandarización de características opcional

### 4. Modelado
Se utilizó un modelo de **Random Forest Classifier** con los siguientes parámetros:
- `max_depth = 150`
- `random_state = 42`

### 5. Evaluación del modelo
- **Accuracy**: 99.95%
- **Recall (fraudes)**: 0.73
- **Precision (fraudes)**: 0.96
- **F1-score (fraudes)**: 0.83
- **Confusion Matrix**:
  - Verdaderos positivos (fraude detectado): 67
  - Falsos negativos (fraudes no detectados): 25
  - Falsos positivos: 3
