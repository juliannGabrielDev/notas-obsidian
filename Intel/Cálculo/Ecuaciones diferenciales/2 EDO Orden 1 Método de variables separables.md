El **método de variables separables** es uno de los métodos más comunes y sencillos para resolver ecuaciones diferenciales ordinarias de primer orden. Este método es aplicable cuando la ecuación diferencial puede escribirse de tal manera que las variables $y$ y $x$ se pueden separar a un lado de la ecuación.

### **Pasos para resolver una ecuación diferencial de primer orden usando el método de variables separables:**

#### 1. **Escribir la ecuación en forma separable:**
   Una ecuación diferencial de primer orden tiene la forma general:
$$\frac{dy}{dx} = f(x)g(y)$$

El objetivo es **separar las variables** $x$ y $y$ ya sea **multiplicando** o **dividiendo**, de manera que todas las expresiones que involucran $y$ estén en un lado de la ecuación y todas las expresiones que involucran $x$ estén en el otro. **Ejemplo:** 
$$\frac{dy}{dx} = \frac{x}{y}$$

En este caso, puedes separarlas así: $y \, dy = x \, dx$

#### 2. **Integrar ambos lados:**
Una vez que las variables estén separadas, integras ambos lados de la ecuación. **Ejemplo:**
$$\int y \, dy = \int x \, dx$$

Al resolver las integrales, obtienes:
$$\frac{y^2}{2} = \frac{x^2}{2} + C$$
Aquí, $C$ es la constante de integración.

#### 3. **Despejar $y$ (si es necesario)**
#### 4. **Aplicar las condiciones iniciales (si las hay)**