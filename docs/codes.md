
=== "Exemple - LED clignotante"
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
=== "Exemple - Clignotement controlé par un potentiomètre"

    ``` c
    int capteurPin = A0;   // select the input pin for the potentiometer
    int ledPin = 13;      // select the pin for the LED
    int capteurVal = 0;
    
    void setup() {
      pinMode(ledPin, OUTPUT);
    }

    void loop() {
      capteurVal = analogRead(capteurPin);
      cl_LED(capteurVal);
    }

    void cl_LED(int attente)
    {
      digitalWrite(ledPin, HIGH);
      delay(attente);
      digitalWrite(ledPin, LOW);
      delay(attente);
    }
    ```

``` c title="LED_bouton"
const int LED_PIN = 12;
const int BUTTON_PIN = 2;

bool ledState = false;
bool lastButtonState = LOW;

void setup() {
  pinMode(LED_PIN, OUTPUT);
  pinMode(BUTTON_PIN, INPUT);

  digitalWrite(LED_PIN, LOW);
}

void loop() {
  bool buttonState = digitalRead(BUTTON_PIN);

  
  if (lastButtonState == LOW && buttonState == HIGH) {
    ledState = !ledState;
    digitalWrite(LED_PIN, ledState);

    delay(50); 
  }

  lastButtonState = buttonState;
}
```
