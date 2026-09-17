

``` c
// The setup function that runs one time at startup
void setup() {  
  pinMode(13, OUTPUT);     // Initialize digital pin 13 as an output.
}

// The main loop that continues forever
void loop() {
  digitalWrite(13, HIGH);  // turn the LED on (HIGH is the voltage level)
  delay(1000);             // wait for a second
  digitalWrite(13, LOW);   // turn the LED off by making the voltage LOW
  delay(1000);             // wait for a second
}
```
