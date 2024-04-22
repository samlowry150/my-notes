The map function is used to stretch and shrink numbers into a given frame.
```
map(mouseX * mouseY, 0, 500 * 500, 0, 255)
```
map(VALUE TO BE STRETCHED AND SHRUNK, ORIGINAL SMALL, ORIGINAL HIGH, STRETCHED SMALL, STRETCHED HIGH );
```

PImage sunshine;
PImage sunshine2; //global variable

void settings()
{
  sunshine = loadImage("Untitled.jpg"); //what is sunshine?
  size(sunshine.width,2 * sunshine.height);
}
void draw()
{
   image (sunshine,0,0); //draw sunshine
   sunshine2 = sunshine.get(); //duplicate sunshine
   
   float t = map(mouseY,0,2 * sunshine.height,0,1.0); //map mouseY
  sunshine2.filter(THRESHOLD,t);   //filter sunshine
  image(sunshine2,0,sunshine.height); //draw sunshine2
}


```

## files and folders
**absolute path names** start from the root dir of the computer.

**relative path names** start from where you are in the file structure, and is therefore easy to share with other computers as you do not need to have the exact same file structure in order to use files.