# CLASS TRIAL

-------

WE ARE DOING THE CODING IN THE P5.JS SITE.

```
var posX=200;
function setup () {
createCanvas(400,400);

}
```

var means we are creating a memory for anything (in the above given code I have created a memory for posX=200).

function setup () {} it's a command given to the program to keep every thing on the place.

We give semi-colon as a full stop.



```
function draw () {
background ("white");
rect(380,mouseY,10,70);
rect(10,150,10,70);
rect(posX,200,10,10);
posX=posX+1;
}
```

We are creating 3 objects in the game that are computerPaddle, playerPaddle, ball.

mouseY command is used for moving the paddle up and down.

Background is used for hiding the loops created on the screen.





# CLASS 1

-----

```
var playerPaddle;

function setup(){
  createCanvas(400,400);
  //player Paddle
  playerPaddle = new Paddle();
}
```

We have made a memory for the playerpaddle above the function setup(){}

We are creating a new playerpaddle.

------------



```
function draw() {
  //set background to white
  background("white");
  
  
  playerPaddle.xPosition = 390;
  playerPaddle.yPosition = mouseY;
  
  playerPaddle.display();
  
```

Here we are giving the background color to hide the loops.

We are giving the player paddle position of X axis=390.

Here we are giving a command to control the Y axis of playerpaddle.

We are also giving a command to display the playerpaddle.

------------



```
//computer paddle
  var computerPaddle = new Paddle();
  computerPaddle.xPosition = 0;
  computerPaddle.yPosition = 150;
  
  computerPaddle.display();
  
  //draw the ball
  rect(200,200,10,10);
}
```

Here we are creating the computerpaddle as our second player.

We are also giving the X and Y axis to the computerPaddle.

We are giving a command to display the computerpaddle.

We are also making a ball to play. 

rect(200 (Xposition),200(Yposition),10(width),10(height))

# CLASS 2

-------------------------

---------------

IN THIS WE ARE DOING THE CODING IN THE CODE.ORG SITE.

```
var ball=createSprite(200,50,20,20);
ball.shapeColor="white";
ball.velocityX=0;
ball.velocityY=-5;
```

Here I have created  a ball which is a square. It has been placed 200X axis and 50Y axis and its height and width are 20.

It's color is white. I have given a velocityY=-5 to move the ball upwards.

------------



```
ball.velocityX=0;
ball.velocityY=5;
```

Here I have given a velocityY=5 means the ball will move downwards.

-----------



```
ball.velocityX=5;
ball.velocityY=0;
```

Here I have given velocityX=5 means the ball will move toward right.

------

```
ball.velocityX=-5;
ball.velocityY=0;
```

Here I have given velocityX=5 means the ball will move toward left.

----------

```
 createEdgeSprites();
```

This code should typed in function draw() {}. this code creates the edges in the game.

----------

```
ball.bounceOff(edges);
```

This command is used for ball to bounce off the edges. This command is typed under the createEdgeSprites(); command.

-------------



```
  ball.bounce(ball2);
```

this command is used for the ball to bounce off the another ball. This command is typed under the ball.bounceOff(edges); command.

-------

```
drawSprites();
```

This command is typed under the function draw() {}. This command is used to display the objects or sprites on the screen.

# CLASS 3

------

----

In this class I learn so much things.

Let's start.

In my third class I learned. How to show any text on the screen, How to show any text when any thing touches anything, How to control anything with arrow like in the game, How to move any thing with arrow only one step when clicked once and How to change the position of anything when it touches anything like a obstacle.

The first command is How to show text anywhere on the Screen and the command is  -    

 `text("anything you want to show there",15,25);`  

I will give a example  -  If I want to indicate that the ball is on the 15X axis and 25Y axis then I will use this [above given command] in the `function draw()`;  the code like this  -     text("ball",15,25); 



The next command is How to show any text when any thing touches anything  - 

        if ( ball.isTouching(goal)) { 
    textSize(40); 
    stroke("red"); 
    text("You Win", 200,200); }

