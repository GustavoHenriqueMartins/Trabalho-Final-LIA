# PROJETO PIANO DE 3 TECLAS

Este projeto tem o objetivo de fazer com que cada tecla do piano toque uma nota específica no buzzer.

Componentes utilizados:

-Arduino Uno.

-Jumpers e Protoboard.

-3 botões.

-1 Buzzer.

-3 Resistores (10kΩ) para os botões e 1 resistor (220Ω) para o buzzer.

COMO FUNCIONA

O código utiliza 3 botões ligados aos pinos 8, 9 e 10 e o buzzer ligado ao pino 11. Quando uma das teclas dos botões é pressionada, o buzzer produz a nota correspondente àquela tecla.

EXPLICAÇÃO DO CÓDIGO

Função setup(): Configura os pinos dos botões como entradas com pull-up interno. Também configura o pino do buzzer como saída.

Função loop(): Verifica continuamente o estado dos botões. Quando um botão é pressionado, o buzzer toca a nota associada. Quando o botão é solto, o som do buzzer para.

CÓDIGO:

Código:

void setup()

{

  pinMode(8, INPUT);

  pinMode(11, OUTPUT);

  pinMode(9, INPUT);

  pinMode(10, INPUT);

}

void loop()

{

  if (digitalRead(8) == HIGH) {

    tone(11, 440, 200); // play tone 57 (A4 = 440 Hz)

  }

  if (digitalRead(9) == HIGH) {

    tone(11, 494, 200); // play tone 59 (B4 = 494 Hz)

  }

  if (digitalRead(10) == HIGH) {

    tone(11, 554, 200); // play tone 61 (C#5 = 554 Hz)

  }

  delay(10); // Delay a little bit to improve simulation performance

}


COMO CARREGAR O CÓDIGO NO ARDUINO IDE

1.Abra a IDE do Arduino.

2.Copie e cole o código no editor.

3.Selecione a placa "Arduino UNO" (ou a placa que você estiver utilizando) e a porta correta.

4.Carregue o código na placa Arduino.

USO

1.Conecte os botões e o buzzer ao Arduino conforme as instruções.

2.Após carregar o código, pressione os botões para tocar as notas correspondentes no buzzer.
