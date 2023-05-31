# Esp32-Ticker
### Codigo no probado
```c++
#include <Ticker.h>

Ticker objeto;

boolean estado = false;

int led = 2;
int segundos = 1;

void parpadear()
{
  estado = !estado;
  digitalWrite(led, estado);
}
void setup() 
{
  pinMode(led, OUTPUT);

  objeto.attach(segundos, parpadear); //Cada 1 segundo va realizar la funcion
}

void loop() 
{
  //Vacio
}
```
