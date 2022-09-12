Arduino LED: https://wokwi.com/projects/333715280525001300

 1. Arduino 3 LED:https://wokwi.com/projects/334348041107538516 <br>

 2. Arduino RGB LED:https://wokwi.com/projects/334340428564267602<br>

 3. LCD: https://wokwi.com/projects/334973098919985748<br>

 4. Servo motor: https://wokwi.com/projects/334977394006819411<br>

 5. Servo motor +potentiometer slide:https://wokwi.com/projects/334979427891937876<br>

 6. Servo motor +push button: https://wokwi.com/projects/335701119415091795
 
       Servo motor using 2 for loops(frwrd&bckwrd):https://wokwi.com/projects/334981103304573523<br>

 7. Buzzer: https://wokwi.com/projects/335064951298196051<br>
 
 8. Buzzer using push Button: https://wokwi.com/projects/335066519134274130<br>

     8* Buzzer using push Button & LED: https://wokwi.com/projects/335616316076458578<br>
   
 9. Buzzer using push Button-long press: https://wokwi.com/projects/335070499832857171<br>
    
 10. Ultrasonic sensor:https://wokwi.com/projects/335071675085226580<br>
 
 11. Ultrasonic sensor+buzzer: https://wokwi.com/projects/335073847080387154<br>

 12.  Ultrasonic sensor with buzzer & LED:  https://wokwi.com/projects/335610859327849042<br>
 
 13. potentiometer with lED:https://wokwi.com/projects/335702269747003986<br>
  
 14. Multipple ultrasonic sensor: https://wokwi.com/projects/335706874922926676
 
 15. DHT22(Humidity and Temperature sensor): https://wokwi.com/projects/338145995428725330
 
 16. DHT22 + LCD(Humidity and Temperature sensor) :https://wokwi.com/projects/338146515814974035
 
 17. LED Chaser : https://wokwi.com/projects/340853047777296978
 
 18. LDR: https://wokwi.com/projects/340853480657781330
 
 19. LDR + LED : https://wokwi.com/projects/340853623478026835
 
 20. IR Receiver + LED : https://wokwi.com/projects/340779619162522195
 
 ---------------------------------------**12/09/2022**------------------------------------------------<br>
 
 1. Seven segment LED display example: https://wokwi.com/projects/342584951158342226
 
 2. Analog Joystick with two axes : https://wokwi.com/projects/342586537358131794
 
 3. DHT22 on the ESP32: https://wokwi.com/projects/342586828010816084
 
 4. Display distance on LCD screen with buzzer and LED  :https://wokwi.com/projects/342587221563408980
                                                         https://wokwi.com/projects/342587671958258260
                                                         
5. Electronic Safe, powered by an Arduino Uno: https://wokwi.com/projects/342588904275182164    

6. Arduino LED Graph Bar - Move the potentiometer knob to control the LEDs:https://wokwi.com/projects/342590008467653203

****************************************************************************************************<br>
**ESP32**<br> 
1.ESP32 LED:https://wokwi.com/projects/336877332872561236   <br> 
2.ESP32 3 LED:https://wokwi.com/projects/336882445805683282  <br> 
3.ESP32 RGB LED: https://wokwi.com/projects/336879976249819732 <br>
4. ESP32 RGB LCD: https://wokwi.com/projects/340854854168609362 <br>
5.servomotor with sliding potentiometer : https://wokwi.com/projects/340872161402028628<br>
6. LED_Chaser: https://wokwi.com/projects/340854632473428562

