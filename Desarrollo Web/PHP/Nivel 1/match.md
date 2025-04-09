---
tags:
  - php
  - nivel-1
---
En PHP, la función `match` es una estructura de control introducida en PHP 8.0. Es similar a switch, pero más expresiva y estricta. Evalúa una expresión y la compara con múltiples valores posibles, devolviendo el resultado correspondiente al primer caso coincidente.

Sintaxis básica de match

```php
$resultado = match($variable) {
    valor1 => expresión1,
    valor2 => expresión2,
    default => valorPorDefecto,
};
```

Características principales:

- **Estricto**: Utiliza comparación estricta (` === `), lo que significa que también verifica el tipo.

- **Devuelve un valor**: El resultado de la expresión `match` puede asignarse directamente a una variable.

- **No requiere break**: A diferencia de switch, no necesita la palabra clave break.

## Ejemplo básico: `match` con `true`

```php
mensaje = match (true) {
    $edad < 18 => "Eres menor de edad.",
    $edad >= 18 && $edad <= 65 => "Eres adulto.",
    $edad > 65 => "Eres adulto mayor.",
    default => "Edad no válida.",
};

echo $mensaje; // Salida: Eres adulto.
```