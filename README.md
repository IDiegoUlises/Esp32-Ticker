# Esp32 Ticker
### Codigo
```c++
#include <Ticker.h>

//Se crea un objeto, para agregar mas debe crear otro objeto de tipo Ticker
Ticker ticker;

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
  ticker.attach(segundos, parpadear);
}

void loop() 
{
  //Esta Vacio
}
```
### Funcionamiento
![](https://github.com/IDiegoUlises/Esp32-Ticker/blob/main/Imagen/esp32-ticker.gif)
* Cada un segundo realiza las instrucciones que estan dentro de la funcion
