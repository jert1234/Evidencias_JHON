<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 2


<!-- Su documentación aquí -->

## Actividad: Repositorio local de ejercicios de estructuras de control iterativas (Trabajo individual)

Crea un repositorio local y resuelve los siguientes ejercicios para practicar bucles `while` y `for`:

## Ejercicios con bucle while:

- **Solicita al usuario que ingrese una lista de números y encuentra el número mayor y el menor** 

```python 
numeros = input("Ingresa una lista de números separados por espacios: ").split()
numeros = [int(x) for x in numeros]
maximo = max(numeros)
minimo = min(numeros)
print(f"El número mayor es: {maximo}")
print(f"El número menor es: {minimo}")
```


- **Solicita al usuario un número e imprime la suma de los números pares entre 1 y ese número** 
```python 
numero = int(input("Ingresa un número: "))
suma_pares = sum(x for x in range(2, numero + 1, 2))
print(f"La suma de los números pares entre 1 y {numero} es: {suma_pares}")
```

- **Solicita al usuario una cadena e imprime cuántas vocales contiene** 
```python 
cadena = input("Ingresa una cadena de texto: ")
vocales = 'aeiouAEIOU'
cantidad_vocales = sum(1 for letra in cadena if letra in vocales)
print(f"La cadena contiene {cantidad_vocales} vocales.")
```

- **Solicita al usuario un número y muestra su tabla de potencias desde 1 hasta 10** 

```python 
numero = int(input("Ingresa un número: "))
for i in range(1, 11):
resultado = numero ** i
print(f"{numero}^{i} = {resultado}")
```
- **Solicita al usuario una lista de números y calcula la media aritmética** 

```python 
numeros = input("Ingresa una lista de números separados por espacios: ").split()
numeros = [float(x) for x in numeros]
media = sum(numeros) / len(numeros)
print(f"La media aritmética de los números ingresados es: {media}")
```

## Ejercicios ciclo for

- **Solicita al usuario una lista de números y calcula la suma de sus elementos** 

```python 
numeros = input("Ingresa una lista de números separados por espacios: ").split()
numeros = [float(x) for x in numeros]
suma = sum(numeros)
print(f"La suma de los elementos de la lista es: {suma}")
```


- **Solicita al usuario una lista de números e imprime cuántos de ellos son pares** 
```python 
numeros = input("Ingresa una lista de números separados por espacios: ").split()
numeros = [int(x) for x in numeros]
cantidad_pares = sum(1 for x in numeros if x % 2 == 0)
print(f"La lista contiene {cantidad_pares} números pares.")
```

- **Solicita al usuario un número y muestra su tabla de multiplicar usando range()** 
```python 
numero = int(input("Ingresa un número para ver su tabla de multiplicar: "))
for i in range(1, 11):
producto = numero * i
print(f"{numero} x {i} = {producto}")
```

- **Solicita al usuario un número e imprime los números pares desde 2 hasta ese número** 

```python 
numero = int(input("Ingresa un número: "))
for i in range(2, numero + 1, 2):
print(i)
```
- **Solicita al usuario un número y muestra la secuencia de números pares desde 2 hasta ese número** 

```python 
numero = int(input("Ingresa un número: "))
for i in range(2, numero + 1, 2):
print(i)
```
