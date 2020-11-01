# Audio-Reactive 3D Shapes

This activity uses TouchDesigner. Please see the TouchDesigner section at the end of the menu on the left for more information about the program.

{% hint style="warning" %}
New TouchDesigner projects open with an example project. Please highlight and delete those operators so the project is empty.
{% endhint %}

## Goal

The goal of this activity is to have audio from a microphone or an audio file effect the shape and color of a 3D object.

## Step 1: 3D Shape Set Up

For 3D shapes, we need the following:

* a light
* a camera
* a shape/geometry
* a way to render it flat

The first two are Component operators or COMPs.

Press the TAB key or right-click and select **Add Operator** to bring up the OP Create Dialog. Go to the COMP tab. Search for and select the Light COMP.

![](../../.gitbook/assets/image%20%28226%29.png)

Click to place.

Do the same with a Camera COMP.

![](../../.gitbook/assets/image%20%28219%29.png)

For the Geometry, it's easier to start with your shape, found in the blue surface operators or SOPs.

Bring up the OP Create Dialog and select the SOP tab. Search for and select the Sphere SOP.

![](../../.gitbook/assets/image%20%28216%29.png)

Click to place.

Right-click on the output of the Sphere SOP and select **Add Operator**. Click the black COMP tab. Search for and select the Geometry COMP.

![](../../.gitbook/assets/image%20%28206%29.png)

This makes it so blue surface operators \(SOPs\) can connect to the Geometry COMP.

![](../../.gitbook/assets/image%20%28231%29.png)

Lastly, bring up the OP Create Dialog and click on the purple texture operator \(TOP\) tab. Search for and select the Render TOP.

This automatically finds and brings in the COMPs to create a flat scene to display.

![](../../.gitbook/assets/image%20%28225%29.png)

To have this appear easily in a separate window, let's use a Null and Out texture operator \(TOP\).

A **Null** operator is like a snapshot of progress.

Right-click on the Render TOP output and add a Null TOP.

The project is looking for a texture operator named "out1" by default to display. Add this by right-clicking on the output of the Null TOP and add an Out TOP.

![](../../.gitbook/assets/image%20%28207%29.png)

Now, you can preview what this looks like by clicking the Open Viewer button at the top left \(looks like a square\).

![](../../.gitbook/assets/image%20%28229%29.png)

## Step 2: Add Some Noise \(Randomness\)

Texture, surface, and channel tops all have random operators named "Noise."

Move the Sphere SOP a little to the left to make room.

Right-click on the connected line and select **Insert Operator**. Under the blue SOP options, search and select the Noise SOP.

![](../../.gitbook/assets/image%20%28220%29.png)

Click to place.

You should now have a moving blob.

![](../../.gitbook/assets/week9bs2%20%281%29.gif)

Play with the parameters to see the effects.

## Step 3: Bring in Some Audio

For Audio, we will use channel operators or CHOPs.

To bring data in from a microphone, add an Audio Device In CHOP.

![](../../.gitbook/assets/image%20%28204%29.png)

Make some noise! The red waveform is the audio the microphone is picking up.

![](../../.gitbook/assets/image%20%28224%29.png)

To turn this into something that can be used as values, right-click on the output of the Audio Device In CHOP and add an Analyze CHOP.

![](../../.gitbook/assets/image%20%28217%29.png)

The default function is Average, but I've noticed the best values come from the RMS Power function.

![](../../.gitbook/assets/image%20%28228%29.png)

The values seem to go from just above 0 to 0.3.

Let's look at the Noise SOP and see what we want to change and what the value range needs to be.

I like the effect the Roughness parameter gives as it goes from 0 to 1.

Let's "map" or change the range of our Analyze CHOP to be 0 to 1 instead by adding a Math CHOP.

Right-click on the output of the Analyze CHOP to add a Math CHOP.

![](../../.gitbook/assets/image%20%28208%29.png)

Select the Math CHOP. Select the Range tab in the parameters.

Have the range go from 0 to 0.3 and 0 to 1.





