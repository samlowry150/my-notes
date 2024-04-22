```
void setup() {
  size(500, 500);
}

void draw() {
  ellipse(mouseX, mouseY, 40, 40);
}
```
The **void setup()** function is **called** precisely _once_ at the _start_ of your program.

the **void draw()** is called upon around 60 times per second.

## Ellipse Parameters

Lets stop for a moment and look in more detail at the ellipse function. You call the ellipse function by writing a statement that looks like this:

```
ellipse(x, y, width, height);
```

[[NO.3]]