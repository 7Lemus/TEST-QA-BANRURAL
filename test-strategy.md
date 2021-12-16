Depuración del código:
Al momento de definir el numero random está definido para 10 números, lo cual esta incorrecto porque se debe declarar para 100 números. 
Solución: let randomNumber = Math.floor(Math.random() * 100) + 1;

Al momento de la definición de los intentos ya que solo está declarado para 5 y el cual debe dar la opción de 10 posibles intentos. 
Solución: cambiar la definición a 10 a la siguiente variable const ATTEMPS = 10;

En el campo en donde se ingresan los datos numéricos permite ingresar lo que son datos alfanuméricos y decimales. 
Solución:  cambio de la definición de la variable input en el campo para que solo admita datos numéricos. 

En la condiciones deben ser arreglados tanto el numero que se ingresa y el mensaje enviado como en el color en el que se presenta el mensaje if (userGuess === randomNumber) { lastResult.textContent = "Felicitaciones! adivinaste el número!"; lastResult.style.backgroundColor = "green";
El mensaje que muestra al momento de terminar el numero de intentos estaba equivocado por lo que se corrige y se le asigna el color correspondiente. else if (guessCount === ATTEMPS) { lastResult.textContent = "!!!Perdistes!!!"; lowOrHi.textContent = ""; setGameOver();
