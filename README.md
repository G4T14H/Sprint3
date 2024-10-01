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

Esse código é para um sensor de movimento que conta quantas vezes algo se move.

Variáveis: FLAG controla se o sensor já foi ativado, e movimentoCount conta as ativações.
Setup: Configura os pinos—19 para saída (LED) e 13 para entrada (sensor).
Loop:
Quando o sensor detecta movimento (HIGH), ele ativa o LED, aumenta a contagem e imprime no serial.
Quando não há movimento (LOW), desativa o LED e imprime que o sensor foi desativado.
A ideia é monitorar movimento de forma simples e eficiente. Se precisar de mais alguma coisa, é só avisar!




link do projeto no site 

https://wokwi.com/projects/410503195127061505

RM do grupo

Gustavo Alves - rm557876
Gabriel Dias - rm556830
Pedro Pawlik - rm556968
Pedro Paulo - rm554880
