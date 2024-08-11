1.  Ejectamos en index. html y abrimos la consola para verificar que errores encontramos en la cual unicamente nos mostraba el error en addeventListener el cual estaba escrito incorrectamente en dos eventos del juego 
manera correcta  resetButton.addEventListener('click', resetGame);

2. Verificando el codigo fuente encontramos los siguientes errores:

2.1 la sintaxis tenia un error que generaba numeros aleatorios unicamente del 0 al 10 lo cual no cumplia con la condicion. 
se reescribio de esta manera 
  let randomNumber = Math.floor(Math.random() * 100)+1;

2.2 En los intentos permitidos solo permitia agregar 5 intentos se corrigio ya que la en el requerimiento indicaba que tenia que ser 10 intentos.

2.3 Se corregio la referencia en  const lowOrHi = document.querySelector('lowOrHi'); a  const lowOrHi = document.querySelector('.lowOrHi');

2.4 No contaba con validacion para los numeros enteros por lo que se agrego 
if(!Number.isInteger(userGuess) || userGuess < 1 || userGuess> 100){
      alert("Por favor, ingresa un número entero válido entre 1 y 100.");
                guessField.value = '';
                guessField.focus();
                return;

    }

2.5 /* if(userGuess === randomNumber) user guess es una cadena y randomnumber 
    es un numero por lo que se corrigio en la condicion 
     UserGuess a  if(Number(userGuess) === randomNumber)para que pueda parahacer  comparacion 

2.6 lasResult lanzaba un mensaje incorrecto ya que cuando la respuesta erra correcta lanzaba el mensaje indicando Perdieste, el color estaba incorrecto
2.7 en esta condicion else if(guessCount === ATTEMPS) cuenta los intentos pero el mensaje estaba incorrecto, y el color no es el que estaba en los requisitos

2.8  se realizo la correccion de 
	  randomNumber = Math.floor(Math.random()) + 1; 
      ya que tenia que usar la misma logica que al incio para generar los numeros aleatorios 

