Permite comparar una variable con múltiples patrones y ejecutar diferentes bloques de código según el patrón coincidente.

```python
# Coincidencia de valores literales
fruta = "manzana"

match fruta:
    case "manzana":
        print("Es una manzana")
    case "plátano":
        print("Es un plátano")
    case _:
        print("No es ni manzana ni plátano")

# Coincidencia de múltiples patrones
punto = (3, 4)

match punto:
    case (0, 0):
        print("El punto está en el origen")
    case (x, 0):
        print(f"El punto está en el eje x en x = {x}")
    case (0, y):
        print(f"El punto está en el eje y en y = {y}")
    case (x, y):
        print(f"El punto está en ({x}, {y})")

# Coincidencia de patrones con condiciones adicionales
número = 10

match número:
    case x if x > 0 and x % 2 == 0:
        print("Es un número par positivo")
    case x if x > 0:
        print("Es un número positivo")
    case x if x < 0:
        print("Es un número negativo")
    case 0:
        print("Es cero")
```