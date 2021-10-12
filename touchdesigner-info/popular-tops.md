# Popular TOPs

Texture operators (TOPs) are colored purple and manipulate 2D images and videos.

![](<../.gitbook/assets/image (154).png>)

## Basics

### Null TOP

Provides a snapshot of sorts of a point within your network. Commonly used to help look at the effects of major changes later and remove them easily when necessary.

![](<../.gitbook/assets/image (162).png>)

### Constant TOP

Provides a solid color chosen by a color picker or RGB values. Can adjust transparency.

![](<../.gitbook/assets/image (163).png>)

### Noise TOP

For when you want some randomness.

![With Monochrome off](<../.gitbook/assets/image (164).png>)

{% hint style="info" %}
Using **absTime.seconds** in different parameters can make this move!
{% endhint %}

![](../.gitbook/assets/tdnoisetop.gif)

### Switch TOP

Takes in multiple texture operators (TOPS) and creates an array. A single element of the array can be accessed by the Switch TOP's Index parameter. ALSO, for TOPs, you can blend between each element. This is great for fading in and out images and videos or representing number values as shades of color.

![](../.gitbook/assets/tdswitchtop.gif)

### Select TOP

Provides a visual "copy" that references another texture operator. This is great for large projects where you are referencing TOPs in other areas far from the one you need it for.

Click and drag the original TOP into the Select TOP or type in the original TOP's name in the Select TOP's parameter.

![](<../.gitbook/assets/image (193).png>)

## Effects

### Level TOP

Where you access elements such as contrast, brightness, gamma, etc.

![](<../.gitbook/assets/image (192).png>)

### Blur TOP

Adds Blur

![](<../.gitbook/assets/image (155).png>)

### Crop TOP

Crops image

![](<../.gitbook/assets/image (159).png>)

### Mirror TOP

Mirrors part of the image.

![](<../.gitbook/assets/image (165).png>)

## Shapes / Primitives / Transforms

### Circle TOP, Rectangle TOP, Text TOP

Creates shapes or text

![](<../.gitbook/assets/image (157).png>)

### Transform TOP

Manipulates position, rotation, scale, etc.

![](<../.gitbook/assets/image (158).png>)

## Images and Videos

### Movie File In TOP

Load any image or video. This banana image is a default image.

![](<../.gitbook/assets/image (180).png>)

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

![](<../.gitbook/assets/image (160).png>)

![](<../.gitbook/assets/image (161).png>)

