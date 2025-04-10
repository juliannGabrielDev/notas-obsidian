---
Fecha: 2024-12-25
Categoría: La entrevista de codificación
tags:
  - front-end
  - curso-9
  - modulo-1
---
## **Introducción**
---
En esta lectura, aprenderá cómo puede incorporar las pruebas en sus tareas para llevar a casa y en una entrevista de codificación, también explorará la práctica de escribir pruebas unitarias.

Las pruebas son una parte fundamental del desarrollo de software. Lo ideal es que el alcance de sus pruebas sea exhaustivo; sin embargo, siempre hay consideraciones externas que pueden afectar a este resultado ideal. Históricamente, las pruebas se han realizado a menudo al final, por lo que si se avecina un plazo de producción, las pruebas pueden ser lo primero que se reduzca. El desarrollo dirigido por pruebas (TDD) es un enfoque desarrollado para evitar este resultado. Este debate sobre las pruebas se centrará en dos casos, una entrevista de codificación y una tarea para llevar a casa.

## **1 Tarea para llevar a casa**
---
Si le han permitido llevarse algo de código a casa, es posible que tenga tiempo para implementar pruebas más exhaustivas.

Hay muchos tipos de pruebas que puede optar por ejecutar. Por ejemplo

- **Pruebas de integración:** Estas prueban cómo interactúan entre sí los distintos componentes de una aplicación. Una prueba de integración no será exhaustiva porque se simularán las dependencias externas en lugar de utilizar instancias reales. Además, las pruebas unitarias evalúan líneas de código individuales, mientras que las pruebas de integración adoptan un enfoque más global.

- **Pruebas funcionales:** Se trata de una prueba automatizada que demuestra que un sistema funciona como se espera. Esta prueba se ocupa de las capacidades del sistema.

- **Pruebas de regresión:** Se trata de probar que un cambio no provoca un error en el código existente. Garantiza que cuando se realiza un cambio en el sistema, éste no afecta a su funcionamiento.

El nivel de pruebas que emplee dependerá siempre del tiempo. Una parte crucial del proceso es crear una aplicación que funcione. Las pruebas demuestran su rigor y garantizan que la aplicación funcionará. El grado en que puede incluir estas estrategias puede verse limitado en función del tiempo de que disponga.

## **2 Entrevista de codificación**
---
Las pruebas unitarias son un enfoque que confirma que su código funciona como se espera. Aunque se escriben muchas pruebas antes de que el código pase a producción, no tendrá la oportunidad de escribirlas todas cuando participe en una entrevista de codificación. Las pruebas unitarias son un enfoque manejable que puede incorporar a su solución, demostrando su atención al detalle. Demostrará su buena práctica a la hora de probar su código.

Una prueba unitaria se preocupa menos del funcionamiento general de una aplicación. En su lugar, comprueba que cada uno de los componentes individuales funciona como se espera.

### **3 Consideraciones al escribir pruebas**
---
- **Legibilidad:** Haga que las pruebas sean legibles para otros desarrolladores. Este hábito debe interiorizarse independientemente de si trabaja en equipo. Las pruebas con un propósito claro identifican los problemas en caso de que surjan. También señalan lo que se supone que debe conseguir una sección de código. Esto tiene el efecto añadido de aumentar la mantenibilidad.

- **Resultados claros:** Siempre que sea posible, sus pruebas deben ser deterministas. Es decir, el resultado debe ser siempre el mismo independientemente de las condiciones. Una prueba determinista siempre fallará cuando se escriba código con errores. Las pruebas que dependen de una combinación de condiciones diferentes pueden ser difíciles de depurar.

- **Automatización:** Las pruebas deben tener siempre la posibilidad de automatizarse para que puedan ejecutarse rápidamente cada vez que se realice un cambio en el código. Esta es una piedra angular de CI/CD (integración continua/desarrollo continuo).

## **4 Poner en práctica las pruebas unitarias**
---
La lectura de definición de soluciones describe los pasos necesarios para realizar un juego de adivinanzas numéricas. A continuación se muestra una captura de pantalla del pseudocódigo utilizado para desarrollar una solución viable.

```
Genetate a question
Take in user input
Compare input with answer
Return a result
```

Tomando este ejemplo, imagine que sólo quedan unos minutos del tiempo asignado, ¿en qué se centraría? Las pruebas unitarias más básicas que se pueden escribir son los casos de aserción, que determinan que lo que se da es lo esperado. Existen bibliotecas de este tipo en la mayoría de los lenguajes de codificación.

```
take in user input 
// assert not null 
// assert all of type integer 
// assert within the range specified 

generate number 
// assert type integer 
// assert within a given range 

comparing number 
generate a mock instance with a given answer 
// assert code checks less than 
// assert code checks qreater than 
// assert code correctly acts when number is correct
```

El primer paso puede ser escribir un caso de prueba para determinar si la entrada del usuario es válida. Las líneas 2 - 4 esbozan algunas pruebas que pueden aplicarse para validar la entrada del usuario, comprobando que se ha introducido algo antes de que el usuario pulsara return. Debe determinar que es del tipo correcto y que no bloqueará el programa. Además, asegúrese de que está dentro de los límites especificados. A continuación, debe considerar la comprobación del número aleatorio generado. ¿Es del tipo correcto y está dentro de los parámetros aceptables? Por último, le ayudaría pensar en incluir comprobaciones que aseguren el resultado correcto cuando se activen las sentencias condicionales.

El proceso para escribir pruebas unitarias está estandarizado. Es una buena idea practicar su ejecución cuando esté escribiendo código. Esto le ayudará a familiarizarse rápidamente con el proceso y puede poner de relieve su atención en un entorno en el que esté probando su código.

## **Conclusión**
---
En esta lectura, ha aprendido cómo puede incorporar las pruebas en sus tareas para llevar a casa y en una entrevista de codificación y también ha explorado la práctica de escribir pruebas unitarias. Después de leer todo el contenido anterior, ahora debería saber que evaluar su código es especialmente importante.

A menudo, la práctica de escribir pruebas puede quedar marginada en comparación con el tiempo dedicado a implementar una aplicación. Para evitar este escollo de codificación, asegúrese de que escribe pruebas a medida que codifica. Mientras que algunas pruebas pueden ser profundas y llevar mucho tiempo, escribir pruebas unitarias puede hacerse rápidamente. Este hábito puede dar peso al argumento de que usted es un candidato idóneo para un puesto. Si puede incorporar pruebas unitarias a una tarea, sobre todo a las que tienen limitaciones de tiempo, estará bien preparado para una entrevista de codificación.