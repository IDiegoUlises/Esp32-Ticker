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
  estado = !estado;
  digitalWrite(led, estado);
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
