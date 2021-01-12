# grupo6-tailwind
Página final de tailwind.


Este proyecto esta diseñado con tailwind com el IDE de desarrollo Visual Studio Code

Seamos sinceros, escribir CSS la mayoría de las veces no es una tarea agradable; es una tarea que requiere de un trabajo artesanal y que suele llevar tiempo.

Tenemos librerías como Bootstrap CSS o Foundation que nos ayudan bastante a aplicar estilos bonitos a nuestras aplicaciones pero el problema es que al final, aunque estos frameworks se pueden personalizar, nos quedan aplicaciones muy parecidas unas de otras.

Por eso quiero hablaros de TailwindCSS.

El creador de TailwindCSS, Adam Wathan, la define como una librería de utilidades agnóstica a los frameworks frontend, es decir, puede funcionar con cualquier herramienta ya sea Angular, React, Vue... Además, Tailwind no es un framework CSS como los mencionados anteriormente que están basados en componentes, Tailwind lo que nos provee son clases CSS predefinidas a más bajo nivel por lo que la creación de los componentes será cosa nuestra.

Se la utiliza como herramienta, simplemente se necesita vincular una cuenta en Pinterest. Tailwind es fácil de usar y brinda un soporte constante a los usuarios. La plataforma funciona online y cuenta con una aplicación para iOS y Android.

Instalación

Primero vamos a realizar la instalación de Tailwind. Para ello escribimos en el terminal el comando:

npm install tailwindcss

Aparte, vamos a hacer algunos cambios en el archivo package.json:

... "scripts": { "ng": "ng", "start": "ng serve", "tw": "node_modules.bin\tailwind build ./src/tailwind.css -c ./tailwind-config.js -o ./src/styles.css", "build": "ng build", "test": "ng test", "lint": "ng lint", "e2e": "ng e2e", "tailwind": "./node_modules/.bin/tailwind init" }, ...

Acto seguido necesitamos crear el archivo de configuración de Tailwind con el siguiente comando:

npx tailwind init

Si escribimos npx tailwind init --full nos mostrará en el archivo tailwind-config.js las configuraciones predefinidas de Tailwind, pero no es necesario. De hecho es mucho mejor no tenerlas, pues así vemos claramente las modificaciones que nosotros le hemos implementado a Tailwind.

A continuación, escribimos los imports de Tailwind en el archivo src/tailwind.css y ejecutamos el comando npm run tw

tailwind.css

@tailwind base;

@tailwind components;

@tailwind utilities;
