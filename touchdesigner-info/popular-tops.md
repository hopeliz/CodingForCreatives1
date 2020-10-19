# Popular TOPs

Texture operators \(TOPs\) are colored purple and manipulate 2D images and videos.

![](../.gitbook/assets/image%20%28179%29.png)

## Basics

### Null TOP

Provides a snapshot of sorts of a point within your network. Commonly used to help look at the effects of major changes later and remove them easily when necessary.

![](../.gitbook/assets/image%20%28172%29.png)

### Constant TOP

Provides a solid color chosen by a color picker or RGB values. Can adjust transparency.

![](../.gitbook/assets/image%20%28175%29.png)

### Noise TOP

For when you want some randomness.

![With Monochrome off](../.gitbook/assets/image%20%28158%29.png)

{% hint style="info" %}
Using **absTime.seconds** in different parameters can make this move!
{% endhint %}

![](../.gitbook/assets/tdnoisetop.gif)

### Switch TOP

Takes in multiple texture operators \(TOPS\) and creates an array. A single element of the array can be accessed by the Switch TOP's Index parameter. ALSO, for TOPs, you can blend between each element. This is great for fading in and out images and videos or representing number values as shades of color.

![](../.gitbook/assets/tdswitchtop.gif)

## Effects

### Blur TOP

Adds Blur

![](../.gitbook/assets/image%20%28138%29.png)

### Crop TOP

Crops image

![](../.gitbook/assets/image%20%28154%29.png)

### Mirror TOP

Mirrors part of the image.

![](../.gitbook/assets/image%20%28159%29.png)

## Shapes / Primitives / Transforms

### Circle TOP, Rectangle TOP, Text TOP

Creates shapes or text

![](../.gitbook/assets/image%20%28184%29.png)

### Transform TOP

Manipulates position, rotation, scale, etc.

![](../.gitbook/assets/image%20%28171%29.png)

## Images and Videos

### Movie File In TOP

Load any image or video. This banana image is a default image.

![](../.gitbook/assets/image%20%28143%29.png)

### Movie File Out TOP

Exports animation, image, and video files.

### Video Device In TOP

Webcam or any other camera attached.

### Video Device Out TOP

A way to output to a video device.

## Blending Modes

The best one is Composite TOP where you can choose the mode within the parameters, but TOPs exist for individual modes.

### Composite TOP

Blends two TOP operators into a single image - similar to blending two Photoshop layers. The layer mode can be updated through the Operation parameter.

![](../.gitbook/assets/image%20%28163%29.png)

![](../.gitbook/assets/image%20%28153%29.png)



