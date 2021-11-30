# Cuarta actividad: tu historia de periodismo de datos pendiente

## Justificación de la visualización de datos

La elección de datos analizados corresponde con el documento facilitado por el profesor (feliz.csv). La base de datos utilizada en las sesiones presenta información relativa al uso de hashtags y tendencias relacionados con la palabra feliz durante el 2020. Analizar estos datos no ha sido sencillo pero he preferido utilizar una gráfica relacionada con dichos datos para aprender a manejar la utilización de ambas herramientas: OpenRefine y Datawrapper. 

Me limité a un espacio de tiempo acotado que fuera interesante y curioso, tras distintos intentos de manipulación de datos utilicé los hashtags y tendencias para felicitar la Pascua en el pasado año. Es una manera original de conocer las diferentes formas de felicitar esta festividad que se hicieron el pasado 12 de abril, domingo del 2020.
En esta primera tarea de selección y filtración se utilizado la herramientas de OpenRefine. 
Los 4 resultados para el análisis fueron: las tendencias “Feliz Pascua”, “Feliz Pascua de Resurreccion”, “Felices Pascuas” y el hashtag “#FelicesPascuas” dando un total de 246.270 resultados. Hay una gran diferencia entre la utilización de estos mensajes en Twitter ya que la tendencia menos utilizada con tan solo 5.500 resultado fue “Feliz Pascua”. El hashtag fue el valor más pequeño contando con 5.280 resultados. Las dos tendencias restantes son considerablemente superiores, “Feliz Pascua de Resurreccion” con la cifra de 99.450 y “Felices Pascuas” es la más utilizada con 136.040 resultados de búsqueda. 

Los gráficos realizados en Datawrapper pretenden visibilizar estos datos de la manera atractiva y simplificada, para ello utilice dos gráficos distintos sobre la misma base de datos.

El gráfico de barras muestra un mayor número de resultados, eran tendencias y hashtags recogidos en el archivo pero con cantidad cero, a pesar de ello me ha parecido interesante ilustrarlo para conocer las diferentes opciones disponibles. En este formato se conoce por tanto un mayor número de posibilidades, y se observa  con mayor facilidad los valores reflejados en la longitud de la línea. El color escogido ha sido un violeta haciendo referencia a uno de los colores más importantes de la festividad. 
El gráfico circular es más dinámico y se observa la comparación entre las cifras que poseen valores. Reflejado una clara competición entre las dos tendencias predominantes. Los colores utilizados son muy distintos entre sí, lo que ayuda a comprender la información representada.
He pretendido reflejar como una misma base de datos puede representarse en distintos gráficos y percibir información diferente.


## Procedimiento

&rarr; Los hashtags y las tendencias más usados para felicitar la Pascua en 2020.

* OpenRefine
Es necesario explicar que para realizar los gráficos el proceso utilizado en OpenRefine fue el mismo por lo que este paso es similar para las dos imágenes. La diferencia radica en la herramienta Datawrapper que explicaré más adelante, pero el procedimiento para selección y filtrar los datos inicial es general.

