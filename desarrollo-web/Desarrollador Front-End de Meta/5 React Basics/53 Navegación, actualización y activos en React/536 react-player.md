---
Fecha: 2024-12-21
Categoría: Uso de activos en React
tags:
  - front-end
  - curso-5
  - modulo-3
---
En esta lectura, aprenderá a instalar el paquete npm react-player.

Puede encontrar este paquete en el sitio web npmjs.org en la siguiente URL:

[https://www.npmjs.com/package/react-player](https://www.npmjs.com/package/react-player "https://www.npmjs.com/package/react-player")

Para instalar este paquete tendrá que utilizar el siguiente comando en el terminal:

```shell
npm install react-player
```

Una vez que tenga instalado este paquete, podrá empezar a utilizarlo en su proyecto.

Existen varias formas de importar y utilizar el paquete instalado. Por ejemplo, para obtener toda la funcionalidad del paquete, utilice la siguiente importación:

```jsx
import ReactPlayer from "react-player";
```

Si, por ejemplo, sólo piensa utilizar vídeos de un sitio como YouTube, para reducir el tamaño del paquete, puede utilizar la siguiente importación:

```jsx
import ReactPlayer from "react-player/youtube";
```

He aquí un ejemplo de uso del paquete react-player en una pequeña aplicación React:

```jsx
import React from "react";
import ReactPlayer from "react-player/youtube";

const App = () => {
  return (
    <div>
      <MyVideo />
    </div>
  );
};

const MyVideo = () => {
  return (
    <ReactPlayer url='https://www.youtube.com/watch?v=ysz5S6PUM-U' />
  );
};

export default App;

```

En esta lectura, ha aprendido a instalar y utilizar el paquete npm react-player.