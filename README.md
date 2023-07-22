# MasterDL
Topic Modeling con datos de ArXiv
1. Estado del arte
   
   A lo largo de la historia se ha almacenado el conocimiento en escritos, escritos que utilizaban mucho papel y que además ocupaban mucho espacio físico. Además, cuánto más se investigaba, más escritos había y más espacio se requería. Todo esto cambió con la llegada de los ordenadores y su capacidad para almacenar grandes cantidades de escritos en un espacio virtual, un espacio donde podía caber toda la información que se tenía hasta la fecha.
   
   Esto supone una ventaja asombrosa, con respecto a los tiempos antiguos, ya que se dejan atrás los libros y escritos y el conocimiento puede tener un lugar seguro y accesible donde ser almacenado. Además, con la llegada de Internet y su capacidad de almacenar todos estos documentos en la nube, la información se volvió aún más accesible, ya que podía ser compartida por usuarios de todo el mundo.
   
   Sin embargo, el internet trajo a su vez la sobrecarga de información. Hay millones de documentos que contienen grandes cantidades de información y es muy difícil para el ser humano poder clasificar y diferir qué información es buena, o cuál le es útil en ese momento. Aquí es cuando entra en acción el Topic Modelling.
   
   La herramienta de Topic modeling aporta al usuario el poder de procesar grandes cantidades de texto, descubriendo la estructura interna que tienen y revelando su temática, pudiendo así clasificar cada texto según su temática.
   Esto supone un gran avance para el ser humano, ya que ahora es capaz de manejar más fácilmente toda la información que tiene en sus manos y puede sacar provecho de ella.

   Existen múltiples técnicas para realizar Topic modeling, siendo una de ellas la llamada BERTopic. Esta se trata de una técnica que aborda el problema como una tarea de agrupación (clustering). Es decir, desarrolla un algorítmo de clustering con una variación de TF-IDF basada en clases. Se trata de generar incrustaciones (embeddings) de documentos con modelos linguísticos basados en transformadores preentrenados.
   
2. El conjunto de datos

	El conjunto de datos a utilizar será el Arxiv Dataset. Este se trata de un conjunto de artículos educativos, que se han ido recopilando a lo largo de 30 años y que incluyen múltiples tópicos, como puede ser matemáticas, estadística, ingeniería biología o economía. En total tiene una cantidad de unos 1.7 millones de artículos, lo cual se trata de una base datos muy extensa, lo que requiere de un buen modelo capaz de clasificarlo en tópicos para ser más accesibles para el usuario.

	En este caso el conjunto de datos se ha tenido que reducir en subconjuntos para que el ordenador sea capaz de procesarlos.

4. Instrucciones de uso

	El usuario deberá cargar el conjunto de datos de los que quiera extraer los tópicos. En este paso es muy importante que el usuario se familiarice con los datos que posee, para que después sea más fácil la comprensión de los resultados.

   El siguiente paso a realizar es el preprocesamiento de los datos cargados, puesto que estos han sido volcados al código sin ningún tipo preprocesamiento, lo que puede dificultar mucho el procesamiento por el modelo. Este preprocesamiento trata de limpiar y preparar el texto, lo que puede incluir eliminar palabras vacías, realizar lematización o stemming, eliminar puntuaciones y caracteres especiales, etc.

   	Se han utilizado varias técnicas de preprocesamiento:
	1. Tokenización: Se divide cada documento en palabras o tokens 			individuales.
    
	2. Eliminación de palabras vacías (stop words): Se eliminan las 		palabras comunes que no aportan un significado importante al 			análisis del texto, como artículos, conjunciones, etc.
    
 	3.  Normalización de texto: Se convierten todas las palabras a 			minúsculas y se eliminan caracteres especiales.
     
  	4. Lematización: Se reducen las palabras a su lema. 

	Ya que el ordenador no es muy potente se ha optado por el preprocesamiento más complejo, es decir, se han usado todas las técnicas mencionadas anteriormente para que los datos puedan ser modelados con más facilidad.

Ahora que el texto está listo, se pasa a la construcción del modelo, analizar e identificar la mejor forma de modelar los datos.
   
   
6. Resultados

Los resultados se dividen en 1032 líneas, cada una de ellas contiene un tópico. En cada línea podemos observar:

	1. Nombre del tópico: se trata de la palabra clave o frase que resume el contenido de los artículos que contiene. 
 
 	2. Aporta una lista de palabras clave que aparecen con frecuencia en los documentos de cada tópico.
  
  	3. Ejemplos de texto de texto que representan el contenido del tópico.
   
   	4. El tamaño del tópico indica qué tópicos son más frecuentes.
    
Observando los resultados, se trata de un total de 1032 tópicos y hay 143253 documentos. El tópico -1 se trata de los "outliers" y deberían ser ignorados. En este caso se han obtenido 78567 documentos que serían parte de los outliers, es decir,, casi la mitad de los documentos no han sido bien clasificados en un tópico. Esto evidencia que la calidad del modelo no es muy alta. Es posible que con un preprocesamiento distinto los resultados hubieran sido diferentes, pero como se ha mencionado anteriormente, no se disponía de un ordenador lo suficientemente potente como para hacer varias compilaciones de modelos diferentes.

En la siguiente imagen se observa un "pie chart" que muestra los tópicos encontrados más frecuentes con su porcentaje dentro del total. Se puede ver que la mayoría de los documentos incluídos en la base de datos tratan del grafeno.

![image](https://github.com/100363504/MasterDL/assets/73606444/0556c7a8-9a2f-4904-9ebf-1b7998843779)

En esta otra imagen se puede observar la distribución de las palabras dentro de los propios tópicos.
![image](https://github.com/100363504/MasterDL/assets/73606444/e899e1d6-578d-4f86-94a7-fd674c3c252f)

Aún más, en la siguiente imagen se puede observar la distribución de los tópicos y su similitud con otros, lo que es un indicativo de la unicidad de cada tópico.
![image](https://github.com/100363504/MasterDL/assets/73606444/ae798f84-34e8-4b57-8e0d-df0ae54dee9e)



7. Referencias

[1] M. Grootendorst, «BERTopic: Neural topic modeling with a class-based TF-IDF procedure,» arXiv preprint arXiv:2203.05794, 2022.
[2] MAARTEN. 2021. "Topic Modeling arXiv Abstract with BERTopic." Kaggle. Disponible en: [URL (https://www.kaggle.com/code/maartengr/topic-modeling-arxiv-abstract-with-bertopic)]
[3] N. Reimers e I. Gurevych, Sentence-BERT: Sentence Embeddings using Siamese BERT-Networks, 2019. arXiv: 1908.10084 [cs.CL].

   
