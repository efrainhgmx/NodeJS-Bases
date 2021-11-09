# Node JS - Bases en español

Esta documentación, no pertenece ni es parte de la documentación oficial de Node JS, por lo cual te invito a que leas la documentación oficial en [NodeJS.org](https://nodejs.org/es/ "NodeJS.org")

Mi objetivo es crear una pequeña documentación en **español** de ciertas características muy útiles para tus proyectos de Backend en JavaScript usando Node JS. 


Esta documentación me ha sido muy útil en mi trabajo profesional en mi día a día trabajando con Node JS. Espero te sirva si has llegado a leer a este punto. 😄

###  **CREAR ARCHIVOS Y EDITARLOS AL EJECUTAR UN PROGRAMA**

**-------------------------------------------------------------------------**

Node JS tiene ciertas funciones que nos permiten crear, editar o acceder a archivos desde la terminal.

Acá te comparto alguno y como ejecutarlos.

#### fs.writeFile(file, data , [options], callback)

**fs**, es una función que nos permite en este caso, crear y escribir un archivo al ejectuar un programa en node. Este archivo es guardado en la carpeta donde esta el programa que se esta ejecutando.

Recibe principalmente **tres argumentos**, **nombre_del_archivo[string]**, **la data que vamos a escribir sobre el archivo[cualquier valor]** y **un callback[una función]** este ultimo es el que se ejecuta en caso de un error.

La sintaxis es la siguiente: 

```javascript
const fs =  require('fs');

let salida =  "Hola Mundo";

fs.writeFile('mensaje.txt', salida, (err) => {
    if(err) throw err;

    console.log('mensaje.txt creado');
});
```

También es posible utlizar **FileSync** el cual es mucho más simple de usar, su sintáxis es la siguiente: 

```javascript
fs.writeFileSync("mensaje.txt", salida);
```
