# TouchOSC

TouchOSC is an app that provides wireless input and output.

You can get it here:

{% embed url="https://hexler.net/products/touchosc" %}

## Step 1: Set Up TouchDesigner to Get OSC Input

Open TouchDesigner and press TAB to pull up the OP Create Dialog. Under the green CHOP tab, search for and select OSCin. Click to place.

![](<../../.gitbook/assets/image (260).png>)

In your parameters, click the arrow to the right of the field for Local Address and select the first option.

![](<../../.gitbook/assets/image (261).png>)

{% hint style="info" %}
If you do not see the parameters, press the P key to toggle it on.
{% endhint %}

## Step 2: Set Up TouchOSC

Open the app and tap "OSC" to access the communication options. Note: You might have "Not configured" the first time you use the app instead of an IP address.

![](<../../.gitbook/assets/image (262).png>)

Type in the IP address (local address) show in the TouchDesigner OSCin CHOP's parameters.

Set the outgoing port to a number (doesn't really matter) that does not match the incoming port number.

![](<../../.gitbook/assets/image (263).png>)

In TouchDesigner, change the Network Port to match the outgoing port in TouchOSC.

![](<../../.gitbook/assets/image (265).png>)

Go back to the settings menu in TouchOSC.

Tap "TouchOSC Bridge" to bring up more settings.

Put "localhost" as the host if it is not automatically filled in.

![](<../../.gitbook/assets/image (264).png>)

Go back to the settings menu and tap "Done."

If everything is working, you should now see values in TouchDesigner that change when you rotate your phone:

![](<../../.gitbook/assets/image (266).png>)

## Step 3: Using TouchOSC

The default channels are data from the accelerometer in your phone.

TouchOSC also has interfaces! The channels for each part of the interface will appear once you use them.

Example:

![How the first interface looks with changed values.](<../../.gitbook/assets/image (268).png>)

![How these changes are reflected in TouchDesigner.](<../../.gitbook/assets/image (267).png>)

Once you have these channels appearing in the OSCin CHOP, use a green Select CHOP to choose one or more of the channels.

Once you connect the Select CHOP, use the arrow to the right of the Channel Names field to select the channels you want to include.

![](<../../.gitbook/assets/image (269).png>)

After that, you can use the value in the Select CHOP to affect other nodes, meaning you can control nodes (color, sound, distortion amount, etc.) with your cell phone!