**ESP32**<br> 
https://wokwi.com/projects/336966830711112275 - LED<br>
https://wokwi.com/projects/336967978479256147 - 3 LED<br>
https://wokwi.com/projects/340880463446934098 - RGB<br>
https://wokwi.com/projects/340882358612787796 - LCD<br>
https://wokwi.com/projects/340886369600537172 - Servo Motor + Pushbutton<br>
https://wokwi.com/projects/340888468071645780 - Servo Motor + Sliding Potentiometer<br>
https://wokwi.com/projects/340890155914101331 - Buzzer + Pushbutton_<br>
https://wokwi.com/projects/340890489300451922 - Buzzer + UltraSonic Sensor<br>
https://wokwi.com/projects/340890896679567955 - Potentiometer + LED<br>
https://wokwi.com/projects/340892440485429842 - DHT22<br>
https://wokwi.com/projects/340893919446303316 - LED CHASER<br>
https://wokwi.com/projects/340936317213868626 - LDR<br>
https://wokwi.com/projects/340936847717827156 - LDR + LED<br>

*****************************************************************************
1. To interface LED/Buzzer with Arduino and write a program to turn ON LED for 1 sec after every 2 seconds.<br>
     https://wokwi.com/projects/334348041107538516 <br>
2. To interface Push button/Digital sensor(IR/LDR) with Arduino and write a program to turn ON LED when push button is pressed or at sensor detection.  <br>
      https://wokwi.com/projects/338224466542723668<br>
3. To interface DHT11(DHT22) sensor with Arduino and write a program to print temperature and humidity readings.<br>
      https://wokwi.com/projects/338145995428725330 <br>
4. To interface motor using relay with Arduino and write a program to turn ON motor when push button is pressed.<br>
      https://wokwi.com/projects/335701119415091795 <br>
5. To interface LCD with Arduino and write a program to print temperature and humidity reading on it.<br>
      https://wokwi.com/projects/338146515814974035 <br>
6. To interface Bluetooth with Arduion and write a program to send sensor data to smartphone using Bluetooth.<br>
7. To interface Bluetooth with Arduion and write a program to turn LED ON/OFF when '1'/'0' is received from smartphone using Bluetooth.<br>
8. write a program on Arduino to upload temperature and humidity data to thingspeak cloud.<br>
9. write a program on Arduino to retrieve temperature and humidity data from thingspeak cloud.<br>
10. write a program on Arduino to subscribe to MQTT broker for temperature data and print it.<br>
11. write a program to create TCP server on Arduino and respond with humidity data to TCP client when required.<br>
12. write a program to create UDP server on Arduino and respond with humidity data to UDP client when required.<br> 


*******************************************************************************************
**LED**<br>
void setup() {<BR>
  pinMode(D5, OUTPUT);<BR>
  pinMode(D6, OUTPUT);<BR>
  pinMode(D7, OUTPUT);<BR>


}<BR>

void loop() {<BR>
  displayColor(0b100);<BR>
  delay(2000);<BR>
  displayColor(0b010);<BR>
  delay(2000);<BR>
  displayColor(0b001);<BR>
  delay(2000);<BR>
  displayColor(0b101);<BR>
  delay(2000);<BR>
  displayColor(0b011);<BR>
  delay(2000);<BR>
  displayColor(0b110);<BR>
  delay(2000);<BR>
  displayColor(0b111);<BR>
  delay(2000);<BR>
<BR>
 
}<BR>
void displayColor(byte color)<BR>
{
  digitalWrite(D5,!bitRead(color,2));<BR>
  digitalWrite(D6,!bitRead(color,1));<BR>
  digitalWrite(D7,!bitRead(color,0));<BR>
}<BR>
 
 ----------------------------------------
 **BUZZER**<br>
const int buzzer = 2;//D4 <BR>
void setup(){<BR>
 
  pinMode(buzzer, OUTPUT); // Set buzzer - pin 2 as an output<BR>

}<BR>

