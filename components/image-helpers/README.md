
Helper Active Events for images
===============

This folder contains an Active Event called **[sys42.imaging.auto-crop-resize]**, which helps you crop and resize your images.
It requires the source image to crop and/or resize as its main **[_arg]** argument, and a **[destination]** to where to save
the transformed image. In addition it requires a **[size]** argument, containing two integer values as **[width]** and **[height]**.

Assuming you have an image called "zen.png" in your user's "temp" folder, below is an example of usage.

```
sys42.imaging.auto-crop-resize:~/temp/zen.png
  destination:~/temp/resized-zen.png
  size
    width:25
    height:25
```

The Active Event provides some math helpers, to automatically determine if and how to crop the image, to match the specified **[size]**,
becoming the output image's size. For instance, if you have an image that is 200x100 pixels, and you provide a destination size of 50x50, then
your destination image will be cropped by having 25% of its left and right parts removed, to make sure the image is not skewed in any ways.

