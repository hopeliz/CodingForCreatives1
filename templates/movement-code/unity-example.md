# Unity Example \(3D\)

{% hint style="danger" %}
You must either name your new script PlayerMovement.cs OR update this code after the word "class" to the name of your script.
{% endhint %}

This is code that uses WASD kets to move the object the script is added to.

It also rotates left and right using the arrow keys and jumps with the space bar.

{% hint style="warning" %}
For jump to work, be sure to add a Rigidbody component to the object. If the object falls over, in the Rigidbody component, free the X and Z rotations.
{% endhint %}

{% hint style="info" %}
This code uses shortcuts. \(See below the code.\)
{% endhint %}

```csharp
using UnityEngine;

public class PlayerMovement : MonoBehaviour
{
    public float moveSpeed = 10;
    public float rotateSpeed = 50;
    public float jumpHeight = 200;

    void Update()
    {
        // Translate / Move
        if (Input.GetKey(KeyCode.W) || Input.GetKey(KeyCode.UpArrow))
        {
            transform.Translate(Vector3.forward * moveSpeed * Time.deltaTime);
        }

        if (Input.GetKey(KeyCode.A))
        {
            transform.Translate(Vector3.left * moveSpeed * Time.deltaTime);
        }

        if (Input.GetKey(KeyCode.S) || Input.GetKey(KeyCode.DownArrow))
        {
            transform.Translate(Vector3.back * moveSpeed * Time.deltaTime);
        }

        if (Input.GetKey(KeyCode.D))
        {
            transform.Translate(Vector3.right * moveSpeed * Time.deltaTime);
        }

        // Rotate
        if (Input.GetKey(KeyCode.LeftArrow))
        {
            transform.Rotate(Vector3.down * rotateSpeed * Time.deltaTime);
        }
        
        if (Input.GetKey(KeyCode.RightArrow)) 
        {
            transform.Rotate(Vector3.up * rotateSpeed * Time.deltaTime);
        }

        // For jump to work, be sure to add a Rigidbody component to your player object
        if (Input.GetKeyDown(KeyCode.Space))
        {
            transform.GetComponent<Rigidbody>().AddForce(Vector3.up * jumpHeight);
        }
    }
}
```

#### **Vector3 Shortcuts:**

| Shortcut | Equivalent |
| :--- | :--- |
| Vector3.up | Vector3\(0, 1, 0\) |
| Vector3.down | Vector3\(0, -1, 0\) |
| Vector3.left | Vector3\(-1, 0, 0\) |
| Vector3.right | Vector3\(1, 0, 0\) |
| Vector3.foward | Vector3\(0, 0, 1\) |
| Vector3.back | Vector3\(0, 0, -1\) |

These can be multiplied and divided as an easy way to adjust the value on just one axis.

