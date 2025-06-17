# Proyecto_PNL_DataMinds
Técnicas del Procesamiento del Habla 

# EQUIPO DOCENTE
Mainero, Alejandro

# GOOGLE COLAB 
Enlace https://colab.research.google.com/drive/1xu1Qo0es6_xjeG-0rvw4MwoI4-6J3zSi?usp=sharing

#  GRUPO DATAMINDS
Ayán, Trinidad
Giordano, Ariel
Herrera, Edgar Fabián
Quiroga, Fernanda
Siccardi, Luis

# # Informe Final – Procesamiento del Habla Basado en PLN
# a. Resumen del proyecto
Se diseñó y evaluó un clasificador de sentimiento para reseñas en español del IMDB Dataset of 50K Movie Reviews.
 El flujo de trabajo fue:

1) Ingesta y exploración
pandas para carga y análisis exploratorio.
Revisión de columnas review_es y sentimiento.

2) Limpieza de texto
Expresiones regulares (re.sub) para eliminar signos de puntuación y caracteres especiales.
Conversión a minúsculas y normalización opcional de acentos con unidecode.

3) Normalización léxica
Stemming: SnowballStemmer (ES).
Lematización: spaCy es_core_news_sm.
Stop-Words: filtro incorporado en CountVectorizer(stop_words='spanish').

4) Vectorización
Modelo Bolsa de Palabras (BoW) mediante CountVectorizer, una elección deliberada por su bajo costo computacional y transparencia para la etapa didáctica.

5) Entrenamiento
Clasificador Multinomial Naïve Bayes – robusto para BoW y escalable a vocabularios grandes.

6) Evaluación
Métricas: accuracy, precision, recall, F1-score y tamaño de vocabulario para siete variantes (baseline, tres técnicas individuales y tres combinaciones).

El objetivo es cuantificar cómo las técnicas de preprocesamiento influyen simultáneamente en la precisión y en la comprensión del vocabulario del modelo.

