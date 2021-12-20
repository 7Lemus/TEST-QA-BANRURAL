Descripción de las falla y correcciones aplicadas 
Número de línea 44: La funcion random estaba mal declarada ya que se estaba multiplicando por 10 y el número aleatorio correcto es hasta 100 y no se le hacia la suma de 1 para su incremento.
Falla: 		let randomNumber = Math.random() * 10;
Corrección:	let randomNumber = Math.floor(Math.random() * 100) + 1;

Número de línea 49: En la constante de tipo querySelector lowOrHi hacía falta el punto para hacer referencia a la propiedad.
Falla: 		const lowOrHi = document.querySelector('lowOrHi');
Corrección:	const lowOrHi = document.querySelector('.lowOrHi'); 

Número de línea 58:  No se indica el tipo de dato que está recibiendo la variable al momento que el usuario ingresa un número. 
Falla:		let userGuess = guessField.value;
Corrección: 	let userGuess = Number(guessField.value);

Números de línea 65 y 70: Los mensajes de alerta según el resultado obtenido no coincidían con las validaciones asignadas por lo que se modificaron para mostrar el mensaje correcto.
Fallas:		lastResult.textContent = '!!!Pérdistes!!!';
		lastResult.textContent = 'Felicitaciones! adivinaste el número!';
Correcciones: 	lastResult.textContent = 'Felicitaciones! adivinaste el número!';
		lastResult.textContent = '!!!Pérdistes!!!';

Números de líneas 66 y 75: Los colores de cada una de las alertas no coinciden con los requerimientos establecidos. 
Fallas: 		lastResult.style.backgroundColor = 'black';
		lastResult.style.backgroundColor = 'green';
Correcciones: 	lastResult.style.backgroundColor = 'green';
		lastResult.style.backgroundColor = 'black';

Número de línea 87:  la constante guessSubmit hacia una referencia fallida porque estaba mal escrita, se le coloco el nombre correcto para solucionarlo. 
Falla: 		guessSubmit.addeventListener('click', checkGuess);
Corrección:	guessSubmit.addEventListener('click', checkGuess); 

Número de línea 95: La variable resetButton hacia una referencia fallida porque estaba mal escrita, se le coloco el nombre correcto para solucionarlo. 
Falla: 		resetButton.addeventListener('click', resetGame);
Corrección: 	resetButton.addEventListener('click', resetGame);

Número de línea 114: La función random estaba mal ya no se está multiplicando por 100 y únicamente se le estaba sumando + 1.
Falla: 		randomNumber = Math.floor(Math.random()) + 1;
Corrección: 	let randomNumber = Math.floor(Math.random() * 100) + 1;

Observaciones del Testing realizado: según los requerimientos indica que el número que ingresara cada jugador debe pertenecer al conjunto de los números enteros, el cual no esta implementado en el sistema y no se pudo desarrollar alguna prueba ya permite ingresar cualquier tipo de dato y cuenta como número de intento al usuario y no muestra mensaje de alerta que solo se permiten ingresar números enteros. 


