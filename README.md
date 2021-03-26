# Práctica React

La idea de esta ejercitación es que puedas poner en práctica, con ejercicios cortos (y no muy realistas) los conceptos vistos hasta ahora. 

## Conceptos básicos

*1) Creando un componente*

- Crea un nuevo proyecto de React 
- En App.js mostrá un título cualquiera con `<h1>` 
- Crea un componente nuevo *Tarjeta.js*
- En Tarjeta.js, mostra un titulo con `<h2>`

*2) Usando variables en JSX*

- En App.js declará la variable `titulo` y dale el contenido del `<h1>`
- Hacé lo mismo en Tarjeta.js con el `<h2>`: declara la variable `titulo` (nota que podes usar variables con el mismo nombre en componentes distintos!)
- Usá esas variables en el JSX para mostrar el contenido en tu web. 

*3) Usando props*

- Desde App.js declará la variable `tituloTarjeta` y pasale el contenido que tiene el h2. Podes borrar la variable antes declarada en Tarjeta.js
- Envia esta variable a Tarjeta.js como una `prop`. 
- Comprobá que se muestre en la web. 

*4) Usando renderizado condicional*
- Declará en App.js una variable llamada `mostrarTituloApp` que tenga como valor `true`. 
- Usando cualquier tecnica de renderizado condicional, logra que el `<h1>` de App.js se muestre solo si mostrarTituloApp es `true`. Probá cambiarla a `false` para comprobar que tu código funciona. 

*5) Usando eventos en JSX*
- En App.js hagamos un `<button>` "Ocultar titulo". 
- Por ahora no tendra funcionalidad: cuando el usuario haga click en el boton, queremos ver en la consola un mensaje que diga "hiciste click en el boton". 

**Problema:** Incluso si completaramos esa funcion para que modifique la variable `mostrarTituloApp` a `false`, veremos que el titulo no se oculta. Por qué ocurre esto?

*5) Usando el estado*
- Borra la variable mostrarTituloApp, y crea una nueva variable en el estado con el mismo nombre, que tenga como valor inicial `true`. 
- Al hacer click en el boton, queremos que la variable del estado mostrarTituloApp pase a ser `false` y, en consecuencia, el titulo se oculte. 

## Trabajando con datos complejos y props

Borrá todo el codigo anterior si puede llegar a confundirte. 

*1) Trabajando con objetos*
- En App.js declara el objeto `gato`:

```js
const gato = {
  nombre: "Garfield",
  color: "naranja", 
  edad: 12, 
  comeLasagna: true,
  amigos: ["Odie", "Jon"],
  img: "https://media.historiahoy.com.ar/adjuntos/231/imagenes/000/033/0000033260.jpg"
}
```

- Crea el componente Gato.js en donde mostraremos los datos de Garfield. 
- En primer lugar, pasa todo el objeto como una prop a Gato.js. Logra que se vean los datos y la imagen.  
- En segundo lugar, pasa cada una de las propiedades del objeto como props diferentes a Gato.js

¿Que estrategia te resulta mas comoda? ¿Por que pensas que podriamos preferir una u otra?



## Usando arrays 

Borrá todo el codigo anterior si sentis que va a confundirte.

*1) Trabajando con arrays en JSX*
- Declará el array `gatitos` en App.js con los siguientes valores:


```js
const gatitos = [
  {
    nombre: "Michifuz", 
    color: "negro",
    id: 1
  },
  {
    nombre: "Cocó", 
    color: "blanco",
    id: 2
  },
  {
    nombre: "Garfield"
    color: "naranja",
    id: 3
  },
]
```

- Comenzá por recorrer el array con un map. Por cada gato del array, queremos mostrar en App.js un `h3` con el nombre del gato. 

*2) Haciendo map de componentes*
- En lugar de retornar un `h3` en el map, ahora vamos a retornar el componente Tarjeta
- Por cada gato, tarjeta debe recibir la prop `nombre` y `color` y mostrarlos. 

*3) El atributo key*
- Nota que en la consola del navegador tenes un `warning` que te indica que estas haciendo un map sin el atributo `key`. 
- Agrega el atributo en el lugar correcto dentro de tu map. 

*4) Usando renderizado condicional*
- Declará en App.js una variable llamada `mostrarGatitos` que tenga como valor `true`. 
- Usando cualquier tecnica de renderizado condicional, logra que el map de gatitos se muestre solo si mostrarGatitos es `true`. Probá cambiarla a `false` para comprobar que tu código funciona. 

*5) Usando eventos en JSX y el estado*
- En App.js hagamos un `<button>` "Ocultar gatitos". 
- Al hacer click en el boton, queremos que los gatitos se oculten. Pensá qué cambios debemos hacer en el código para que esto funcione, y agregalos.  

*6) Continuacion eventos en JSX y estado*
- En Tarjeta.js hagamos un `<button>` que diga "Ocultar color del gatito"
- Al hacer click en el boton, queremos que se oculte el color del gato de esa tarjeta, y no de ninguna de las demas. 



