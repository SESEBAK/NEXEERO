# 1. In-class Practice

<br>
<img style="float: center;" width=900 src="IMAGE/processing.png">

      int y = 180;
      int x = 0;

     void setup() {
      size (640, 640);
  
      strokeWeight (10);
     }

      void draw() {
      background(0); 
      stroke (255,0,100);
      line(0, y, width, y);
      y = y+1;
     if (y > 640) {
      y = 50;
     }
     stroke(100,0,100);
     line(x, 0, x, height); 
      x = x+50;
     if (x > 640) {
      x = 50;
     }
    
 
  
     }

# 2. Homework: Snake Game 
<br>
<img style="float: center;" width=900 src="IMAGE/snake.png">

     //BY Ian151 (ChromeWing)
     //inspired by the original snake game
     //this is a test for creating small games in processing.

     int angle=0;
     int snakesize=5;
     int time=0;
     int[] headx= new int[2500];
     int[] heady= new int[2500];
     int applex=(round(random(47))+1)*8;
     int appley=(round(random(47))+1)*8;
     boolean redo=true;
     boolean stopgame=false;
     void setup()
     {
     restart();
     size(400,400);
     textAlign(CENTER);
     }
     void draw()
     {
     if (stopgame)
     { 
      //do nothing because of game over (stop playing)
     }
     else
     {
      //draw stationary stuff
     time+=1;
     fill(255,0,0);
     stroke(0);
     rect(applex,appley,8,8);
     fill(0);
     stroke(0);
     rect(0,0,width,8);
     rect(0,height-8,width,8);
     rect(0,0,8,height);
     rect(width-8,0,8,height);
     //my modulating time by 5, we create artificial frames each 5 frames
     //(otherwise the game would go WAY too fast!)
     if ((time % 5)==0)
     {
      travel();
      display();
      checkdead();
      }
      }
     }
     //controls:
     void keyPressed()
     {
     if (key == CODED)
     {
     //what key was pressed? is the previous angle the opposite direction?
     //we wouldn't want to go backwards into our body, that would hurt!
     //also, is the previous body segment in front of the direction? 
     //(based on the previous question, but added for secure turning without suicide)
     if (keyCode == UP && angle!=270 && (heady[1]-8)!=heady[2])
     {
        angle=90;
     }
     if (keyCode == DOWN && angle!=90 && (heady[1]+8)!=heady[2])
     {
     angle=270;
      }if (keyCode == LEFT && angle!=0 && (headx[1]-8)!=headx[2])
     {
       angle=180;
      }if (keyCode == RIGHT && angle!=180 && (headx[1]+8)!=headx[2])
     {
       angle=0;
     }
     if (keyCode == SHIFT)
     {
      //restart the game by pressing shift
      restart();
       }
     }
     }
     void travel()
     {
     for(int i=snakesize;i>0;i--)
     {
     if (i!=1)
     {
      //shift all the coordinates back one array
      headx[i]=headx[i-1];
      heady[i]=heady[i-1];
     }
     else
     {
      //move the new spot for the head of the snake, which is
      //always at headx[1] and heady[1].
      switch(angle)
      {
        case 0:
        headx[1]+=8;
        break;
        case 90:
        heady[1]-=8;
        break;
        case 180:
        headx[1]-=8;
        break;
        case 270:
        heady[1]+=8;
        break;
      }
     }
     }
  
     }
     void display()
     {
     //is the head of the snake eating the apple?
     if (headx[1]==applex && heady[1]==appley)
     {
     //grow and spawn the apple somewhere away from the snake
     //(currently some of the code below might not be working, but the game still works.)
     snakesize+=round(random(3)+1);
     redo=true;
     while(redo)
     {
      applex=(round(random(47))+1)*8;
      appley=(round(random(47))+1)*8;
      for(int i=1;i<snakesize;i++)
      {
        
        if (applex==headx[i] && appley==heady[i])
        {
          redo=true;
        }
        else
        {
          redo=false;
          i=1000;
         }
       }
      }
     }
     //draw the new head of the snake...
     stroke(sinecolor(1),sinecolor(0),sinecolor(.5));
     fill(0);
     rect(headx[1],heady[1],8,8);
     //...then erase the back end of the snake.
     fill(255);
     rect(headx[snakesize],heady[snakesize],8,8);
  
     }
     void checkdead()
     {
     for(int i=2;i<=snakesize;i++)
     { 
      //is the head of the snake occupying the same spot as any of the snake chunks?
      if (headx[1]==headx[i] && heady[1]==heady[i])
     {
      fill(255);
      rect(125,125,160,100);
      fill(0);
      text("GAME OVER",200,150);
      text("Score:  "+str(snakesize-1)+" units long",200,175);
      text("To restart, press Shift.",200,200);
      stopgame=true;
      }
      //is the head of the snake hitting the walls?
      if (headx[1]>=(width-8) || heady[1]>=(height-8) || headx[1]<=0 || heady[1]<=0)
     {
      fill(255);
      rect(125,125,160,100);
      fill(0);
      text("GAME OVER",200,150);
      text("Score:  "+str(snakesize-1)+" units long",200,175);
      text("To restart, press Shift.",200,200);
      stopgame=true;
      }
     }
     }
     void restart()
     {
     //by pressing shift, all of the main variables reset to their defaults.
     background(255);
     headx[1]=200;
     heady[1]=200;
     for(int i=2;i<1000;i++)
     {
     headx[i]=0;
     heady[i]=0;
     }
     stopgame=false;
     applex=(round(random(47))+1)*8;
     appley=(round(random(47))+1)*8;
     snakesize=5;
     time=0;
     angle=0;
     redo=true;
     }
     float sinecolor(float percent)
     {
     float slime=(sin(radians((((time +(255*percent)) % 255)/255)*360)))*255;
     return slime;
     }

