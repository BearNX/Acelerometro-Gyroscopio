# Sensor Acelerómetro + Giroscopio MPU6050
Descubre el potencial de medición de movimiento con el sensor MPU6050, que combina un acelerómetro y un giroscopio en un solo chip.

## Introducción
El **MPU6050** es un sensor de 6 ejes utilizado en diversas aplicaciones como drones, robots, juegos y dispositivos portátiles. Permite medir aceleración lineal y angular en tres ejes (X, Y, Z).

## Características clave
* Rango de medición: +/- 2g a +/- 16g para aceleración y +/- 250°/s a +/- 2000°/s para giroscopio.
* Comunicación: interfaz **I2C** para la transferencia de datos.
* Baja potencia: consumo de energía optimizado para aplicaciones con restricciones de batería.
## Uso del MPU6050
1. Configuración: Inicializa el MPU6050 y establece los rangos de medición adecuados.
2. Lectura de datos: Recopila información del acelerómetro y el giroscopio a través de I2C.
3. Procesamiento: Aplica algoritmos para interpretar y filtrar los datos en bruto.
4. Aplicaciones: Control de movimiento, detección de orientación, estabilización, seguimiento de movimiento, etc.
## Ejemplo de codigo (C++)
```cpp
// Ejemplo de código para leer datos del MPU6050 utilizando la biblioteca "MPU6050" para Arduino.

#include <Wire.h>
#include <MPU6050.h>

MPU6050 mpu;

void setup() {
  Wire.begin();
  mpu.initialize();
  
  // Configuración adicional (rangos de medición, filtros, etc.)
}

void loop() {
  // Lectura de datos del acelerómetro y el giroscopio
  int16_t ax, ay, az;
  int16_t gx, gy, gz;
  mpu.getMotion6(&ax, &ay, &az, &gx, &gy, &gz);
  
  // Procesamiento y uso de los datos obtenidos
  // ...
}
```
## Video test del sensor
[![IMAGE ALT TEXT HERE](http://img.youtube.com/vi/a37xWuNJsQI/0.jpg)](http://www.youtube.com/watch?v=a37xWuNJsQI)
## Conclusiones
El **MPU6050** es un sensor versátil que proporciona datos precisos de aceleración y giroscopio en un solo paquete. Su facilidad de uso y amplio rango de aplicaciones lo hacen ideal para proyectos de control de movimiento, detección de orientación, estabilización y seguimiento de movimiento.
