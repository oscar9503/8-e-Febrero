# 8-e-Febrero
int t1; int t2; int t3;
int ledrojo = 5; int ledverde = 6; int ledazul = 7;

void setup() {
  Serial.begin(9600);
  Serial.println("¿Cuantos milisegundos deseas que permanezca encendido el led rojo?");
  while (Serial.available() == 0) {
  }
  t1=Serial.parseInt();
  pinMode(ledrojo, OUTPUT);
////////////////////////////////////////////////////////
  Serial.begin(9600);
  Serial.println("¿Cuantos milisegundos deseas que permanezca encendido el led verde?");
  while (Serial.available() == 0) {
  }
  t2=Serial.parseInt();
  pinMode(ledverde, OUTPUT);
///////////////////////////////////////////////////////////////
  Serial.begin(9600);
  Serial.println("¿Cuantos milisegundos deseas que permanezca encendido el led azul?");
  while (Serial.available() == 0) {
  }
  t3=Serial.parseInt();
  pinMode(ledazul, OUTPUT);
///////////////////////////////////////////////////////////////

}
void loop() {
 digitalWrite(ledrojo,HIGH);
delay (t1);
digitalWrite(ledrojo,LOW);
delay (t1);
digitalWrite(ledverde,HIGH);
delay (t2);
digitalWrite(ledverde,LOW);
delay (t2);
digitalWrite(ledazul,HIGH);
delay (t3);
digitalWrite(ledazul,LOW);
delay (t3);
}
