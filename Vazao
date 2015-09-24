float vazao;
int volume = 0;
int garrafa = 0;
int tamanho = 600;
int contaPulso;
int t = 0;
int ledA = 10;
int ledB = 11;

void setup() {
  Serial.begin(9600);
  pinMode(2, INPUT);
  pinMode(13, OUTPUT);
  pinMode(10, OUTPUT);
  pinMode(11, OUTPUT);
  attachInterrupt(0, incpulso, RISING);
  Serial.println("Escolha o tamanho:");
  Serial.println("A - 300ml");
  Serial.println("B - 600ml");
}

void loop() {
  if (Serial.available()) {
    switch (Serial.read()) {
      case 'A':
        Serial.println("Iniciando 300ml...");
        for (int fadeValue = 0 ; fadeValue <= 255; fadeValue += 1) {
          analogWrite(ledA, fadeValue);
          delay(30);
        }
        Serial.println("Garrafa Cheia!");
        delay(3000);
        analogWrite(ledA, 0);
        Serial.println();
        Serial.println("Escolha o tamanho:");
        Serial.println("A - 300ml");
        Serial.println("B - 600ml");
        break;
      case 'B':
        Serial.println("Iniciando 600ml...");
        for (int fadeValue = 0 ; fadeValue <= 255; fadeValue += 1) {
          analogWrite(ledB, fadeValue);
          delay(30);
        }
        Serial.println("Garrafa Cheia!");
        delay(3000);
        analogWrite(ledB, 0);
        Serial.println();
        Serial.println("Escolha o tamanho:");
        Serial.println("A - 300ml");
        Serial.println("B - 600ml");
        break;
    }
  }
}

void incpulso ()
{
  contaPulso++; // Incrementa a variável de contagem dos pulsos
}
