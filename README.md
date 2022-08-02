# Sencor-Analog-and-Digital
Making an electronic circuit and programming it for a sensor Analog and Digital


1- Login to tinkercad

2-Making an electronic circuit and programming it for a sensor Analog and Digital

3-Writing code

```
#include <LiquidCrystal.h>                 

LiquidCrystal lcd(12, 11, 5, 4, 3, 2); //declaring pin uses
int echoPin = 6;
int trigPin = 7;
long duration;
int distance;

void setup()
{
  lcd.begin(16, 2);  
  pinMode(trigPin,OUTPUT);
  pinMode(echoPin, INPUT);
}

void loop()
{
  digitalWrite(trigPin, LOW);  
  delayMicroseconds(2);          
  digitalWrite(trigPin, HIGH); 
  delayMicroseconds(10);          
  digitalWrite(trigPin,LOW); 
  duration = pulseIn(echoPin,HIGH);
  distance = duration * 0.0342/2;
  lcd.setCursor(0, 0);
  lcd.print("Saeed");
  lcd.print(distance);
  lcd.print("cm");
  delay(10);
}

```
