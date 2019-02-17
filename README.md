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

