rust-bmp
========
Small module for reading and writing bitmap images.
Currently only 24-bit BMP images is supported.

Usage
-----
Initialize a new image with the `new` function, specifying `width` and `height`.
```
let mut img = BMPimage::new(100, 100);
```
Edit image data using the `get_pixel` and `set_pixel` functions.
Save an image with the `save` function, specifying the `path`.
```
let pixel = img.get_pixel(0, 0);
img.set_pixel(50, 50, BMPpixel{r: 255, g: 255, b: 255});
img.save("path/to/img.bmp");
```
Open an existing image with the `open` function, specifying the `path`.
```
let mut img = BMPimage::open("path/to/img.bmp");
```
