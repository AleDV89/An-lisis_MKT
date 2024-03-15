# Análisis de Marketing 💻
![Imagen marketing](https://github.com/AleDV89/An-lisis_MKT/blob/main/Marketing.png
)
### Resumen:
Se analiza la situación de una empresa con el objetivo de comprender el problema con las campañas de marketing y proponer soluciones basados en los datos con Python 3.x.

### Requisitos: 

`pandas` , `numpy` , `seaborn`, `plt`

### 🔍 Obtención de Datos:
En esta sección, se detalla cómo obtener los datos necesarios para el análisis de la campaña de marketing. 
Estos datos fueron extraidos de un archivo CSV pero puedes poner tus propios datos como:  bases de datos internas, registros de clientes, encuestas, plataformas de análisis web, entre otros.

### Fuentes de Datos:

- **Base de datos interna**

### 📊 Procesamiento de los Datos
* Los datos se cargan en un DataFrame de Pandas y se procede a la lectura del mismo.
* Se inspeccionan los datos y se verifican los nulos con `seaborn`
  
![Verificar Nulos ](https://github.com/AleDV89/An-lisis_MKT/blob/main/seaborn.png
)

También se verifica que la columna Income tiene 1% de datos nulos.


```python
df.isnull().sum()/len(df)*100


```
* Se realiza una corrección con el espacio de la columna Income
```python

```
* Se quita el simbolo $ a los datos de la columna Income

```python
df['Income'] = df['Income'].str.replace('$', '')

```
### Análisis Exploratorio 📝

* Se realizan el  análisis visual para ver la distribución de los ingresos de las familias en la columna Income.
Función: Utiliza `sns.histplot` con seaborn para crear este tipo de gráfico.
 Ejemplo de uso:
```python
plt.figure(figsize=(12, 4))
sns.histplot(df['Income'])
plt.title('Distribucion de la columna "Income"', size=25)
plt.ylabel('Conteo')
plt.show()

 ``` 
![Distribucion ](https://github.com/AleDV89/An-lisis_MKT/blob/main/seaborn.png
)

* Se rellenan los nulos
```python
df_income = df['Income'].median()

```
#### Grafico Pie para ver con claridad las campañas más aceptadas por los clientes.
Función: Utiliza `plt.pie`
Ejemplo de uso:
```python
plt.figure(figsize=(8, 6))
plt.pie(campaña_totales, labels=nombres_campañas, autopct='%1.1f%%', startangle=140)
plt.title('Distribución de las campañas más aceptadas por los clientes')
plt.axis('equal') 
plt.show()
```
![pie](https://github.com/AleDV89/An-lisis_MKT/blob/main/.pie.png)

#### Contribuciones 💡 :
* Puedes contribuir con este análisis y agregar tus perpectivas!

