# Mouse Interaction

## Mouse Interaction

* many languages use built-in keywords and variables to provide information

{% hint style="info" %}
The examples below can be slightly different for each program (case, spelling, use of periods and brackets, extra information and arguments. etc.).
{% endhint %}

Examples:

### mouseX & mouseY

* provides coordinates of the mouse cursor
* type of value: float
* updated every frame

### OnMouseUp() or MouseClicked()

* provides a "true" value during the frame when a mouse button is released
* type of value: boolean
* some languages require more information about what button to listen to
* languages with OnMouseDrag() could interfere when the mouse is moved while the button is pressed

### OnMouseDown() or MousePressed()

* provides a "true" value during the frame when a mouse button is held down
* type of value: boolean
* some languages require more information about what button to listen to

### OnMouseDrag() or MouseDragged()

* provides a "true" value when a mouse button is pressed and the mouse is moved
* type of value: boolean
* some languages require more information about what button to listen to
