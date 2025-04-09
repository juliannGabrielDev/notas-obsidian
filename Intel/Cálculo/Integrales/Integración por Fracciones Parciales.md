---
tags:
  - math
  - integrales
---
**Identificar el tipo de fracción**

| Tipo              | Descripción                                                    | Ejemplo                           | Método a utilizar           |
| ----------------- | -------------------------------------------------------------- | --------------------------------- | --------------------------- |
| Fracción Impropia | Si el grado del numerador **mayor o igual** al del denominador | $$\frac{x^3 + x^2 + 5}{x^2 + 3}$$ | **DIVISIÓN**                |
| Fracción propia   | El grado del numerador es menor                                | $$\frac{2x}{x^2 + 3x + 2}$$       | Alguno de los **4 MÉTODOS** |
## EN CASO DE DIVISIÓN

**Paso 1. Identificar factores**

| Tipo                 | Formula                         | Ejemplos                     |
| -------------------- | ------------------------------- | ---------------------------- |
| Factores lineales    | $(ax + b)$                      | $(x)$, $(2x + 1)$, $(x - 3)$ |
| Factores cuadráticos | $(ax^2 + b)$, $(ax^2 + bx + c)$ | $(x^2 + x + 3)$              |
>[!WARNING]
>Para que un **factor cuadrático** sea considerado como tal este **NO debe poderse factorizar**.
>**Ejemplo:**
>Podríamos confundir a $(x^2 - 4)$ con un factor cuadrático, pero lo cierto es que no lo es, esto se debe a que puede ser factorizado como $(x + 2)(x - 2)$.

>[!TIP]
>Para identificar si una expresión es un **factor cuadrático** puedes utilizar la siguiente regla:
>Sí $(b^2 - 4ac) < 0$ la expresión no es factorizable, por lo tanto es un **factor cuadrático**.
>**Ejemplo:**
>$(x^2 + x + 3)$. En este caso basándonos en $(ax^2 + bx + c)$ tenemos que $a = 1$, $b = 1$ y $c = 3$. Sustituyendo en la formula $(b^2 - 4ac) < 0$ quedaría así $(1)^2 - 4(1)(3) = -11$. Al obtener un resultado menor a $0$ comprobamos que $(x^2 + x + 3)$ es un factor cuadrático.

**Paso 2.  Dividir**
Ejemplo:
$$\int \frac{x^2 + x + 3}{x-2} dx$$

```
  x^2 + 3  + 3    | x - 2
- x^2 + 2x        -------
--------------      x + 3
    0 + 3x + 3
      - 3x + 6
    ​-----------
             9  = x + 3 + ( 9 / x - 2 )

Comprobación:
( x - 2 )( x + 3 ) + 9 = ( x^2 + 3x - 2x - 6 ) + 9 = x^2 + x + 3

( x - 2)( x + 3 )       9
​------------------ + --------- = ) + 9 = x^2 + x + 3

( x - 2)( x + 3 )       9
----------------- + --------- = x + 3 + ( 9 / x - 2 )
     ( x - 2 )      ( x - 2 )
```

**Paso 3.  Resolver la integral.**

---
## Método 2. Factores lineales distintos

El denominador se puede factorizar en factores lineales de la forma $(ax + b)$, y ninguno de estos factores se repite.

$$\frac{P(x)}{(x-a)(x-b)(x-c)} = \frac{A}{x-a} + \frac{B}{x-b} + \frac{C}{x-c}$$

## Método 2. Factores lineales repetidos

El denominador contiene factores lineales repetidos, es decir, factores de la forma $(ax + b)^n$, donde $n$ es un entero mayor que 1.

$$\frac{P(x)}{(x-a)^3(x-b)} = \frac{A}{x-a} + \frac{B}{(x-a)^2} + \frac{C}{(x-a)^3} + \frac{D}{x-b}$$

El denominador contiene factores lineales repetidos, es decir, factores de la forma $(ax + b)^n$, donde $n$ es un entero mayor que 1.

## Método 3. Factores cuadráticos distintos

El denominador contiene factores cuadráticos irreducibles (es decir, que no se pueden factorizar en factores lineales con coeficientes reales) de la forma $ax^2 + bx + c$, y ninguno de estos factores se repite.

$$\frac{P(x)}{(x-a)(x^2+bx+c)} = \frac{A}{x-a} + \frac{Bx+C}{x^2+bx+c}$$

## Método 4. Factores cuadráticos repetidos

El denominador contiene factores cuadráticos irreducibles repetidos, es decir, factores de la forma $(ax^2 + bx + c)^n$, donde n es un entero mayor que 1.

$$\frac{P(x)}{(x-a)(x^2+bx+c)^2} = \frac{A}{x-a} + \frac{Bx+C}{x^2+bx+c} + \frac{Dx+E}{(x^2+bx+c)^2}$$