# 3. Group Exercise: Mouse Interaction
STEP 1: Setting up a tab for the player(mouse) with below code:
           class Player {
            //props
           float x,y,w,h;
 
           //constructor
            Player() {
            x = width/2;
            y = height/2;
            w = 100;
            h = 100;
           }
           //methods
           void update(){
  
           }
  
           void display(){
           fill(255,0,0);
            ellipse(x,y,w,h);
           }
          }

<br>
<img style="float: center;" width=500 src="IMAGE/proc1.png">

STEP 2: setting up the mouse movement

<br>
<img style="float: center;" width=700 src="IMAGE/proc2.png">

STEP 3: Adding another tab for the other circle
                        class Thing {
                         //props
                         float x,y,w,h,speedX,speedY;
                         color c;

                //constructor
                Thing() {
                x = random(100, width-100);
                y = random(100, height-100);
                w = 200;
                h = 200;
                speedX = random(-3,3);
                speedY = random(-3,3);
                c = color(random(255), random(255), random(255));
                }
                //methods
               void update(){
                 x += speedX;
                 y += speedY;
                }
  
               void display(){
                fill(c);
                ellipse(x,y,w,h);
               }
              }

<br>
<img style="float: center;" width=700 src="IMAGE/proc4.png">

STEP 4: Setting a change of background color when the circles intersect

<br>
<img style="float: center;" width=700 src="IMAGE/proc5.png">

STEP 5: Reducing the big circle from 200 to 50, and Adding 10 more circles. The red circle intercept the 10 small circles as they do a straight horizontal fall. 

<br>
<img style="float: center;" width=700 src="IMAGE/proc6.png">

STEP 6: FINAL OUTCOME

<br>
<video style="float:center;" width="900" height="540" controls autoplay="autoplay">
  <source src="VIDEOS/proc1.mp4">
  <source src="movie.ogg" type="video/ogg">
Your browser does not support the video tag.
</video>  

## FINAL CODES
### TAB 1: SKETCH
        Player p;
         //Thing t;
         Thing[] things;
         void setup (){
          size(800,600);
          p = new Player();
           //t = new Thing();
           things = new Thing[10];
          for(int i = 0; i < things.length; i++){
          things[i] = new Thing();
          }
         }

            void draw(){
            clearBackground();
            p.update();
            p.display();
            for(int i=0; i < things.length; i++){
            things[i].update();
            things[i].display();
            if (circleIntersect(p,things[i]) == true){
            fill(0,255,0,100);
            rect(0,0,width,height);
             things[i].caught();
            }
          }
         }

             void clearBackground(){
              fill(200,100);
              rect(0,0,width,height);
             } 

             boolean circleIntersect(Player a, Thing b){
              float sumOfRadii = a.w/2 + b.w/2;
             float distOfCenters = dist(a.x,a.y,b.x,b.y);
              if(distOfCenters < sumOfRadii) {
               return true;
              } else {
              return false;
             }
            }


### TAB 2: PLAYER
          class Player {
         //props
         float x,y,w,h;
 
          //constructor
          Player() {
            x = width/2;
            y = height/2;
            w = 100;
            h = 100;
         }
          //methods
         void update(){
            x = mouseX;
            y = mouseY;
         }
  
          void display(){
          fill(255,0,0);
          ellipse(x,y,w,h);
         }
         }

### TAB 3: THING
         class Thing {
          //props
         float x,y,w,h,speedX,speedY;
          color c;
          //constructor
          Thing(){
             x = random(100, width-100);
             y = random(100, height-100);
             w = 50;
             h = 50;
             speedX = 0;//random(-3,3);
             speedY = 5;//random(-3,3);
             c = color(random(255), random(255), random(255));
          }
           //methods
           void update(){
            x += speedX;
            y += speedY;
           checkBounds();
          }
  
           void display(){
             fill(c);
             ellipse(x,y,w,h);
          }
  
           void caught(){
            speedX = 0;
            speedY = 0;
            x = -1000;
          }
           void reset(){
            x = random(100, width-100);
            y = 0;
            speedX = 0;//random(-3,3);
            speedY = random(-3,7);
            c = color(random(255), random(255), random(255));
 
          }
            void checkBounds(){
              if(x<-w){x = width;}
              if(x>width){x=-w;}
              if(y<-h){y=height;}
              if(y>height){y=-h;}
          } 
        }