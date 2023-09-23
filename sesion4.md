<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 4


<!-- Su documentación aquí -->

Actividad: Resolver utilizando funciones en Python
Calculadora Básica: Crea una función llamada calculadora que tome tres argumentos: dos números y un operador (+, -, *, /). La función debe realizar la operación indicada en los dos números y devolver el resultado.
Ejemplo de uso:


`resultado = calculadora(5, 3, '+')  # Debe devolver 8`

Conteo de Vocales: Crea una función llamada contar_vocales que tome una cadena como argumento y devuelva el número de vocales (a, e, i, o, u) que contiene la cadena.
Ejemplo de uso:

`num_vocales = contar_vocales("Hola, mundo!")  # Debe devolver 4`

Primo o No Primo: Escribe una función llamada es_primo que tome un número entero positivo como argumento y determine si es un número primo (es decir, solo es divisible por 1 y por sí mismo). La función debe devolver True si es primo y False si no lo es.
Ejemplo de uso:

`resultado = es_primo(17)  # Debe devolver True `

Contador de Palabras: Escribe una función llamada contar_palabras que tome una cadena como argumento y devuelva el número de palabras en esa cadena. Supón que las palabras están separadas por espacios.
Ejemplo de uso:

`num_palabras = contar_palabras("Hola, este es un ejemplo.")  # Debe devolver 5`

Cálculo de Potencia: Escribe una función llamada potencia que tome dos números enteros como argumentos, uno como base y otro como exponente, y devuelva el resultado de elevar la base al exponente.
Ejemplo de uso:

`resultado = potencia(2, 3)  # Debe devolver 8 (2^3 = 2 * 2 * 2)`

## Solucion
```python
# Ejercicio 1 
def calculadora(num1, num2, operador):
    if operador == '+':
        return num1 + num2
    elif operador == '-':
        return num1 - num2
    elif operador == '*':
        return num1 * num2
    elif operador == '/':
        if num2 == 0:
            return "Error: División por cero"
        return num1 / num2
    else:
        return "Operador no válido"

# Ejemplo de uso:
resultado = calculadora(5, 3, '+')
print(resultado)  # Debe devolver 8

# Ejercicio 2
def contar_vocales(cadena):
    cadena = cadena.lower()  # Convertir la cadena a minúsculas para contar todas las vocales
    contador = 0
    for letra in cadena:
        if letra in "aeiou":
            contador += 1
    return contador

# Ejemplo de uso:
num_vocales = contar_vocales("Hola, mundo!")
print(num_vocales)  # Debe devolver 4

# Ejercicio 3
def es_primo(numero):
    if numero <= 1:
        return False
    if numero <= 3:
        return True
    if numero % 2 == 0 or numero % 3 == 0:
        return False
    i = 5
    while i * i <= numero:
        if numero % i == 0 or numero % (i + 2) == 0:
            return False
        i += 6
    return True

# Ejemplo de uso:
resultado = es_primo(17)
print(resultado)  # Debe devolver True

# Ejercicio 4
def contar_palabras(cadena):
    palabras = cadena.split()  # Dividir la cadena en palabras usando espacios como separadores
    return len(palabras)

# Ejemplo de uso:
num_palabras = contar_palabras("Hola, este es un ejemplo.")
print(num_palabras)  # Debe devolver 5

# Ejercicio 5
def potencia(base, exponente):
    return base ** exponente

# Ejemplo de uso:
resultado = potencia(2, 3)
print(resultado)  # Debe devolver 8
```



