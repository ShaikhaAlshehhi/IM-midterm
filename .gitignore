// to make the snake's body
ArrayList<Integer> x = new ArrayList<Integer>(), y = new ArrayList<Integer>();




//global variables
int w=30, h=30, blockSize=20, dir=2, foodX=15, foodY=15, speedNum = 8, fc = 255, life = 30, score;

//font variable
PFont f; 

//coordinates for x and y
int[] Xdir={0, 0, 1, -1};
int[] Ydir={1, -1, 0, 0}; 

//game condition 
boolean gameOver=false;

  
import processing.sound.*;
SoundFile foodSound;

void setup() { 
  size(600, 600); 
  // font initializer
  f = createFont("Georgia", 35);
  //snake's starting position 
  x.add(0); y.add(15); 

  foodSound = new SoundFile(this, "0.aif");

  
}   

void draw() { 
  
  background(0);
  
  //snake's body color
  fill(3, 252, 169); 
  
  //snake's body
  for (int i = 0; i < x.size(); i++){
    
    rect(x.get(i)*blockSize, y.get(i)*blockSize, blockSize, blockSize);
    }
    
  if (!gameOver) { 
    // white food
    fill(fc); 
    ellipse(foodX*blockSize+10, foodY*blockSize+10, blockSize, blockSize); 
    // score on player screen
    textAlign(LEFT); 
    textFont(f);
    textSize(25);
    fill(255);
    text("score : " + x.size(), 30, 30, width - 20, 50);
    
    
    //add more blocks to the snake
    if (frameCount%speedNum==0) { 
      x.add(0, x.get(0) + Xdir[dir]); 
      y.add(0, y.get(0) + Ydir[dir]);
      
      
      
      
      // lives
      
      
      
      
      
      
      
      
      
      
      
        score = x.size();
        if (score >10 && score <20){
        
        
        
        
        
        
        
        }
      
      
      
      
      
      
      
      // game over if snake touches the window
      if (x.get(0) < 0 || y.get(0) < 0 || x.get(0) >= w || y.get(0) >= h) {
        
        life = life - 10;
    }
      
      // game over if the snake touches itself
      for (int i=1; i<x.size(); i++) 
        if (x.get(0)==x.get(i)&&y.get(0)==y.get(i)) life = life - 10; 
        
        
        //if (life == 0){
       
        //  gameOver = true;
        //}
        
         // eaitng food 
        if (x.get(0)==foodX && y.get(0)==foodY) { 
         if (x.size() %5==0 && speedNum>=2) speedNum-=1;  // speed increases every 5 points 
          foodSound.play();
         // generates new food position
        foodX = (int)random(0, w);
        foodY = (int)random(0, h);
       
 
      } else {
        // so that the snake size doesnt become infinite
        x.remove(x.size()-1); 
        y.remove(y.size()-1);
      }
    }
  }
  
  
  if (life == 20){
  
    life+=40;
    fill(255); 
    textSize(30); 
    textFont(f);
    textAlign(CENTER); 
    text("You Just Lost a Life\n 2 Remain \n Press ENTER", width/2, height/3+30);
    
    if (keyCode == ENTER){
      x.clear(); 
      y.clear(); 
      x.add(0);  
      y.add(15);
      dir = 2;
      speedNum = 8;
      gameOver = false;
      life =20;
    }
  
  }
  
  
  if (life ==10){
  
    
    life = 10;
    fill(255); 
    textSize(30); 
    textFont(f);
    textAlign(CENTER); 
    text("You Just Lost a Life\n 1 Remain \n Press ENTER", width/2, height/3+30);
    
    if (keyCode == ENTER){
      x.clear(); 
      y.clear(); 
      x.add(0);  
      y.add(15);
      dir = 2;
      speedNum = 8;
      gameOver = false;
      life = 10;
    }
  
  }
  
  
  
  if (life == 0) {
    // game is over screen
    fill(255); 
    textSize(30); 
    textFont(f);
    textAlign(CENTER); 
    text("GAME OVER \n Your Score is: "+ x.size() +"\n Press ENTER", width/2, height/3+30);
    if (keyCode == ENTER) { 
      x.clear(); 
      y.clear(); 
      x.add(0);  
      y.add(15);
      dir = 2;
      speedNum = 8;
      gameOver = false;
    }
  }
}









void keyPressed() { 
  int newDir=keyCode == DOWN? 0:(keyCode == UP?1:(keyCode == RIGHT?2:(keyCode == LEFT?3:-1)));
  if (newDir != -1) {
  
    dir = newDir;
    
  

}
}
