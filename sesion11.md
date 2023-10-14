<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 11 


<!-- Su documentación aquí -->




```python
## Actividad: Filtros en pandas (loc-iloc)

import pandas as pd
import numpy as np

# Crear datos de ejemplo
marcas = ['Toyota', 'Honda', 'Ford', 'Chevrolet', 'Nissan', 'BMW', 'Mercedes-Benz', 'Audi', 'Volkswagen', 'Hyundai']
modelos = ['Camry', 'Civic', 'F-150', 'Silverado', 'Altima', 'X5', 'C-Class', 'A4', 'Jetta', 'Elantra']
anios = [2018, 2020, 2019, 2017, 2016, 2021, 2018, 2020, 2019, 2017]
precios = np.random.randint(15000, 50000, 10)

# Crear DataFrame con los datos
df_autos = pd.DataFrame({'marca': marcas, 'modelo': modelos, 'anio': anios, 'precio': precios})

# Mostrar el DataFrame
print(df_autos)
```

## 1. Ejercicios loc
Utilizando el DataFrame de autos con 20 filas y 4 columnas, realiza las siguientes consultas utilizando el método loc de Pandas:

- Seleccionar todas las filas de la columna "marca".
- Seleccionar las filas de los autos cuyo precio es mayor a $40,000.
- Seleccionar las filas de los autos que son de la marca "BMW".
- Seleccionar las filas de los autos que son de la marca "Toyota" y tienen un precio menor a $20,000.
- Seleccionar las filas de los autos que son del año 2019.
- Seleccionar las filas de los autos que son del año 2016 o anteriores.
- Seleccionar las filas de los autos que son de la marca "Honda" y el modelo es "Civic".
- Seleccionar las filas de los autos que tienen un precio entre $25,000 y $30,000.
- Seleccionar las filas de los autos que tienen un precio mayor a $30,000 y el modelo es "C-Class".
- Seleccionar las filas de los autos que son de la marca "Volkswagen" y el modelo no es "Jetta".



```python
import pandas as pd
import numpy as np

# Crear datos de ejemplo
marcas = ['Toyota', 'Honda', 'Ford', 'Chevrolet', 'Nissan', 'BMW', 'Mercedes-Benz', 'Audi', 'Volkswagen', 'Hyundai']
modelos = ['Camry', 'Civic', 'F-150', 'Silverado', 'Altima', 'X5', 'C-Class', 'A4', 'Jetta', 'Elantra']
anios = [2018, 2020, 2019, 2017, 2016, 2021, 2018, 2020, 2019, 2017]
precios = np.random.randint(15000, 50000, 10)

# Crear DataFrame con los datos
df = pd.DataFrame({'marca': marcas, 'modelo': modelos, 'anio': anios, 'precio': precios})
marca = df.loc[:, 'marca']
# Mostrar el DataFrame
print(marca)
# -----------------------------------------------------------------------------------------------------------------------------------------------
preciosfiltrados =df.loc[df['precio'] > 40000, :]
print(preciosfiltrados)
# -----------------------------------------------------------------------------------------------------------------------------------------------
bmw = df.loc[df["marca"] == "BMW" , :]
print(bmw)
# -----------------------------------------------------------------------------------------------------------------------------------------------

toyota20 = df.loc[ (df['marca'] == "Toyota")  & (df["precio"] < 20000), :]
print(toyota20)
# -----------------------------------------------------------------------------------------------------------------------------------------------
anio29 = df.loc[df["anio"] == 2019, :]
print (anio29)
# -----------------------------------------------------------------------------------------------------------------------------------------------
anioanterior = df.loc[df["anio"] <= 2016, :]
print ( anioanterior)

# -----------------------------------------------------------------------------------------------------------------------------------------------
hondacivic = df.loc[ (df['marca'] == "Honda")  & (df["modelo"] == "Civic"), :]

print(hondacivic)

# -----------------------------------------------------------------------------------------------------------------------------------------------
preciosrango =df.loc[ (df['precio'] > 25000) & (df['precio'] <= 30000), :]
print(preciosrango)
# -----------------------------------------------------------------------------------------------------------------------------------------------
preciomodelo = df.loc[ (df['precio'] > 30000) & (df['modelo'] == "C-Class"), :]

print(preciomodelo)
# -----------------------------------------------------------------------------------------------------------------------------------------------
md = df.loc[ (df['marca'] == "Volkswagen") & (df['modelo'] != "Jetta"), :]
print(md)
```







