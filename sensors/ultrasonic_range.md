# Ultrasonic Range Finder

![Circuit for theRange Finder](images/range_finder.png)

```
// defines pins numbers
const int trigPin = 11;
const int echoPin = 12;



void setup() {
  pinMode(trigPin, OUTPUT); // Sets the trigPin as an Output
  pinMode(echoPin, INPUT); // Sets the echoPin as an Input
  Serial.begin(9600); // Starts the serial communication
}
void loop() {
 
  Serial.print("Distance: ");
  Serial.println(readSensor());
   
}


int readSensor(){
  // defines variables
  long duration;
  int distance;
  
  // Clears the trigPin
  digitalWrite(trigPin, LOW);
  delayMicroseconds(2);
  // Sets the trigPin on HIGH state for 10 micro seconds
  digitalWrite(trigPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(trigPin, LOW);
  // Reads the echoPin, returns the sound wave travel time in microseconds
  duration = pulseIn(echoPin, HIGH);
  // Calculating the distance
  distance = duration * 0.034 / 2;
  
  return distance;
  
 }
 ```
