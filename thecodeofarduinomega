#include <Servo.h>

Servo servo;

uint8_t servoPin = 7;

uint8_t servoPos = 0;
uint8_t runDelay = 3;
uint8_t step = 1;

uint8_t joyYPin = A1;
uint8_t yValue = 0;

void setup() {
  initServo();
}

void loop() {
  yValue = analogRead(joyYPin);
  runServo();
}

void initServo() {
  servo.attach(servoPin);
  servo.write(0);
}


void runServo() {
  if (yValue == 0 && servoPos < 180) { servoPos += step; }
  if (yValue == 1023 && servoPos > 0) { servoPos -= step; }

  servo.write(servoPos);
  delay(runDelay);
}
