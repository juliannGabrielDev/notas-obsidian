## Cadena larga

```python
my_variable = "Esta es \
una cadena muy larga \
en varias líneas"
```

## Métodos y funciones de cadenas

| Función/Método  | Descripción breve                                                                                            | Ejemplo                                   | Resultado                |
| --------------- | ------------------------------------------------------------------------------------------------------------ | ----------------------------------------- | ------------------------ |
| `len()`         | Devuelve la longitud (número de caracteres) de la cadena.                                                    | `len("Python")`                           | `6`                      |
| `.lower()`      | Convierte todos los caracteres de la cadena a minúsculas.                                                    | `"PYTHON".lower()`                        | `"python"`               |
| `.upper()`      | Convierte todos los caracteres de la cadena a mayúsculas.                                                    | `"python".upper()`                        | `"PYTHON"`               |
| `.strip()`      | Elimina espacios (u otros caracteres) al inicio y al final de la cadena.                                     | `" hola ".strip()`                        | `"hola"`                 |
| `.split()`      | Divide la cadena en una lista, utilizando un separador especificado.                                         | `"uno,dos,tres".split(",")`               | `["uno", "dos", "tres"]` |
| `.join()`       | Une los elementos de una secuencia (como una lista) en una sola cadena, utilizando la cadena como separador. | `" ".join(["Hola", "Mundo"])`             | `"Hola Mundo"`           |
| `.find()`       | Retorna el índice de la primera aparición de una subcadena; si no la encuentra, retorna -1.                  | `"Python".find("t")`                      | `2`                      |
| `.replace()`    | Reemplaza todas las ocurrencias de una subcadena por otra en la cadena.                                      | `"hola mundo".replace("mundo", "Python")` | `"hola Python"`          |
| `.startswith()` | Verifica si la cadena comienza con una subcadena dada.                                                       | `"Python".startswith("Py")`               | `True`                   |
| `.endswith()`   | Verifica si la cadena termina con una subcadena dada.                                                        | `"Python".endswith("hon")`                | `True`                   |
| `.isdigit()`    | Comprueba si la cadena contiene únicamente dígitos.                                                          | `"1234".isdigit()`                        | `True`                   |
| `.isalpha()`    | Comprueba si la cadena contiene únicamente letras.                                                           | `"Python".isalpha()`                      | `True`                   |
| `.isalnum()`    | Comprueba si la cadena contiene únicamente caracteres alfanuméricos (letras y números).                      | `"Python3".isalnum()`                     | `True`                   |
| `.capitalize()` | Convierte la primera letra de la cadena a mayúscula y el resto a minúsculas.                                 | `"python".capitalize()`                   | `"Python"`               |
| `.title()`      | Convierte la primera letra de cada palabra a mayúsculas.                                                     | `"hola mundo".title()`                    | `"Hola Mundo"`           |
| `.count()`      | Cuenta cuántas veces aparece una subcadena en la cadena.                                                     | `"hola hola".count("hola")`               | `2`                      |
| `.center()`     | Centra la cadena en un campo de ancho especificado, rellenando con espacios o el carácter que se indique.    | `"hola".center(10, "*")`                  | `"***hola***"`           |
| `.ljust()`      | Justifica la cadena a la izquierda en un campo de ancho indicado, rellenando a la derecha.                   | `"hola".ljust(10, "-")`                   | `"hola------"`           |
| `.rjust()`      | Justifica la cadena a la derecha en un campo de ancho indicado, rellenando a la izquierda.                   | `"hola".rjust(10, "-")`                   | `"------hola"`           |