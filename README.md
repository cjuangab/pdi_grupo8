#SentaIA: Evaluación de Reacciones en Avant-Premières

## Visión General
Este proyecto utiliza técnicas de **Visión Artificial** para analizar la respuesta emocional de la audiencia durante las funciones de pre-estreno (avant-premières). El objetivo es mapear las reacciones del público con los momentos clave de la narrativa fílmica, permitiendo a directores y productores identificar:

* **Impacto Emocional:** ¿La escena de terror realmente asusta? ¿El chiste causó gracia?
* **Engagement:** Identificación de momentos de desinterés o fatiga.
* **Sincronización Narrativa:** Correlación entre el *timestamp* de la película y la emoción predominante en la sala.

---

## Dataset
El modelo se entrena utilizando el dataset **Emotion Recognition from Faces**, que permite clasificar expresiones faciales en diversas categorías emocionales.

* **Fuente:** [Kaggle - Emotion Recognition Dataset](https://www.kaggle.com/code/gabrielenoaro/emotion-recognition-from-faces-with-cnn-eda)
* **Clases objetivo para el cine:**
    * **Surprise:** Ideal para medir giros de trama o *jump scares*.
    * **Happy:** Para medir la efectividad del humor o finales satisfactorios.
    * **Fear:** Crucial para cine de suspenso y terror.
    * **Sad:** Evaluación de momentos dramáticos.
    * **Neutral/Boredom:** Identificación de escenas con ritmo lento.

---

## Metodología Técnica
Se implementa una **Red Neuronal Convolucional (CNN)** optimizada para trabajar en condiciones de iluminación variable (comunes en salas de cine).

### Flujo de Trabajo:
1.  **Detección Facial:** Localización de múltiples rostros en una sola toma de la audiencia.
2.  **Clasificación de Emociones:** Inferencia individual por cada espectador detectado.
3.  **Agregación de Datos:** Cálculo del "Sentimiento Promedio de la Sala" en intervalos de tiempo específicos.
4.  **Visualización de Resultados:** Generación de una línea de tiempo emocional comparada con el metraje de la película.


---

Aplicaciones Futuras
* **A/B Testing de Finales:** Comparar qué versión de un final genera mejores reacciones.
* **Optimización de Trailers:** Seleccionar las escenas que generaron mayor "Surprise" para el material promocional.
* **Mapas de Calor:** Identificar qué zonas de la sala están más conectadas con la experiencia.

---
