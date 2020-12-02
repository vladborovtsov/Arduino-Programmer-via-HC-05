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

<img src="https://github.com/vladborovtsov/Arduino-Programmer-via-HC-05/raw/master/doc/images/step2_bb.png" height="400" />
<img src="https://github.com/vladborovtsov/Arduino-Programmer-via-HC-05/raw/master/doc/images/photo_2020-12-02_15-16-21.jpg" height="400" />
  
Time to setup our HC-05. At step 1 you have flashed arduino with sketch that will set up bluetooth module.

- Press and hold KEY button on HC-05 module
- Plug USB cable to power on arduino 
- Keep holding the button, wait about 5 seconds
- Unplug and re plug USB for reset from AT command mode

If everything went well - after replug you should be able to to discover a bluetooth device named "ArduinoNano-Flasher". Also red led will be blinking fast on HC-05 module. 



## Step 3


