# Sprint3
Codigo no Workiwi

int FLAG = 0;
int movimentoCount = 0; // Variável para contar os movimentos

void setup() {
  Serial.begin(115200);
  Serial.println("Sensor de Movimento");
  pinMode(19, OUTPUT);
  pinMode(13, INPUT); // Certifique-se de que o pino 13 é configurado como entrada
}

void loop() {
  if ((digitalRead(13) == HIGH) && (FLAG == 0)) {
    FLAG = 1;
    movimentoCount++; // Incrementa a contagem de movimentos
    digitalWrite(19, HIGH);
    Serial.print("Sensor Ativado. Total de movimentos: ");
    Serial.println(movimentoCount);
  }

  if ((digitalRead(13) == LOW) && (FLAG == 1)) {
    FLAG = 0;
    digitalWrite(19, LOW);
    Serial.println("Sensor Desativado");
  }
}

link do projeto no site 

https://wokwi.com/projects/410503195127061505

RM do grupo

Gustavo Alves - rm557876
Gabriel Dias - rm556830
Pedro Pawlik - rm556968
Pedro Paulo - rm554880
