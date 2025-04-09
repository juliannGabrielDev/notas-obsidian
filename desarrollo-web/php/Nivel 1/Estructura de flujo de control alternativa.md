---
tags:
  - php
  - nivel-1
---
La estructura de flujo de control alternativa en PHP es una forma más concisa y legible de escribir condiciones y bucles. En el contexto de insertar bloques HTML, es especialmente útil para crear páginas web dinámicas.

## ¿Cómo funciona?

En lugar de usar las llaves `{}` para delimitar los bloques de código, se utilizan dos puntos `:` para iniciar el bloque y una palabra clave `endif;`, `endwhile;`, `endfor;`, `endforeach;` o `endswitch;` para cerrarlo, dependiendo de la estructura de control.

**Ejemplo con `if`**:

```php
<?php
if ($edad >= 18):
?>
    <p>Eres mayor de edad.</p>
<?php else: ?>
    <p>Eres menor de edad.</p>
<?php endif; ?>

```

**Ejemplo con foreach**:

```php
<?php
$frutas = ['manzana', 'banana', 'pera'];
foreach ($frutas as $fruta):
?>
    <li><?php echo $fruta; ?></li>
<?php endforeach; ?>

```

**Ejemplo con for**:

```php
<?php
for ($i = 0; $i < 5; $i++):
?>
    <p>Iteración número: <?php echo $i; ?></p>
<?php endfor; ?>
```

**Ejemplo con switch**:

```php
<?php
$diaSemana = "lunes";

switch ($diaSemana):
    case "lunes":
        echo "Es lunes, ¡a trabajar!";
        break;
    case "viernes":
        echo "Es viernes, ¡casi fin de semana!";
        break;
    default:
        echo "Es otro día de la semana.";
        break;
endswitch;
```

**Ejemplo con while**:

```php
<?php
$contador = 0;
while ($contador < 10):
?>
    <p>El contador es: <?php echo $contador; ?></p>
    <?php $contador++; ?>
<?php endwhile; ?>
```