The above command used when the ball reaches its goal and on the screen the text is given - You Win - and the color of the text is red, and the text size is 40.

The next command is How to control anything with arrow like in the game - 

 

```
 `if (keyDown("UP_ARROW")) {`
    `ball.velocityX=0;`

`ball.velocityY=-4;`

`}`
```



The above command is when we press up arrow the ball will move up when you press the arrow key once it will move up wards continuously.

----





   `if (keyDown("DOWN_ARROW")) {`
    `ball.velocityX=0;`
`ball.velocityY=4;`



  `}` 

The above command is when we press down arrow the ball will move down when you press the down key once it will move down wards continuously.



.............................................................................................................................................................................................



   `if (keyDown("RIGHT_ARROW")) {`
    `ball.velocityX=4;`
`ball.velocityY=0;`



  `}` 

The above command is when we press right arrow the ball will move right when you press the right key once it will move right continuously.

.............................................................................................................................................................................................



   `if (keyDown("LEFT_ARROW")) {`

​    `ball.velocityX=-4;`
`ball.velocityY=0;`



  `}` 

The above command is when we press left arrow the ball will move left when you press the left key once it will move left continuously.

.............................................................................................................................................................................................

The next command is  -  How to move any thing with arrow only one step when clicked once

    if(keyWentUp(UP_ARROW) || keyWentUp(DOWN_ARROW)|| keyWentUp(RIGHT_ARROW)|| {keyWentUp(LEFT_ARROW)){
    ball.velocityX=0;
    ball.velocityY=0;}

  }

When you use this and the above given commands together then the ball will move only one step further.

.............................................................................................................................................................................................

The next command is - How to change the position of anything when it touches anything like obstacle.

    if (ball.isTouching(obstacle)) {
    
    ball.x=10;
    ball.y=10;
    }

