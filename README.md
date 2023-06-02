# Esp32-Ticker
### Codigo probado
```c++
#include <Ticker.h>

//Se crea el objeto
Ticker objeto;

//Se crea una variable booleana para cambiar el estado del led
boolean estado = false;

int led = 27; //Puerto
int segundos = 1; //Cantidad de segundos

//Funcion que se activa cada cierto tiempo
void parpadear()
{
  estado = !estado; //Cambia la variable al estado contrario
  digitalWrite(led, estado); //Enciende o apaga el led
}

void setup() 
{
  //Se declara el puerto
  pinMode(led, OUTPUT);

  //Se invoca a la funcion que se realizara cada cierto tiempo
  objeto.attach(segundos, parpadear);
}

void loop() 
{
  //Esta Vacio
}
```
