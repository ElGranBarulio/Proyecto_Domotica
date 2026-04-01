IA de Detección de Derroche Energético

Este proyecto utiliza técnicas de Machine Learning y Deep Learning para predecir situaciones de derroche de calefacción en edificios educativos. El sistema analiza datos de sensores de temperatura y contacto para identificar cuándo se está perdiendo energía de forma ineficiente.
  Características Principales

    Inferencia Térmica (ML Lineal): Estimación de temperaturas en aulas sin sensores físicos mediante regresión lineal basada en sensores de referencia.

    Lógica de Pesos (Tarea 6): Sistema de puntuación ponderada para aperturas:

         Puertas: Peso x4.

         Ventanas Grandes: Peso x2.

         Ventanas Pequeñas: Peso x1.

    Red Neuronal Predictiva: Modelo MLP (Perceptrón Multicapa) entrenado para predecir el derroche en la próxima hora.

    Gestión de Desequilibrio: Uso de class_weight y ajuste de umbral de decisión para maximizar la detección de casos críticos.

 Arquitectura del Modelo IA

El modelo de Red Neuronal ha sido implementado con TensorFlow/Keras:

    Capa de Entrada: Datos climáticos, hora, estado de calefacción y puntos de apertura.

    Capas Ocultas: Tres capas densas (64, 32, 16 neuronas) con activación ReLU.

    Regularización: Capas de Dropout al 30% para evitar el sobreajuste (overfitting).

    Capa de Salida: Neurona única con activación Sigmoid para clasificación binaria.

Shutterstock

    Explorar

 Resultados del Modelo

Tras los ajustes de sensibilidad, el modelo presenta las siguientes métricas de rendimiento:

    Exactitud (Accuracy): 90.59%

    Precisión (Clase Derroche): 40.62%

    Sensibilidad (Recall): 38.61%

    F1-Score: 39.59%

    Nota técnica: Se priorizó el Recall sobre la Precisión ajustando el umbral de decisión a 0.3. Esto permite detectar un mayor número de derroches reales, asumiendo un margen controlado de falsos positivos, ideal para un sistema de alerta temprana.

 Tecnologías Utilizadas

    Lenguaje: Python 3.x

    Entorno: Google Colab / Jupyter Notebooks

    Librerías: * Pandas & NumPy (Procesamiento de datos)

        Scikit-learn (ML Lineal y Escalado)

        TensorFlow & Keras (Redes Neuronales)

        Matplotlib & Seaborn (Visualización)

 Estructura del Repositorio

    CODIGO_PROPUESTO_IA.ipynb: Notebook principal con el flujo completo.

    DATASET_ENTRENAMIENTO_IA.csv: Datos procesados listos para la red neuronal.

    analisis_derroche_final.csv: Exportación de resultados y predicciones.

 Cómo usar este proyecto

    Sube los archivos CSV (resultado_final.csv y History...) a tu entorno de ejecución.

    Ejecuta las celdas de limpieza y entrenamiento.

    El sistema generará automáticamente las gráficas de rendimiento y descargará los resultados.
