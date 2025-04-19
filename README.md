Aprendizaje de Máquina para el Análisis del Rendimiento de Ventas en Comercio Electrónico

En este proyecto se utiliza el conjunto de datos Online Retail II del Repositorio de Aprendizaje Automático de UCI Irvine Machine Learning Repository
(https://archive.ics.uci.edu/ml/datasets/Online+Retail+II). El análisis y prueba con modelos de aprendizaje automático estan enfocados en
- Clasificación de clientes
- Segmentación mediante clustering
- Predicción de ventas

Dataset El conjunto de datos Online Retail II contiene transacciones de una tienda de comercio electrónico con sede en el Reino Unido, registradas entre 
diciembre de 2009 y diciembre de 2011. Cada fila representa una compra individual. 

Parte 0: Preparación de datos
-  Unificación de las hojas de registro por año en un solo archivo
- limpieza de valores nulos y duplicados, así como exclusion de transacciones sin "CustumerID"
- Análisis exploratorio de cantiades de producto más vendidos, comportamiento de compras en el tiempo, productos más polpulares entre clientes y evolución promedio de los precios
- - Se entrenó un modelo de clasificación 
    - Random Forest Classifier
    - Metricas de evaluación: Matriz de confusión, accuracy, precision, recall y F1-score
      
Parte 1: Clasificación de clientes
- Se definieron dos clases: cliente normal y cliente premium basadas en el volument todas de compras por cliente
- Se entrenaron un modelos de clasificación  
    - K-means y Mean Shift
    - Comparación entre los dos métodos de segmantación
      
Parte 3: Predicción de ventas
- Se generaron nuevas características:
-    DiaSemana-para ver que días hay más venta
-    Mes-para detección de pratones mensuales
-    Hora-para saber que tiempo es mas activo mañana/tarde
-    TemporadaAlta-valor binario para picos de nov-dic
-    LongitudDescripcion-ara identificar descripcion producto con su tamaño de caracteres
-    EsPromo-identificar palabras relacionadas a sale/discount/promo
- División de datos para entrenamiento y prueba
- Modelo evaluado: RandomForestRegressor
- Métricas MAE, MSE, R² Score
- Visualización de valores reales vs predichos y distribución de errores
