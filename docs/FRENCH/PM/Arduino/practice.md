 # 1. DEVOIR EN CLASSE
<br>
 <img style="float: center;" width=700 src="IMAGE/arduino1.png">

          const int LED1=12;
          const int LED2=13;
          int val=0; 
           void setup()
         { 
           pinMode(LED1, OUTPUT); 
           pinMode(LED2, OUTPUT); 
           pinMode(7, INPUT);     
          }
         void loop(){
          val=digitalRead(7);
          if(val==HIGH)
         {
          digitalWrite(LED1,HIGH);
         digitalWrite(LED2,LOW);
         }
         else
         { 
          digitalWrite(LED2,HIGH);
          digitalWrite(LED1,LOW);  
         }
         delay(1000);
         }

<br>
 <img style="float: center;" width=300 src="IMAGE/A11.jpg">

 <br>
 <img style="float: center;" width=300 src="IMAGE/A12.jpg">

<br>
<video style="float:center;" width="900" height="540" controls autoplay="autoplay">
  <source src="VIDEOS/1st.mp4">
  <source src="movie.ogg" type="video/ogg">
Your browser does not support the video tag.
</video>  

# 2. DEVOIR EN CLASSE 2
          const int LED1=13;
          const int LED2=12;
          const int LED3=11;
           const int LED4=10;
          const int LED5=9;
          const int LED6=6;

         int val=0; 
           void setup()
          { 
            pinMode(LED1, OUTPUT); 
            pinMode(LED2, OUTPUT); 
            pinMode(LED3, OUTPUT); 
            pinMode(LED4, OUTPUT); 
            pinMode(LED5, OUTPUT); 
            pinMode(LED6, OUTPUT); 
            pinMode(7, INPUT);     
         }
         void loop(){
         val=digitalRead(7);
         if(val==HIGH)
         {
          digitalWrite(LED1,HIGH);
          digitalWrite(LED2,LOW);
          digitalWrite(LED3,HIGH);
          digitalWrite(LED4,LOW);
          digitalWrite(LED5,HIGH);
          digitalWrite(LED6,LOW);
         }
         else
         { 
          digitalWrite(LED1,LOW);
          delay(50);
          digitalWrite(LED1,HIGH);
          digitalWrite(LED2,LOW);
          delay(50);
          digitalWrite(LED2,HIGH);
          digitalWrite(LED3,LOW);
          delay(50);
          digitalWrite(LED3,HIGH);
          digitalWrite(LED4,LOW);
          delay(50);
          digitalWrite(LED4,HIGH);
          digitalWrite(LED5,LOW);
          delay(50);
          digitalWrite(LED5,HIGH);
          digitalWrite(LED6,LOW);
          delay(50);
          digitalWrite(LED6,HIGH);
    
         }
         delay(100);
         
         }

<br>
 <img style="float: center;" width=300 src="IMAGE/A13.jpg">

 <br>
 <img style="float: center;" width=300 src="IMAGE/A14.jpg">

 <br>
<video style="float:center;" width="900" height="540" controls autoplay="autoplay">
  <source src="VIDEOS/2nd.mp4">
  <source src="movie.ogg" type="video/ogg">
Your browser does not support the video tag.
</video>  


# 3. ARDUINO ULTRASONIC SENSOR + LEDs 
<br>
 <img style="float: center;" width=500 src="IMAGE/ultrasonic.png">


        const int trig = 12;
        const int echo = 13;

        const int LED1 = 8;
        const int LED2 = 7;
        const int LED3 = 6;
        const int LED4 = 5;
        const int LED5 = 4;
        const int LED6 = 3;
        const int LED7 = 2;

        int duration = 0;
        int distance = 0;

       void setup() 
       {
        pinMode(trig , OUTPUT);
        pinMode(echo , INPUT);
  
        pinMode(LED1 , OUTPUT);
        pinMode(LED2 , OUTPUT);
        pinMode(LED3 , OUTPUT);
        pinMode(LED4 , OUTPUT);
        pinMode(LED5 , OUTPUT);
        pinMode(LED6 , OUTPUT);
        pinMode(LED7 , OUTPUT);
  
       Serial.begin(9600);

       }

       void loop()
      {
        digitalWrite(trig , HIGH);
        delayMicroseconds(3000);
        digitalWrite(trig , LOW);


        duration = pulseIn(echo , HIGH);
        distance = (duration/2) / 28.5 ;
        Serial.println(distance);
  

        if ( distance <= 7 )
       {
        digitalWrite(LED1, HIGH);
       }
       else
       {
        digitalWrite(LED1, LOW);
       }
        if ( distance <= 14 )
       {
        digitalWrite(LED2, HIGH);
       }
       else
       {
        digitalWrite(LED2, LOW);
       }
        if ( distance <= 21 )
       {
        digitalWrite(LED3, HIGH);
       }
       else
       {
        digitalWrite(LED3, LOW);
       }
       if ( distance <= 28 )
       {
       digitalWrite(LED4, HIGH);
       }
       else
       {
       digitalWrite(LED4, LOW);
       }
       if ( distance <= 35 )
       {
       digitalWrite(LED5, HIGH);
       }
       else
       {
       digitalWrite(LED5, LOW);
       }
       if ( distance <= 42 )
       {
       digitalWrite(LED6, HIGH);
        }
       else
       {
       digitalWrite(LED6, LOW);
       }
       if ( distance <= 49 )
       {
       digitalWrite(LED7, HIGH);
       }   
       else
       {
       digitalWrite(LED7, LOW);
       }
     }


 <br>
 <img style="float: center;" width=500 src="IMAGE/ultrasonic2.jpg">

 <br>