void loop(){<BR>
 
  tone(buzzer, 50); // Send 1KHz sound signal...<BR>
  delay(100);        // ...for 1 sec<BR>
  noTone(buzzer);     // Stop sound...<BR>
  delay(1000);        // ...for 1sec<BR>
  
}<BR>
 ----------------------------------------------
 **DHT11**<br>
 #include <Adafruit_Sensor.h><br>
    #include <DHT.h>;<br>
    #define DHTPIN 2     // what pin we're connected to<br>
    #define DHTTYPE DHT11   // DHT 22  (AM2302)<br>
    DHT dht(DHTPIN, DHTTYPE); //// Initialize DHT sensor for normal 16mhz Arduino<br>
    //Variables<br>
    int chk;<br>
    float hum;  //Stores humidity value<br>
    float temp; //Stores temperature value<br>
    void setup()<br>
    {<br>
      Serial.begin(9600);<br>
      dht.begin();<br>
    }<br>
    void loop()<br>
   {<br>
       delay(2000);<br>
       //Read data and store it to variables hum and temp<br>
       hum = dht.readHumidity();<br>
       temp= dht.readTemperature();<br>
       //Print temp and humidity values to serial monitor<br>
       Serial.print("Humidity: ");<br>
       Serial.print(hum);<br>
       Serial.print(" %, Temp: ");<br>
       Serial.print(temp);<br>
       Serial.println(" Celsius");<br>
       delay(1000); //Delay 2 sec.<br>
   }<br>
 
 
 --------------------------------------------------------
 const int trigPin = 12;<BR>
const int echoPin = 14;<BR>


//define sound velocity in cm/uS<BR>
#define SOUND_VELOCITY 0.034<BR>
#define CM_TO_INCH 0.393701<BR>

long duration;<BR>
float distanceCm;<BR>
float distanceInch;<BR>
int LED = D0;<BR>

void setup() {<BR>
  Serial.begin(9600); // Starts the serial communication<BR>
  pinMode(trigPin, OUTPUT); // Sets the trigPin as an Output<BR>
  pinMode(echoPin, INPUT); // Sets the echoPin as an Input<BR>

  pinMode(LED,OUTPUT);<BR>
}<BR>

void loop() {<BR>
  // Clears the trigPin<BR>
  digitalWrite(trigPin, LOW);<BR>
  delayMicroseconds(2);<BR>
  // Sets the trigPin on HIGH state for 10 micro seconds<BR>
  digitalWrite(trigPin, HIGH);<BR>
  delayMicroseconds(10);<BR>
  digitalWrite(trigPin, LOW);<BR>
  
  // Reads the echoPin, returns the sound wave travel time in microseconds<BR>
  duration = pulseIn(echoPin, HIGH);<BR>
  
  // Calculate the distance<BR>
  distanceCm = duration * SOUND_VELOCITY/2;<BR>
  
  // Convert to inches<BR>
  distanceInch = distanceCm * CM_TO_INCH;<BR>
  if(distanceInch < 10)<BR>

  digitalWrite(LED,HIGH);<BR>
  else<BR>
  digitalWrite(LED,LOW); <BR>
  
  //Prints the distance on the Serial Monitor<BR>
  Serial.print("Distance (cm): ");<BR>
  Serial.println(distanceCm);<BR>
  Serial.print("Distance (inch): ");<BR>
  Serial.println(distanceInch);<BR>
  delay(1000);<BR>
}<BR>
 
------------------------------------------------------
 
**IR Sensor**<BR>
int ir=D7;<BR>
int led=D5;<BR>
void setup() {<BR>
  // put your setup code here, to run once:<BR>
  pinMode(ir,INPUT);<BR>
    pinMode(led,OUTPUT);<BR>
    Serial.begin(9600);<BR>
    
}<BR>

void loop() {<BR>
  // put your main code here, to run repeatedly:<BR>
  int irvalue=digitalRead(ir);<BR>
  if(irvalue==LOW)<BR>
  {<BR>
    Serial.println("LOW");<BR>
    digitalWrite(led,HIGH);<BR>
  }<BR>
  else<BR>
  {<BR>
    Serial.println("HIGH");<BR>
    digitalWrite(led,LOW);<BR>
  }<BR>
delay(100);<BR>
}<BR>
 
---------------------------------------------------------------------------------
 
**CHASING LED**<BR>
int pinsCount=7; // declaring the integer variable pinsCount<BR>
int pins[] = {D0,D1,D2,D3,D4,D5,D6}; // declaring the array pins[]<BR>

