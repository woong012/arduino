# LED 예제 1
## LED 깜빡이기
![led].(./images/led02.png).

## Source code

```c
#define LED1 5
#define LED2 9
#define LED3 7

void setup() {

pinMode(LED1, OUTPUT); pinMode(LED2, OUTPUT);  pinMode(LED3, OUTPUT);  
}

void loop() {
  digitalWrite(LED1, HIGH);
  digitalWrite(LED2, HIGH);
  digitalWrite(LED3, HIGH);
  delay(1000);
  digitalWrite(LED1, LOW);
  digitalWrite(LED2, LOW);
  digitalWrite(LED3, LOW);
 delay(1000);  
} 
```
