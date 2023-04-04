# 1. 草图
<br>
 <img style="float: center;" width=500 src="IMAGE/sketch1.jpg">

 <br>
 <img style="float: center;" width=500 src="IMAGE/sketch2.jpg">


# 2. CAD
<br>
 <img style="float: center;" width=500 src="IMAGE/sketch2.jpg">


# 3. 材料分析
<br>
 <img style="float: center;" width=500 src="IMAGE/material.jpg">

在材料方面，需要进行研究以了解哪种材料更适合您的产品。
我们有两种主要类型的材料
1. 对于 3D 打印：这包括
 - PLA（非常流行，易于打印和可生物降解），
 - ABS（耐用、坚固且耐温，在 Logo 玩具等许多家用产品中都有使用，但 ABS 在打印过程中会释放有臭味和有毒的化学物质）
 - PETG 由聚对苯二甲酸乙二醇酯 (PET) 制成，这是您从塑料水瓶中了解到的材料。 PETG 不擅长桥接，因为它非常粘，但这确实意味着它具有很好的层粘附力。它的吸湿性也比 PLA 强，因此如果不放置，它很容易拉丝和吸收空气中的水分
 - PVA 可溶于水，它的用途包括洗碗机洗涤剂“豆荚”的包装或装满鱼饵的袋子。 （将袋子扔进水中，观察它溶解，释放诱饵。）使用 PVA 优于 HIPS 的优势在于它可以支持比 ABS 更多的材料。
- 尼龙是合成聚合物的一个分支，是一种坚韧耐用的材料，最初出现在纺织品中。该材料以其韧性以及耐高温和冲击的能力而著称。它还具有极低的摩擦系数，使其成为需要良好拉伸强度和机械强度的部件的理想 3D 打印材料。尼龙的缺点是它不容易打印出来。
- HIPS 与 ABS 非常相似，但顾名思义，它可以承受更高的冲击力。它易于涂漆、可加工，并可与大量粘合剂配合使用。此外，它是食品安全的，被宣布符合 FDA 的食品加工应用要求。
- 木材：木材 3D 打印机灯丝通常是注入木纤维的 PLA。请注意打印木材的温度，因为过多的热量会导致几乎烧焦或焦糖化的外观。另一方面，您的木制作品的基本外观可以通过一些印后处理得到极大改善！您可以切割、打磨或涂漆。

还有更多像塑料、金属、标准树脂等。..

2. 用于激光切割
<br>
 <img style="float: center;" width=500 src="IMAGE/lasercut.png">


### 最适合我们项目的材料是 ABS（丙烯腈丁二烯苯乙烯
<br>
 <img style="float: center;" width=500 src="IMAGE/ABS.webp">


### 但对于我们的实验，我们将使用亚克力作为可用材料.

 <br>
 <img style="float: center;" width=500 src="IMAGE/acrylic.jpg">



# 4. 激光切割

 <br>
 <img style="float: center;" width=500 src="IMAGE/fpro.jpg">

<br>

 <video style="float:center;" width="720" height="340" autoplay="autoplay">
  <source src="VIDEOS/fpro.mp4">
  <source src="movie.ogg" type="video/ogg">
Your browser does not support the video tag.
</video>

# 5. 组装
<br>
 <img style="float: center;" width=500 src="IMAGE/fpro.jpg">

<br>

 <video style="float:center;" width="720" height="340" autoplay="autoplay">
  <source src="VIDEOS/fpro2.mp4">
  <source src="movie.ogg" type="video/ogg">
Your browser does not support the video tag.
</video>



# 6. 示范
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