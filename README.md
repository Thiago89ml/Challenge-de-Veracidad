# Challenge-de-Veracidad

Primero de todo se leyo el Csv respectivo con el read y se uso el shape para ver el temañao de datos que se manejan

ELIMINACIÓN / MODIFICACIÓN DE COLUMNAS

Primero se uso el null().sum() para ver la cantidad de nulos.

La columna Cargo del Orador, por ejemplo, se eliminó porque contenía una gran cantidad de valores nulos → (919).

La columna Estado también, al igual que la anteriormente mencionada, se eliminó porque contenía una gran cantidad de datos nulos → (704), los cuales no aportaban valor a las variables que se utilizarían en el modelo.

En el caso de la columna Contexto, ocurrió un proceso de eliminación, pero con un motivo diferente: se tomó esa decisión debido a que el mapeo de los objetos a números resultaba demasiado tedioso.

La columna Afiliación Política contenía una cantidad considerable de objetos que podían mapearse para generar datos útiles al momento de entrenar el modelo.

¿Por qué solo mapear la columna de Afiliación Política?

Dicha columna poseía objetos con una cantidad de caracteres mucho menor que otras, como por ejemplo Contexto.
Además, presentaba una mayor repetición de los mismos valores, lo que facilitaba el proceso de mapeo, ya que existía una menor diversidad de categorías (objetos) en comparación con otras columnas del mismo tipo.

Se utilizó un boxplot con el propósito de eliminar los outliers de las variables Cantidad Verdadera y Cantidad Falsa, con el objetivo de eliminar valores que se encontraban fuera del rango normal.

DATOS ELEGIDOS

Los datos que más me convencieron para el uso futuro del modelo fueron Cantidad Verdadera y Cantidad Falsa.
El hecho de ser datos numéricos permitía una mayor eficacia y rapidez al usar el modelo.
Estos datos se unieron al grupo de variables que se utilizarían como independientes.

Una vez se realizó el mapeo de la columna Afiliación Política, quedó lista para poder incluirse en el modelo, permitiendo contar con más datos y, por ende, obtener un resultado más eficiente.

También se tomó la columna Etiquetas como variable dependiente, tal como lo indicaba la consigna.

Como conclusión de este apartado, se seleccionaron como variables independientes (características):
['Afiliación Política', 'Cantidad Verdadera', 'Cantidad Falsa']
y como variable dependiente, la columna Etiquetas.

DIVISIÓN DE DATOS

Antes de aplicar el modelo, se optó por separar los datos de entrenamiento y prueba mediante la función train_test_split.

MODELO A UTILIZAR

Se eligió el modelo KNN (K-Nearest Neighbors) debido a que se buscaba una binaridad en el veredicto, por lo que era el modelo más indicado para la situación.

Luego de importar Neighbors, se importó también el StandardScaler, entre otros elementos necesarios.

TESTEO DE USO

En este apartado se repitieron los procesos anteriores, pero aplicados al archivo CSV destinado para la prueba.

ENVÍO

Por último, se creó un archivo CSV que almacenaba los resultados generados desde el .ipynb que contenía el trabajo con los distintos archivos CSV, con el objetivo de poder subirlos al ranking.

El archivo de salida se generó mediante el comando output.

<img width="1133" height="293" alt="Para que lo ves Guille" src="https://github.com/user-attachments/assets/47328123-1705-4154-a161-628e0a9f19c7" />