void setup() {<BR>
for (int i=0; i<pinsCount; i=i+1){ // counting the variable i from 0 to 9<BR>
pinMode(pins[i], OUTPUT); // initialising the pin at index i of the array of pins as OUTPUT<BR>
}<BR>
}<BR>
void loop() {<BR>
for (int i=0; i<pinsCount; i=i+1){ // chasing right<BR>
digitalWrite(pins[i], HIGH); // switching the LED at index i on<BR>
delay(100); // stopping the program for 100 milliseconds<BR>
digitalWrite(pins[i], LOW); // switching the LED at index i off<BR>
}<BR>
for (int i=pinsCount-1; i>0; i=i-1){ // chasing left (except the outer leds)<BR>
digitalWrite(pins[i], HIGH); // switching the LED at index i on<BR>
delay(100); // stopping the program for 100 milliseconds<BR>
digitalWrite(pins[i], LOW); // switching the LED at index i off<BR>

}<BR>
}<BR>

--------------------------------------------------------------------
 
 **flood monitoring using thingspeak:**

#include <ThingSpeak.h><BR>
#include <ESP8266WiFi.h><BR>
const int trigPin1 = D6;<BR>
const int echoPin1 = D7;<BR>
#define redled D2<BR>
#define grnled D4<BR>
#define BUZZER D1 //buzzer pin<BR>
unsigned long ch_no =  1841332;//Replace with Thingspeak Channel number<BR>
const char * write_api = "85PL62D0DSVPLPKF";//Replace with Thingspeak write API<BR>
char auth[] = "mwa0000027193644";<BR>
char ssid[] = "Sadika's Galaxy A12";<BR>
char pass[] = "sadika123";<BR>
unsigned long startMillis;<BR>
unsigned long currentMillis;<BR>
const unsigned long period = 10000;<BR>
WiFiClient client;<BR>
long duration1;<BR>
int distance1;<BR>
void setup() {<BR>
pinMode(trigPin1, OUTPUT);<BR>
pinMode(echoPin1, INPUT);<BR>
pinMode(redled, OUTPUT);<BR>
pinMode(grnled, OUTPUT);<BR>
digitalWrite(redled, LOW);<BR>
digitalWrite(grnled, LOW);<BR>
Serial.begin(115200);<BR>
WiFi.begin(ssid, pass);<BR>
while (WiFi.status() != WL_CONNECTED)<BR>
{<BR>
delay(1000);<BR>
Serial.print(".");<BR>
}<BR>
Serial.println("WiFi connected");<BR>
Serial.println(WiFi.localIP());<BR>
ThingSpeak.begin(client);<BR>
startMillis = millis(); //initial start time<BR>
}<BR>
void loop()<BR>
{<BR>
digitalWrite(trigPin1, LOW);<BR>
delayMicroseconds(2);<BR>
digitalWrite(trigPin1, HIGH);<BR>
delayMicroseconds(10);<BR>
digitalWrite(trigPin1, LOW);<BR>
duration1 = pulseIn(echoPin1, HIGH);<BR>
distance1 = duration1 * 0.034 / 2;<BR>
Serial.println(distance1);<BR>
if (distance1 <= 400)<BR>
{<BR>
digitalWrite(D2, HIGH);<BR>
tone(BUZZER, 300);<BR>
digitalWrite(D4, LOW);<BR>
delay(1500);<BR>
noTone(BUZZER);<BR>
}<BR>
else<BR>
{<BR>
digitalWrite(D4, HIGH);<BR>
digitalWrite(D2, LOW);<BR>
}<BR>
currentMillis = millis();<BR>
if (currentMillis - startMillis >= period)<BR>
{<BR>
ThingSpeak.setField(1, distance1);<BR>
ThingSpeak.writeFields(ch_no, write_api);<BR>
startMillis = currentMillis;<BR>
}<BR>
}<BR>
-------------------------------------------------------------------------------
https://wokwi.com/projects/321525495180034642

https://theiotprojects.com/iot-based-flood-monitoring-system-using-nodemcu-thingspeak/
