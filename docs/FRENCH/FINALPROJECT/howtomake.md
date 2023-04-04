# 1. SKETCH
<br>
 <img style="float: center;" width=500 src="IMAGE/sketch1.jpg">

 <br>
 <img style="float: center;" width=500 src="IMAGE/sketch2.jpg">


# 2. CAD


# 3. MATERIEL ANALYSE
<br>
 <img style="float: center;" width=500 src="IMAGE/material.jpg">

En matière de matière, une recherche s'impose pour savoir quelle matière est la plus adaptée à vos produits.
Nous avons deux principaux types de matériaux
1. POUR L'IMPRESSION 3D : cela inclut
 - PLA (très populaire, facile à imprimer et biodégradable),
 - ABS (qui est durable, robuste et résistant à la température et se trouve dans de nombreux produits ménagers comme les jouets Logo, etc. Cependant, l'ABS libère des produits chimiques malodorants et toxiques lors de l'impression)
 - Le PETG est fabriqué à partir de polyéthylène téréphtalate (PET), le matériau que vous connaissez des bouteilles d'eau en plastique. Le PETG n'est pas excellent pour le pontage car il est super collant, mais cela signifie qu'il a une excellente adhérence de couche. Il est également plus hygroscopique que le PLA, il peut donc être sujet à la fois à des cordages lourds et à l'absorption de l'humidité de l'air s'il est laissé de côté
 - Le PVA est soluble dans l'eau, il utilise notamment des emballages pour les "pods" de détergent pour lave-vaisselle ou des sacs remplis d'appâts de pêche. (Jetez le sac dans l'eau et regardez-le se dissoudre, libérant l'appât.) L'avantage d'utiliser du PVA par rapport au HIPS est qu'il peut supporter plus de matériaux que l'ABS.
- Le nylon, une branche de polymères synthétiques, est un matériau solide et durable que l'on trouve à l'origine dans les textiles. Le matériau se distingue par sa ténacité et sa résistance aux températures élevées et aux impacts. Il possède également un très faible coefficient de frottement, ce qui en fait le matériau d'impression 3D idéal pour les pièces nécessitant une bonne résistance à la traction et mécanique. L'inconvénient du nylon est qu'il ne s'imprime pas facilement.
- HIPS est très similaire à l'ABS, mais comme son nom l'indique, il peut résister à des forces d'impact beaucoup plus élevées. Il est facilement peint, usinable et fonctionne avec un grand nombre d'adhésifs. De plus, il est sans danger pour les aliments, étant déclaré conforme à la FDA pour les applications de transformation des aliments.
- BOIS : Le filament d'imprimante 3D en bois est généralement un PLA infusé de fibre de bois. Soyez prudent avec la température à laquelle vous imprimez le bois, car trop de chaleur peut donner un aspect presque brûlé ou caramélisé. D'autre part, l'aspect de base de vos créations en bois peut être grandement amélioré avec un peu de traitement post-impression ! Vous pouvez le couper, le poncer ou le peindre.

ET BEAUCOUP D'AUTRES COMME LE PLASTIQUE, LE MÉTAL, LES RÉSINES STANDARD ETC...

2. POUR LASERCUTTING
<br>
 <img style="float: center;" width=500 src="IMAGE/lasercut.png">


### LE MATÉRIAU LE PLUS ADAPTÉ À NOTRE PROJET SERAIT L'ABS (ACROLONITRILE BUTADIENE STYRENE)
<br>
 <img style="float: center;" width=500 src="IMAGE/ABS.webp">


### MAIS POUR NOTRE EXPÉRIMENTATION, NOUS UTILISERONS L'ACRYLIQUE COMME MATÉRIAU DISPONIBLE.

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

# 5. ASSEMBLER
<br>
 <img style="float: center;" width=500 src="IMAGE/fpro.jpg">

<br>

 <video style="float:center;" width="720" height="340" autoplay="autoplay">
  <source src="VIDEOS/fpro2.mp4">
  <source src="movie.ogg" type="video/ogg">
Your browser does not support the video tag.
</video>



# 6. DEMONSTRATION
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
  <source src="VIDEOS/demo.mp4">
  <source src="movie.ogg" type="video/ogg">
Your browser does not support the video tag.
</video>