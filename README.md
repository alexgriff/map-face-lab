# `map` Face Lab

![follow wherever you go](https://s3.amazonaws.com/upperline/curriculum-assets/p5js/labs/map-face.gif)

Woa! Excuse me, staring isn't very polite-- what's that-- you're using the `map` function-- o, how interesting!

If you think about it, the way the pupils are moving is *mapping* from the position of the mouse, which is a large range across the whole canvas, to a small range just within the white circles. That's just what the `map` function is designed for!

Use the provided starter code to get started trying to implement this. Notice that there are actually two thick rings (`ellipse`s with no `fill` and heavy `strokeWeight`) around the eyes that are the same color as the face and *above* most other elements.  You can use these to allow the range of the pupils to extend slightly beyond the diameter of the white circle.

Take a look at the [`map` documentation](https://p5js.org/reference/#/p5/map) if you need a refresher.

```javascript
function setup() {
  createCanvas(600, 600)
}

function draw() {

  noStroke();
  // yellow face
  fill(255, 225, 0);
  ellipse(width/2, height/2, 400, 400);

  // eye whites
  // Left
  fill(255)
  ellipse(width/2 - 80, height/2 - 60, 100, 100);

  // Right
  fill(255)
  ellipse(width/2 + 80, height/2 - 60, 100, 100);

  // pupils
  // Left
  fill(0)
  ellipse(width/2 - 80, height/2 - 60, 40, 50);

  // Right
  fill(0)
  ellipse(width/2 + 80, height/2 - 60, 40, 50);

  // Rings
  noFill();
  stroke(255, 225, 0)
  strokeWeight(40);
  ellipse(width/2 - 80, height/2 - 60, 130, 130);

  ellipse(width/2 + 80, height/2 - 60, 130, 130);

  // smile
  stroke(0);
  strokeWeight(8);
  noFill();
  arc(width/2, height/2, 300, 300, 0.25, PI - 0.25)

}

```

Once you get it working, play around with the values and the ranges. What if one axis has a much bigger range than the other, or both eyes move differently.  What if you reverse the starting and ending points of the range.

## Extended Challenges
Can you do anything else with this idea.

- The eyes could follow something that randomly moved across the screen.  What if the face was a frog whose eyes followed a fly as it randomly buzzed around and on a mouse click the frog caught the fly with it's tongue... just an idea!

- What if the entire face slowly moved but the eyes stayed fixated on a single point.

- Use the mouse moving up and down to open and close the face's mouth. Make it sing a long to your favorite song.

- While the mouse is pressed the face can grow sleepy:

 ![sleepyness](https://s3.amazonaws.com/upperline/curriculum-assets/p5js/sleepynes.gif)
