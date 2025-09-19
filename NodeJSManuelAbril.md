# Node JS

### 1. Introducción a Node.js y su importancia en el Front-End

Node.js es un entorno que permite ejecutar JavaScript fuera del navegador.  
Antes, JavaScript solo funcionaba dentro del navegador, pero con Node.js también se puede usar en un servidor.

**¿Por qué es importante?** 
- Permite trabajar en Front-End y Back-End con el mismo lenguaje (Full-Stack).  
- Es muy rápido gracias al motor V8 de Google Chrome.  
- Ideal para crear:  
  - Servidores web  
  - Chats en tiempo real  
  - Aplicaciones modernas  
- Funciona en Windows, Mac y Linux (cross-platform).  
- Permite manejar conexiones asíncronas, atendiendo muchas conexiones al mismo tiempo sin bloquearse.

---

### 2. Cómo funciona Node.js fuera del navegador

Node.js actúa como un servidor interno en nuestro ordenador:  
- Permite probar y ejecutar aplicaciones localmente sin necesidad de Internet.  
- Nuestro ordenador se convierte en un servidor web temporal.  
- Abrimos el navegador en:  http://localhost:...

Node.js usa un event loop que permite manejar muchas solicitudes al mismo tiempo sin bloquearse.


---

### 3. Qué es NPM y Yarn

- **NPM (Node Package Manager)**  
  Permite:  
  - Descargar librerías  
  - Instalar dependencias  
  - Ejecutar scripts
   
   **Ejemplos de comandos útiles:**  
  ```
  npm install express --save
  npm install nodemon --save-dev
  npm run nombre-script
  ```

- **Yarn**  
  Hace lo mismo que NPM, con algunas mejoras en velocidad y control de dependencias.  

---

### 4. Demo: Crear un servidor básico con Node.js

**Paso 1: Crear proyecto**

```
mkdir demo-node
cd demo-node
npm init -y
```

**Paso 2: Instalar Express**

```
npm install express
```

**Paso 3: Crear index.js**

```
const express = require("express");
const app = express();

// Ruta principal
app.get("/", (req, res) => {
  res.send("¡Hola desde mi primer servidor con Node.js!");
});

// Escucha en el puerto 3000
app.listen(3000, () => {
  console.log("Servidor corriendo en http://localhost:3000");
});
```

**Paso 4: Ejecutar el servidor**

```
node index.js
```
De esta manera cuando abrimos el navegador: http://localhost:3000 se mostraraáel mensaje: “¡Hola desde mi primer servidor con Node.js!”

**Paso 6: Detener el servidor**

En la terminal, presionar Ctrl + C para detener el servidor, de esta forma se libera el puerto 3000 y cierra el servidor.