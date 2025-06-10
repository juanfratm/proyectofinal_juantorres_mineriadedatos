# proyectofinal_juantorres_mineriadedatos
Datasets, codigo, README, jupyter notebook del proyecto final. Juan Torres, Grupo 1CA219, E-8-160393
ANÁLISIS DE OPINIONES Y CARACTERÍSTICAS DE LISTADOS DE AIRBNB MÉXICO USANDO MINERÍA DE TEXTO Y APRENDIZAJE SUPERVISADO
===============================================================

Este proyecto tiene como objetivo analizar los comentarios de usuarios en Airbnb, aplicando técnicas de minería de texto y modelos de aprendizaje supervisado, con el fin de analizar los os los factores que influyen en las calificaciones de los alojamientos de Airbnb en México. El flujo de trabajo incluye limpieza de datos, filtrado por idioma, preprocesamiento de texto, modelado con machine learning y análisis de interpretabilidad.

REQUISITOS
----------

Antes de ejecutar el proyecto, se debe tener instalado:

- Python 3.8 o superior

- Las siguientes librerías:

  pandas  
  numpy  
  seaborn  
  matplotlib  
  nltk  
  scikit-learn  
  imbalanced-learn  
  shap  
  wordcloud  
  langdetect  
  emoji  

Se pueden instalar todas con:

pip install pandas numpy seaborn matplotlib nltk scikit-learn imbalanced-learn shap wordcloud langdetect emoji

También debes descargar los recursos de NLTK ejecutando: 

```python
import nltk
nltk.download('stopwords')
nltk.download('punkt')
nltk.download('wordnet')
nltk.download('vader_lexicon')

ARCHIVOS DE ENTRADA
Los únicos archivos que se necesitan al comienzo son:
•	listings.csv
•	reviews.csv
Ambos deben estar ubicados en la misma carpeta donde se encuentran los dos códigos principales.
PASOS DE EJECUCIÓN
I.	Ejecutar el CÓDIGO PRINCIPAL (PROYECTO FINAL), hasta antes del PREPROCESAMIENTO DE TEXTO
1.	Limpiar y transformar los archivos listings.csv y reviews.csv.
2.	Unir ambos en un solo archivo llamado: Datos_Completos_finales.csv

II.	Ejecutar el CÓDIGO DE FILTRADO POR IDIOMA (Filtrado_EN):
Este script toma como entrada el archivo generado en el paso anterior: Datos_Completos_finales.csv.
1.	Limpiar y filtrar los comentarios para dejar solo aquellos que estén escritos claramente en inglés.
2.	El resultado final será: Archivo_Filtrado_EN.csv
Este proceso puede tardar varios minutos u horas, dependiendo del equipo, ya que analiza más de 1 millón de comentarios.
III.	Volver al CÓDIGO PROYECTO FINAL:
A partir del archivo Archivo_Filtrado_EN.csv, se realiza:

1.	Preprocesamiento de texto (tokenización, lematización, etc.)
2.	Vectorización con TF-IDF
3.	Integración con variables estructuradas
4.	Entrenamiento de modelos (Regresión Logística, Random Forest, Gradient Boosting)
5.	Evaluación de modelos
6.	Interpretación con SHAP
7.	Análisis de sentimientos y visualizaciones
IV.	RESULTADOS ESPERADOS
Al completar la ejecución de los scripts, se generarán:
a)	Archivos intermedios (Datos_Completos_finales.csv, Archivo_Filtrado_EN.csv)
b)	Gráficos y visualizaciones (.png): nubes de palabras, matrices de confusión, curvas ROC, importancia de variables
c)	Métricas de rendimiento de modelos y análisis de sentimiento
V.	RECOMENDACIONES
a.	Si el equipo es lento o tiene poca memoria, se puede reducir el tamaño del dataset con .sample(n=...) en las secciones donde se cargan los datos.
b.	Mantener todos los archivos en una misma carpeta para evitar errores de ruta.
