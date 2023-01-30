<!--hide-->
# Traffic Light with React
<!--endhide-->

A veces queremos crear componentes que mantengan un estado interno en el tiempo, imaginemos un semáforo que cambia de color cada 3 segundos, para implementar eso tendríamos una variable `color` que puede tener como valor cualquier color entre [amarillo, rojo, verde]

```js
let color = "blue";
```

Pero solo con tener esa variable no basta, necesitamos que cada vez que la variable color cambie también lo haga el código HTML del semáforo, para eso utilizamos el hook de react llamado `useState`:

```js
//        ↓ variable name             ↓ default value
const [ color, setColor] = useState("red");
//               ⬆ function to change the color
```
De ahora en adelante, cada vez que utilicemos la function setColor para cambiar el valor de la variable color, el HTML del componente también se actualizará para reflejar el cambio.

> Puedes [leer más sobre hooks aquí](https://content.breatheco.de/lesson/react-hooks-explained).

## 🌱  Cómo iniciar este proyecto

No clones este repositorio. El primer paso para comenzar a codificar es clonar el [react.js boilerplate](https://github.com/4GeeksAcademy/react-hello) en tu computador local o con Gitpod.

a) Si usas Gitpod puedes clonar el boilerplate [clic aquí](https://gitpod.io#https://github.com/4GeeksAcademy/react-hello).

b) Si trabajas localmente, escribe el siguiente comando en tu terminal: `git clone https://github.com/4GeeksAcademy/react-hello`.

💡 Importante: Recuerda actualizar el `remote` del proyecto con el de tu repositorio usando `git remote set-url origin <your new url>`, y luego guardar tu código en tu nuevo repositorio usando `add`, `commit` y `push`.

# 📝 Instrucciones

Simulemos un semáforo [como este](https://github.com/breatheco-de/exercise-traffic-light-react/blob/master/preview.gif).

La luz tiene que brillar cuando se hace clic.

- Todo el propósito del componente es mostrar un semáforo con luces de lectura, amarillas y verdes.
- Cuando se hace clic (se selecciona) alguna luz, ésta debe brillar, pero las otras luces deben dejar de brillar.
- El componente debe tener un estado que almacene el color actual que debe brillar, por eso debes usar el hook `useState` de la siguiente manera:
```js
const [ color, setColor] = useState("red");
```
- Utiliza ReactDOM.render para procesar el componente en el DOM de esta manera
```js
ReactDOM.render(<TrafficLight />, document.querySelector('#app'));
```
## 🔥 Bonus

+ 2 Crea un botón que, al hacer clic en él, alterna el color seleccionado del semáforo entre rojo, verde y amarillo.

+ 10 Tener un botón que al hacer clic en él anuncie un color extra "púrpura" al semáforo.