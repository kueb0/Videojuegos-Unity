# Creación de Videojuegos
<p align="center">
    <img src="https://media.es.wired.com/photos/6442f341a566376ee967ba24/16:9/w_2560%2Cc_limit/GettyImages-1424828162.jpg" alt="Logo" width=1200 height=385>

  <p align="center">
    Repositorio para documentar las lecciones y desafíos desarrollados con Unity. 
  </p>
</p>

## Contenido
- [Lecciones](#lecciones)
  - [Lección 1 - Control del jugador](#lección-1---control-del-jugador)
  - [Lección 2 - Jugabilidad básica](#lección-2---jugabilidad-básica)
  - [Lección 3 - First Game 2D](#lección-3---first-game-2d)
    - [Parte 1](#parte-1)
    - [Parte 2](#parte-2)
    - [Parte 3](#parte-3)
    - [Parte 4](#parte-4)
    - [Parte 5](#parte-5)
    - [Parte 6](#parte-6)
- [Desafíos](#desafíos)
  - [Desafío 1](#desafío-1)
  - [Desafío 2](#desafío-2)
  - [Desafío 3](#desafío-3)
- [Autor](#autora)

## Lecciones

### Lección 1 - Control del jugador
<p align="center">
  <img src="https://github.com/user-attachments/assets/512fd9d1-508c-4abc-aea3-8c087de974ae" alt="image">
</p>

  * > Descripción:
<p align="justify">
Este proyecto en Unity presenta una camioneta pickup roja, con un componente Rigidbody que tiene una masa de 20,000, lo que permite una simulación realista de su física. El vehículo también cuenta con un Mesh Collider.
La camioneta se controla mediante un script llamado MuevePerrona, que permite al jugador mover el vehículo hacia adelante, atrás y girar, utilizando las teclas W (adelante), S (atrás), A (izquierda), D (derecha), o las flechas del teclado. El script toma los inputs horizontales y verticales del jugador para mover el vehículo usando la función Translate para avanzar y Rotate para girar.
El escenario incluye diversos obstáculos distribuidos a lo largo de una carretera que deben ser esquivados por el jugador.
</p>

  * > [Aplicación Unity](https://github.com/kueb0/Videojuegos-Unity/blob/main/Prototipos/Prototipo1/Prototipo1-unidad1_AlvarezSandra.unitypackage)
  * > Creado el 13 de septiembre del 2024 por Sandra Karina Álvarez González.

### Lección 2 - Jugabilidad básica
<p align="center">
  <img src="https://github.com/user-attachments/assets/475c97fa-f672-4ecb-b9f3-788bfdf23c9d")
</p>

  * > Descripción:
<p align="justify">
Se presenta un entorno en el que un jugador puede moverse de izquierda a derecha y disparar alimento (una pera) para destruir a tres diferentes tipos de animales. Tanto los animales como la pera tienen un Box Collider para manejar las colisiones.
</p>
<p align="justify">
El player está controlado por el script PlayerController, que permite su movimiento horizontal usando las teclas de dirección. El jugador tiene límites definidos, por lo que no puede desplazarse más allá de ciertos puntos. Además, el jugador puede disparar una pera usando la barra espaciadora, la pera se genera en la posición actual del jugador. Los animales y la pera utilizan el script Move, que les permite avanzar a lo largo del eje Z. Cuando un animal o la pera exceden ciertos límites en el escenario, son destruidos automáticamente. 
</p>
<p align="justify">
El script DetectaColision se encarga de las colisiones. Cuando la pera colisiona con un animal, ambos objetos se destruyen, simulando que el animal ha sido eliminado. Por último, el script CreaAnimales, aplicado a un objeto vacío, genera nuevos animales aleatoriamente a intervalos regulares.
</p>

  * > [Aplicación Unity](https://github.com/kueb0/Videojuegos-Unity/blob/main/Prototipos/Prototipo2/Prototipo2.unitypackage)
  * > [Evidencia del proceso](https://github.com/kueb0/Videojuegos-Unity/blob/main/Prototipos/Prototipo2/LECCI%C3%93N2_SandraKarinaAlvarezGonzalez.pdf)
  * > Creado el 25 de septiembre del 2024 por Sandra Karina Álvarez González.

### Lección 3 - First Game 2D
#### PARTE 1

<p align="center">
  <img src="https://github.com/user-attachments/assets/735440ca-7b84-4bb3-aae1-03e5ca9cdfc7")
</p>

  * > Descripción:
<p align="justify">
First Game 2D, utiliza imágenes PNG para crear un juego en 2D con sprites animados. Las imágenes fueron importadas y configuradas adecuadamente con el tipo de textura Sprite (2D and UI), el modo de sprite configurado como Multiple, y el Filter Mode establecido en Point (no filter) para mantener la calidad pixelada.
</p> 
<p align="justify">
Para el jugador y los enemigos, se crearon objetos vacíos (empties) a los cuales se les añadió el componente Sprite Renderer. Posteriormente, las imágenes cortadas correspondientes a los diferentes movimientos de cada personaje fueron asignadas a estos objetos vacíos, y se guardaron como animaciones.
</p> 
<p align="justify">
Este proceso se repitió tanto para el jugador como para el primer enemigo, y luego se creó un segundo enemigo desde cero. De esta forma, se estableció un flujo de trabajo para crear animaciones 2D a partir de sprites, implementando movimientos y acciones visuales mediante las secuencias de imágenes.
</p> 

  * > [Aplicación Unity](https://github.com/kueb0/Videojuegos-Unity/blob/main/Prototipos/FirstGame2D/Parte%201/FirstGame2D_PARTE1.unitypackage)
  * > [Evidencia del proceso](https://github.com/kueb0/Videojuegos-Unity/blob/main/Prototipos/FirstGame2D/Parte%201/LECCI%C3%93N2_GAME2D_SandraKarinaAlvarezGonzalez.pdf)
  * > Creado el 07 de ocubre del 2024 por Sandra Karina Álvarez González.

#### PARTE 2
<p align="center">
  <img src="https://github.com/user-attachments/assets/441d5d38-4d21-4bc6-be5b-43e273a90b3b")
</p>

  * > Descripción: 
<p align="justify">
En este proyecto se añaden características físicas y de animación al player. Se implementan componentes como Box Collider 2D y Rigidbody 2D dinámico, configurando la gravedad en 0 para evitar que el personaje caiga. Además, se le asigna el tag de "Player" y una layer llamada "Blocking", mientras que la sorting layer se configura bajo el nombre "Characters". El objeto del player se convierte en un prefab, reemplazando su instancia en la jerarquía.
</p> 
<p align="justify">
En cuanto a las animaciones, en la pestaña Animator, se conectan las diferentes animaciones del player con el estado Any State usando la opción Make Transition. Se añade un parámetro del tipo Int llamado AnimationState en la pestaña de Parameters. Cada animación se configura con una transición sin duración (0) y una condición basada en el valor del parámetro AnimationState.
</p> 
<p align="justify">
El personaje puede caminar en cuatro direcciones (norte, sur, este y oeste), además de tener una posición inicial en estado de idle (sin movimiento). El script MovementController controla el movimiento y las animaciones del jugador. Se define una velocidad de movimiento y se utiliza un Rigidbody2D para aplicar la física. El script también gestiona un componente Animator que permite cambiar entre los estados de animación dependiendo de la dirección en la que se mueva el jugador.
</p> 

  * > [Aplicación Unity](https://github.com/kueb0/Videojuegos-Unity/blob/main/Prototipos/FirstGame2D/Parte%202/FirstGame2D_Parte2.unitypackage)
  * > [Evidencia del proceso](https://github.com/kueb0/Videojuegos-Unity/blob/main/Prototipos/FirstGame2D/Parte%202/LECCI%C3%93N2_GAME2D_PARTE2_SandraKarinaAlvarezGonzalez.pdf)
  * > Creado el 09 de octubre del 2024 por Sandra Karina Álvarez González.

#### PARTE 3
<p align="center">
  <img src="https://github.com/user-attachments/assets/e8205906-d809-45bb-be3c-ea85ce2d627e")
</p>

  * > Descripción: 
<p align="justify">
Se creó un entorno más detallado utilizando herramientas como Tile Palette y Cinemachine. Se implementaron múltiples Tilemaps, específicamente una capa de suelo y otra de obstáculos, que incluyen elementos como árboles y piedras. Para controlar la superposición de objetos y evitar espacios en blanco, se usaron Sorting Layers, asignando la capa correspondiente a cada Tilemap. Además, se añadieron Tilemap Colliders 2D combinados con Composite Colliders para definir las zonas inaccesibles.
</p>
<p align="justify">
Se utilizó Cinemachine para seguir al jugador de forma fluida, añadiendo un collider para evitar que la cámara lo siga más allá de los límites del entorno. La estabilidad de la cámara se optimizó mediante la aplicación de materiales y un script personalizado que alinea los movimientos de la cámara con una cuadrícula basada en píxeles, evitando movimientos inconsistentes. El Movement Controller mantiene la lógica de desplazamiento en cuatro direcciones, permitiendo al jugador explorar el entorno diseñado.
</p>


  * > [Aplicación Unity](https://github.com/kueb0/Videojuegos-Unity/blob/main/Prototipos/FirstGame2D/Parte%203/FirstGame2D_PARTE3.unitypackage)
  * > [Evidencia del proceso](https://github.com/kueb0/Videojuegos-Unity/blob/main/Prototipos/FirstGame2D/Parte%203/FirstGame2D_PARTE3.pdf)
  * > Creado el 16 de octubre del 2024 por Sandra Karina Álvarez González. 

#### PARTE 4
<p align="center">
  <img src="https://github.com/user-attachments/assets/c7f4d003-306a-4997-88e7-3d5d29890773")
</p>

  * > Descripción: 
<p align="justify">
En esta fase del desarrollo de FirstGame2D, se reordenaron los scripts en carpetas específicas: Monobehaviours y ScriptableObjects. Se añadieron los sprites de las monedas y los corazones. Las monedas se configuraron con la Sorting Layer en "objects", un collider con Is Trigger activado, el Tag "CanBePickedUp" y la capa "consumables". Para las monedas se añadió un script Consumable, donde el objeto es de tipo COIN. Los corazones se configuraron de manera similar, con el tag "CanBePickedUp", la capa "consumables", y el script Consumable asignado a un objeto del tipo HEALTH.
</p> 
<p align="justify">
El jugador se mantuvo en la capa Blocking. Se crearon nuevas capas para diferenciar entre consumables (monedas y corazones) y enemies. En los ajustes de proyecto, específicamente en Physics 2D, se deseleccionó la casilla de intersección entre las capas de consumables y enemies, para evitar conflictos de interacción. Se implementó la lógica para que, al pasar sobre una moneda, esta desaparezca y se registre la acción en la consola. Aunque todavía no se han agregado los corazones a la escena del juego, la mecánica de recolección ya está parcialmente funcional.
</p> 
<p align="justify">
En cuanto a los scripts, se añadieron varias clases nuevas. Character es una clase abstracta que representa a cualquier tipo de personaje en el juego y contiene atributos como puntos de vida actuales y máximos. El script Consumable gestiona los objetos que el jugador puede recoger. Player, que hereda de Character, maneja las colisiones con objetos recolectables y ajusta los puntos de vida cuando el jugador recoge un corazón. Finalmente, en la carpeta ScriptableObjects, se creó un script para definir los Items, permitiendo que cada objeto recolectable tenga atributos como nombre, sprite, cantidad, si es apilable, y su tipo (como moneda o corazón).
</p> 

  * > [Aplicación Unity](https://github.com/kueb0/Videojuegos-Unity/blob/main/Prototipos/FirstGame2D/Parte%204/FirstGame2D_PARTE4.unitypackage)
  * > [Evidencia del proceso](https://github.com/kueb0/Videojuegos-Unity/blob/main/Prototipos/FirstGame2D/Parte%204/FirstGame2D_PARTE4.pdf)
  * > Creado el 17 de octubre del 2024 por Sandra Karina Álvarez González. 

#### PARTE 5
<p align="center">
  <img src="https://github.com/user-attachments/assets/d51730ce-7095-446e-9936-913893f5fe2a")
</p>

  * > Descripción: 
<p align="justify">
Se implementó una barra de salud que se actualiza visualmente cuando el jugador recoge corazones y se le incrementan sus puntos de vida. Para lograrlo, se creó un canvas en la vista jerárquica del juego, el cual fue renombrado como HealthBarObject. Dentro de este objeto, se configuraron varios sprites que conforman la barra de salud, comenzando con una imagen de fondo llamada Background, que contiene a su vez un objeto con máscara llamado BarMask. Este último incluye una imagen denominada Meter, la cual representa el medidor que irá llenándose a medida que el jugador recupere salud. También se importaron fuentes personalizadas y se añadió un objeto de texto sobre el fondo de la barra, en el cual se mostrará el puntaje que va acumulando el jugador.
</p> 
<p align="justify">
Para controlar el funcionamiento de la barra de salud, se creó un script llamado HealthBar. Este script utiliza componentes de la interfaz gráfica, como Image y Text, para modificar tanto el medidor de salud como el texto mostrado, basado en los puntos de vida del jugador. En el script, se hace referencia a un jugador (character) y se inicializa la barra de salud con un valor de cero. Durante la ejecución del juego, el medidor de la barra se actualiza continuamente con base en la proporción entre los puntos de vida actuales y los máximos permitidos.
</p> 
<p align="justify">
Además, se modificó la clase Character para incluir una variable hitPoints, que almacena los puntos de vida del jugador, así como el valor máximo que puede alcanzar (maxHitPoints). La clase Player, que hereda de Character, fue actualizada para manejar la interacción del jugador con la barra de salud. Cuando el jugador recoge un objeto con la etiqueta CanBePickedUp, como un corazón, se incrementan los puntos de vida y la barra se actualiza. Si los puntos de vida se modifican, el objeto consumido desaparece de la escena.
</p> 

  * > [Aplicación Unity](https://github.com/kueb0/Videojuegos-Unity/blob/main/Prototipos/FirstGame2D/Parte%205/FirsGame2D_PARTE5.unitypackage)
  * > [Evidencia del proceso](https://github.com/kueb0/Videojuegos-Unity/blob/main/Prototipos/FirstGame2D/Parte%205/FirsGame2D_PARTE5.pdf)
  * > Creado el 19 de octubre del 2024 por Sandra Karina Álvarez González.

### PARTE 6 
<p align="center">
  <img src="https://github.com/user-attachments/assets/68e63bcb-fa5d-42d6-8b02-2457a8096796")
</p>

  * > Descripción: 

<p align="justify">
En esta parte, se añadió un enemigo al juego 2D con movimiento dinámico y capacidad de interacción con el jugador. Se configuró un prefab del enemigo con un Circle Collider 2D (radio 1, activado IsTrigger) y un Animator que alterna entre las animaciones de caminar (walk) e inactivo (idle). Al enemigo se le asignó el script Wander.cs, que permite un movimiento aleatorio o persecución del jugador según corresponda.
</p> 
<p align="justify">
El script define velocidades para deambular (0.8) y perseguir (1.4), con cambios de dirección cada 3 segundos. Cuando el enemigo detecta al jugador, lo persigue y reduce su barra de salud en 10 puntos con cada colisión. Si los puntos llegan a 0, el jugador se desactiva. Al salir del rango del jugador, el enemigo vuelve a deambular.
</p> 
<p align="justify">
Este sistema proporciona una mecánica interactiva y dinámica al enemigo, mejorando la jugabilidad y las interacciones dentro del juego.
</p> 

  * > [Aplicación Unity](https://github.com/kueb0/Videojuegos-Unity/blob/main/Prototipos/FirstGame2D/Parte%206/FirstGame2D_Parte6.unitypackage)
  * > [Evidencia del proceso](https://github.com/kueb0/Videojuegos-Unity/blob/main/Prototipos/FirstGame2D/Parte%206/FirstGame2D_PARTE6.pdf)
  * > Creado el 15 de noviembre del 2024 por Sandra Karina Álvarez González.

## Desafíos

### Desafío 1
<p align="center">
  <img src="https://github.com/user-attachments/assets/e26aa970-6992-4120-a869-a14b6c1da7c2")
</p>

  * > Descripción: 
<p align="justify">
Se abordaron los siguientes problemas en el funcionamiento del avión: avanzaba hacia atrás en lugar de adelante; era demasiado rápido; se inclinaba de manera automática; la cámara estaba frente al avión y no lo seguía adecuadamente y la hélice no giraba. Para resolver estos problemas se ajustaron algunos scripts y configuraciones en Unity.
</p> 
<p align="justify">
En cuanto a la cámara, se estableció su posición en (30, 0, 10) y su rotación en (0, -90, 0) para que siguiera al avión desde atrás, logrando una perspectiva de tercera persona. Luego, se corrigieron tres scripts que resolvieron el comportamiento del avión y de la cámara. El primero, FollowPlayerX, hace que la cámara siga al avión manteniendo un desplazamiento fijo para dar la impresión de que la cámara está siempre detrás del avión. El segundo script, PlayerControllerX, controla el movimiento del avión, obteniendo la entrada del usuario a través de las flechas de dirección. Finalmente, el tercer script, SpinPropellerX, hace girar la hélice del avión continuamente, dándole un efecto visual de movimiento constante. En cada actualización, la hélice rota en el eje forward a una velocidad predefinida.
</p> 

  * > [Aplicación Unity](https://github.com/kueb0/Videojuegos-Unity/blob/main/Desaf%C3%ADos/Challenge1/Challenge1.unitypackage)
  * > [Evidencia del proceso](https://github.com/kueb0/Videojuegos-Unity/blob/main/Desaf%C3%ADos/Challenge1/Challenge1.pdf)
  * > Creado el 23 de octubre del 2024 por Sandra Karina Álvarez González.
  
  ### Desafío 2
<p align="center">
  <img src="https://github.com/user-attachments/assets/9491c39c-594e-444c-8496-1269e5f5e290")
</p>

  * > Descripción: 
<p align="justify">
Se corrigieron los siguientes aspectos: los perros aparecían en la parte superior de la pantalla; el jugador lanzaba pelotas en lugar de perros; las pelotas se destruían antes de acercarse a los perros; nada desaparecía al salir de la escena; sólo un tipo de pelota aparecía; las pelotas se lanzaban a intervalos idénticos y el jugador podía lanzar perros sin esperar un intervalo de tiempo. Para resolver estos problemas, se reorganizaron los prefabs en los objetos correctos dentro de Unity: las pelotas se asignaron al SpawnManager y los perros al PlayerObject. Luego, se ajustó el Box Collider de los perros con Edit Collider para corregir las interacciones.  
</p> 
<p align="justify">
Posteriormente, se corrigieron tres scripts. DestroyOutOfBoundsX destruye objetos que salen de los límites de la escena: los perros son destruidos si su posición x es menor que un límite izquierdo definido y las pelotas son destruidas si su posición y es menor que un límite inferior.PlayerControllerX permite al jugador lanzar perros al presionar la barra espaciadora, pero añade un intervalo de espera de un segundo (espera = 1). Esto se logra verificando que el tiempo actual (Time.time) sea mayor que el momento de la siguiente aparición permitida, registrado en la variable siguiente. SpawnManagerX permite la aparición de pelotas desde una posición superior a la pantalla en intervalos aleatorios. En el método SpawnRandomBall, se genera un intervalo de aparición aleatorio entre 2 y 4 segundos y una posición x aleatoria dentro de los límites.
</p> 

  * > [Aplicación Unity](https://github.com/kueb0/Videojuegos-Unity/blob/main/Desaf%C3%ADos/Challenge2/Challenge2.unitypackage)
  * > [Evidencia del proceso](https://github.com/kueb0/Videojuegos-Unity/blob/main/Desaf%C3%ADos/Challenge2/Challenge2.pdf)
  * > Creado el 18 de octubre del 2024 por Sandra Karina Álvarez González. 

### Desafío 3
<p align="center">
  <img src="https://github.com/user-attachments/assets/85739461-827a-4cae-bb4b-63c083525c95")
</p>

  * > Descripción: 
<p align="justify">
En este desafío se configuró un entorno de juego utilizando un Tilemap con dos capas: suelo y objetos colisionables, empleando los tile maps del paquete Pixel Art Top Down - Basic (Obtenido de Unity Assets Store). Se añadieron dos personajes, un jugador y un enemigo, ambos con animaciones de movimiento en cuatro direcciones (norte, sur, este, oeste). Para el jugador, se implementó un script que permite controlarlo mediante las teclas de dirección. El enemigo, configurado con un script similar, responde a teclas específicas (J, K, L, Y) para simular su movimiento. Ambos scripts gestionan el movimiento físico con RigidBody2D y las transiciones de animaciones mediante Animator, asegurando fluidez y consistencia en la velocidad.
</p> 

  * > [Aplicación Unity](https://github.com/kueb0/Videojuegos-Unity/blob/main/Desaf%C3%ADos/Challenge3/Challenge3_Movimiento2D.unitypackage)
  * > [Evidencia del proceso](https://github.com/kueb0/Videojuegos-Unity/blob/main/Desaf%C3%ADos/Challenge3/Challenge3.pdf)
  * > Creado el 24 de noviembre del 2024 por Sandra Karina Álvarez González. 

<!--  ### Desafío 4
<p align="center">
  <img src="")
</p>

  * > Descripción: 
<p align="justify">

</p> 

  * > [Aplicación Unity]()
  * > [Evidencia del proceso]()
  * > Creado el 13 de octubre del 2024 por Sandra Karina Álvarez González. 

  ### Desafío 5
<p align="center">
  <img src="")
</p>

  * > Descripción: 
<p align="justify">

</p> 

  * > [Aplicación Unity]()
  * > [Evidencia del proceso]()
  * > Creado el 13 de octubre del 2024 por Sandra Karina Álvarez González.-->


## Autora
Sandra Karina Álvarez González / Developer [kueb0](http://github.com/kueb0) 

