# Overview

TouchDesigner is a program that uses node-based programming and Python scripting.

## Operators \(Nodes\)

Each operator or node is like a [function](../glossary/functions-and-methods/). Many will have input notches, parameters \(values within the operator\), and an output \(similar to a return\) that can go into another node.

## Inputs

Input notches are on the **left side** of the operators.

_Example of an operator that has one input:_

![](../.gitbook/assets/image%20%28185%29.png)

_Example of an operator that has three outputs:_

![](../.gitbook/assets/image%20%28132%29.png)

_Example of an operator that takes in multiple inputs to create a list or something like an array:_

![Notice that this input is larger than the others.](../.gitbook/assets/image%20%28160%29.png)

_Example of an operator that has no inputs:_

![](../.gitbook/assets/image%20%28144%29.png)

### How to see what input is wanted

Hover your mouse over the input notch - a description will come up with the input number and description.

Examples:

![ ](../.gitbook/assets/image%20%28180%29.png)

Here, the operator is looking for a connected operator to provide an audio/video source as an input.

![](../.gitbook/assets/image%20%28181%29.png)

Here, the operator is looking for an operator with at least one channel connected to the first input to see if changes warrant a count change.

![](../.gitbook/assets/image%20%28176%29.png)

Here, the operator is looking for an operator connected to the second input that will fire "true" when the count should reset, if wanted.

![](../.gitbook/assets/image%20%28186%29.png)

Here, the operator is looking for an operator connected to the third input that will provide the increment value if different than the default. Note: this value can be negative!

## Parameters

Each operator will have a related parameters window appear when the operator is selected.

{% hint style="info" %}
If you do not see the Parameters window, this can be toggled on and off with the P key.
{% endhint %}

Example of a Parameters window:

![](../.gitbook/assets/image%20%28143%29.png)

Things to notice:

On the top left, the **type of operator** is shown \(Movie File In\).

Followed by the **name of the operator** that you can update. This will update the name that appears at the bottom of the operator node. \(moviefilein1\)

The next line has **icons for help** on the left and **advanced features** like tags, comments, language, and views on the right.

To save space, most Parameter windows will have **tabs** - here, they are Play, Image, Trim, Tune, and Common. These will change depending on the operator.

The rest are parameters - like in a function - that are values that change how something in a node looks, sounds, acts, etc.

### Common Parameters

For TOPs \(purple texture operators\), the **Common** tab is where you can update the resolution and aspect of the output image. It usually defaults to "Use Input," but can be changed. Free versions are limited, though.

![](../.gitbook/assets/image%20%28155%29.png)

For CHOPs \(green channel operators\), the **Common** tab is where you can change how a node appears \(line graph vs. moving bar graph, called a "Time Slice"\).

![](../.gitbook/assets/image%20%28158%29.png)

![](../.gitbook/assets/image%20%28171%29.png)

### Referencing Other Operators in Parameters

There are times when you want a value from an operator that isn't connected into the input. You can reference it instead!

There are two ways to do this.

First, expand the parameter you want to have the value in by pressing the plus sign that appears next to it when you hover over the name of the parameter:

![](../.gitbook/assets/image%20%28172%29.png)

![](../.gitbook/assets/image%20%28133%29.png)

This will show the variable name of the parameter. 

The colored squares next to the value mean:

**Gray** - Value typed in

**Cyan** - An "expression" using Pyton to reference an operator or variable like absTime.seconds

**Green** - An exported value \(references through file organization\)

**Lavender** - Bind....this is new, so I have no idea.

We will use the Cyan expression option, so click on the cyan square.

![](../.gitbook/assets/image%20%28162%29.png)

It defaults to whatever the current type value was.

The syntaxes to reference operator values is:

```python
op('operatorname')['channelname']
```

or

```python
op('operatorname')[index]
```

or \(for parameter values\)

```python
op('operatorname').par.parametername
```

In this example, I want this count CHOP value to be the seed value of my noise CHOP

![](../.gitbook/assets/image%20%28150%29.png)

So here are my options:

#### Option 1: Typing in an expression

![](../.gitbook/assets/image%20%28164%29.png)

or

![](../.gitbook/assets/image%20%28134%29.png)

Let's say instead of this output value, I want the Reset Value parameter of the count CHOP instead:

![](../.gitbook/assets/image%20%28175%29.png)

I could use the following expression:

![](../.gitbook/assets/image%20%28153%29.png)

#### Option 2: Click and Drag Output Values

Toggle the Viewer Active option on the bottom right of the channel operator.

![](../.gitbook/assets/image%20%28141%29.png)

This will fill the operator with the output value.

![](../.gitbook/assets/image%20%28174%29.png)

Select your target operator to bring up its parameters.

Click and drag from your source operator to the field for your target parameter and choose **CHOP Reference**.

![](../.gitbook/assets/tdref.gif)



