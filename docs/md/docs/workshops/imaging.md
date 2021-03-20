# Image and video processing


>PImage image1, image2;
>void setup() {
>  size(1000, 1000);
>  image1 = loadImage("landscape.jpg");
>  image2 = loadImage("landscape.jpg");
>}

>void draw() {
>  background(0,0,0);
>  int halfImage = width*height/2;
>  image1.resize(1000,500);
>  image(image1, 0, 0);
>  loadPixels();
>  for (int i = 0; i < halfImage; i++) {
>      float r = 255-red(pixels[i]);
>      float g = 255-green(pixels[i]);
>      float b = 255-blue(pixels[i]);
>      color c = color(r,g,b);
>      pixels[i+halfImage] = c;
>  }
>  updatePixels();
>}

> :ToCPrevNext