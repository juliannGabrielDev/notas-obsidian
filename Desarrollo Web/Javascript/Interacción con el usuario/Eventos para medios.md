---
tags:
  - js
  - interaccion-usuario
---
## Eventos

| Evento           | Descripción                                                                                                |
| ---------------- | ---------------------------------------------------------------------------------------------------------- |
| `play`           | Se dispara cuando la reproducción del medio comienza.                                                      |
| `pause`          | Se dispara cuando la reproducción del medio se pausa.                                                      |
| `ended`          | Se dispara cuando la reproducción del medio llega al final.                                                |
| `timeupdate`     | Se dispara cuando la posición de reproducción del medio cambia.                                            |
| `volumechange`   | Se dispara cuando el volumen del medio cambia.                                                             |
| `loadedmetadata` | Se dispara cuando se cargan los metadatos del medio (duración, dimensiones, etc.).                         |
| `canplay`        | Se dispara cuando el navegador puede comenzar a reproducir el medio.                                       |
| `canplaythrough` | Se dispara cuando el navegador estima que puede reproducir el medio sin interrupciones por falta de datos. |

## Métodos

|Método|Descripción|
|---|---|
|play()|Inicia la reproducción del medio.|
|pause()|Pausa la reproducción del medio.|
|load()|Recarga el medio.|
|currentTime|Establece u obtiene la posición de reproducción del medio (en segundos).|
|volume|Establece u obtiene el volumen del medio (un valor entre 0 y 1).|
|muted|Establece u obtiene si el medio está silenciado (true) o no (false).|