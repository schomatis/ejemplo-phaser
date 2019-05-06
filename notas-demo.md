# Que podemos mostrar durante la demo a los chicos?

Anotamos 3 o 4 cambios para experimentar y que tengan una idea de que se trata el juego y las posibilidades que da la programacion cuando tienen acceso al codigo.

Una tecnica sencilla es comentar/descomentar partes del codigo para ver como afecta al juego (en VS Code se puede hacer rapido con Ctrl+Shift+7). Antes de correr el ejemplo con la modificacion PENSAR que creen que deberia suceder.

## Invertir la gravedad

En la configuracion del juego (`gravity: { y: 300 }`) poner un valor negativo y ver como las cosas "flotan" hacia arriba. Por que las estrellas se "escapan" de la escena y el jugador no?

## Cambiar logica de flecha arriba

El jugador salta cuando la flecha arriba esta presionada y tiene un objeto abajo, apagar una de las dos condiciones (o las dos) y ver que pasa. (Tener cuidado de que para que funcione hay que comentar tambien el `&&` porque queda el `if` desbalanceado sino).

## Cambiar los parametros de las animaciones

Jugar con los parametros de `agregar_animacion`, mas que nada el `frameRate` (bajandolo a 2 o subiendolo a 20) para que se vea la diferencia entre la imagen que se mueve y la secuencia de frames (animacion) que da la *sensacion* de que hay movimiento, y cuando esas dos cosas se desincronizan se ve feo pero ademas es mas sencillo ver que habia dos partes por separado.

## Cambiar figuras

En la funcion `crear` cambiar las imagenes que le asignamos a cada uno, por ejemplo, en la definicion de `jugador` cambiar la imagen de `chabon` por la de `estrella`.

Donde esta esta el jugador ahora? Lo identificaron? Como pueden estar seguros que realmente es un jugador y no una estrella? (Probar usando las flechas.)

ESTO NO FUNCIONA porque se activan las animaciones despues que pisan a la imagen seteada en `agregar_sprite`.

Otra posibilidad, cambiar la imagen de la plataforma a una estrella, cambiar en una de las `plataformas.create` la imagen de `piso` por la de `estrella`. Ver como la estrella queda quieta, no cae como el resto.
