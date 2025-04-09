---
tags:
  - js
  - variables
---
Significa que podemos declarar una variable global y una variable local con el mismo nombre.

En el ámbito local, en el que declaramos una variable local utilizando su nombre, tendremos acceso al valor local (==la variable global está oculta detrás de la local, por lo que no tenemos acceso a ella en este ámbito local==). **Sin embargo, esta no es la mejor práctica de programación y deberíamos evitar este tipo de situaciones.** 

```js
let  number  =  100;
console.log(number);  //  ->  100
{
	let  number  =  200;
	console.log(number);  //  ->  200
}
console.log(number);  //  ->  100
```