2. Ejercicios iloc
Utilizando el DataFrame de autos con 20 filas y 4 columnas, realiza las siguientes consultas utilizando el método iloc de Pandas:

Seleccionar las filas de los autos de los primeros 5 fabricantes en el DataFrame.
Seleccionar las filas de los autos de los últimos 5 fabricantes en el DataFrame.
Seleccionar la primera columna de todas las filas del DataFrame.
Seleccionar las celdas de la primera fila y primera columna del DataFrame.
Seleccionar las filas pares del DataFrame.
Seleccionar las filas impares del DataFrame que tienen un precio mayor a $25,000.
Seleccionar las filas de los autos que son de la marca "Ford" y el modelo es "F-150".
Seleccionar las filas de los autos que son del año 2018 y tienen un precio mayor a $20,000.
Seleccionar las filas de los autos que tienen un precio mayor a $30,000 y la marca es "Toyota".
Seleccionar las filas de los autos que son de la marca "Honda" y el modelo no es "Civic".

```python
import pandas as pd
import numpy as np

# Crear datos de ejemplo
marcas = ['Toyota', 'Honda', 'Ford', 'Chevrolet', 'Nissan', 'BMW', 'Mercedes-Benz', 'Audi', 'Volkswagen', 'Hyundai']
modelos = ['Camry', 'Civic', 'F-150', 'Silverado', 'Altima', 'X5', 'C-Class', 'A4', 'Jetta', 'Elantra']
anios = [2018, 2020, 2019, 2017, 2016, 2021, 2018, 2020, 2019, 2017]
precios = np.random.randint(15000, 50000, 10)

# Crear DataFrame con los datos
df = pd.DataFrame({'marca': marcas, 'modelo': modelos, 'anio': anios, 'precio': precios})
primeros_cinco_fabricantes = df.iloc[:5, :]
print(primeros_cinco_fabricantes)
# -----------------------------------------------------------------------------------------------------------------------------------------------
ultimos_cinco_fabricantes = df.iloc[-5:, :]
print(ultimos_cinco_fabricantes)

# -----------------------------------------------------------------------------------------------------------------------------------------------
primera_columna = df.iloc[:, 0]
print(primera_columna)
# -----------------------------------------------------------------------------------------------------------------------------------------------
primera_celda = df.iloc[0, 0]
print(primera_celda)
# -----------------------------------------------------------------------------------------------------------------------------------------------
filas_pares = df.iloc[::2]
print(filas_pares)
# -----------------------------------------------------------------------------------------------------------------------------------------------
ford_f150 = df.iloc[[i for i in range(len(df)) if df.iloc[i, 0] == 'Ford' and df.iloc[i, 1] == 'F-150'], :]
print(ford_f150)
# -----------------------------------------------------------------------------------------------------------------------------------------------
anio_2018_precio = df.iloc[[i for i in range(len(df)) if df.iloc[i, 2] == 2018 and df.iloc[i, 3] > 20000], :]
print(anio_2018_precio)

# -----------------------------------------------------------------------------------------------------------------------------------------------
preciotoyota = df.iloc[[i for i in range(len(df)) if df.iloc[i, 3] > 30000 and df.iloc[i, 0] == 'Toyota'], :]
print(preciotoyota)
# -----------------------------------------------------------------------------------------------------------------------------------------------
honda_no_civic = df.iloc[[i for i in range(len(df)) if df.iloc[i, 0] == 'Honda' and df.iloc[i, 1] != 'Civic'], :]
print(honda_no_civic)
# -----------------------------------------------------------------------------------------------------------------------------------------------

# -----------------------------------------------------------------------------------------------------------------------------------------------
```