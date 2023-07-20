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

3. Instrucciones de uso

	El usuario deberá cargar el conjunto de datos de los que quiera extraer los tópicos. En este paso es muy importante que el usuario se familiarice con los datos que posee, para que después sea más fácil la comprensión de los resultados.

   El siguiente paso a realizar es el preprocesamiento de los datos cargados, puesto que estos han sido volcados al código sin ningún tipo preprocesamiento, lo que puede dificultar mucho el procesamiento por el modelo. Este preprocesamiento trata de limpiar y preparar el texto, lo que puede incluir eliminar palabras vacías, realizar lematización o stemming, eliminar puntuaciones y caracteres especiales, etc.

	Ahora que el texto está listo, se pasa a la construcción del modelo, analizar e identificar la mejor forma de modelar los datos.
   
   
   
