
[![Link to YouTube Video](https://github.com/falconphysics/electronics/blob/main/chap2/Screen%20Shot%202023-01-31%20at%208.13.09%20AM.png)](https://www.youtube.com/watch?v=ap8lc19qhoo&embeds_euri=http%3A%2F%2Fwww.highschoolmaker.com%2F&feature=emb_imp_woyt)


```
/*
  Blink
  Turns on an LED on for one second, then off for one second, repeatedly.
 
  This example code is in the public domain.
 */
 
// Pin 13 has an LED connected on most Arduino boards.
// give it a name:
int led = 13;

// the setup routine runs once when you press reset:
void setup() {                
  // initialize the digital pin as an output.
  pinMode(led, OUTPUT);     
}

// the loop routine runs over and over again forever:
void loop() {
  digitalWrite(led, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(1000);               // wait for a second
  digitalWrite(led, LOW);    // turn the LED off by making the voltage LOW
  delay(1000);               // wait for a second
}
```
