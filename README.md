# Creación de Videojuegos
<p align="center">
    <img src="https://media.es.wired.com/photos/6442f341a566376ee967ba24/16:9/w_2560%2Cc_limit/GettyImages-1424828162.jpg" alt="Logo" width=1200 height=385>

  <p align="center">
    Repositorio para documentar las lecciones y desafíos desarrollados con Unity. 
  </p>
</p>


## Contenido
- [Lecciones](#lecciones)
- [Desafíos](#desafíos)
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

  * > [Aplicación Unity](https://github.com/kueb0/Videojuegos-Unity/blob/main/Prototipo1/Prototipo1-unidad1_AlvarezSandra.unitypackage)
  * > Creado el 13 de septiembre del 2024 por Sandra Karina Álvarez González.

### Lección 2 - Jugabilidad básica
<p align="center">
  <img src="https://github.com/user-attachments/assets/475c97fa-f672-4ecb-b9f3-788bfdf23c9d")
</p>

  * > Descripción:
<p align="justify">
Se presenta un entorno en el que un jugador puede moverse de izquierda a derecha y disparar alimento (una pera) para destruir a tres diferentes tipos de animales. Tanto los animales como la pera tienen un Box Collider para manejar las colisiones.

El player está controlado por el script PlayerController, que permite su movimiento horizontal usando las teclas de dirección. El jugador tiene límites definidos, por lo que no puede desplazarse más allá de ciertos puntos. Además, el jugador puede disparar una pera usando la barra espaciadora, la pera se genera en la posición actual del jugador. Los animales y la pera utilizan el script Move, que les permite avanzar a lo largo del eje Z. Cuando un animal o la pera exceden ciertos límites en el escenario, son destruidos automáticamente. 

El script DetectaColision se encarga de las colisiones. Cuando la pera colisiona con un animal, ambos objetos se destruyen, simulando que el animal ha sido eliminado. Por último, el script CreaAnimales, aplicado a un objeto vacío, genera nuevos animales aleatoriamente a intervalos regulares.
</p>

  * > [Aplicación Unity](https://github.com/kueb0/Videojuegos-Unity/blob/main/Prototipo2/Prototipo2.unitypackage)
  * > [Evidencia del proceso](https://github.com/kueb0/Videojuegos-Unity/blob/main/Prototipo2/Prototipo2_EvidenciaProceso.pdf)
  * > Creado el 25 de septiembre del 2024 por Sandra Karina Álvarez González.

### Lección 3 - First Game 2D
#### PARTE 1

<p align="center">
  <img src="https://github.com/user-attachments/assets/735440ca-7b84-4bb3-aae1-03e5ca9cdfc7")
</p>

  * > Descripción:
<p align="justify">

First Game 2D, utiliza imágenes PNG para crear un juego en 2D con sprites animados. Las imágenes fueron importadas y configuradas adecuadamente con el tipo de textura Sprite (2D and UI), el modo de sprite configurado como Multiple, y el Filter Mode establecido en Point (no filter) para mantener la calidad pixelada.

Para el jugador y los enemigos, se crearon objetos vacíos (empties) a los cuales se les añadió el componente Sprite Renderer. Posteriormente, las imágenes cortadas correspondientes a los diferentes movimientos de cada personaje fueron asignadas a estos objetos vacíos, y se guardaron como animaciones.

Este proceso se repitió tanto para el jugador como para el primer enemigo, y luego se creó un segundo enemigo desde cero. De esta forma, se estableció un flujo de trabajo para crear animaciones 2D a partir de sprites, implementando movimientos y acciones visuales mediante las secuencias de imágenes.
</p> 

  * > [Aplicación Unity](https://github.com/kueb0/Videojuegos-Unity/blob/main/FirstGame2D/Parte%201/FirstGame2D_PARTE1.unitypackage)
  * > [Evidencia del proceso](https://github.com/kueb0/Videojuegos-Unity/blob/main/FirstGame2D/Parte%201/LECCI%C3%93N2_GAME2D_SandraKarinaAlvarezGonzalez.pdf)
  * > Creado el 07 de ocubre del 2024 por Sandra Karina Álvarez González.

#### PARTE 2
<p align="center">
  <img src="https://github.com/user-attachments/assets/441d5d38-4d21-4bc6-be5b-43e273a90b3b")
</p>

  * > Descripción: 
<p align="justify">
En este proyecto se añaden características físicas y de animación al player. Se implementan componentes como Box Collider 2D y Rigidbody 2D dinámico, configurando la gravedad en 0 para evitar que el personaje caiga. Además, se le asigna el tag de "Player" y una layer llamada "Blocking", mientras que la sorting layer se configura bajo el nombre "Characters". El objeto del player se convierte en un prefab, reemplazando su instancia en la jerarquía.

En cuanto a las animaciones, en la pestaña Animator, se conectan las diferentes animaciones del player con el estado Any State usando la opción Make Transition. Se añade un parámetro del tipo Int llamado AnimationState en la pestaña de Parameters. Cada animación se configura con una transición sin duración (0) y una condición basada en el valor del parámetro AnimationState.

El personaje puede caminar en cuatro direcciones (norte, sur, este y oeste), además de tener una posición inicial en estado de idle (sin movimiento). El script MovementController controla el movimiento y las animaciones del jugador. Se define una velocidad de movimiento y se utiliza un Rigidbody2D para aplicar la física. El script también gestiona un componente Animator que permite cambiar entre los estados de animación dependiendo de la dirección en la que se mueva el jugador.
</p> 



  * > [Aplicación Unity](https://github.com/kueb0/Videojuegos-Unity/blob/main/FirstGame2D/Parte%202/FirstGame2D_Parte2.unitypackage)
  * > [Evidencia del proceso](https://github.com/kueb0/Videojuegos-Unity/blob/main/FirstGame2D/Parte%202/LECCI%C3%93N2_GAME2D_PARTE2_SandraKarinaAlvarezGonzalez.pdf)
  * > Creado el 09 de octubre del 2024 por Sandra Karina Álvarez González.

#### PARTE 3
<p align="center">
  <img src="")
</p>

  * > Descripción: 
<p align="justify">
Se creó un entorno más detallado utilizando herramientas como Tile Palette y Cinemachine. Se implementaron múltiples Tilemaps, específicamente una capa de suelo y otra de obstáculos, que incluyen elementos como árboles y piedras. Para controlar la superposición de objetos y evitar espacios en blanco, se usaron Sorting Layers, asignando la capa correspondiente a cada Tilemap. Además, se añadieron Tilemap Colliders 2D combinados con Composite Colliders para definir las zonas inaccesibles.
    
Se utilizó Cinemachine para seguir al jugador de forma fluida, añadiendo un collider para evitar que la cámara lo siga más allá de los límites del entorno. La estabilidad de la cámara se optimizó mediante la aplicación de materiales y un script personalizado que alinea los movimientos de la cámara con una cuadrícula basada en píxeles, evitando movimientos inconsistentes. El Movement Controller mantiene la lógica de desplazamiento en cuatro direcciones, permitiendo al jugador explorar el entorno diseñado.
</p> 

  * > [Aplicación Unity](https://github.com/kueb0/Videojuegos-Unity/blob/main/FirstGame2D/Parte%203/FirstGame2D_PARTE3.unitypackage)
  * > [Evidencia del proceso](https://github.com/kueb0/Videojuegos-Unity/blob/main/FirstGame2D/Parte%203/FirstGame2D_PARTE3.pdf)
  * > Creado el 16 de octubre del 2024 por Sandra Karina Álvarez González. 

#### PARTE 4
<p align="center">
  <img src="")
</p>
  * > Descripción: 
<p align="justify">

</p> 
  * > [Aplicación Unity](https://github.com/kueb0/Videojuegos-Unity/blob/main/FirstGame2D/Parte%203/FirstGame2D_PARTE3.unitypackage)
  * > [Evidencia del proceso](https://github.com/kueb0/Videojuegos-Unity/blob/main/FirstGame2D/Parte%203/FirstGame2D_PARTE3.pdf)
  * > Creado el 13 de septiembre del 2024 por Sandra Karina Álvarez González. 

#### PARTE 5
<p align="center">
  <img src="")
</p>
  * > Descripción: 
<p align="justify">

</p> 
  * > [Aplicación Unity]()
  * > [Evidencia del proceso]()
  * > Creado el 13 de septiembre por Sandra Karina Álvarez González.

<!-- ### Lección 4 - Mecánicas de jugabilidad 
<p align="center">
  <img src="")
</p>
  * > Descripción: 
<p align="justify">

</p> 
  * > [Aplicación Unity]()
  * > [Evidencia del proceso]()
  * > Creado el 13 de septiembre por Sandra Karina Álvarez González.

### Lección 5 - Interfaz de usuario
<p align="center">
  <img src="")
</p>
  * > Descripción: 
<p align="justify">

</p> 
  * > [Aplicación Unity]()
  * > [Evidencia del proceso]()
  * > Creado el 13 de septiembre por Sandra Karina Álvarez González. -->


## Autora
Sandra Karina Álvarez González / Developer [kueb0](http://github.com/kueb0) 

