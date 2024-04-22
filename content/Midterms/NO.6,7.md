## Displaying an Image in Processing

Here’s a program that displays an image; note that this assumes there’s an image named [`kandinsky.jpg`](https://courseskmu.github.io/processing/downloads/kandinsky.jpg) (which is 1098 pixels wide, and 757 pixels high) in your program’s `data` folder:

```
PImage imgw;
void setup(){
 size(400,400); 
 imgw = loadImage("Untitled.jpg");
}
void draw(){
 tint(0, 153, 204, 126);
 image(imgw,0,0);
  //filter(THRESHOLD, 0.5);
  filter(GRAY);
  //filter(INVERT);
  //filter(POSTERIZE, 4);
  //filter(BLUR, 6);
  //filter(ERODE);
  //filter(DILATE);
}
```
THRESHOLD  
Converts the image to black and white pixels depending on if they are above or below the threshold defined by the level parameter. The parameter must be between 0.0 (black) and 1.0 (white). If no level is specified, 0.5 is used.  
  
GRAY  
Converts any colors in the image to grayscale equivalents. No parameter is used.  
  
OPAQUE  
Sets the alpha channel to entirely opaque. No parameter is used.  
  
INVERT  
Sets each pixel to its inverse value. No parameter is used.  
  
POSTERIZE  
Limits each channel of the image to the number of colors specified as the parameter. The parameter can be set to values between 2 and 255, but results are most noticeable in the lower ranges.  
  
BLUR  
Executes a Gaussian blur with the level parameter specifying the extent of the blurring. If no parameter is used, the blur is equivalent to Gaussian blur of radius 1. Larger values increase the blur.  
  
ERODE  
Reduces the light areas. No parameter is used.  
  
DILATE  
Increases the light areas. No parameter is used.

```
PImage cat;
PImage dog;

void setup() {
  // load the image files from the "data" folder
  cat = loadImage("cat.jpg"); // 220 x 210
  dog = loadImage("dog.jpg"); // 240 x 180

  // apply some special effects
  cat.filter(POSTERIZE, 4);
  dog.filter(GRAY);

  // set the window to be big enough to display both images
  // side-by-side
  size(220 + 240, 210);
}

void draw() {
  // display the images side-by-side
  image(cat, 0, 0);
  image(dog, cat.width, 0);
}
```
*notes*
- you can apply filter to individual photos in the void setup function.
- image.width is apparently a thing.

## Copying an Entire Image

Suppose you want to display two copies of the same image. While you could call `loadImage` twice, that’s inefficient. Instead, `PImage` objects let you make copies using the `get()` function like this:

```
PImage original;
PImage duplicate;

void setup() {

  original = loadImage("cat.jpg");
  duplicate = original.get();  // makes a new copy of original
}
```

[[NO.8,9]]
