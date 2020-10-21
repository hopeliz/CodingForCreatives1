# Popular CHOPs

Channel operators \(CHOPs\) are colored green and manipulate number data, booleans \(on/off or true/false\), and audio.

![](../.gitbook/assets/image%20%28148%29.png)

## Basics

### Null CHOP

Provides a snapshot of sorts of a point within your network. Commonly used to help look at the effects of major changes later and remove them easily when necessary.

![](../.gitbook/assets/image%20%28149%29.png)

### Constant CHOP

Provides a number, usually typed in. You can have multiple channels/numbers. The slider makes values 0-1 easy to get, but you can type in larger numbers and negative numbers.

![](../.gitbook/assets/image%20%28169%29.png)

![](../.gitbook/assets/image%20%28137%29.png)

### Noise CHOP

For when you want some randomness.

![Line graph version](../.gitbook/assets/image%20%28187%29.png)

To see it moving in real-time, use the **Common &gt; Time Slice** parameter

![](../.gitbook/assets/tdnoisechop.gif)

### Switch CHOP

Takes in multiple channel operators \(CHOPS\) and creates an array. A single element of the array can be accessed by the Switch CHOP's Index parameter.

![](../.gitbook/assets/image%20%28185%29.png)

### Select CHOP

Provides a "copy" that displays selected channels from the original channel operator.

Click and drag the original CHOP onto the Select CHOP or type the original CHOP's name into the Select CHOP's CHOP parameter.

Click the dropdown arrow to the right of the Channels parameter to select \(one-by-one\) one or more channels.

![](../.gitbook/assets/image%20%28192%29.png)

{% hint style="info" %}
When wanting all possible channels, use an asterisk \* ... This can be also used to get all possible channels that start with a certain letter or phrase.
{% endhint %}

![Example of getting only channels starting with &quot;blob0&quot;](../.gitbook/assets/image%20%28193%29.png)

## Math

### Math CHOP

Does math including absolute powers, turning numbers, negative, etc.

_Example of adding two CHOPs:_

![](../.gitbook/assets/image%20%28156%29.png)

_Example of subtracting two channels from the same CHOP:_

![](../.gitbook/assets/image%20%28161%29.png)

_Example of making a number negative:_

![](../.gitbook/assets/image%20%28139%29.png)

_Example of rounding up to the next integer:_

![](../.gitbook/assets/image%20%28135%29.png)

_Example of getting a square root of a number:_

![](../.gitbook/assets/image%20%28150%29.png)

### Using Math CHOP to adjust range/map values

The top way you'll use a Math CHOP is to adjust the range of values. Many operators expect a value from 0 to 1, so finding what the upper and lower bounds of a number are allows the Math CHOP to adjust it to fit.

_Example of having the 0-255 RGB values, but need a 0-1 RGB value for a Constant TOP:_

![](../.gitbook/assets/image%20%28165%29.png)

## Logic

### Logic CHOP

Will turn on/fire true under certain circumstances - kinda like an if statement or while loop.

_Example of the Logic CHOP being true when the input is 2:_

![](../.gitbook/assets/image%20%28181%29.png)

### Count CHOP

Counts the times the input is true or on.

_Example of counting the times the timer is "done":_

{% hint style="info" %}
This GIF is at 30 fps and doesn't show each time it's done, but you can see it in the program.
{% endhint %}

![](../.gitbook/assets/tdcountchop.gif)

## Timers

### Timer CHOP

Provides a timer and whether it is "ready" or "done."

![](../.gitbook/assets/tdcountchop.gif)

## Audio

### Audio Device In CHOP

Brings in audio from microphones.

### Audio Device Out CHOP

Plays audio through your speakers and headphones.

### Audio File In CHOP

Gets audio from an audio OR video file.

### Audio File Out CHOP

Exports an audio file.

