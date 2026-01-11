void setup() { 
  // connect IR sensor module to Arduino pin A0
  Serial.begin(9600); // Init Serial at 9600 Baud Rate.
  Serial.println("Serial Working"); // Test to check if serial is working or not

  pinMode(5, OUTPUT);
  pinMode(6, OUTPUT);
  pinMode(9, OUTPUT);
  pinMode(10, OUTPUT);
  pinMode(7, OUTPUT);
}

void loop() {
  int sensorStatus = analogRead(A0);
  Serial.println(sensorStatus); // Print sensor value

  if (sensorStatus < 900) {
    Serial.println("fire");
    turnOnFan();
    mstop();
  } else {
    turnOffFan();
    Serial.println("no fire");
    forward();
  }
}

void forward() {
  digitalWrite(5, HIGH);
  digitalWrite(6, LOW);
  digitalWrite(9, HIGH);
  digitalWrite(10, LOW);
}

void backward() {
  digitalWrite(5, LOW);
  digitalWrite(6, HIGH);
  digitalWrite(9, HIGH);
  digitalWrite(10, LOW);
}

void mstop() {
  digitalWrite(5, LOW);
  digitalWrite(6, LOW);
  digitalWrite(9, LOW);
  digitalWrite(10, LOW);
}

void turnOnFan() {
  digitalWrite(7, HIGH);
}

void turnOffFan() {
  digitalWrite(7, LOW);
}
