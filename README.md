# hw3

# Classwork wrapup
# 1

var y = 250
var y2=y
var speed = 5;


function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(0);
  noStroke();
  
  rect(0,0,400,70);
  
  ellipse(200,y,50)
  
  ellipse(200,y2,50)

 if(y>height)
    speed=-1
    
  y=y+speed

  
}

# 2

function setup() {
  createCanvas(400, 400);
}

// track the circle to draw next frame
var x = 1000;
var y = 1000;
var x1=x
var y2=y

function draw() {
  colorMode(HSB);
  stroke(255);

  // draw circle with random hue
  fill(random(55), 100, 100);
  rect(x, y, 20, 20)
  rect(x1, y2, 45, 45)
  
  // set up next circle
  x = x + 25;

  // if we hit the right edge, go down a line
  if (x > width-25) {
    x = 25;
    y = y + 25;
  }

  // if we hit the bottom edge, reset to top
  if (y > height-25) {
    y = 25;
  }
}

# 3
var x = 210;
var y = 290;
var r = 0;

function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(0);
  noStroke();

  // draw smokestack
  fill(255);
  rect(195, height, 30, -100);

  // darker as it gets closer to 0
  fill(y);
  
  translate(x, y);
  rotate(r);
  rect(-111, -10, 250, 10);

  // up 3 pixels
  y -= 2;

  // rotate 0.05 radians ~= 2.8 degrees per frame
  r += 2

  // if reach past the top a bunch
  if (y < -300) {
    y = 290;
  }
}

#  Lawn Simulator

#  Answer the questions

A1)line(x, height-10, x+random(-10, 10), height-10-random(h));

A2) if (random() > 0.999) {
    fill(255);
    rect(0, 0, width, height-15);
    h = 10;
    
A3)h helps in determining the height that keeps changing-making animations happen by making it a variable.

A4)-10 ensures the existence,irregularity in height,height of the grass and how smoothly is grows bigger.

#  speedy-lawnmower.js.

function setup() {
  createCanvas(400, 200);
  colorMode(HSB);
}
 
var x = 0;
var h = 10;
 
function draw() {
  stroke(random(60, 70), 100, 90);
  line(x, height-10, x+random(-10, 10), height-10-random(h));
  noStroke();
 
  x = x + 1;
 
  if (x > width) {
    x = random(10);
    h = h + 3;
  }
 
  if (random() > 0.999) {
    fill(255);
    rect(0, 0, width, height-15);
    h = 10;
  }
 
  fill(40, 100, 60);
  rect(0, height-10, width, 10);
}

#  height-lawnmower.js

function setup() {
  createCanvas(400, 200);
  colorMode(HSB);
}
 
var x = 0;
var h = 10;
 
function draw() {
  stroke(random(60, 70), 100, 90);
  line(x, height-10, x+random(-10, 10), height-10-random(h));
  noStroke();
 
  x = x + 10;
 
  if (x > width) {
    x = random(10);
    h = h + 3;
  }
 
  if (h > 50) {
    fill(255);
    rect(0, 0, width, height-15);
    h = 10;
  }
 
  fill(40, 100, 60);
  rect(0, height-10, width, 10);
}

#  windy-lawnmower.js

function setup() {
  createCanvas(400, 200);
  colorMode(HSB);
}
 
var x = 0;
var h = 10;
 
function draw() {
  stroke(random(60, 70), 100, 90);
  line(x-50, height-10, x+random(-10, 10), height-10-random(h));
  noStroke();
 
  x = x + 10;
 
  if (x > width) {
    x = random(10);
    h = h + 3;
  }
 
  if (random() > 0.999) {
    fill(255);
    rect(0, 0, width, height-15);
    h = 10;
  }
 
  fill(40, 100, 60);
  rect(0, height-10, width, 10);
}

 










