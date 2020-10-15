# Unity Example \(2D Platformer\)

This code should be placed on the player sprite.

The player sprite should have a Rigidbody2D component.

Both the player sprite and the ground sprite should have BoxCollider2D components.

```csharp
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class PlayerMovement2D : MonoBehaviour
{
    public float speed = 5;
    public float jumpHeight = 200;

    public bool isJumping = false;

    public int direction = 0;  // 0 = right and 1 = left

    // Start is called before the first frame update
    void Start()
    {
        
    }

    // Update is called once per frame
    void Update()
    {
        // Moves right while right arrow is pressed
        if (Input.GetKey(KeyCode.RightArrow))
        {
            transform.position += Vector3.right * Time.deltaTime * speed;
            
            // Switch direction of sprite image if originally facing left
            if (direction == 1)
            {
                transform.localScale = new Vector3(transform.localScale.x * -1, transform.localScale.y, transform.localScale.z);
            }

            direction = 0;
        }

        // Moves left while left arrow is pressed
        if (Input.GetKey(KeyCode.LeftArrow))
        {
            transform.position += Vector3.left * Time.deltaTime * speed;

            // Switch direction of sprite image if originally facing right
            if (direction == 0)
            {
                transform.localScale = new Vector3(transform.localScale.x * -1, transform.localScale.y, transform.localScale.z);
            }

            direction = 1;
        }

        // Pushes upward when the space bar is pressed
        if (Input.GetKeyDown(KeyCode.Space))
        {
            // !isJumping is another way of saying isJumping != true
            if (!isJumping)
            {
                transform.GetComponent<Rigidbody2D>().AddForce(Vector2.up * jumpHeight);
                isJumping = true;
            }
        }
    }

    public void OnCollisionEnter2D(Collision2D collision)
    {
        // When the sprite hits something, it turns off isJumping, allowing to jump again
        // You might want to specify only hitting the ground, accessing the name of the ground via collision.gameObject.name

        isJumping = false;
    }
}

```

