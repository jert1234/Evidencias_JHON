<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 9 


<!-- Su documentación aquí -->

## Actividad: Ejercicio de limpieza de datos con Pandas
- Crear un proyecto de Python y utilizar la librería pandas para realizar la limpieza de datos del siguiente conjunto de datos de venta de vehículos
- Descargar - Conjunto de Datos "Venta de Vehiculos"
- Documentar los problemas de datos encontrados



## Ejercicio 

```python
import pandas as pd
import streamlit as st
import os


ruta_csv = os.path.abspath('ventas_vehiculos .csv')


if not os.path.isfile(ruta_csv):
    st.error(f"No se encontró el archivo CSV en la ruta: {ruta_csv}")
else:
    
    df = pd.read_csv(ruta_csv)

  
    df = df.drop_duplicates()

   
    df = df.dropna()

    filtro_opcion = st.selectbox("Selecciona una opción de filtro:", ['Nuevo/Usado', 'Color', 'Fecha', 'Vendido', 'Precio'])

    if filtro_opcion == 'Nuevo/Usado':
      
        df = df.sort_values(by='Año', ascending=False)

    elif filtro_opcion == 'Color':
      
        df = df.sort_values(by='Color')

    elif filtro_opcion == 'Fecha':
    
        df['Fecha'] = pd.to_datetime(df['Fecha'])
        df = df.sort_values(by='Fecha', ascending=False)

    elif filtro_opcion == 'Vendido':

        df = df.sort_values(by='Vendido', ascending=False)

    elif filtro_opcion == 'Precio':
    
        df = df.sort_values(by='Precio', ascending=False)

 
    df = df[df['Marca'].apply(lambda x: isinstance(x, str))]

  
    df.to_csv('ventas_vehiculos_filtrados.csv', index=False)
    st.dataframe(df)
    st.write(f"Registros restantes: {len(df)}")
```
## Enlace hacia el repositorio donde se encuentra el ejercicio
-  

[Enlace de GitHub ](https://github.com/jert1234/Ejercicio9-10.git)