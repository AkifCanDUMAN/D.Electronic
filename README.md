# D.Electronic
Final Project

# Members
Akif Can DUMAN COM20-B

Furkan AY COM20-B

## Project Smart Bin

# What we did and the events we experienced in the project:

We started the project by buying a garbage box and then we used the microcontroller, motion sensor, motor and a few cables we needed from the lab at the university. We wrote the microcontroller codes beforehand and then transferred this code to the microcontroller. Then we combined all the materials. After combining the materials, we made holes on the garbage box so that the sensor would not look bad from the outside, and we passed the sensor there, only the sensing parts of the sensor were visible on the outside and this problem disappeared. Finally, we placed all the materials inside the cover of the baton box with the help of silicone, and in this way, the smart baton box became functional.

# The materials we use:

-Garbage

-HC-SR04 Ultrasonic Distance Sensor

-Mini Servomotor

-Arduino Uno R3

-Enough jumper wires

-Umbrella wire or about 20 cm of flat wire (to be mounted on the servo motor and will allow the lid to open and close as it rotates)

# Setup() Function

The Setup() function is the part of the code with the .ino extension uploaded to the Arduino that is first executed when the Arduino is started or restarted. The Setup() function prepares the environment for startup and is not run again until a reboot after completing its task.

# Loop() Function

The loop() function is run after the setup function is run and acts as an endless loop. By using this infinite loop feature of the loop function, it is ensured that our operations that will be repeated continuously are carried out. For example; It can be used in repetitive operations such as turning a LED on and off at 1 second intervals, as in the example of Blink, which is perhaps the most basic example of Arduino.

# Smart bin Arduino Circuit

![Image](https://user-images.githubusercontent.com/73740265/171911407-a5c0bd4b-e733-45d0-92f1-de6c1e90f8e3.jpg)

# Smart bin Code;

#include <Servo.h>

#define echo 6
#define trig 7

Servo motor;

void setup() {
  pinMode(echo,INPUT);
  pinMode(trig,OUTPUT);
  motor.attach(9);
  Serial.begin(9600);

}

void loop() {
  digitalWrite(trig,LOW);
  delayMicroseconds(2);
  
  digitalWrite(trig,HIGH);
  delayMicroseconds(2);
  digitalWrite(trig,LOW);
float zaman = pulseIn(echo,HIGH);
  float cm = zaman / 58.2;
  Serial.println(cm);

  if(cm < 10){
    motor.write(90);
    delay(4000);
    motor.write(0);
  }
}

# Video Link;

https://youtube.com/shorts/YsTRrHtIU_E?feature=share

## Google Drive Link;

https://drive.google.com/drive/u/1/folders/1rB4S-1BwglSdHFdP1yWh_TMG9WOH9cuu


