 1. INCLASS WORK (2 leds)
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

2. INCLASS WORK (6 LEDs)
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