<video style="float:center;" width="900" height="540" controls autoplay="autoplay">
  <source src="VIDEOS/ultrasonic.mp4">
  <source src="movie.ogg" type="video/ogg">
Your browser does not support the video tag.
</video>  

# 4. SERVO DISTANCE INDICATEUR
<br>
<img style="float: center;" width=500 src="IMAGE/servodistance.jpg">

<br>
<img style="float: center;" width=500 src="IMAGE/arduino2.jpg">


          #include <Servo.h>

          #include <NewPing.h>

         const int ServoPin = 10;
         const int TriggerPin = 6;
         const int EchoPin = 7;

         // 100 = maxDistance
         NewPing sonar (TriggerPin, EchoPin, 100);
         Servo servo;

         void setup() {
         Serial.begin(9600);
         servo.attach(ServoPin);
         }

         void loop() {
         int cm = sonar.ping_cm();
         Serial.println(cm);

         int angle = map(cm, 2, 15, 15, 100);
         servo.write(angle);

          delay(50);
         }

<br>
<video style="float:center;" width="900" height="540" controls autoplay="autoplay">
  <source src="VIDEOS/arduino2.mp4">
  <source src="movie.ogg" type="video/ogg">
Your browser does not support the video tag.
</video>  

# 5. TEMPERATURE AND HUMIDITE 
<br>
<img style="float: center;" width=500 src="IMAGE/temperature.jpg">


     #include <DHT.h>
     #define DHTPIN 7 // what digital pin we're connected to
     #define DHTTYPE DHT11  //DHT 11

     // LCD display

     #include <LiquidCrystal.h>;
     LiquidCrystal lcd(12, 11, 5, 4, 3, 2);

      DHT dht (DHTPIN, DHTTYPE); //Initialize DHT sensor.


      void setup() {
       // put your setup code here, to run once:


      // Serial.begin(9600);
     dht.begin();

     }

     void loop() {
     delay(10000); // Waiting time between measurements
 
     float t = dht.readTemperature(); // Read temperature in *C (default)
     float h = dht.readHumidity(); // Read humidity %

     float hic = dht.computeHeatIndex(t, h);


     /*Serial.print("Temerature: ");
     Serial.print(t);
     Serial.print("*C\t");
     Serial.print("Humidity: ");
     Serial.print(h);
     Serial.print("%\t");
     Serial.print("Heat index: ");
     Serial.println(hic);
     */



     // LCD display

     lcd.begin(16, 2); // display diamensions
     lcd.setCursor(0,0);
     lcd.print("T=");
     lcd.setCursor(2,0);
     lcd.print(t);
     lcd.setCursor(4,0);
     lcd.print("*C ");
     lcd.setCursor(0,1);
     lcd.print("H=");
     lcd.setCursor(2,1);
     lcd.print(h);
     lcd.setCursor(4,1);
     lcd.print("%  ");
     lcd.setCursor(8,1);
     lcd.print("HI=");
     lcd.print(hic);

     }

<br>
<img style="float: center;" width=500 src="IMAGE/temperatureconnection.jpg">

<br>
<video style="float:center;" width="900" height="540" controls autoplay="autoplay">
  <source src="VIDEOS/temp1.mp4">
  <source src="movie.ogg" type="video/ogg">
Your browser does not support the video tag.
</video>  

### Pour changer la température, j'ai dû mettre une bouillotte devant le capteur. Dans la vidéo ci-dessous, nous pouvons voir la température passer de 23*C à 28*C :

<br>
<video style="float:center;" width="900" height="540" controls autoplay="autoplay">
  <source src="VIDEOS/temp.mp4">
  <source src="movie.ogg" type="video/ogg">
Your browser does not support the video tag.
</video>  