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
de los displays y sus respectivos contadores. Otra manera por la que podemos acceder a los contadores es mediante la fotoresistencia, que se evaluara
una determinada iluminacion. Para cambiar de tipo de contador, utilizamos el switch.
# Esquema del circuito 
[ESQUEMA CIRCUITO.pdf](https://github.com/BrendaCandy/ParcialDomiciliarioSPD/files/12972110/ESQUEMA.CIRCUITO.pdf)
# Funcion Principal: Motor de CC
Con esta funcion controlamos el estado del motor. Todas las demas operaciones dependen de que el motor este encendido, o bien que halla una buena iluminacion(fotoresistencia).
- FUNCIONAMIENTO:
Dada una temperatura entre 60°(TEMPERATURAMINIMA) y 90°C(TEMPERATURAMAXIMA), el motor va a encenderse. Caso contrario
el motor se mantiene apagado.
~~~ C (lenguaje en el que esta escrito)
bool controlarMotor(int lecturaSensor)
{
  bool estadoDelMotor;//Definimos la variable que vamos a retornar
  temperatura = map(lecturaSensor, 20, 358, -40, 125);//Establecemos los valores de tempertura que vamos a utilizar
  if (temperatura >= TEMPERATURAMINIMA && temperatura <= TEMPERATURAMAXIMA)//Verificar si la temperatura está dentro del rango requerido
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
# Sensor de Temperatura
Es un componente que fue diseñado para medir la temperatura y nos dará valores analógicos de ella. 
La utilizamos para detectar el rango de grados validos para el correcto funcionamiento de los contadores.
# Fotoresistencia
Es un componente cuya resistencia eléctrica varía en función de la intensidad de la luz. 
En condiciones de oscuridad, la fotoresistencia tiene una resistencia alta, lo que significa que permite pasar muy poca corriente eléctrica. A medida que la luz incide sobre la fotoresistencia, la resistencia disminuye, permitiendo que pase más corriente eléctrica a través de ella. 
En este proyecto la aplicamos para que el correcto funcionamiento de los contadores se de cuando halla buena iluminacion. En caso de que nos de la iluminacion necesaria permitira 
la visualizacion de los contadores.
## :robot: Link al proyecto
- [proyecto](https://www.tinkercad.com/things/8YnSWzFuR6l?sharecode=zWcwQIw50gMu8HispR4PdkUBU1Z2434c62Z-CY3R1Ws)
