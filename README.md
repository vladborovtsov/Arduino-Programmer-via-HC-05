# Arduino-Programmer-via-HC-05

## Step 1 
First of all, you need to configure your HC-05 module. Sketch is below. 

```c++
void setup() {

  Serial.begin(38400);
  delay(500);

  Serial.println("AT+NAME=ArduinoNano-Flasher");
  delay(500);

  /*Use this baudrate if using for Arduino Uno, Bluino and Mega2560*/
  //Serial.println("AT+UART=115200,0,0");

  /*Use this baudrate if using for Arduino Nano, Leonardo, Micro, Pro Mini 3V3/5V and Duemilanove */
  Serial.println("AT+UART=57600,0,0");
  delay(500);

  Serial.println("AT+POLAR=1,0");
  delay(500);

  //Set the password
  Serial.println("AT+PSWD=0000");
  delay(500); 
}

void loop() {

} 
```

copy/paste it and flash it onto your arduino. Sketch file is also available in the repo. 


## Step 2

Hardware: 
- Capacitor 1uf/16v 
- Arduino Nano
- Bluetooth HC-05 module
- Mini breadboard
- Jumper wires
- Resistor 100 ohm
