# Wallet_Arduino
Wearables
/* 
Expressive Wearables 
Stephen Low
GDES-3015-001 Wearable Computing
OCAD University 
Created on February 16, 2017 
Based on: 
Button, DojoDave https://www.arduino.cc/en/Tutorial/Button
An easy way to make noise with Arduino using tone, N.A., https://programmingelectronics.com/an-easy-way-to-make-noise-with-arduino-using-tone/ & https://www.youtube.com/watch?v=1_LMAgO14z0
Tone, Arduino, https://www.arduino.cc/en/Reference/Tone
*/

// set pin numbers:
const int buttonPin = 2;     // the number of the switch pin
int Buzzer1 = 9;

// variables will change:
int buttonState = 0;         // variable for reading the pushbutton status

void setup() {
  // setting up the piezo as output:
  pinMode(Buzzer1, OUTPUT);  
  // initialize the pushbutton pin as an input:
  pinMode(buttonPin, INPUT);     
}

void loop(){
  // read the state of the pushbutton value:
  Serial.begin(9600);
  buttonState = digitalRead(switchPin);
  // make the pushbutton's pin an input:
  pinMode(switchPin, INPUT);
  
  // check if the switchbutton is pressed.
  // if it is, the buttonState is HIGH:
  if (buttonState == HIGH) {     
    // play tones (pin, frequency, duration)
      tone(Buzzer1,400,200);
      delay(500);
      tone(Buzzer1,400,200);
      delay(500);
      tone(Buzzer1,450,225);
      delay(300);
      tone(Buzzer1,450,225);
      delay(500);
      tone(Buzzer1,400,200);
      delay(500);
      tone(Buzzer1,450,200);
      delay(300);
      tone(Buzzer1,600,300);
      delay(300);
      tone(Buzzer1,400,200);
      delay(500);
      tone(Buzzer1,600,300);
      delay(500);
      tone(Buzzer1,600,300);
      delay(500);
      tone(Buzzer1,800,300);
      delay(500);
      tone(Buzzer1,800,300);
      delay(500);

    // Print out in serial monitor.
      Serial.println(buttonState);

  } 
}
