# ParcialDomiciliarioSPD
![ArduinoTinkercad](https://github.com/BrendaCandy/ParcialDomiciliarioSPD/assets/138243185/3912db3a-098a-4a23-aabd-681c622abdc3)
# Integrantes
- Brenda Candy
- Luciana Radimak
- Lautaro Chirino Chiesa
- Thiago Bongioanni
- Nicolas Azucena
# Proyecto: Contadores con display de 7 segmentos
![ARDUINO](https://github.com/BrendaCandy/ParcialDomiciliarioSPD/assets/138243185/bd94c607-b118-4b70-87ee-5a6f6a985105)
# Descripcion 
Contador de numeros enteros positivos y numeros primos con display de siete
segmentos.
Dada una temperatura entre 60° y 90°C, se enciende el motor. El cual habilita la visualizacion
de los displays y sus respectivos contadores. Para cambiar de tipo de contador, presionar el switch.
# Funcion Principal
Con esta funcion controlamos el estado del motor. Todas las demas operaciones dependen de que el motor este encendido.
- FUNCIONAMIENTO:
Dada una temperatura entre 60°(TEMPERATURAMINIMA) y 90°C(TEMPERATURAMAXIMA), el motor va a encenderse. Caso contrario
el motor se mantiene apagado.
~~~ C (lenguaje en el que esta escrito)
bool controlarMotor(int lecturaSensor)
{
  bool estadoDelMotor;
  temperatura = map(lecturaSensor, 20, 358, -40, 125);
  //Verificar si la temperatura está dentro del rango requerido
  if (temperatura >= TEMPERATURAMINIMA && temperatura <= TEMPERATURAMAXIMA)
  {
    digitalWrite(MOTOR, HIGH); // Enciende el motor
    estadoDelMotor = true;
  }
  else
  {
    digitalWrite(MOTOR, LOW); // Apaga el motor
    estadoDelMotor = false;
  }
  return estadoDelMotor;
}
~~~
## :robot: Link al proyecto
- [proyecto](https://www.tinkercad.com/things/8YnSWzFuR6l?sharecode=zWcwQIw50gMu8HispR4PdkUBU1Z2434c62Z-CY3R1Ws)
