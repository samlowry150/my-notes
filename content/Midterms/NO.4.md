### Lines

The processing function 
```
line(x, y, a, b)
```
draws a straight-line segment between the points (`x`, `y`) and (`a`, `b`).

By default, a rectangle is positioned by it’s upper-left corner, while an ellipse is positioned by it’s center.

### Quads

In  Processing, a `quad` is a quadrilateral, i.e. a polygon with 4 sides. The function `quad(a, b, c, d, e, f, g, h)` specifies the four corners of the quad: (`a`, `b`), (`c`, `d`), (`e`, `f`), and (`g`, `h`).

### Arcs

The Processing function `arc` draws a portion of the edge of an ellipse, i.e. an arc. It takes 6 or 7 inputs:
arc(x, y, w, h, startAngle, stopAngle,[drawMode]).
the angles are expected to be in radians.It may be more convenient to let the program do the converting for you with the function ```
```
radians(d)
```
![[스크린샷 2024-04-22 오후 12.31.36.png]]
## Drawing More Complex Shapes
```
void setup() {
  size(500, 500);
}

void draw() {
  background(255);
  beginShape();
  vertex(100, 100);
  vertex(200, 100);
  vertex(200, 200);
  vertex(300, 200);
  vertex(mouseX, mouseY);
  vertex(300, 300);
  vertex(100, 300);
  endShape(CLOSE);
}
```
 beginShape(POINTS) will draw just the points of the shape.
[[NO.5]]