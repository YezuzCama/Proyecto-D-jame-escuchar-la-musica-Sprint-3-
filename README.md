# Proyecto-D-jame-escuchar-la-musica-Sprint-3-
Análisis comparativo de los hábitos de escucha entre los usuarios de ciudades: Springfield y Shelbyville. El objetivo principal fue validar tres hipótesis críticas sobre cómo el tiempo, la ubicación y el género musical influyen en el comportamiento del usuario, proporcionando una base sólida para futuras estrategias de recomendación algorítmica.
📝 Descripción Técnica del Proyecto
1. El Dataset y su Calidad
El análisis se basó en un conjunto de datos con las siguientes dimensiones clave:

user_id: Identificador único del oyente.

track: Nombre de la canción.

artist: Nombre del artista.

genre: Género musical (punto crítico de limpieza).

city: Ubicación (Springfield o Shelbyville).

time / day: Momento exacto y día de la semana de la actividad.

2. Metodología de Procesamiento de Datos
El flujo de trabajo siguió un estándar riguroso de Data Cleaning y EDA (Exploratory Data Analysis):

Tratamiento de Valores Ausentes: Se identificaron valores nulos en las columnas de canción, artista y género, los cuales fueron reemplazados por la etiqueta 'unknown' para evitar sesgos en el conteo.

Eliminación de Duplicados: Se procesaron duplicados obvios y, de manera más estratégica, se corrigieron duplicados implícitos en la columna de géneros (por ejemplo, normalizando variantes de 'hip-hop' como 'hip', 'hop' y 'hip-hop' a una sola categoría).

Segmentación Dinámica: Se crearon funciones personalizadas para filtrar datos por ciudad, día y rangos horarios específicos.

🔍 Prueba de Hipótesis y Hallazgos
El proyecto se centró en la validación de tres teorías principales:

Hipótesis 1: Actividad por día y ciudad
Teoría: La actividad de los usuarios varía según el día de la semana y la ciudad.

Resultado: Confirmado. Springfield muestra picos de actividad los lunes y viernes, mientras que los miércoles la actividad decae notablemente. Shelbyville, por el contrario, alcanza su mayor nivel de escucha los miércoles.

Hipótesis 2: Preferencias en horas pico
Teoría: Los lunes por la mañana y los viernes por la tarde, los géneros preferidos varían significativamente entre ambas ciudades.

Resultado: Rechazado parcialmente. Ambas ciudades mantienen perfiles muy similares en estos horarios, con el Pop liderando el ranking. Springfield muestra una presencia más fuerte de Rock y Jazz, mientras que Shelbyville se inclina ligeramente más por el World Music.

Hipótesis 3: Géneros dominantes por ciudad
Teoría: Springfield prefiere el Pop, mientras que Shelbyville tiene una inclinación mayor por el Rap.

Resultado: Rechazado. El análisis demostró que el Pop es el género #1 en ambas ciudades. Sorprendentemente, el Rap ocupa un lugar similar en los rankings de popularidad tanto en Springfield como en Shelbyville.

✅ Conclusiones y Valor de Negocio
El análisis arroja luz sobre la homogeneidad de los gustos musicales en mercados aparentemente distintos:

Uniformidad Global: A pesar de las diferencias geográficas, el consumo de géneros principales (Pop, Dance, Rock) es consistente.

Estrategia de Engagement: Los esfuerzos de marketing en Springfield deberían concentrarse en lunes y viernes, mientras que en Shelbyville la oportunidad de oro está en los miércoles.

Habilitación de Modelos: La limpieza realizada en la columna de géneros es fundamental para entrenar cualquier sistema de recomendación (Machine Learning) posterior, evitando que el modelo se confunda con categorías redundantes.
