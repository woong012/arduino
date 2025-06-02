
![LED03](https://github.com/user-attachments/assets/6e8d7879-a2e3-41a1-ae85-f04015f6fc94)



```c
#define BUTTON 5
#define LED_BLUE 9
#define LED_RED 7
#define DELAY_TIME 80

int state = 0;

void setup() {

  Serial.begin(9600);
  pinMode(BUTTON, INPUT_PULLUP);
  pinMode(LED_BLUE, OUTPUT);
  pinMode(LED_RED, OUTPUT);
  
}

void loop() {
  int buttonValue=!digitalRead(BUTTON);
 
  if(buttonValue == 1){
    state = !state;
    delay(500);
  }
  
  if(state == 0){
    digitalWrite(LED_BLUE, HIGH);
    digitalWrite(LED_RED, LOW);
      delay(DELAY_TIME);
       digitalWrite(LED_RED, HIGH);
     digitalWrite(LED_BLUE, LOW);
    delay(DELAY_TIME);
  }
  
  else if (state == 1){
      digitalWrite(LED_BLUE, LOW);  
     digitalWrite(LED_RED, LOW);
    
  }
} 
  
```
