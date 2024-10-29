# Ponderada do Semáforo

&ensp; **Descrição:** O objetivo era montar e programar um semáforo que garanta a segurança de pedestres e veículos, seguindo a lógica de tempo de cada fase das luzes, desde a montagem dos LEDs até a programação da sequência correta.

### Parte 1: Montagem Física do Semáforo

&ensp; Os itens utilizados para a montagem desse protótipo foram: 

- 3 LED´s (Vermelho, amarelo e verde);
- 8 Jumpers;
- 2 Resistores;
- 1 Buzzer;
- 1 ESP32;
- 1 Protoboard.

<div align="center">
  <sub>Figura 1 - Protótipo do semáforo</sub> <br>

  <img src="C:\Users\Inteli\Desktop\Ponderada_Semaforo\Foto e Vídeo\PrototipoSemaforo.jpg" width=300px>

  <sup>Fonte: Material produzido pelos autores (2024).</sup>
</div>

##### Parte 1.1 O diferencial 

&ensp; O diferencial desse protótipo de semáforo foi a utilização de um Buzzer para que fosse liberado um sinal sonoro junto ao período em que o LED vermelho estivesse ligado com o objetivo de avisar e destacar que a função do LED vermelho/Sinal vermelho.


### Parte 2:  Programação e Lógica do Semáforo

```
int led_vermelho = 33;
int led_amarelo = 5;
int led_verde = 18;

void setup() {
  // put your setup code here, to run once:
  pinMode(led_vermelho, OUTPUT);
  pinMode(led_amarelo, OUTPUT);
  pinMode(led_verde, OUTPUT);
}

void loop() {
  // put your main code here, to run repeatedly:

  digitalWrite(led_vermelho, HIGH);
  digitalWrite(led_amarelo, LOW);
  digitalWrite(led_verde, LOW);
  delay(6000);

  digitalWrite(led_vermelho, LOW);
  digitalWrite(led_amarelo, HIGH);
  digitalWrite(led_verde, LOW);
  delay(2000);

  digitalWrite(led_vermelho, LOW);
  digitalWrite(led_amarelo, LOW);
  digitalWrite(led_verde, HIGH);
  delay(4000);

  digitalWrite(led_vermelho, LOW);
  digitalWrite(led_amarelo, HIGH);
  digitalWrite(led_verde, LOW);
  delay(2000);
}

```

### Parte 3: Avaliação de Pares

### Avaliador: Enzo Salvador

| Critério                                                                                                 | Contempla (Pontos) | Contempla Parcialmente (Pontos) | Não Contempla (Pontos) | Observações/Pontuação do Avaliador |
|---------------------------------------------------------------------------------------------------------|--------------------|----------------------------------|--------------------------|---------------------------|
| Montagem física com cores corretas, boa disposição dos fios e uso adequado de resistores                | Até 3              | Até 1,5                            | 0                        |    3          |
| Temporização adequada conforme tempos medidos com auxílio de algum instrumento externo                  | Até 3              | Até 1,5                          | 0                        |        3                  |
| Código implementa corretamente as fases do semáforo e estrutura do código (variáveis representativas e comentários) | Até 3              | Até 1,5                          | 0                        |             3             |
| Extra: Implmeentou um componente de liga/desliga no semáforo e/ou usou ponteiros no código | Até 1              |  Até 0,5                         | 0                        |             1             |
|  |                                                             |  | |*Pontuação Total*: 10 pontos|
