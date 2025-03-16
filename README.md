**Informacion sobre el juego:**

**Funciones de las principales clases usadas**:

*   **Program:** Esta clase es el punto de entrada del programa y contiene el método `Main` que inicia el juego y controla el flujo principal. Define el tamaño del tablero y la cantidad de trampas, obstáculos y objetos. Además, permite a los jugadores seleccionar sus fichas al inicio del juego y controla el movimiento de las fichas en el tablero, aplicando efectos de trampas u objetos.
*   **GenerarTablero:** Esta clase genera el tablero del juego, colocando caminos, obstáculos, trampas y objetos de manera aleatoria. Utiliza un enum para definir los tipos de casillas (Camino, Obstaculo, Trampa, Objeto). Los métodos de esta clase crean el tablero, inicializan los bordes como obstáculos, generan caminos conectados y distribuyen obstáculos, trampas y objetos de manera aleatoria.
*   **Ficha:** Esta clase representa a las fichas que controlan los jugadores, cada una con atributos y habilidades únicas. Los atributos incluyen nombre, habilidad, puntos de vida, cooldown, y la posición actual en el tablero. Los métodos permiten mover la ficha, usar su habilidad especial, perder puntos al caer en una trampa y recoger objetos para aumentar sus puntos de vida.
*   **Trampa:** Esta clase representa las trampas en el tablero y sus efectos sobre las fichas. Utiliza un enum para definir los tipos de trampas (Disminuyen cierta cantidad de "vida",aumentan el cooldown..). Los métodos aplican el efecto de la trampa a la ficha que la activa y verifican si una ficha ha caído en una trampa para aplicar el efecto correspondiente.
*   **TableroDrawer:** Esta clase se encarga de dibujar el tablero en la consola utilizando la librería Spectre.Console. El método `DibujarTablero` muestra el tablero en la consola, utilizando colores para representar los diferentes tipos de casillas y las fichas.

El juego termina cuando una un jugador reune de primero  3 "objetos amarrillos",ganando automaticamente la partida,pero si durante el juego un jugador pierde todos sus puntos,pues gana el otro jugador.

**Como jugar**:
* Al "correr" el juego en la consola,el jugador1 escoge entre las 5 fichas,y luego el jugador2 escoge entre las 4 restantes.Los jugadores escogen las fichas en base a la informacion que se muestra sobre la habilidad,el color..
* Durante el turno mietras el cooldown se muetre activo,no puede usar las habilidades.Usar una habilidad no influye en el turno,el turno solo cambia cuando el jugador presiona "mover ficha".
* Las fichas pueden moverse hasta 2 casillas por tunrno,al presionar la tecla "Enter" en "Mover Ficha",puede usar las teclas de direccion para moverse a dos casillas que desee siempre y cuando no sean obstaculos.

  **Habilidades**:
* Teletransportación Aleatoria: Teletransporta la ficha a una casilla aleatoria del tablero que sea un camino libre. Cooldown.
* Inmunidad Temporal: Otorga inmunidad a la ficha durante 3 turnos,lo que permite no perder vida si cae en una casilla trampa.
* Paso Fantasma: Permite a la ficha atravesar obstáculos durante 3 turnos. Cooldown.
* Curación Rápida: Aumenta la "vida" de la ficha al maximo.
* Avance Triple: Permite a la ficha realizar 1 movimiento mas de los que ya puede. 
