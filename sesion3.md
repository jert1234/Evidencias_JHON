<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 3 


<!-- Su documentación aquí -->
# Actividad:
## 1. practicar con listas, tuplas, conjuntos y diccionarios en Python.
Genera un nuevo cuaderno en Google Colab y añade cuatro bloques de código, asignándoles títulos respectivos: "Listas", "Tuplas", "Conjuntos" y "Diccionarios". A continuación, comparte el cuaderno empleando la configuración de "Acceso general - Cualquier persona con el enlace - Editor". A continuación, resuelve los ejercicios que se presentan a continuación:

- **Listas** 
- Crea una lista que contenga los números del 1 al 10.
- Imprime la lista en el orden en que fue creada.
- Ordena la lista en orden ascendente.
- Ordena la lista en orden descendente.
- Encuentra el número más pequeño en la lista.
- Encuentra el número más grande en la lista.
- Cuenta el número de veces que aparece el número 5 en la lista.
- Elimina el número 5 de la lista.
- Agrega el número 11 a la lista.
- Imprime la lista nuevamente.
- **Tuplas** 
- Crea una tupla que contenga las palabras "Hola", "mundo" y "Python".
- Imprime la tupla en el orden en que fue creada.
- Ordena la tupla en orden alfabético.
- Encuentra la primera palabra en la tupla.
- Encuentra la última palabra en la tupla.
- Cuenta el número de palabras en la tupla.
- Elimina la palabra "mundo" de la tupla.
- Agrega la palabra "Hola" a la tupla.
- Imprime la tupla nuevamente.
- **Conjuntos** 
- Crea un conjunto que contenga los números del 1 al 10.
- Imprime el conjunto.
- Agrega el número 11 al conjunto.
- Elimina el número 5 del conjunto.
- Cuenta el número de elementos en el conjunto.
- Comprueba si el número 5 está en el conjunto.
- Comprueba si el número 11 está en el conjunto.
- Crea un conjunto que contenga las palabras "Hola", "mundo" y "Python".
- Imprime el conjunto.
- Comprueba si la palabra "Hola" está en el conjunto.
- Comprueba si la palabra "mundo" está en el conjunto.
- **Diccionarios** 
-Crea un diccionario que asigne los nombres de los días de la semana a sus números correspondientes.
- Imprime el diccionario.
- Obtén el número del día de la semana "Lunes".
- Obtén el día de la semana del número 2.
- Elimina el día de la semana "Lunes" del diccionario.
- Imprime el diccionario nuevamente.

## Solucion 

**Listas** 
```python
lista = [2,1,3,5,4,7,6,9,8,10]


lista_orden_ascendente = sorted(lista)
print("Ascendente:", lista_orden_ascendente)


lista_orden_descendente = sorted(lista, reverse=True)
print("Descendente:", lista_orden_descendente)

print("Original:", lista)

elnumeromenor = min(lista)
print ("el numero menor: ",elnumeromenor)

elnumeromayor = max(lista)
print ("el numero mayor: ",elnumeromayor)

print("las veces que aparece el 5 : ",lista.count(5))
lista.remove(5)
print ("lista con el numero 5 eliminado",lista)
lista.append(11)
print("lista con el numero 11 agregado", lista)
```

**Tuplas** 
```python
tupla = ("hola" , "mundo" , "Python")
print (tupla)

tupla_alfabetica = sorted(tupla)
tupla_alrevez = sorted (tupla , reverse=True)
print (tupla_alfabetica)
print(tupla_alrevez)

primera_palabra = tupla[0]
print("Primera palabra:", primera_palabra)

ultima_palabra = tupla[-1]
print("Última palabra:", ultima_palabra)
#  no se puede eliminar y agregar elementos a la tupla
numeropalabras = len(tupla)
print ("numero de palabras en la tupla :",  numeropalabras)
```
**Conjuntos** 
```python
# Conjuntos
# Crea un conjunto que contenga los números del 1 al 10.
conjunto_numeros = set(range(1, 11))

# Imprime el conjunto.
print("Conjunto de números del 1 al 10:", conjunto_numeros)

# Agrega el número 11 al conjunto.
conjunto_numeros.add(11)

# Elimina el número 5 del conjunto.
conjunto_numeros.remove(5)

# Cuenta el número de elementos en el conjunto.
num_elementos = len(conjunto_numeros)
print("Número de elementos en el conjunto:", num_elementos)

# Comprueba si el número 5 está en el conjunto.
if 5 in conjunto_numeros:
    print("El número 5 está en el conjunto.")
else:
    print("El número 5 no está en el conjunto.")

# Comprueba si el número 11 está en el conjunto.
if 11 in conjunto_numeros:
    print("El número 11 está en el conjunto.")
else:
    print("El número 11 no está en el conjunto.")

# Crea un conjunto que contenga las palabras "Hola", "mundo" y "Python".
conjunto_palabras = {"Hola", "mundo", "Python"}

# Imprime el conjunto.
print("Conjunto de palabras:", conjunto_palabras)

# Comprueba si la palabra "Hola" está en el conjunto.
if "Hola" in conjunto_palabras:
    print("La palabra 'Hola' está en el conjunto.")
else:
    print("La palabra 'Hola' no está en el conjunto.")

# Comprueba si la palabra "mundo" está en el conjunto.
if "mundo" in conjunto_palabras:
    print("La palabra 'mundo' está en el conjunto.")
else:
    print("La palabra 'mundo' no está en el conjunto.")
```
**Diccionarios** 
```python
# Diccionarios
# Crea un diccionario que asigne los nombres de los días de la semana a sus números correspondientes.
dias_semana = {
    "Lunes": 1,
    "Martes": 2,
    "Miércoles": 3,
    "Jueves": 4,
    "Viernes": 5,
    "Sábado": 6,
    "Domingo": 7
}

# Imprime el diccionario.
print("Diccionario de días de la semana:", dias_semana)

# Obtiene el número del día de la semana "Lunes".
numero_lunes = dias_semana["Lunes"]
print("Número del día de la semana 'Lunes':", numero_lunes)

# Obtiene el día de la semana del número 2.
for dia, numero in dias_semana.items():
    if numero == 2:
        print("Día de la semana del número 2:", dia)
        break

# Elimina el día de la semana "Lunes" del diccionario.
del dias_semana["Lunes"]

# Imprime el diccionario nuevamente.
print("Diccionario de días de la semana después de eliminar 'Lunes':", dias_semana)
```

