# S3----MUSIC-
Estudio de actividad en plataforma de música por días de la semana en dos ciudades distintas.
Data wrangling:  Exploración de datos, preprocesamiento de datos y comprobación de hipótesis mediante adrupamiento de datos y filtrado de dataframes.

## Descripción

"La actividad de los usuarios y las usuarias difiere según el día de la semana y dependiendo de la ciudad." 
es la hipótesis a probar en este proyecto.

Siempre que investigamos, necesitamos formular hipótesis que después podamos probar. 
En este proyecto, se utilizan datos reales de transmisión de música online para comparar las preferencias musicales de las ciudades de Springfield y Shelbyville.

## Hereramientas utilizadas 

![Python](https://img.shields.io/badge/:Python-024A86?style=for-the-badge&logo=python&logoColor=white&labelColor=101010)</br>
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)

![Colab](https://img.shields.io/badge/Colab-F9AB00?style=for-the-badge&logo=googlecolab&color=525252)
![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)


## Conclusiones 
El comportamiento en cada una de las ciudades son semejantes el lunes y el viernes. Sin embargo, los miércoles es el día favorito para escuchar música en Shelbyville, mientras que ese mismo día el de menos escucha en Springfield. 
Con lo cual se confirma la hipótesis: La actividad de los usuarios y las usuarias difiere según el día de la semana y dependiendo de la ciudad.

## Profundización técnica
* Descripción de los datos
* * Abrir datos: pd.read_csv('')
  * Examinar los datos:
  * * df.head() - Primeras filas ¿con que información/campos contamos?
    * df.info() - Tipos de datos
    * df.describe() - Estadísticas descriptivas, en este caso de columnas 'objecto' :  count- número de valores no nulos, unique - número de valores únicos, top - el valor más común y freq - la frecuencia del valor más común.
    * df.duplicated() / df.duplicated().sum() - Valores duplicados / cantidad de valores duplicados
    * df.isnull() /df.isnull().sum()  - Valores auscentes 
* Preprocesamiento de los datos:
* * Formato de encabezados - se recomienda usar snake_case.
  * Manejo de valores auscentes - Investigar razones por los que faltan y cómo afectaran los coómputos.  df[col].fillna(value, inplace=True)
  * Manejo duplicados explícitos- df.drop_duplicates(inplace=True) - Eliminar solo una de las filas que son completamente iguales.
  * Manejo duplicados implícitos - df[col].unique() , df[col].replace(old_value, new_value), df[col].nunique()
* Prueba de hipótesis
* * Agrupamiento por grupos- df.groupby(by='....')['col'].count()
  * Filtrado de dataframes - df[df['col']== values]
