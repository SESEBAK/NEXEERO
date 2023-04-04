# 1. SKETCH
<br>
 <img style="float: center;" width=500 src="IMAGE/sketch1.jpg">

 <br>
 <img style="float: center;" width=500 src="IMAGE/sketch2.jpg">


# 2. CAD
<br>
 <img style="float: center;" width=700 src="IMAGE/box.png">


<iframe src="https://myhub.autodesk360.com/ue28cacf9/shares/public/SH512d4QTec90decfa6ebe690782f8d98544?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

# 3. MATERIAL ANALYSIS
<br>
 <img style="float: center;" width=500 src="IMAGE/material.jpg">

In terms of material, a research needs to be made to know which material is more suitable for your products.
We have two main type of materials
1. FOR 3D PRINTING: this includes 
 - PLA (very popular, easy to print and biodegradable), 
 - ABS (which is durable,robust and resistant to temperature and is found in many household products like Logo toys etc, However, ABS releases smelly and toxic chemicals during printing)
 - PETG is made from Polyethylene Terephthalate (PET), the material you know from plastic water bottles. PETG isn’t great at bridging because it’s super sticky, but this does mean it has great layer adhesion. It’s also more hygroscopic than PLA, so it can be prone to both heavy stringing and air-moisture absorption if left out
 - PVA is soluble in water, It uses include packaging for dishwasher detergent “pods” or bags full of fishing bait. (Throw the bag in water and watch it dissolve, releasing the bait.) The advantage of using PVA over HIPS is that it can support more materials than just ABS.
- Nylon, a branch of synthetic polymers, is a tough and durable material originally seen in textiles.The material stands out for its toughness and its resistance to high temperatures and impacts. It also has a very low coefficient of friction,  making it the ideal 3D printing material for parts that require good tensile and mechanical strength. The downside of Nylon is that it doesn't easily print out.
- HIPS is very similar to ABS, but as the name implies, it can withstand much higher impact forces. It’s easily painted, machinable, and works with a large number of adhesives. Moreover, it’s food-safe, being declared FDA-compliant for food processing applications.
- WOOD: Wood 3D printer filament is typically a PLA infused with wood fiber. Be careful with the temperature at which you print wood, as too much heat can result in an almost burnt or caramelized appearance. On the other hand, the base appearance of your wooden creations can be greatly improved with a little post-print processing! You can cut it, sand it, or paint it.

AND SO MANY MORE LIKE PLASTIC, METAL, STANDARD RESINS ETC...

2. FOR LASERCUTTING
<br>
 <img style="float: center;" width=500 src="IMAGE/lasercut.png">


### THE MATERIAL MOST SUITED FOR OUR PROJECT WOULD BE ABS (ACROLONITRILE BUTADIENE STYRENE)
<br>
 <img style="float: center;" width=500 src="IMAGE/ABS.webp">


### BUT FOR OUR OUR EXPERIMENTATION WE WILL USE ACRYLIC AS THE AVAILABLE MATERIAL.

 <br>
 <img style="float: center;" width=500 src="IMAGE/acrylic.jpg">


# 4. LASERCUTTING
<br>
 <img style="float: center;" width=500 src="IMAGE/fpro.jpg">

<br>

 <video style="float:center;" width="720" height="340" autoplay="autoplay">
  <source src="VIDEOS/fpro.mp4">
  <source src="movie.ogg" type="video/ogg">
Your browser does not support the video tag.
</video>

# 5. ASSEMBLING
<br>
 <img style="float: center;" width=500 src="IMAGE/fpro.jpg">

<br>

 <video style="float:center;" width="720" height="340" autoplay="autoplay">
  <source src="VIDEOS/fpro2.mp4">
  <source src="movie.ogg" type="video/ogg">
Your browser does not support the video tag.
</video>

# 7. FINAL OUTCOME
<br>
 <img style="float: center;" width=700 src="IMAGE/fpro6.jpg">



# 8. DEMONSTRATION
CODE
       #include <LiquidCrystal_I2C.h>
         LiquidCrystal_I2C lcd(0x27, 16, 2);
 
        void setup() {
        Serial.begin(9600);
        lcd.init();
        lcd.backlight();
        lcd.clear();
        pinMode(2, OUTPUT);
        digitalWrite(2, HIGH);
        delay(1000);
        lcd.setCursor(0, 0);
        lcd.print("IRRIGATION");
        lcd.setCursor(0, 1);
        lcd.print("SYSTEM IS ON ");
        lcd.print("");
        delay(3000);
        lcd.clear();
        }
 
        void loop() {
        int value = analogRead(A0);
        Serial.println(value);
        if (value > 950) {
        digitalWrite(2, LOW);
        lcd.setCursor(0, 0);
        lcd.print("Water Pump is ON ");
        } else {
        digitalWrite(2, HIGH);
        lcd.setCursor(0, 0);
        lcd.print("Water Pump is OFF");
        }
 
        if (value < 300) {
        lcd.setCursor(0, 1);
        lcd.print("Moisture : HIGH");
        } else if (value > 300 && value < 950) {
        lcd.setCursor(0, 1);
        lcd.print("Moisture : MID ");
        } else if (value > 950) {
        lcd.setCursor(0, 1);
        lcd.print("Moisture : LOW ");
        }
      }

<br>

 <video style="float:center;" width="720" height="340" autoplay="autoplay">
  <source src="VIDEOS/DEMO2.mp4">
  <source src="movie.ogg" type="video/ogg">
Your browser does not support the video tag.
</video>


<br>

 <video style="float:center;" width="720" height="340" autoplay="autoplay">
  <source src="VIDEOS/demo.mp4">
  <source src="movie.ogg" type="video/ogg">
Your browser does not support the video tag.
</video>

<br>
 <img style="float: center;" width=500 src="IMAGE/fpro.jpg">