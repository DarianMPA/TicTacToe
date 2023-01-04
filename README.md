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

# Tiempos de los peores casos y los mejores casos

La inteligencia artificial está solo un nivel por encima de la programación informática básica. La gente está en un nivel superior. Los desarrollos y avances recientes en IA están más estrechamente relacionados que nunca con la inteligencia humana. Sin embargo, las máquinas todavía están mucho más allá de las capacidades del cerebro humano. Los seres humanos se diferencian en nuestra capacidad para aplicar los conocimientos adquiridos a través de la lógica, el razonamiento, la comprensión, el aprendizaje y la experiencia. Inteligencia artificial Los robots no pueden procesar tanta información como los humanos. Inteligencia artificial Los robots no pueden procesar tanta información como los humanos. Dado que la IA aún se encuentra en sus primeras etapas, el futuro dependerá de cómo los humanos controlen las aplicaciones de IA para respetar los valores humanos y las medidas de seguridad. Aunque las máquinas pueden imitar el comportamiento humano hasta cierto punto, su conocimiento puede corromperse al tomar decisiones racionales como las nuestras. Las máquinas impulsadas por IA toman decisiones basadas en eventos y su relación con ellos, pero carecen de "sentido común".

Se puede concluir que entre el humano y maquina existe una respuesta a los mejores o peores casos, la cual es abismal. la computadora puede realizar analisis y acciones casi inmediatas tardando no mas de 1 seg segun la operacion que se le presente. en este caso del juego simulado la computadora es aun mas eficiente en sus tiempos de respuesta que el humano. El ser humano para dar un analisis concreto llega a tardar en promedio hasta 2 minutos en dar su respuesta mas larga.

# Estudio combinatorio del juego

El modelo que puede encontrar aquí muestra el algoritmo minimax aplicado a un árbol de juego aleatorio para un juego donde los nodos finales tienen valores entre 0 y 10. Además, el modelo proporciona una manera fácil de permitir que los árboles se representen en un manera equilibrada.

# Instrucciones para ejecutar el código en Windows y en Linux

Para compilar el programa, una opción es descargar un IDE con todas las configuraciones necesarias, como Visual Studio Code, abrir la documentación a través del IDE, verificar si el complemento de idioma está configurado, en este caso C, y compilar. Ademas existen opciones en linea para la compilacion de programas realizados en C++ como son Onlinegdb o replit. la opcion de replit permite trabajar de manera colaborativa con otros usuario para la creacion de codigo, esta el la forma mas viable para realizar codigo en C++ de forma cooperativa y rapida. Tan solo se necesita abrir un navegador e ingresar en cualquiera de las 2 opciones que tenemos disponibles para la ejecucion del codigo.
