# 3.3 – SEQUENCE LEDS WITH FOR
![Arduino with 5 LEDs](Arduino-5LEDs.png)

In this lesson you’ll be learning about the “for” command. The “for” command is the next iteration of our repetition lessons. It will keep repeating what ever is in the brackets as long as the “condition” is true. You’ll need to set up your circuit so that you have an LED (with appropriate resistors) plugged into pins digital pins 9-13. Upload the following to your Adruino.
```
void setup() {
    
}

void loop() {
    for (int ledPin = 13; ledPin >= 9; ledPin = ledPin -1)
    {
        pinMode(ledPin, OUTPUT);
        // Turn on your LED
        // Wait
        // Turn off your LED
    }   
}
```
Again, the results should look very familiar. The for function above will light up each pin starting at 13 and counting down to 9 in sequence, turning it off before it lights the next one. You’ll notice int ledPin=13 in the for statement. In this case ledPin only has meaning inside the for loop, this variable is not declared at the beginning of the program.

The basic structure of “for” is as follows:
```
// for(initialization; condition; increment)
```
