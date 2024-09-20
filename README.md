# Detección Automática de Neumonía en Radiografías con una CNN Personalizada

Este proyecto presenta una red neuronal convolucional (CNN) personalizada para detectar neumonía en imágenes de radiografías de tórax. El modelo fue entrenado desde cero utilizando un conjunto de datos público de Kaggle, logrando una alta precisión en la clasificación binaria de neumonía.

## Descripción del Proyecto
La neumonía es una enfermedad respiratoria aguda que puede ser mortal si no se diagnostica a tiempo. Este proyecto tiene como objetivo desarrollar un modelo de IA capaz de apoyar a los médicos en el diagnóstico de neumonía a partir de radiografías. El modelo se centra en la extracción de características visuales para detectar patrones que indiquen la presencia de la enfermedad.

## Dataset
El conjunto de datos utilizado proviene de Kaggle, compuesto por imágenes de rayos X clasificadas en dos categorías:
- **PNEUMONIA**: Imágenes de pacientes diagnosticados con neumonía.
- **NORMAL**: Imágenes de pacientes sin neumonía.

## Preprocesamiento de Imágenes
Las imágenes se preprocesaron para mejorar el rendimiento del modelo:
- Conversión a escala de grises.
- Redimensionamiento a 150x150 píxeles.
- Normalización (valores entre 0 y 1).
- Aumentación de datos (rotación, zoom, desplazamiento, volteo horizontal).

## Arquitectura del Modelo
La arquitectura de la CNN incluye las siguientes capas:
- **Capas Convolucionales**: 5 capas con filtros que aumentan progresivamente de 32 a 256.
- **Capas de Pooling**: MaxPooling2D para reducir la dimensionalidad.
- **Dropout**: Para evitar el sobreajuste.
- **Capas Densas**: Capa final para la clasificación binaria con función de activación sigmoide.

## Resultados
El modelo obtuvo los siguientes resultados en el conjunto de prueba:
- **Precisión Global**: 92%.
- **AUC (Área Bajo la Curva)**: 0.96.
- **Matriz de Confusión**: Sensibilidad del 97% en la clase 'PNEUMONIA'.

## Instrucciones para Ejecutar el Proyecto
1. Clona este repositorio:
    ```bash
    git clone https://github.com/usuario/repo_neumonia.git
    ```
2. Instala las dependencias necesarias:
    ```bash
    pip install -r requirements.txt
    ```
3. Ejecuta el Jupyter Notebook:
    ```bash
    jupyter notebook ModeloNeumonia.ipynb
    ```

## Conclusiones
Este proyecto demuestra la efectividad de las redes neuronales convolucionales en la clasificación de radiografías de tórax para la detección de neumonía. Si bien el modelo tiene un alto rendimiento, se recomienda su uso como herramienta complementaria al diagnóstico médico.

## Referencias
- Paul Mooney. Chest X-Ray Images (Pneumonia). Kaggle, 2018. Disponible en: https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia
- F. Chollet. Keras. GitHub, 2015. Disponible en: https://github.com/fchollet/keras
