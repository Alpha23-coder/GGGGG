# GGGGG
Tic Tac Toe Game
Este proyecto es un juego simple de Tic Tac Toe desarrollado con React. El código está organizado en tres componentes principales: Square, Board, y Game.

Square

Este es un componente funcional que representa una casilla del tablero. Toma dos props: value, que es el valor de la casilla ('X', 'O', o null), y onSquareClick, que es una función que se ejecuta cuando se hace clic en la casilla.

Board

Este componente es responsable de manejar la lógica del juego. Toma tres props: xIsNext, que es un booleano que indica si el siguiente jugador es 'X'; squares, que es un array de 9 elementos que representa el estado actual del tablero; y onPlay, que es una función que se ejecuta cuando un jugador realiza una jugada.

El componente contiene una función interna llamada handleClick que se ejecuta cuando el jugador hace clic en una casilla. Esta función verifica si el juego ha terminado o si la casilla ya ha sido seleccionada, y si no es así, actualiza el estado del tablero con la nueva jugada y llama a la función onPlay para actualizar el estado del juego.

Game

Este componente es el componente principal del juego. Es el componente que se representa en la pantalla y contiene todo el estado y la lógica necesaria para manejar el juego.

El componente contiene dos estados: history, que es un array que mantiene un registro de los estados anteriores del tablero, y currentMove, que es un número que indica el índice del estado actual en el array history.

El componente también contiene dos funciones internas: handlePlay, que se ejecuta cuando se realiza una jugada, actualiza el estado de history y currentMove para registrar la nueva jugada y jumpTo, que se ejecuta cuando se hace clic en uno de los movimientos anteriores y actualiza el estado de currentMove para mostrar el tablero correspondiente.

Por último, el componente renderiza el tablero actual y una lista de movimientos anteriores con botones para volver atrás.

calculateWinner

Esta es una función pura que toma un array squares y verifica si hay un ganador. La función utiliza un array lines que contiene todas las combinaciones posibles de casillas ganadoras y las verifica comparando el valor de las casillas correspondientes en el array squares. Si hay un ganador, la función devuelve el valor del ganador ('X' o 'O'). Si no hay ganador, devuelve null.
