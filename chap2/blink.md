# 2.2 – BLINK
## Introduction

When you plug in a new Arduino for the first time there is a light on the board that starts to flash. The Arduino is running a program that was pre-loaded into memory. As soon as it is powered up the Arduino will run whatever program is already in it’s memory. For our first programming task we are going to change this program.
[![Link to YouTube Video](https://github.com/falconphysics/electronics/blob/main/chap2/Screen%20Shot%202023-01-31%20at%208.13.09%20AM.png)](https://www.youtube.com/watch?v=ap8lc19qhoo&embeds_euri=http%3A%2F%2Fwww.highschoolmaker.com%2F&feature=emb_imp_woyt)
## Getting Started

Arduino programs are called Sketches. The Arduino was created to help make it easier for artists to incorporate electronics into their projects. Sketch was adopted to make the whole process less intimidating.

Sketches are written in C or C++, both are popular programming languages. Believe it or not this is fairly close to plain English. Once you start getting the hang of things this will become more evident. The Arduino software converts this into a form the Arduino board will understand and be able to execute.

Copy the code below, paste into Arduino, and upload to your board.

Here’s the complete code:

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
Right now, I’m sure this doesn’t mean much to you. We will break it down a piece at a time.

## Comments

You’ll notice that there is quite a bit of grey text in the sketch. This text is completely understandable by humans, but the Arduino can’t understand it. This text is Comments. Comments are added by the programmer to explain what the various parts of the code do. It is important to include comments in your code for two very important reasons.

First, if you share your code other people will be able to understand what you did, or may even be able to learn from you. The second reason for commenting your code is so that you can remember why you did what you did. I don’t know how many times I’ve had to help a student figure out how their own code works after we get back from a long weekend or a vacation.

There are two ways for creating comments. This is an example of Block Comments:
