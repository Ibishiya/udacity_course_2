Hallazgos clave del análisis de datos
•	Se creó exitosamente un formulario utilizando ipywidgets para capturar los detalles de las transacciones, incluyendo características numéricas y un tipo categórico.
•	Se desarrolló una función predict_fraud para procesar la entrada del formulario.
•	El procesamiento implicó la codificación one-hot de la característica categórica 'type' y el escalado de las características numéricas utilizando un escalador pre-entrenado.
•	La entrada preprocesada se convirtió en un DataFrame de pandas con las columnas ordenadas para que coincidieran con los datos de entrenamiento utilizados por el modelo.
•	Se utilizó el método .predict_proba() del modelo entrenado para predecir la probabilidad de fraude para la transacción de entrada.
•	Se extrajo y mostró al usuario la probabilidad predicha de fraude (clase 1).
Ideas o próximos pasos
•	El formulario interactivo permite probar en tiempo real el modelo de detección de fraude entrenado con datos de transacciones personalizados.
•	Las mejoras adicionales podrían incluir la adición de validación de entrada al formulario y proporcionar una indicación visual más clara del resultado de la predicción (por ejemplo, codificación por colores basada en la probabilidad).
