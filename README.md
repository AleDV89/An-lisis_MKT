# Análisis de Marketing
![Imagen marketing](https://github.com/AleDV89/An-lisis_MKT/blob/main/Marketing.png
)
### Resumen:
Se analiza la situación de una empresa con el objetivo de comprender el probelma con las campañas de marketing y proponer soluciones basados en los datos con Python 3.x.

### Requisitos: 

`pandas` , `numpy` , `seaborn`, `plt`

### Obtención de Datos:
Los datos fueron proporcionados en formato .CSV

### Procesamiento de los Datos
- Los datos se cargan en un DataFrame de Pandas y se procede a la lectura del mismo.
- Se inspeccionan los datos y se verifican los nulos con `seaborn`
  
![Verificar Nulos ](https://github.com/AleDV89/An-lisis_MKT/blob/main/seaborn.png
)

También se verifica que la columna Income tiene 1% de datos nulos.

```python
df.isnull().sum()/len(df)*100