1. El paso previo fue realizar la acción “git clone” en la terminal para descargar una copia del repositorio uc3m-periodismo-datos en Github, en la cuenta de Pontedatos
2. En la terminal, con el comando “ls”, se listaron todos los archivos de la carpeta src/data para confirmar la descarga del archivo feliz.csv, que es el que nos interesa del repositorio clonado.
3. Desde la herramienta de OpenRefine se cargó el archivo para comenzar a limpiarlo
4. Se configuró el archivo con una separación por comas (csv), se eliminó la opción de “use character…, la de “parse next” y se creó un proyecto formado por 5981 filas.
5. Cambié el formato a fecha en la columna 2 y a número en la 6, además de eliminar los datos de 1970 con una faceta de línea de tiempo en la columna seis.
6. Con la misma, eliminé todos los datos que no correspondían con el intervalo entre los meses de marzo y abril de 2020, ya que me interesaban las fechas de Pascua y no siempre se celebran en el mismo mes, varía según el año. 
7. En relación con el paso anterior el resultado fue una gran filtración de datos,  pasando de 5981 filas iniciales a 837, esto correspondía con los valores utilizados en Twitter entre las fechas seleccionadas.
8. Con una faceta de texto en la columna 3 eliminé todas las filas que no hacían referencia a las felicitaciones analizadas, por lo que pasé de tener 837 filas a tener tan solo 32, cifra que podría utilizarse con facilidad en Datawrapper.
9. A todas aquellas celdas de la columna 6 que no contenían ningún número les puse un valor de 1 para poner un valor concreto y que el Datawrapper pudiera identificarlo, a pesar de que no fuera significativo en comparación con el resto.
10. Eliminé varias columnas que no me interesaban para mi conjunto de datos, la 1 (información relativa a la fecha que no comprendía), 4 (link de Twitter que no es necesario para este gráfico), y 5 (información que no comprendía). Ya que al ser la primera vez que utilicé la herramienta preferí tener un conjunto de datos lo más sencillo posible.
11. Eso quiere decir que me quedé con las columnas 2 (fecha), 3 (hashtag y tendencias) y 6 (número).
12. Cambié el nombre de la columna 6 a “cantidad” y cambié el nombre de la 3 a “hashtags y tendencias”.
13. Después, llegué a la conclusión de que haber puesto un 1 en las celdas en blanco de la columna “cantidad” no tenía sentido, ya que era mucho más sincero poner un 0 y se vería prácticamente igual en datawrapper
14. De este modo, como distintas celdas de hashtags y tendencias aparecían en numerosas ocasiones con cifras diferentes, sumé los valores de la columna cantidad agrupándolos según el día concreto, especificado en la columna de las fechas
15. Exporté el archivo en csv. 



* Datawrapper

16. Desde la primera pestaña de la herramienta Datawrapper “upload data” subí el archivo generado en OpenRefine con mi base de datos. La información representada eran dos columnas relativas a los hashtags y tendencias y la cantidad de los tweets generados con dichos nombres.
17. En la pestaña “check & describe” acepté la opción de que “hashtags y tendencias” fuera una etiqueta, para reflejar que los nombres que aparecerían se referían a esta categoría.
18. La pestaña de visualización fue la principal para generar el diseño y tipo de gráfico, es donde cambiaron los pasos según el tipo de gráfico utilizado.

![Gráfico circular tendencias y hashtags Pascua](/practica-4-imagenes/graficocircular.png)
Gráfico circular sobre las tendencias y hashtags más utilizados para felicitar la Pascua en 2020



18.1. Gráfico circular

18.1.1 Elegí el gráfico circular ya que la información se adecuaba muy bien y aparecían los “hashtags y tendencias” con cifras de manera muy comprensible.

18.1.2 Posteriormente modifiqué los colores a mi gusto, el formato de número (1.000 con una K para facilitar la visualización) y el radio del gráfico. Opté por la opción de visualización de datos tanto en las categorías como el total en el centro de la composición.

18.1.3 Rellené la información del gráfico: título, leyenda, fuente…

18.1.4. Exporté el archivo en png con fondo blanco.

![Gráfico de barras tendencias y hashtags Pascua](/practica-4-imagenes/graficobarras.png)
Gráfico de barras sobre las tendencias y hashtags más utilizados para felicitar la Pascua en 2020



18.2 Gráfico de barras (bullet bars)

18.2.1 Elegí este gráfico para utilizar otro formato con la misma base de datos. En este se observan las categorías sin datos aparentes, por lo que era interesante saber que eran una opción. Dentro de las opciones de barras el “bullet bars” era el que mejor se entendía y mejor quedaba.

18.2.2 Modifiqué el color, morado referido al color de Pascua y borre la K para conocer otras posibilidades.

18.1.3 Rellené la información del gráfico: título, leyenda, fuente…

18.1.4. Exporté el archivo en png con fondo blanco.
