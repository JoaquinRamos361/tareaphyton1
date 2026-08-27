# Bot de Discord - Clasificador de Imágenes

## Descripción

Este proyecto es un bot de Discord capaz de recibir imágenes enviadas por los usuarios y clasificarlas automáticamente mediante un modelo de inteligencia artificial entrenado previamente.

El bot utiliza un modelo de aprendizaje automático desarrollado con TensorFlow/Keras (`keras_model.h5`) y un archivo de etiquetas (`labels.txt`) para determinar a qué clase pertenece una imagen.

Cuando un usuario envía una imagen al bot, este:

1. Detecta que el mensaje contiene una imagen.
2. Descarga la imagen enviada.
3. La procesa y la adapta al tamaño requerido por el modelo.
4. Utiliza el modelo entrenado para realizar una predicción.
5. Obtiene la clase con mayor probabilidad.
6. Responde en Discord indicando la clasificación y el nivel de confianza.

## Funcionamiento 

El modelo `keras_model.h5` contiene la red neuronal entrenada para reconocer las diferentes clases de imágenes.

El archivo `labels.txt` contiene los nombres de las clases que el modelo puede reconocer.

Antes de realizar la predicción, la imagen se convierte al formato RGB, se redimensiona a **224x224 píxeles** y se normalizan sus valores para que puedan ser procesados correctamente por el modelo.

Finalmente, el bot obtiene la predicción con mayor probabilidad y muestra un mensaje como:

`Class: nombre_de_la_clase | Confidence Score: 95.23%`

## Uso

Para utilizar el bot:

1. Ejecutar el programa.
2. Invitar el bot a un servidor de Discord.
3. Enviar una imagen en un canal donde el bot tenga permisos.
4. El bot analizará automáticamente la imagen y responderá con su clasificación.

## Archivos principales

- `keras_model.h5` → modelo de inteligencia artificial entrenado.
- `labels.txt` → etiquetas de las clases.
- Código Python → controla el bot y realiza la clasificación de imágenes.

## Objetivo

El objetivo del proyecto es integrar un modelo de clasificación de imágenes con Discord para crear un sistema capaz de analizar imágenes automáticamente dentro de un servidor.
