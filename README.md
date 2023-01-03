# UNIVERSIDAD DE LAS AMÉRICAS (UDLA) ECUADOR
## POYECTO TIC TAC TOE 
# Integrantes:
Erick Rosero
, Juan Carrillo
, Gustavo Guevara
, Oscar Albuja
, Darian Proaño
# Tres en raya (Descripción general del juego):
Un juego entre dos jugadores: O y X, que se turnan para marcar espacios en un tablero de 3×3. 
El jugador gana si logra hacer una línea de tres símbolos: la línea puede ser horizontal, vertical o diagonal.}
# Construcción del problema:
El código consta de las siguientes funciones:

 1.Funcion que muestra el status actual del tablero
* void showBoard(char board[][SIDE])

 2.Funcion que muestra las instrucciones
* void showInstructions()

 3.Funcion para incializar el juego
* void initialise(char board[][SIDE])

 4.Funcion para declarar el ganador del juego
* void declareWinner(int whoseTurn)

 5.Una función que devuelve true si alguna de las filas se cruza con la jugada del mismo jugador
* bool rowCrossed(char board[][SIDE])

 6.Una función que devuelve true si alguna de las columnas se cruza con la jugada del mismo jugador
* bool columnCrossed(char board[][SIDE])

 7.Una función que devuelve true si alguna de las diagonales se cruza con la jugada del mismo jugador
* bool diagonalCrossed(char board[][SIDE])

 8.Una funcion que regresa true si eljuego se acaba caso contrario regresa false
* bool gameOver(char board[][SIDE])

 9.Funcion que calcula el mejor score
* int minimax(char board[][SIDE], int depth, bool isAI)

 10.Funcion que calcula el mejor movimiento
* int bestMove(char board[][SIDE], int moveIndex)

 11.Una funcion para jugar Tres en raya
* void playTresEnRaya(int whoseTurn)

 12.Sigue jugando hasta que el juego termine o haya un empate.
* while (gameOver(board) == false && moveIndex != SIDE * SIDE)

 13.Si el juego ha empatado
* if (gameOver(board) == false && moveIndex == SIDE * SIDE)

# El algoritmo MinMax

Más específicamente, la idea es comenzar desde su posición actual en el juego y usar un generador de movimientos legales para generar posibles posiciones sucesivas hasta alcanzar un límite de nivel determinado (desarrolle un árbol completo si es posible según lo permita el juego). jugar hasta la última posición). Luego se aplica una función de evaluación estática al último estado alcanzado, que puede juzgar si cada estado es bueno o malo y elegir la mejor posición para el jugador respectivo, retrocediendo el valor un nivel para continuar con la evaluación. Todos los niveles anteriores.

![imagen](https://user-images.githubusercontent.com/62720636/210416857-f660249b-2f5d-4836-bec2-d7a578085315.png)

## ETAPAS:

El arbol de juegos es el que da el estado inicial y los movimientos legales en el juego. Considerando un árbol de juegos, la estrategia óptima puede determinarse examinando el valor minimax de cada nodo. El valor minimax de un nodo es la utilidad (Para MAX) de estar en el estado correspondiente, asumiendo que ambos jugadores juegan óptimamente desde allí al final del juego.

![imagen](https://user-images.githubusercontent.com/62720636/210417503-47f8e711-0f85-41ce-8c95-8acf81f000ef.png)


![imagen](https://user-images.githubusercontent.com/62720636/210417536-dd835b0a-cd0c-462e-89bf-4cf2fc7de347.png)


![imagen](https://user-images.githubusercontent.com/62720636/210417670-21f2d486-a707-4f01-a8c8-530b89394aed.png)


