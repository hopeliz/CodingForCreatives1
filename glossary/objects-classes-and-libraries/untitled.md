# Accessing Objects

Each language has its own way of creating objects, but generally have the same way of accessing aspects of objects.

Generally, it's with dots and it starts with the largest object or class and gets smaller each time.

**Example:** if we had Census data to access from outside of a USPopulation object and we wanted the name of the head of household of 101 N. Court Street.

USPopulation.Midwest.Ohio.Southeast.Athens.Athens.UpTown.NorthCourtStreet.0-300.100.Household.Head.name

Each dot is looking deeper into the object until we get what we want - usually a value or a function related to it.

**Examples of where we've used it before in class:**

Seeing if the space bar is pressed:

```csharp
if (Input.GetKeyDown(KeyCode.Space) == true)
{

}
```

**Input** is a class and we use the dot to access the class' **GetKeyDown\(\)** function.

**KeyCode** is not a class, but is similar, proving the key code for Space.

```csharp
gameObject.transform.position.y
```

If we have access to a game object in Unity, we can dig deeper and get to its Transform component, then into its position property, and then its position on the y-axis.

```csharp
gameObject.GetComponent<SpriteRenderer>().sprite
```

In Unity, we can access any Component on a game object using GetComponent&lt;NameOfComponent&gt;\(\) and then a dot to go into the component to access its variables and functions.

```csharp
public void OnCollisionEnter2D(Collision2D collision)
{
    if (collision.gameObject.name == "Ground")
    {
    }
}
```

When a function provides information such as a Collision2D type here named collision, we can use it to access the game object and all its features.

