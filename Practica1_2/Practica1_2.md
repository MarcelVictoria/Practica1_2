# PRACTICA 1 
# Ejercicio Voluntario 1

Leer el valor de un convertidor A/D de entrada; sacarlo por el puerto serie y sacar el valor por otro pin D/A


## MATERIAL
- Potenciometro
- Cables
- Microcontrolador ESP32

## EXPLICACIÓN DEL CÓDIGO

Sólo necesitaremos la librería de Arduino:
```cpp 
#include <Arduino.h>
```
Empezamos definiendo el GPIO al que está connectado el potenciometro
```cpp
const int potPin = 34;
```

En el setup(), la comunicación serie entre el ordenadr y el ESP32 tendrá una velocidad de 115200 bit por segundo.

```cpp
Serial.begin(115200);
```
En el loop() usamos la función analogRead() para leer la entrada del potPin.

```cpp
potValue = analogRead(potPin);
 ``` 

Finalmente mostramos los valores leídos del potenciometro en el monitor. 

```cpp
Serial.println(potValue);
 ``` 
