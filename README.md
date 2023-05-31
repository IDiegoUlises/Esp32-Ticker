# Esp32-Ticker
### Codigo
```c++
#include <Ticker.h>

Ticker objeto;

boolean estado = false;

int led = 2;
int segundos = 1;

void parpadear()
{
  digitalWrite(led, estado);
  estado = !estado;
}
void setup() 
{
  pinMode(led, OUTPUT);

  objeto.attach(segundos, parpadear);
}

void loop() 
{
  //Vacio
}
```
