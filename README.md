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
 
****************************************************************************************************<br>

ESP32 LED:https://wokwi.com/projects/336877332872561236

1.ESP32 3 LED:https://wokwi.com/projects/336882445805683282

2.ESP32 RGB LED:https://wokwi.com/projects/336879976249819732


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
