# Experiment 1 - Hello World LED Blinking

> A basic Program similar to printing "*Hello World* " in any programming language. The Aim is to blink an LED using **Arduino Uno Board**.

> Arduino Uno is an open-source microcontroller board developed by Arduino.cc. It has several advantages over the conventional microcontrollers. It comes with a pre-tested software and hardware libraries and has its own integrated development environment (IDE). Also it is less expensive & beginner friendly.

## Components Required  
* Arduino Uno Board 
* USB Cable 
* LED (Any Color) x 1 Nos
* 220 OHM Resistor X 1 Nos
* Breadboard 
* Jumper Wires (Male to Male ) X 2 Nos

## Circuit Diagram

![1634898879183](https://user-images.githubusercontent.com/91405741/138440483-6eeb5475-4946-42e7-9f6b-3860c91efa42.jpg)

![5h7X9_3102_1627394356](https://user-images.githubusercontent.com/91405741/137279765-8a82a34f-1dc0-4afc-9bd3-a31d7f62c428.png)

## Code

```

int ledPin = 10; // define digital pin 10.
void setup()
{
pinMode(ledPin, OUTPUT);// define pin with LED connected as output.
}
void loop()
{
digitalWrite(ledPin, HIGH); // set the LED on.
delay(1000); // wait for a second.
digitalWrite(ledPin, LOW); // set the LED off.
delay(1000); // wait for a second
}

```

## Output

> The LED is blinked with a time interval od 1 second

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/91405741/137283496-04e4fe43-bc6a-4ca5-a6e0-0f7ecdcd56c5.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Experiment 2 : Traffic Light

> In the previous program, we have done the LED blinking experiment with one LED. Now, it’s time to up the stakes and do a bit more complicated experiment-traffic lights. Actually, these two experiments are similar. While in this traffic lights experiment, we use 3 LEDs with different colors rather than 1 LED.

## Components Required 

* Arduino board *1
* USB cable *1
* Red M5 LED*1
* Yellow M5 LED*1
* Green M5 LED*1
* 220Ω resistor *3

## Circuit Diagram

![1634898905963](https://user-images.githubusercontent.com/91405741/138440549-c4c958ec-0893-4e80-8aba-3a43cafe865e.jpg)

![yiU1x_3102_1627566759](https://user-images.githubusercontent.com/91405741/137288387-e85f8db9-ae97-49d0-888d-a2fc15e4c496.png)

## Code

```

int redled =10; // initialize digital pin 10.
int yellowled =7; // initialize digital pin 7.
int greenled =4; // initialize digital pin 4.
void setup()
{
pinMode(redled, OUTPUT);// set the pin with red LED as “output”
pinMode(yellowled, OUTPUT); // set the pin with yellow LED as “output”
pinMode(greenled, OUTPUT); // set the pin with green LED as “output”
}
void loop()
{
digitalWrite(greenled, HIGH);//// turn on green LED
delay(5000);// wait 5 seconds
digitalWrite(greenled, LOW); // turn off green LED
for(int i=0;i<3;i++)// blinks for 3 times
{
delay(500);// wait 0.5 second
digitalWrite(yellowled, HIGH);// turn on yellow LED
delay(500);// wait 0.5 second
digitalWrite(yellowled, LOW);// turn off yellow LED
} 
delay(500);// wait 0.5 second
digitalWrite(redled, HIGH);// turn on red LED
delay(5000);// wait 5 seconds
digitalWrite(redled, LOW);// turn off red LED
}

```

## Output

> In Traffic light the green LED blink about 5 second, then it is turnoff. Then the yellow LED blinks 3 times with a time interval of 0.5 second.Then the red LED blink about 5 seconds. This process continues.

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/91405741/137290512-e479c4b3-1810-4b72-966f-42348620b1f4.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Experiment 3 : LED Chasing Effect

> We often see billboards composed of colorful LEDs. They are constantly changing to form various light effects. In this experiment, we compile a program to simulate LED chasing effect. The long lead of LED is the positive side; short lead is negative.

## Components Required

* Led *6
* Arduino board *1
* 220Ω resistor *6
* Breadboard *1
* USB cable*1
* Breadboard wire *13

## Circuit Diagram

![1634898830010](https://user-images.githubusercontent.com/91405741/138440641-844673fc-0cc9-4e67-bf8c-f1dd30d7a970.jpg)

![s5yR0_3102_1627567167](https://user-images.githubusercontent.com/91405741/137292096-feb60c91-1a9a-474b-a596-300285f7b011.png)

## Code

```

int BASE = 2 ;  // the I/O pin for the first LED
int NUM = 6;   // number of LEDs
void setup()
{
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     pinMode(i, OUTPUT);   // set I/O pins as output
   }
}
void loop()
{
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, LOW);    // set I/O pins as “low”, turn off LEDs one by one.
     delay(200);        // delay
   }
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, HIGH);    // set I/O pins as “high”, turn on LEDs one by one
     delay(400);        // delay
   }  
}

```

## Output

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/91405741/137293394-f7b99c4d-4659-44fc-87ca-d331f3b6ebaf.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Experiment 4: Button Controlled LED

> An experiment to light an LED using a Push Button.

## Components Required 

* Arduino Uno
* Button switch*1
* Red M5 LED*1
* 220ΩResistor*1
* 10KΩ Resistor*1
* Breadboard*1
* Breadboard Jumper Wire*6
* USB cable*1

## Circuit Diagrams

![1634898715966](https://user-images.githubusercontent.com/91405741/138440748-60c27803-19c4-42f1-a4ec-cc198598bae8.jpg)

![Ztk6E_3102_1628160172](https://user-images.githubusercontent.com/91405741/137344162-7149dfcf-836c-43ec-a01c-177d48958d12.png)

![wQGca_3102_1628160139](https://user-images.githubusercontent.com/91405741/137344321-3e662dee-cb00-421d-a34d-848c2ffd1a6f.png)

## Code

```

int ledpin=11;// initialize pin 11
int inpin=7;// initialize pin 7
int val;// define val
void setup()
{
pinMode(ledpin,OUTPUT);// set LED pin as “output”
pinMode(inpin,INPUT);// set button pin as “input”
}
void loop()
{
val=digitalRead(inpin);// read the level value of pin 7 and assign if to val
if(val==LOW)// check if the button is pressed, if yes, turn on the LED
{ digitalWrite(ledpin,LOW);}
else
{ digitalWrite(ledpin,HIGH);}
}

```
## Output

> When the push button is pressed the LED is turned on otherwise it is off.

<iframe width="560" height="315"
src="https://user-images.githubusercontent.com/91405741/137346113-b41f1d56-84b5-4437-9d7a-3f11ab84991a.mp4"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Experiment 5 : Buzzer

> An experiment to understand the working of a buzzer.

## Components Required

* Arduino Uno
* Buzzer*1
* Breadboard*1
* Breadboard Jumper Wire*2
* USB cable*1

![BBr05_3102_1628160460](https://user-images.githubusercontent.com/91405741/137346830-1fa2408c-2a1d-4fdf-a049-5736aeb803ec.png)

![e9Pdc_3102_1628160446](https://user-images.githubusercontent.com/91405741/137346912-0f871dbf-8e86-4734-a337-fceeff454e33.png)

## Code

```

int buzzer=8;// initialize digital IO pin that controls the buzzer
void setup() 
{ 
  pinMode(buzzer,OUTPUT);// set pin mode as “output”
} 
void loop() 
{
digitalWrite(buzzer, HIGH); // produce sound
}

```

## Output

> The Buzzer makes beep sound.

![1634194968124](https://user-images.githubusercontent.com/91405741/137345459-3ad2e1ac-b091-40fd-bf7b-1bcccf29baec.jpg)


# Experiment 6 : RGB LED

> An experiment to understand the working of a RGB LED.

## Components Required

* Arduino Uno
* USB Cable * 1
* RGB LED * 1
* Resistor *3
* Breadboard jumper wire*5

## Circuit Diagrams

https://drive.google.com/file/d/1bDv9XzsQwxKkAbMQ2d7FdhwT8368cu0T/view?usp=sharing

## Code

```

int redLED = 11;
int blueLED = 10;
int greenLED = 9;
int val;

void setup() {
  pinMode(redLED, OUTPUT);
  pinMode(blueLED, OUTPUT);
  pinMode(greenLED, OUTPUT);
  Serial.begin(9600);
}

void loop()
{
  for (val = 255; val > 0; val--)
  {
    analogWrite(11, val);
    analogWrite(10, 255 - val);
    analogWrite(9, 128 - val);
    delay(1);
  }
  for (val = 0; val < 255; val++)
  {
    analogWrite(11, val);
    analogWrite(10, 255 - val);
    analogWrite(9, 128 - val);
    delay(1);
  }
  Serial.println(val, DEC);
}

```

## Output

> The RGB LED blinks.

<iframe width="560" height="315"
src="https://drive.google.com/file/d/1bDF6kjx_ksgmsZ-uUJKtRNaVgUGCyKvK/view?usp=sharing"
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>


