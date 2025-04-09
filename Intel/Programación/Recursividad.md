# Recursividad en Programación

La recursividad es una técnica de programación en la que una función se llama a sí misma para resolver un problema. Es una herramienta poderosa que permite resolver problemas complejos dividiéndolos en casos más simples.

## Conceptos Fundamentales

Para entender la recursividad, es importante familiarizarse con estos conceptos:

- **Caso base:** Condición que detiene la recursión. Sin un caso base, la función se llamaría a sí misma indefinidamente.
- **Caso recursivo:** La parte donde la función se llama a sí misma con un problema más pequeño o simplificado.
- **Pila de llamadas:** Estructura que almacena información sobre las funciones activas durante la ejecución del programa.

## Ejemplo Simple: Factorial

```python
def factorial(n):
    # Caso base
    if n == 0 or n == 1:
        return 1
    # Caso recursivo
    else:
        return n * factorial(n-1)

# Ejemplo: factorial(5) = 5 * 4 * 3 * 2 * 1 = 120
print(factorial(5))  # Resultado: 120

```

## Ventajas de la Recursividad

- Código más limpio y legible para ciertos problemas
- Soluciones elegantes para estructuras de datos recursivas (árboles, grafos)
- Implementación directa de algoritmos recursivos (divide y vencerás)

## Desventajas

- Mayor consumo de memoria debido a la pila de llamadas
- Posible desbordamiento de pila (stack overflow) con recursiones profundas
- Posible ineficiencia en comparación con soluciones iterativas

## Tipos de Recursividad

### Recursividad Directa

Una función se llama directamente a sí misma.

```python
def countdown(n):
    if n <= 0:
        print("¡Despegue!")
    else:
        print(n)
        countdown(n-1)  # Llamada directa

```

### Recursividad Indirecta

Ocurre cuando una función A llama a una función B, y B eventualmente llama a A.

```python
def es_par(n):
    if n == 0:
        return True
    return es_impar(n-1)

def es_impar(n):
    if n == 0:
        return False
    return es_par(n-1)

```

### Recursividad de Cola

La llamada recursiva es la última operación en la función, lo que permite optimizaciones por parte del compilador.

```python
def factorial_cola(n, acumulador=1):
    if n <= 1:
        return acumulador
    return factorial_cola(n-1, n*acumulador)  # Recursión de cola

```

## Problemas Clásicos Resueltos con Recursividad

- **Torres de Hanoi:** Problema matemático que demuestra elegantemente el poder de la recursividad
- **Recorrido de árboles:** En orden, pre-orden, post-orden
- **Algoritmos de búsqueda:** Búsqueda binaria, búsqueda en profundidad (DFS)
- **Ordenamiento:** Quicksort, Mergesort
- **Fibonacci:** Aunque ineficiente de forma recursiva simple, es un ejemplo clásico

## Optimización de Recursividad

- **Memoización:** Almacenar resultados previos para evitar cálculos redundantes
- **Recursividad de cola:** Permite a los compiladores optimizar el uso de la pila
- **Convertir a iterativo:** Transformar algoritmos recursivos a iterativos para mayor eficiencia

La recursividad es una herramienta fundamental en el arsenal de todo programador, especialmente útil para problemas que pueden descomponerse naturalmente en subproblemas similares.