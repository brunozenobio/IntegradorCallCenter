# Integrador de Call Center

En este proceso se llevó a cabo el análisis de un conjunto de datos de un Call Center. En la carpeta "dataset" se incluye el archivo .csv junto con su respectiva documentación.

Para realizar un análisis adecuado, se plantearon las siguientes preguntas que llevaron a definir KPI clave para mejorar el rendimiento:

### Preguntas 
* ¿Cuál es el nivel de servicio para los clientes prioritarios?
* ¿Ofrecemos un mejor servicio a los clientes prioritarios en comparación con los clientes normales?
* ¿Cuál es el volumen de llamadas que atendemos?
* ¿Cuáles son los cuellos de botella? ¿En qué días y en qué bandas horarias ocurren?
* ¿Cuál es la eficiencia y productividad de nuestros agentes?
* ¿Existen clientes recurrentes en el uso del servicio?
* ¿Cuáles son los tipos de servicio más recurrentes?
* ¿Podemos estimar la dotación necesaria para cumplir con una calidad de servicio determinada? Ejemplo: si queremos que nuestro tiempo promedio de espera sea menor a 60 segundos, ¿cuántos agentes necesitamos?

## A continuación se detalla el proceso realizado.

### Proceso de Limpieza y Transformación:

- Se normalizaron los nombres de los campos.
- Se realizaron búsquedas de errores y valores duplicados.
- Se corrigieron los duplicados en el campo IdLlamada concatenándolos con LineaVRU.
- Según la documentación, los registros de salida de llamada por el método PHANTOM son llamadas que se ignoran; estos registros fueron eliminados.
- En la columna del tiempo en servicio, se detectaron valores de segundos negativos. Dado que no se contaba con suficiente información para corregirlos, los registros se conservaron, pero estos valores no se tuvieron en cuenta al realizar análisis con este campo, ya que representaban menos del 1% de los registros.
- Se encontraron outliers en todos los campos de intervalo temporal: "tiempo en servicio", "tiempo en cola" y "tiempo en VRU". Debido a la falta de información, no se aplicó un tratamiento específico.
- Se crearon las tablas "Servicio VRU Cola" y "Tipo de Servicio" a partir de la tabla del Call Center.
- Se agregó la columna "Día de la Semana" en la tabla del Call Center para determinar el día de la semana de la llamada.
- Se agregó la columna "Dio Servicio".

### Proceso de Visualización:

- **Tiempo en Cola por Prioridad: Gráfico de Barras**

- **Volumen de Llamadas: Tarjeta con Número**

- **Llamadas por Hora del Día : Gráfico de Líneas**

- **Atendidas vs Ignoradas : Gráfico Circular**

- **Top 10 Clientes Más Recurrentes : Gráfico de Barras**


- **Distribución de Llamadas por Tipo de Servicio : Gráfico de Barras**

- **Porcentaje de Servicios de Alta Prioridad  : Grafico de Barras**



 