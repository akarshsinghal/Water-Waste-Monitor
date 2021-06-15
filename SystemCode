//Name: Akarsh
//Date: 2020/01/11
//Purpose: create program to run final project
//Coded in C++

#include <LiquidCrystal.h> //Load Liquid Crystal Library
LiquidCrystal LCD(11,10,9,2,3,4,5);  //Create Liquid Crystal Object called LCD

#define trigPin 13 //Sensor Echo pin connected to Arduino pin 13
#define echoPin 12 //Sensor Trip pin connected to Arduino pin 12
int soundSensor=7; // Digital Pin 7 on the Arduino is where the "DO" of the Sound Sensor is connected.
int sensorValue = analogRead(A0); //This is where the "AO" of the Sound Sensor is connected.
int threshold = 1;
int waterUseAllowedDuration = 15000;

//Simple program just for testing the HC-SR04 Ultrasonic Sensor with LCD dispaly 
//URL:

void setup() 
{ 
  Serial.begin(9600);
  pinMode(trigPin, OUTPUT);
  pinMode(echoPin, INPUT);
  
  LCD.begin(16,2); //Tell Arduino to start your 16 column 2 row LCD
  LCD.setCursor(0,0);  //Set LCD cursor to upper left corner, column 0, row 0
  LCD.print("Water Waste:");  //Print Message on First Row

  pinMode(soundSensor,INPUT);
  pinMode(sensorValue, OUTPUT);
}

void loop() {
  int sensorValue=analogRead(sensorValue);
  Serial.println(sensorValue);
  Serial.println("analog");
  int SensorData=digitalRead(soundSensor);
  Serial.println(SensorData);
  Serial.println("digital");
  
  Serial.print(sensorValue);
  LCD.setCursor(0,1);  //Set cursor to first column of second row
  LCD.print("                "); //Print blanks to clear the row
  LCD.setCursor(0,1);   //Set Cursor again to first column of second row
  LCD.print("Water Off");  //Print your units.
  delay(3000);
    
  if(SensorData=1){
    if(sensorValue>621){
    LCD.setCursor(0,1);  //Set cursor to first column of second row
    LCD.print("                "); //Print blanks to clear the row
    LCD.setCursor(0,1);   //Set Cursor again to first column of second row
    LCD.print("Water On");  //Print your units.
    delay(waterUseAllowedDuration);
    LCD.setCursor(0,1);  //Set cursor to first column of second row
    LCD.print("                "); //Print blanks to clear the row
    LCD.setCursor(0,1);   //Set Cursor again to first column of second row
    LCD.print("Turn Off Water");  //Print your units.
    delay(7000);
    }
  }

  //For the ultrasonic sensor to work
  long duration, distance;
  digitalWrite(trigPin, LOW);
  delayMicroseconds(2);
  digitalWrite(trigPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(trigPin, LOW);
  duration = pulseIn(echoPin, HIGH);
  distance = (duration/2) / 29.1;

  if(distance<15){
  LCD.setCursor(0,1);  //Set cursor to first column of second row
  LCD.print("                "); //Print blanks to clear the row
  LCD.setCursor(0,1);   //Set Cursor again to first column of second row
  //LCD.print(distance); //Print measured distance
  LCD.print("Don't Harm");  //Print your units.
  delay(2500); //pause to let things settle
}
}
