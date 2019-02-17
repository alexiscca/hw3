## What code draws the blades of grass?
```
var x = 0;
var h = 10;

function draw() {
  stroke(random(60, 70), 100, 90);
  // The next line draws individual "grasses" :-)
  line(x, height-10, x+random(-10, 10), height-10-random(h));
  noStroke();

  x = x + 10;

  if (x > width) {
    x = random(10);
    h = h + 3;
  }

}
```
  
  
## What code makes the "lawnmower" come by? How often does it come by?
```
  if (random() > 0.999) {
    fill(255);
    // Next line is what actually does the mow.
    rect(0, 0, width, height-15);
    h = 10;
  }

  fill(40, 100, 60);
  rect(0, height-10, width, 10);
```  
  
  This is a trick question because it’s a little bit random when the law mower comes. It comes when the random number generator, which generates numbers from 0 to 1, generates a number that’s > 0.999.
  
  
## What's the point of the h variable?
The h variable represents the height of the grass. It grows +3 everytime the grass grows across the full width of the canvas. 

## What does the -10 do in the second and fourth arguments of the line function, height-10-random(h)? Why is it there?
The -10 sets the grass to be drawn above the brown dirt. 



## What's the point of an object?
Objects help to organize variables that describe some entity and keep them in a neat and tidy way. 

## What's an example of a range you might use for the map function?
map(mouseX, 0, 600, 0, 255);

## What line of code would give me a random year in the last century?
random(1919, 2019);
