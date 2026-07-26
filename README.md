# Pre-entrega-1

## Contexto
Este repositorio fue creado en el marco de la primera entrega del curso: Data Science III: NLP & Deep Learning aplicado a Ciencia de Datos, brindado por CoderHouse.

## Objetivo
El objetivo de este trabajo es armar un pipeline de entrenamiento y validación en PyTorch. Se utilizó el dataset Iris para entrenar un modelo que clasifica sus tres especies.

## Estructura
- `data/`: contiene la referencia al dataset utilizado (en este caso, solo se utilizó un dataset artificial cargado en el notebook).
- `notebooks/`: contiene el notebook con el entrenamiento y la validación.
- `requirements.txt`: contiene las dependencias del proyecto.

## Preparación y modelo
El dataset se dividió en 80% para entrenamiento y 20% para validación. Los datos se normalizaron usando solamente el conjunto de entrenamiento.

El modelo utilizado es un MLP con 4 variables de entrada (las cuatro medidas que describen a cada flor), una capa oculta de 16 neuronas con ReLU y una salida de 3 clases. El entrenamiento se realizó con Adam y CrossEntropyLoss durante 100 épocas.

El notebook detecta automáticamente si puede utilizar CUDA, MPS o CPU.

## Configuración
- PyTorch: 2.13.0
- Learning rate: 0.001
- Batch size: 16
- Épocas: 100

## Resultados
La pérdida de entrenamiento bajó de 1.0332 a 0.1215 durante las 100 épocas. La pérdida final de validación fue de 0.1689 y la accuracy alcanzó un 93.33%. Estos resultados muestran que el modelo aprendió a clasificar la mayoría de los datos de validación.