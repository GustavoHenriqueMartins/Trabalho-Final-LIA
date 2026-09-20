# 3-KEY PIANO PROJECT

The goal of this project is to make each piano key play a specific note on the buzzer.

## Components used:

Arduino Uno
Jumper wires and Breadboard
3 pushbuttons
1 Buzzer
Three 10kΩ resistors (for the buttons) and one 220Ω resistor (for the buzzer)

## How it works

The code uses 3 pushbuttons connected to pins 8, 9, and 10, and the buzzer connected to pin 11. When one of the buttons is pressed, the buzzer produces the note corresponding to that key.

## Code Explanation

setup() function: Configures the button pins as inputs and the buzzer pin as an output. (Nota técnica: embora o texto original mencione pull-up interno, o código fornecido usa INPUT comum com resistores externos de 10kΩ).

loop() function: Continuously checks the state of the buttons. When a button is pressed, the buzzer plays the associated note. When the button is released, the buzzer stops emitting sound.

## Code:

Code:

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




## How to upload the code to the Arduino IDE

1.Open the Arduino IDE.
2.Copy and paste the code into the editor.
3.Select the "Arduino UNO" board (or the board you are currently using) and the correct port.
4.Upload the code to the Arduino board.


## Usage

1.Connect the buttons and the buzzer to the Arduino according to the instructions.
2.After uploading the code, press the buttons to play the corresponding notes on the buzzer.
