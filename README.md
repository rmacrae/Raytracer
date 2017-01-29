# Raytracer

After discovering Andrew Kensler's version of Paul Heckbert's Ray Tracer Business Card Challenge, I thought that it would be interesting
to create a version of the raytracer that would easily accept anyone's initals and render an image with them.

Andrew Kensler's version can be found here: http://eastfarthing.com/blog/2016-01-12-card/

Kensler's version of the raytracer uses an integer array (1x9), which renders a sphere every place there is a 1 when every number
in the integer array is converted back to binary.

In order to allow the raytracer to render anyone's initials, I created a text file with the letters drawn out with 1's.  The program
will then search the file for the letters entered by the user and add them to a 7x21 array.  Once the letters are in the array, then
the program will read each line and convert the lines from a binary string to integers, which are then saved into a 1x7 integer array.

The rest of the ray tracer functions uses Kensler's design, with the only changes being the colors of the "sky" in the image
and the resolution of the image, which was increased to reduce the size of the initials, relative to the total image.

The resulting image is saved in a ppm image with a resolution of 1024x1024.  This can be easily converted to another format using the
"convert" command in linux.

An example of the final product using my initials (jrm) can be seen below: 

![alt tag](https://github.com/rmacrae/Raytracer/blob/master/image.jpg)
