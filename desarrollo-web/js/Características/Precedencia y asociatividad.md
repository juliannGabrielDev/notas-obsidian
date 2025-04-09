---
tags:
  - js
  - caracteristicas
---
El intérprete de JavaScript utiliza dos propiedades de operador para determinar la secuencia de operaciones: **precedencia** y **asociatividad**. La precedencia se puede tratar como una prioridad, y algunos operadores tienen la misma precedencia (por ejemplo, la suma y la resta). La asociatividad permite especificar el orden de ejecución si hay varios operadores con las mismas prioridades uno al lado del otro.

| Precedencia | Tipo de Operador                                                      | Asociatividad | Operadores                                       |
| ----------- | --------------------------------------------------------------------- | ------------- | ------------------------------------------------ |
| 19          | Agrupación                                                            | n/a           | ( )                                              |
| 18          | Acceso a propiedades                                                  | Izquierda     | ., [ ], new, (), ?.                              |
| 17          | new                                                                   | Derecha       | new                                              |
| 16          | Incremento/Decremento (postfijo)                                      | n/a           | ++, --                                           |
| 15          | NOT lógico, NOT a nivel de bits, unarios, typeof, void, delete, await | Derecha       | !, ~, +, -, typeof, void, delete, await          |
| 15          | Incremento/Decremento (prefijo)                                       | Derecha       | ++, --                                           |
| 14          | Exponenciación                                                        | Derecha       | **                                               |
| 13          | Multiplicación, División, Resto                                       | Izquierda     | *, /, %                                          |
| 12          | Suma, Resta                                                           | Izquierda     | +, -                                             |
| 11          | Desplazamiento de bits                                                | Izquierda     | <<, >>, >>>                                      |
| 10          | Relacionales, in, instanceof                                          | Izquierda     | <, <=, >, >=, in, instanceof                     |
| 9           | Igualdad, Desigualdad                                                 | Izquierda     | ==, !=, ===, !==                                 |
| 8           | AND a nivel de bits                                                   | Izquierda     | &                                                |
| 7           | XOR a nivel de bits                                                   | Izquierda     | ^                                                |
| 6           | OR a nivel de bits                                                    | Izquierda     | `                                                |
| 5           | AND lógico                                                            | Izquierda     | &&                                               |
| 4           | OR lógico, Coalescencia nula                                          | Izquierda     | `                                                |
| 3           | Condicional (ternario)                                                | Derecha       | ? :                                              |
| 2           | Asignación                                                            | Derecha       | =, +=, -=, *=, /=, %=, <<=, >>=, >>>=, &=, ^=, ` |
| 2           | yield, yield*                                                         | Derecha       | yield, yield*                                    |
| 1           | Coma                                                                  | Izquierda     | ,                                                |
