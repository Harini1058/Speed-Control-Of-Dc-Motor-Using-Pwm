# Speed-Control-Of-Dc-Motor-Using-Pwm
# Aim
To control the speed of a DC motor using Pulse Width Modulation (PWM) with a development board.

# Algorithm
Initialize the development board and set the motor control pin as an output. Generate a PWM signal at the required frequency.
Set an initial PWM duty cycle.
Apply the PWM signal to the DC motor through a suitable motor driver.
Vary the duty cycle to increase or decrease the motor speed.
Observe the corresponding change in motor speed.
Repeat the process for different duty-cycle values.
Procedure
Connect the DC motor to the motor driver circuit.
Connect the motor driver to the development board.
Connect the required power supply and ensure a common ground.
Configure the motor control pin for PWM output.
Upload the PWM motor-control program to the dev…
# PROGRAM
```
int MPin = 9;   //motor pin
int Analog = A0;  // Analog Input
int Ainp = 0; // Read analog input, initialized to zero  
  
void setup()
{
  
  Serial.begin(9600);
  pinMode(MPin, OUTPUT);
  pinMode(Analog, INPUT);
}

void loop()
{

Ainp = analogRead(A0);

int Speed = map(Ainp, 0, 1024, 0, 255);
delay(100);
Serial.println(Speed);
analogWrite(MPin, Speed);  

}
```

# OUTPUT

<img width="1917" height="1022" alt="image" src="https://github.com/user-attachments/assets/de8ea2a8-e045-4635-8e64-eb2dd90038aa" />


# RESULT
Thus the speed of a DC motor using Pulse Width Modulation (PWM) with a development board is controlled.
