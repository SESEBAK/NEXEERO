 # 1. INCLASS WORK (2 leds)
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

# 2. INCLASS WORK (6 LEDs)
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
 <img style="float: center;" width=500 src="IMAGE/ultrasonic.png">

 <br>
 <img style="float: center;" width=500 src="IMAGE/ultrasonic2.jpg">

 <br>
<video style="float:center;" width="900" height="540" controls autoplay="autoplay">
  <source src="VIDEOS/ultrasonic.mp4">
  <source src="movie.ogg" type="video/ogg">
Your browser does not support the video tag.
</video>  