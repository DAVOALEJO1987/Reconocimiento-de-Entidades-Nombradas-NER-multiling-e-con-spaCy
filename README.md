# Reconocimiento-de-Entidades-Nombradas-NER-multiling-e-con-spaCy
Implementar un flujo de procesamiento de lenguaje natural que identifique y clasifique entidades nombradas en textos en inglés y español, utilizando la librería spaCy, y generar un resumen estadístico del número de entidades detectadas por tipo.
El programa:
1.	Carga modelos lingüísticos especializados en inglés y español.
2.	Procesa textos definidos por el usuario, identificando automáticamente entidades como personas, organizaciones, ubicaciones, fechas, etc.
3.	Muestra resultados detallados por cada texto, listando la entidad y su tipo.
4.	Acumula datos globales para generar un conteo total de entidades por categoría.
5.	Facilita la interpretación de resultados a través de un resumen estadístico.

1. Carga de modelos spaCy
•	Se utilizan dos modelos preentrenados:
o	en_core_web_sm para inglés.
o	es_core_news_sm para español.

•	El programa valida si los modelos están instalados; si no, los descarga automáticamente.

2. Definición de textos de entrada
•	Se incluyen dos textos en inglés y dos en español.
•	Cada texto debe contener al menos tres entidades nombradas para garantizar una prueba adecuada.
3. Procesamiento y detección de entidades
•	Función procesar_y_mostrar:
o	Aplica el modelo correspondiente a cada texto.
o	Extrae entidades y sus etiquetas (PERSON, ORG, GPE, DATE, etc.).
o	Muestra el resultado de manera legible para el usuario.

4. Acumulación de resultados
•	Uso de collections.Counter para almacenar y contar el número de entidades por tipo a lo largo de todos los textos procesados.
5. Resumen global
•	El programa finaliza mostrando un resumen con el conteo total de entidades por tipo.
•	Este resumen permite comparar qué tipo de entidades fueron más comunes en el conjunto de textos.