## Analizar y probar el funcionamiento del siguiente ejercicio:
Este código en Python tiene como objetivo simular el proceso de creación y actualización de una lista de compras, incluyendo artículos, cantidades y la capacidad de resaltar los artículos importantes. Ahora, desglosemos cada parte del código:

- Crear lista de compras (lista_compras): En esta parte del código, se crea una lista llamada lista_compras que contiene varios elementos, que representan los artículos que el usuario planea comprar en el supermercado. Los artículos mencionados son "Manzanas", "Leche", "Pan", "Huevos" y "Cereal".

- Crear conjunto de artículos importantes (articulos_importantes): Aquí, se define un conjunto llamado articulos_importantes que contiene algunos de los elementos de la - - lista de compras. En este caso, los elementos "Leche" y "Pan" se consideran artículos importantes.

- Crear diccionario de cantidades (cantidades): Se establece un diccionario llamado cantidades que relaciona cada artículo con una cantidad. Esto permitirá llevar un registro de cuántos de cada artículo se planea comprar. Las cantidades predeterminadas están asignadas para cada artículo.

- Mostrar la lista de compras, resaltando los artículos importantes: En esta sección, el código recorre la lista de compras utilizando un bucle for y verifica si cada artículo está en el conjunto articulos_importantes. Si es así, imprime el artículo con una marca de resaltado (un asterisco) junto con la cantidad asociada desde el diccionario cantidades. Si no es un artículo importante, lo imprime de manera normal.

- Agregar un nuevo artículo a la lista de compras: El programa le pide al usuario ingresar un nuevo artículo para agregar a la lista de compras (nuevo_articulo) y también solicita la cantidad de ese artículo que desea comprar (nueva_cantidad).

- Actualizar la lista, el conjunto y el diccionario: Aquí, el nuevo artículo se agrega a la lista de compras usando el método append, se agrega al conjunto de artículos importantes utilizando add, y se actualiza el diccionario de cantidades con la nueva cantidad asociada al nuevo artículo.

- Mostrar la lista de compras final: Finalmente, el código recorre la lista de compras actualizada y resalta los artículos importantes con un asterisco y sus respectivas cantidades.

```python
# Crear lista de compras
lista_compras = ["Manzanas", "Leche", "Pan", "Huevos", "Cereal"]

# Crear conjunto de artículos importantes
articulos_importantes = {"Leche", "Pan"}

# Crear diccionario de cantidades
cantidades = {
    "Manzanas": 5,
    "Leche": 2,
    "Pan": 1,
    "Huevos": 12,
    "Cereal": 1
}

# Mostrar la lista de compras, resaltando los artículos importantes
print("Lista de Compras:")
for articulo in lista_compras:
    if articulo in articulos_importantes:
        print(f"* {articulo} - {cantidades[articulo]}")
    else:
        print(f"  {articulo} - {cantidades[articulo]}")

# Agregar un nuevo artículo a la lista de compras
nuevo_articulo = input("\nIngrese un nuevo artículo para la lista de compras: ")
nueva_cantidad = int(input(f"Ingrese la cantidad de {nuevo_articulo} que desea comprar: "))

# Actualizar la lista, el conjunto y el diccionario
lista_compras.append(nuevo_articulo)
articulos_importantes.add(nuevo_articulo)
cantidades[nuevo_articulo] = nueva_cantidad

# Mostrar la lista de compras final
print("\nLista de Compras Actualizada:")
for articulo in lista_compras:
    if articulo in articulos_importantes:
        print(f"* {articulo} - {cantidades[articulo]}")
    else:
        print(f"  {articulo} - {cantidades[articulo]}") 
```

- Se define una lista llamada lista_compras que contiene algunos elementos iniciales como "Manzanas", "Leche", "Pan", "Huevos" y "Cereal".

- Se crea un conjunto llamado articulos_importantes, que inicialmente contiene los elementos "Leche" y "Pan". Este conjunto se utiliza para resaltar los artículos importantes en la lista de compras.

- Se crea un diccionario llamado cantidades que asocia cada artículo de la lista de compras con una cantidad. Por ejemplo, "Manzanas" tiene una cantidad de 5, "Leche" tiene una cantidad de 2, y así sucesivamente.

- Luego, el código muestra la lista de compras original, resaltando los artículos importantes (los que están en el conjunto articulos_importantes). Imprime cada artículo junto con su cantidad del diccionario cantidades.

- El código solicita al usuario que ingrese un nuevo artículo para la lista de compras utilizando la función input. Luego, pide al usuario que ingrese la cantidad deseada de ese nuevo artículo.

- Después de recibir la entrada del usuario, el código actualiza la lista de compras agregando el nuevo artículo, el conjunto de artículos importantes incluye el nuevo artículo y el diccionario de cantidades registra la cantidad ingresada para el nuevo artículo.

- Finalmente, el código muestra la lista de compras actualizada, nuevamente resaltando los artículos importantes y mostrando las cantidades correspondientes.