Use this command in the function draw () { then it will work.

----



# CLASS 4 

-----

-----

```
//creating ball for pong game
var ball= createSprite(200,200,10,10);
//giving ball a color
ball.shapeColor="red";

//creating playerPaddle to play
var playerPaddle=createSprite(380,200,10,100);
//giving playerPaddle color 
playerPaddle.shapeColor="yellow";

//creating computerPaddle as our opponent
var computerPaddle=createSprite(20,200,10,100);
//giving computerPaddle color
computerPaddle.shapeColor="black";
```

Here we are making memory for the ball and the playerpaddle and computerpaddle. We are also giving the shape and the color to the objects.



# CLASS 5

------

-----

In this class I learned how to create a row or how to create a line or a net using a loop.

```
for (var i = 0; i < 400; i=i+20) {
   line (200,i , 200, i+10);
```

Here I am creating a line with the help of loops.

i+20 stands for length for each and every line.

i+10 stands for distance between the lines



```
function serve() {
  ball.velocityX = 14;
  ball.velocityY = 14;
}
```

Here I have made a new function for the serve state. When the ball serves then the  velocity of the ball is 14.

```
function reset() {
  ball.x = 200;
  ball.y = 200;
  ball.velocityX = 0;
  ball.velocityY = 0;
}
```

Here I have set the ball x position when the ball resets. And the ball velocity will be 0.

# CLASS 6

-----

-------

In this class I learned .In every game there are game states that are as per how is the game is it a Infinite game or it is a normal game.

```
var gameState = "serve";
```

Here we are creating a memory for our game state you will learn about it later in this chapter.

------



```
var computerScore=0;
var playerScore=0;
```

Here we are creating a memory for the scores.

```
computerpaddle.x = ball.x;
```

Here we are creating a artificial Intelligence to the computerpaddle to not to be defeated in the game.

```
  if (gameState === "serve") {
    textSize(30)
    text("Press Space to Serve",100,180);
  }
```

  Here we are  giving text serving the ball when clicked space.

```
   text(computerScore,10,100);
   text(playerScore,10,300);
```

Here we are telling the program to show the scores.

```
   if (keyDown("up")){
     if(playerpaddle.y)
    {
      playerpaddle.y = playerpaddle.y-10;
    }
   }
```

Here we are telling the program that not to let the playerpaddle go above 250 and we are controling the playerpaddle.



```
   if (keyDown("down")){
     if(playerpaddle.y)
     {
       playerpaddle.y =playerpaddle.y+10;
     }
   }
```

Here we are telling the program that not to let the playerpaddle go below 120 and we are controling the playerpaddle.

```
computerpaddle.x = ball.x;

if (ball.isTouching(goal1) ||ball.isTouching(goal2) )
{
  if(ball.isTouching(goal2))
  {
    computerpaddleScore=computerpaddleScore + 1;
  }

  if(ball.isTouching(goal1))
  {
    playerpaddleScore = playerpaddleScore +1;
  }
  reset();
  gameState ="serve";
}
```

Here we are giving the scores to the playerpaddle and computerpaddle. before this we were starting the game when clicked space.

```
if (playerpaddleScore===8||computerpaddleScore===8){
   gameState="over";
//giving a size to game over
    textSize(30);
   text("game over",150,150);
   //giving size to press r to restart
   textSize(30);
   text("press r to restart",120,190);
 } 
```

Here we are creating a limit for the game when the scores reach 8 then the game is over. And we are giving the text as press restart.

```
 if (keyDown("r")){
    gameState="serve";
  //resetting the scores of computerpaddle and playerpaddle
  computerscore=0;
  playerscore=0;
  
  }
```

Here we are giving the command that when we press r then the game will reset and then the scores will also reset.

```
if (keyDown("space") && gameState === "serve") {
    serve();
    gameState = "play";
  }
```

And here the command is when we click on the space button then the gameState will change into play state.

```
function serve() {
  ball.velocityX = 10;
  ball.velocityY = 10  ;
}
```

We have made a new command for to serve the ball. When the ball will serve then the ball velocity will be velocityX=10 and the velocityY =10;

```
function reset() {
  ball.x = 200;
  ball.y = 200;
  ball.velocityX = 0;
  ball.velocityY = 0;
}
```

And when the game will reset then the ball will be on the center of the game and the ball and the computerpaddle will also stop.

# CLASS 7

---------------

----------------

 In this class I learned how to give the animations to the game.

First we need to insert a animation or a png Image and go in the animation section.

![](C:\Users\Ketan\Pictures\Screenshots\Screenshot (6)_LI.jpg)



--------------------

Here we will add a new Animation.

![](C:\Users\Ketan\Pictures\Screenshots\Screenshot (7)_LI.jpg)



And from here we can add a animation.

And then add his name then  do like given below.

```
var  tomato = createSprite(100, 50, 20, 20);
   tomato.setAnimation("tomato");
   tomato.scale=0.5;

}
```

Here I have gave a animation to a object or a sprite 

# CLASS 8

-----------------------

In this class I learned how to give the sound to to the game.

```
  playSound("sound123.mp3", true);
```

This code will play the sound123, if you will put false in the place of true then it will not play.

If you put it in the function setup it will play the sound till the game ends.

# CLASS 9

--------------------

In this I was doing the coding in the p5.js editor again.

In this p5.js editor I was making the trex game.

```
function preload(){}
```

This was a new function. In this function we will add animations in this function then we will give the animations to the trex and the other things in the game but in this game you need to see the animations in the library.

![]()![Screenshot (31)_LI](C:\Users\Ketan\Pictures\Screenshots\Screenshot (31)_LI.jpg)

In this section you will find the animations but you will need to add the animations in this also.

```
function preload(){
  trex_running = loadAnimation("trex1.png","trex3.png","trex4.png");
```

Like this you will need to add the animation.

```

function preload(){
  trex_running = loadAnimation("trex1.png","trex3.png","trex4.png");
  groundImage = loadImage("ground2.png")
}

```

Here I have the Image of the ground. Like this we will add the animations and the Images in the game.

```
  trex = createSprite(50,160,20,50);
  trex.addAnimation("running", trex_running);
    trex.scale = 0.5;
  trex.x = 50
```

This is how you will add the animation to the trex. This function works in the function setup.

And you will also need to add the scale to the animation.

```
  console.log(trex.y)
```

In this p5.js we are using the console because after this game we are making the angry birds game so we will use the console.

This function is wrote in the function draw. And this will show the position of the y position of the trex.

```
  trex.velocityY = trex.velocityY + 1;
```

Here we are creating the gravity for the trex to come back to the ground.

```
  trex.collide(edges[3])
```

This is for the trex to walk on the edges.

# CLASS 10

---------

---------

```
ground = createSprite(200,180,400,20);
ground.addImage("ground",groundImage);
ground.x = ground.width /2;
ground.velocityX = -4;
```

Here I have created a ground and added a Image next and I have set the width so that it won't be end and I have gave the velocity to the ground so that we see a illusion that the trex is moving.

```
if (ground.x < 2) {
  ground.x = ground.width / 2;
}
```

We are looping the ground so the ground never ends.

# CLASS 11

------------

-----------

```
var invisibleGround;
```

Here we created a memory for the invisibleGround.

```
  invisibleGround = createSprite(200,190,400,10);
  invisibleGround.visible = false;
```

Here we are creating the invisible Ground so that the trex will look like the trex is running on the sand.

```
  if(keyDown("space")&& trex.y >= 100) {
    trex.velocityY = -10;
  }
```

Here we are giving a command for the trex to jump and we are also giving the command so that the trex won't go above 100.

```
trex.collide(invisibleGround);
```

We are telling the trex to collide on invisible Ground so that the trex will look like the trex is running on the sand.

```
function spawnClouds() {
  //write code here to spawn the clouds
  if (frameCount % 60 === 0) {
     cloud = createSprite(600,100,40,10);
    cloud.y = Math.round(random(10,60));
    cloud.addImage(cloudImage);
    cloud.scale = 0.5;
    cloud.velocityX = -3;
    
     //assign lifetime to the variable
    cloud.lifetime = 134;
    
    //adjust the depth
    cloud.depth = trex.depth;
    trex.depth = trex.depth + 1;
    
    //adding cloud to the group
   cloudsGroup.add(cloud);
  }
  
}
```

Here I have created a new function to spawnClouds and then the clouds are formed in the 10,60 y axis. The lifetime is very important for  the clouds to pass all the way out and the clouds depth is for the clouds to be above the trex.

-----------



# CLASS 12

-----------

-------

In this class I learned how to make the obstacles, and made a group of obstacles, I also made a score for it.

```
var obstaclesGroup,obstacle1,obstacle2,obstacle3,obstacle4,obstacle5,obstacle6;
```

First I made a variable for the group of obstacles and the made the other obstacles (obstacle1,obstacle2,obstacle3,obstacle4,obstacle5,obstacle6).

```
var score;
```

I also made a variable for the score.

```
 
  function preload(){
  
  obstacle1 = loadImage("obstacle1.png");
  obstacle2 = loadImage("obstacle2.png");
  obstacle3 = loadImage("obstacle3.png");
  obstacle4 = loadImage("obstacle4.png");
  obstacle5 = loadImage("obstacle5.png");
  obstacle6 = loadImage("obstacle6.png");
  }
```

I also added the img for the obstacles in function preload.

```
  console.log("Hello"+  "white")
```

We were also working on console.log.

```
  score=0;
```

We made the score in function setup and then we will add the left over one in the function draw ( ){}.

```
  score=score+Math.round(frameCount/60);
  text("score - "+score,500,50);
```

And this in the left over one that we are making in the function draw. its a math code when we increase the number that divides The number with frame count the speed will decrease of the score. 

The text is for to show the score on the top corner in the right.

```
  spawnClouds();
  spwanObstacles();
```

In function draw we also put a code to spwan the obstacles. and then we will also make a function for the spwan obstacles.

```
function spwanObstacles() {
  
  if (frameCount%60===0) {
    var obstacle=createSprite(600,170,10,40);
    obstacle.velocityX=-6;
    var rand=Math.round(random(1,6));
    switch (rand) {
      case 1:obstacle.addImage(obstacle1);
                   break;
        
            case 2:obstacle.addImage(obstacle2);
                   break;
                         case 3:obstacle.addImage(obstacle3);
                   break;
                         case 4:obstacle.addImage(obstacle4);
                   break
                         case 5:obstacle.addImage(obstacle5);
                   break;
                         case 6:obstacle.addImage(obstacle6);
                   break;
                   default:break;
        
        
        
    }
  obstacle.scale=0.5;
    obstacle.lifetime=400;
  }
  }
```

we have made a new function for the spwan obstacles.

the frame count counts the frame and sends the obstacles.

then we create a sprite.

and gave the velocity.

then again a math code the math code is used to send the random obstacles from (obstacle1) to (obstacle6).

below switch rand there is a case1. It adds the images to the obstacle one and the other ones.

and the break is used for not to continue the same image continously.

then we are giving default to continue the same process again and again.

------

# CLASS 13

------------

```
var PLAY = 1;
var END = 0;
var gameState = PLAY;

```

We are making a memory for the play and end state. The play state is the important section that's why we are creating game state play.

```
if(gameState === PLAY){
   
    if(obstaclesGroup.isTouching(trex)){
        gameState = END;
    }
  }
```

we are creating a if condition for the game state play. Inside the play state we will keep commands for jumping the trex, making the ground move continously, giving gravity to the trex, giving velocity to the trex and tthe ground to move, creating the clouds and the obstacles. The if conditions is for to enter in the end state so that the obstacles stop when the trex touches it.

```
else if (gameState === END) {
      ground.velocityX = 0;
     
     obstaclesGroup.setVelocityXEach(0);
     cloudsGroup.setVelocityXEach(0);
   }
  
 
```

We are giving the else condition because when the obstacle touches the trex it should stop the ground, obstaclesGroup, cloudsGroup.

# CLASS 14

------------------------

```
 trex.setCollider("circle",0,0,40);
  trex.debug = true
```

We are now making a collider for trex .When the obstacle touches the collider 



```
var jumpSound , checkPointSound, dieSound;
```

We made a variable for the jumpsound, checkpointsound and for diesound.

```
function preload(){
jumpSound = loadSound("jump.mp3")
  dieSound = loadSound("die.mp3")
  checkPointSound = loadSound("checkPoint.mp3")
}
```

Then in function preload we added the sound.

# CLASS 15

--------------

```
if(mousePressedOver(restart)) {
      reset();
    }
```

In function draw we are giving command that when we click on the restart button then the game will reset.

# CLASS 16

--------------------------

```
  trex.setCollider("rectangle",0,0,trex.width,trex.height);
  trex.debug = true
```

Now we are making a rectangle collider for the trex and we are debuging it.

```
ground.velocityX = -(4 + 3* score/100)
```



# CLASS 17

---------------

```
function reset(){
  gameState = PLAY;
  gameOver.visible = false;
  restart.visible = false;
  
  obstaclesGroup.destroyEach();
  cloudsGroup.destroyEach();
  
  trex.changeAnimation("running",trex_running);
  
  if(localStorage["HighestScore"]<score){
    localStorage["HighestScore"] = score;
  }
  console.log(localStorage["HighestScore"]);
  
  score = 0;
  
}
```

in function reset we are telling to hide gameOver and restart button to hide then in the second line we are telling that to destroy all the clouds and the obstacles then we are changing the animation and in the last we are reseting the score.

```
if(mousePressedOver(restart)) {
      reset();
    }
  }
  
```

here we are telling the program that when the user presses the restart button then redirect to function reset.

# CLASS 18

-----------







# CLASS 20- 33

-------------

baseclass.js

```

class BaseClass{
    constructor(x, y, width, height, angle) {
        var options = {
             // restitution is the bounciness of the object
            'restitution':0.8,
            'friction':1.0,
            'density':1.0
        }
        this.body = Bodies.rectangle(x, y, width, height, options);
        this.width = width;
        this.height = height;
        this.image = loadImage("sprites/base.png");
        // world is a imaginary world created for the objects using matter.js library
        World.add(world, this.body);
      }
      display(){
        var angle = this.body.angle;
        //push is for changing positions
        push();
        //translate is used for updating all the positions
        translate(this.body.position.x, this.body.position.y);
        //rotate is used to give angles in the program
        rotate(angle);
        //for keeping image in center of the screen , no matter what is the canvas size
        imageMode(CENTER);
        image(this.image, 0, 0, this.width, this.height);
        //pop is used for to reset
        pop();
      }
}
```

----------

bird.js

```
//extends is used for refering it to parent file 
class Bird extends BaseClass {
  constructor(x,y){
    //extracting all the information
    super(x,y,50,50);
    this.image = loadImage("sprites/bird.png");
    this.smokeImage = loadImage("sprites/smoke.png");
    //the path followed - it will follow the bird movement 
    this.trajectory =[];
  }

  display() {
    //this.body.position.x = mouseX;
    //this.body.position.y = mouseY;

    super.display();
    // it is used for the trajectory to follow the bird when flying
    if(this.body.velocity.x > 10 && this.body.position.x > 200){
      var position = [this.body.position.x, this.body.position.y];
      this.trajectory.push(position);
    }
   
    // loop is used to give the clouds on the screen
    for(var i=0; i<this.trajectory.length; i++){
      image(this.smokeImage, this.trajectory[i][0], this.trajectory[i][1]);
    }
  }
}

```

-------------



ground.js

```
class Ground {
    constructor(x,y,width,height) {
      var options = {
          isStatic: true
      }
      this.body = Bodies.rectangle(x,y,width,height,options);
      this.width = width;
      this.height = height;
      World.add(world, this.body);
    }
    display(){
      var pos =this.body.position;
      rectMode(CENTER);
      fill("brown");
      rect(pos.x, pos.y, this.width, this.height);
    }
  };

```

------------

pig.js

```
class Pig extends BaseClass {
  constructor(x, y){
    super(x,y,50,50);
    this.image = loadImage("sprites/enemy.png");
    // any thing which is visible on the screen 
    //255 stands for white color and 0 is for black
    this.Visiblity = 255;
  }

 display(){
   //console.log(this.body.speed);
   // when the speed is less than 3 then the pig will be on the screen
   if(this.body.speed < 3){
    super.display();
   }
   //when the speed is greater than 3 then the pig will disappear
   else{
    //removing the world for the pig
     World.remove(world, this.body);
     push();
     //for slowly fading away for the pig
     this.Visiblity = this.Visiblity - 5;
     //for balancing the colors on the screen
     tint(255,this.Visiblity);
     image(this.image, this.body.position.x, this.body.position.y, 50, 50);
     pop();
   }
  }

  //it will calculate the time till the pig completely fade away
  score(){
    if (this.Visiblity < 0 && this.Visiblity > -1005){
      score++;
    }
  }



};
```



-------------------

sketch.js

```
//const is used for memory for physics conditions applied (on objects )
// engine is the object on which the physics conditions are applied 
//world is used for making a world for the object 
//Body is for giivng a physical apperance of object on screen 
const Engine = Matter.Engine;
const World= Matter.World;
const Bodies = Matter.Bodies;
//constraint is a force which will help the object to come on its orignal place
const Constraint = Matter.Constraint;

var engine, world;
var box1, pig1,pig3;
var backgroundImg,platform;
var bird, slingshot;

var gameState = "onSling";
var bg = "sprites/bg1.png";
var score = 0;

function preload() {
    getBackgroundImg();
}

function setup(){
    var canvas = createCanvas(1200,400);
    engine = Engine.create();
    world = engine.world;


    ground = new Ground(600,height,1200,20);
    platform = new Ground(150, 305, 300, 170);

    box1 = new Box(700,320,70,70);
    box2 = new Box(920,320,70,70);
    pig1 = new Pig(810, 350);
    log1 = new Log(810,260,300, PI/2);

    box3 = new Box(700,240,70,70);
    box4 = new Box(920,240,70,70);
    pig3 = new Pig(810, 220);

    log3 =  new Log(810,180,300, PI/2);

    box5 = new Box(810,160,70,70);
    log4 = new Log(760,120,150, PI/7);
    log5 = new Log(870,120,150, -PI/7);

    bird = new Bird(200,50);
//Pi stands for the angle 180 degree
    //log6 = new Log(230,180,80, PI/2);
    slingshot = new SlingShot(bird.body,{x:200, y:50});
}

function draw(){
    if(backgroundImg)
        background(backgroundImg);
    
        noStroke();
        textSize(35)
        fill("white")
        text("Score  " + score, width-300, 50)
    // updating the changes inside the object
    Engine.update(engine);
    //strokeWeight(4);
    box1.display();
    box2.display();
    ground.display();
    pig1.display();
    pig1.score();
    log1.display();

    box3.display();
    box4.display();
    pig3.display();
    pig3.score();
    log3.display();

    box5.display();
    log4.display();
    log5.display();

    bird.display();
    platform.display();
    //log6.display();
    slingshot.display();    
}

function mouseDragged(){
    //if (gameState!=="launched"){
        Matter.Body.setPosition(bird.body, {x: mouseX , y: mouseY});
    //}
}


function mouseReleased(){
    slingshot.fly();
    gameState = "launched";
}

function keyPressed(){
    if(keyCode === 32){
        bird.trajectory=[];
        Matter.Body.setPosition(bird.body, {x:200, y:50});
       slingshot.attach(bird.body);
    }
}
//async not merging with the big data base
async function getBackgroundImg(){
    
    var response = await fetch("http://worldtimeapi.org/api/timezone/Asia/Kolkata");
    //JSON format of writing the web codes
    var responseJSON = await response.json();

    var datetime = responseJSON.datetime;
    var hour = datetime.slice(11,13);
    
    if(hour>=0600 && hour<=1900){
        bg = "sprites/bg1.png";
    }
    else{
        bg = "sprites/bg2.jpg";
    }

    backgroundImg = loadImage(bg);
    console.log(backgroundImg);
}
```

---------------

slinghshot.js

```
class SlingShot{
    constructor(bodyA, pointB){
        var options = {
            bodyA: bodyA,
            pointB: pointB,
            //giving rigidity so that it works like a  rubberband 
            stiffness: 0.04,
            length: 10
        }
        this.sling1 = loadImage('sprites/sling1.png');
        this.sling2 = loadImage('sprites/sling2.png');
        this.sling3 = loadImage('sprites/sling3.png');
        this.pointB = pointB
        //giving a property of a rubber band
        this.sling = Constraint.create(options);
        World.add(world, this.sling);
    }
    // function created for attaching the bird with the slingshot
    attach(body){
        this.sling.bodyA = body;
    }
    
    fly(){
        //null is 0
        this.sling.bodyA = null;
    }

    display(){
        image(this.sling1,200,20);
        image(this.sling2,170,20);
        if(this.sling.bodyA){
            var pointA = this.sling.bodyA.position;
            var pointB = this.pointB;
            push();
            
            stroke(48,22,8);
            if(pointA.x < 220) {
                strokeWeight(7);
                //adding multiple line to create the slingshot , as it works like a  rubberband 
                line(pointA.x - 20, pointA.y, pointB.x -10, pointB.y);
                line(pointA.x - 20, pointA.y, pointB.x + 30, pointB.y - 3);
                image(this.sling3,pointA.x -30, pointA.y -10,15,30);
            }
            else{

                //when bird will fly weight will be less 
                strokeWeight(3);
                //adding multiple line to create the slingshot , as it works like a  rubberband 
                line(pointA.x + 25, pointA.y, pointB.x -10, pointB.y);
                line(pointA.x + 25, pointA.y, pointB.x + 30, pointB.y - 3);
                image(this.sling3,pointA.x + 25, pointA.y -10,15,30);
            }
           
            
            pop();
        }
    }
    
}
```

--------------

# CLASS 34-37

----------------

form.js

```
class Form {

  constructor() {
    this.input = createInput("Name");
    this.button = createButton('Play');
    this.greeting = createElement('h2');
    this.title = createElement('h2');
  }
  hide(){
    this.greeting.hide();
    this.button.hide();
    this.input.hide();
    this.title.hide();
  }

  display(){
    this.title.html("Car Racing Game");
    this.title.position(displayWidth/2 - 50, 0);
    
    //adjusting the input and button position acording to the screen size
    this.input.position(displayWidth/2 - 40 , displayHeight/2 - 80);
    this.button.position(displayWidth/2 + 30, displayHeight/2);
2
    this.button.mousePressed(()=>{
      this.input.hide();
      this.button.hide();
      player.name = this.input.value();
      playerCount+=1;
      player.index = playerCount;
      player.update();
      player.updateCount(playerCount);
      this.greeting.html("Hello " + player.name)
      this.greeting.position(displayWidth/2 - 70, displayHeight/4);
    });

  }
}
```

------

game.js

```
class Game {
  constructor(){

  }

  getState(){
  
    var gameStateRef  = database.ref('gameState');
    //.on is used for extracting the data form the database
    gameStateRef.on("value",function(data){
       gameState = data.val();
    })

  }

  update(state){
    database.ref('/').update({
      gameState: state
    });
  }

  async start(){
    if(gameState === 0){
      player = new Player();
      var playerCountRef = await database.ref('playerCount').once("value");
      if(playerCountRef.exists()){
        playerCount = playerCountRef.val();
        player.getCount();
      }
      form = new Form()
      form.display();
    }

    car1 = createSprite(100,200);
    car2 = createSprite(300,200);
    car3 = createSprite(500,200);
    car4 = createSprite(700,200);
    cars = [car1, car2, car3, car4];
  }

  play(){
    form.hide();

    Player.getPlayerInfo();
    
    if(allPlayers !== undefined){
      //var display_position = 100;
      
      //index of the array
      var index = 0;

      //x and y position of the cars
      var x = 0;
      var y;

      for(var plr in allPlayers){
        //add 1 to the index for every loop
        index = index + 1 ;

        //position the cars a little away from each other in x direction
        x = x + 200;
        //use data form the database to display the cars in y direction
        y = displayHeight - allPlayers[plr].distance;
        cars[index-1].x = x;
        cars[index-1].y = y;

        if (index === player.index){
          cars[index - 1].shapeColor = "blue";
          camera.position.x = displayWidth/2;
          camera.position.y = cars[index-1].y
        }
       
        //textSize(15);
        //text(allPlayers[plr].name + ": " + allPlayers[plr].distance, 120,display_position)
      }

    }

    if(keyIsDown(UP_ARROW) && player.index !== null){
      player.distance +=10
      player.update();
    }

    drawSprites();
  }
}
```

----------

player.js

```
class Player {
  constructor(){
    this.index = null;
    this.distance = 0;
    this.name = null;
  }

  getCount(){
    var playerCountRef = database.ref('playerCount');
    playerCountRef.on("value",(data)=>{
      playerCount = data.val();
    })
  }

  updateCount(count){
    database.ref('/').update({
      playerCount: count
    });
  }

  update(){
    var playerIndex = "players/player" + this.index;
    database.ref(playerIndex).set({
      name:this.name,
      distance:this.distance
    });
  }
//static is used for the stable information on the screen 
//reffering it to database for the complete database
  static getPlayerInfo(){
    var playerInfoRef = database.ref('players');
    playerInfoRef.on("value",(data)=>{
      allPlayers = data.val();
    })
  }
}
```

------------

