# Week 2 Mad Libs Exercise

## Step 1: Start with the Starter Code

Copy the following code to paste in a blank Processing sketch. This will save you time.

```java
/* Variables needed:
- 4 adjectives
- time of day
- name
- pronoun
- 3 objects
- animal
- number higher than 20
- 2 whole numbers
- measurement number
- action
- liquid
- 2 types of people
*/


void setup() {
  println("One (adjective 1) and (adjective 2) (time of day), (name) was delivered a(n) (object 1) by an owl" +
" and attached was an acceptance letter to Hogwarts School of Witchcraft and Wizardry. This seemed weird to (name)," +
" not only because the (object 1) could have been sent through the regular mail, but because (pronoun) was/were" + 
"(number higher than 20)" +
" years old. \n\n"  +
"The letter said classes start in (whole number 1) days and that (pronoun) has/have to go to Diagon Ally to pick up three things: " + 
" a set of textbooks that (action 1), a pet (animal or creature), and (whole number 2) (type of container 1)s of (measurement number)-ounce" +
" of potion starter base (also known as (liquid)). (type of container 2)s are provided. (name) was unfamiliar with Diagon Ally" + 
" and wandered the town of (object 2)ville. (Pronoun) easily found a stray (animal), which (pronoun) named (adjective  3)" +
"(object 3) and it was the most (adjective 4) (animal) (pronoun) had/have ever seen! (Name) couldn't find any potion starter" + 
" base - especially not the (total number of ounces) ounces needed, but luckily found a textbook that (action)ed. \n\n" +
"Despite the struggles, (pronoun) made friends with other witches, wizards, (type of person 1)s , and (type of person 2)s and" + 
"excelled in school.");
}
```

If played, the console shows this:

```markup
One (adjective 1) and (adjective 2) (time of day), (name) was delivered a(n) (object 1) 
by an owl and attached was an acceptance letter to Hogwarts School of Witchcraft and 
Wizardry. This seemed weird to (name), not only because the (object 1) could have been 
sent through the regular mail, but because (pronoun) was/were(number higher than 20) 
years old. 

The letter said classes start in (whole number 1) days and that (pronoun) has/have to 
go to Diagon Ally to pick up three things:  a set of textbooks that (action 1), a pet 
(animal or creature), and (whole number 2) (type of container 1)s of (measurement 
number)-ounce of potion starter base (also known as (liquid)). (type of container 2)s 
are provided. (name) was unfamiliar with Diagon Ally and wandered the town of (object 
2)ville. (Pronoun) easily found a stray (animal), which (pronoun) named (adjective  
3)(object 3) and it was the most (adjective 4) (animal) (pronoun) had/have ever seen! 
(Name) couldn't find any potion starter base - especially not the (total number of 
ounces) ounces needed, but luckily found a textbook that (action)ed. 

Despite the struggles, (pronoun) made friends with other witches, wizards, (type of 
person 1)s , and (type of person 2)s andexcelled in school.
```

## Step 2: Create Needed Variables

Variables in Processing need to have their data type declared along with the name.

The naming convention for variable names is using descriptive short phrases/names and [camel case](../../glossary/variables/declaring-variables.md#naming-conventions).

Since you might want to use these variables in more than just setup\(\) or draw\(\), create them outside the setup\(\) and draw\(\) functions at the top of the code. This will allow any block to access the variables.

```java
String adj1 = "manic";
String adj2 = "shiny";
String adj3 = "uncomfortable";
String adj4 = "rainy";
String timeOfDay = "dusk";
String name = "Bartholowmew";
String pronoun = "they";
String obj1 = "orb";
String obj2 = "wand";
String obj3 = "flying car";
String animal = "owl";
float num1 = 21.1;
int num2 = 19;
int num3 = 4007;
float measurement = 2.6;
String action = "burst";
String liquid = "Razzwheat Gaterade";
String typeOfPerson1 = "Half man half snake";
String typeOfPerson2 = "Clone";
String typeOfContainer1 = "potion bottle";
String typeOfContainer2 = "tupperware";
```

{% hint style="info" %}
In Week 3, we will look at ways to make one variable hold all 4 adjectives, all 3 objects, etc. making long lists of variables like this shorter and easier to access.
{% endhint %}

## Step 3: Add the Variables to the Final Output Message

Replace the areas in the parentheses with the variable.

**REMEMBER:** To put in the variables, you must:

1. End the string with a quotation symbol \(a double quote is used in this activity\)
2. Use the concatenator symbol \( + \).
3. The variable name.
4. Another concatenator symbol \( + \).
5. Then begin the string again with a quotation symbol.

Example:

```java
println("That is a (adjective 1) (animal)!");
```

becomes

```java
println("That is a " + adj1 + " " + animal + "!");
```

{% hint style="warning" %}
Remember to end the string and add a concatenator \( + \) symbol at the end of a line if you break the line up to be readable. Also, restart the string on the next line. End the full line of code with a semicolon \( ; \).
{% endhint %}

The result will look like:

```java
/* Variables needed:
- 4 adjectives
- time of day
- name
- pronoun
- 3 objects
- animal
- number higher than 20
- 2 whole numbers
- measurement number
- action
- liquid
- 2 types of people
*/

String adj1 = "manic";
String adj2 = "shiny";
String adj3 = "uncomfortable";
String adj4 = "rainy";
String timeOfDay = "dusk";
String name = "Bartholowmew";
String pronoun = "they";
String obj1 = "orb";
String obj2 = "wand";
String obj3 = "flying car";
String animal = "owl";
float num1 = 21.1;
int num2 = 19;
int num3 = 4007;
float measurement = 2.6;
String action = "burst";
String liquid = "Razzwheat Gaterade";
String typeOfPerson1 = "Half man half snake";
String typeOfPerson2 = "Clone";
String typeOfContainer1 = "potion bottle";
String typeOfContainer2 = "tupperware";

void setup() {
  println("Numbers: " + num3 + measurement);
  println("Numbers: " + (num3 + measurement));
  println(num3 + measurement);
  
  println("One " + adj1 + " and " + adj2 + " " + timeOfDay + ", " + name + " was delivered a(n) " + obj1 + " by an owl" +
" and attached was an acceptance letter to Hogwarts School of Witchcraft and Wizardry. This seemed weird to " + name + "," +
" not only because the " + obj1 + " could have been sent through the regular mail, but because " + pronoun + " was/were " + 
num1 +
" years old. \n\n"  +
"The letter said classes start in " + num2 + " days and that " + pronoun + " has/have to go to Diagon Ally to pick up three things: " + 
" a set of textbooks that " + action + ", a pet " + animal + ", and " + num3 + " " + typeOfContainer1 + "s of " + measurement + "-ounce" +
" of potion starter base (also known as " + liquid + "). " + typeOfContainer2 + "s are provided. " + name + " was unfamiliar with Diagon Ally" + 
" and wandered the town of " + obj2 + "ville. " + pronoun + " easily found a stray " + animal + ", which " + pronoun + " named " + adj3 + " " +
obj3 + " and it was the most " + adj4 + " " + animal + " " + pronoun + " had/have ever seen! " + name + " couldn't find any potion starter" + 
" base - especially not the " + num3 * measurement + " ounces needed, but luckily found a textbook that " + action + "ed. \n\n" +
"Despite the struggles, " + pronoun + " made friends with other witches, wizards, " + typeOfPerson1 + "s, and " + typeOfPerson2 + "s and" + 
" excelled in school.");
}
```

The output will look like this:

> One manic and shiny dusk, Bartholowmew was delivered a\(n\) orb by an owl and attached was an acceptance letter to Hogwarts School of Witchcraft and Wizardry. This seemed weird to Bartholowmew, not only because the orb could have been sent through the regular mail, but because they was/were 21.1 years old.
>
> The letter said classes start in 19 days and that they has/have to go to Diagon Ally to pick up three things: a set of textbooks that burst, a pet owl, and 4007 potion bottles of 2.6-ounce of potion starter base \(also known as Razzwheat Gaterade\). tupperwares are provided. Bartholowmew was unfamiliar with Diagon Ally and wandered the town of wandville. they easily found a stray owl, which they named uncomfortable flying car and it was the most rainy owl they had/have ever seen! Bartholowmew couldn't find any potion starter base - especially not the 10418.199 ounces needed, but luckily found a textbook that bursted.
>
> Despite the struggles, they made friends with other witches, wizards, Half man half snakes, and Clones and excelled in school.

### Notation

Certain notation can be used within strings to accomplish things like creating a new line \(equivalent to pressing the enter or return key\), inserting an apostrophe when single quotes are used, inserting a tab, etc.

**\n** = new line  
**\r** = carriage return  
**\t** = tab  
**\'** = apostrophe \(to use when single quotes are used for a string\)  
**\"** = quotation marks \(to use when double quotes are used for a string\)

## **Step 4: Polishing It a Little**

Let's make the beginning of some of the sentences have a capital letter instead of lowercase that the variable is in.

Some languages have functions that can capitalize just the first letter, but Processing and Java has just uppercase and lowercase functions. 

To capitalize the first letter and leave the rest lowercase, we can use two substrings. Substrings are parts of a defined string.

_.substring\(index of first letter\)_ starts the string with the index/location of the first letter.

_.substring\(index of first letter, index of limit letter\)_ starts the string with the index/location of the first letter and ends on the letter before the limit letter

You can add more effects/functions to the string by attaching them. For example, add _.toUpperCase\(\)_ to make the substring uppercase.

Example:

```java
String pronoun = "they";

println(pronoun + " was/were...");

// Prints "they was/were..."
```

becomes

```java
String pronoun = "they";

println(pronoun.substring(0,1).toUpperCase() + pronoun.substring(1) + " was/were...");

// Prints "They was/were..."
```

Updated code:

```java
/* Variables needed:
- 4 adjectives
- time of day
- name
- pronoun
- 3 objects
- animal
- number higher than 20
- 2 whole numbers
- measurement number
- action
- liquid
- 2 types of people
*/

String adj1 = "manic";
String adj2 = "shiny";
String adj3 = "uncomfortable";
String adj4 = "rainy";
String timeOfDay = "dusk";
String name = "Bartholowmew";
String pronoun = "they";
String obj1 = "orb";
String obj2 = "wand";
String obj3 = "flying car";
String animal = "owl";
float num1 = 21.1;
int num2 = 19;
int num3 = 4007;
float measurement = 2.6;
String action = "burst";
String liquid = "Razzwheat Gaterade";
String typeOfPerson1 = "Half man half snake";
String typeOfPerson2 = "Clone";
String typeOfContainer1 = "potion bottle";
String typeOfContainer2 = "tupperware";

void setup() {
  println("One " + adj1 + " and " + adj2 + " " + timeOfDay + ", " + name + " was delivered a(n) " + obj1 + " by an owl" +
" and attached was an acceptance letter to Hogwarts School of Witchcraft and Wizardry. This seemed weird to " + name + "," +
" not only because the " + obj1 + " could have been sent through the regular mail, but because " + pronoun + " was/were " + 
num1 +
" years old. \n\n"  +
"The letter said classes start in " + num2 + " days and that " + pronoun + " has/have to go to Diagon Ally to pick up three things:" + 
" a set of textbooks that " + action + ", a pet " + animal + ", and " + num3 + " " + typeOfContainer1 + "s of " + measurement + "-ounce" +
" of potion starter base (also known as " + liquid + "). " + typeOfContainer2.substring(0,1).toUpperCase() + typeOfContainer2.substring(1) + 
"s are provided. " + name + " was unfamiliar with Diagon Ally" + " and wandered the town of " + obj2.substring(0,1).toUpperCase() + 
obj2.substring(1) + "ville. " + pronoun.substring(0,1).toUpperCase() + pronoun.substring(1) + " easily found a stray " + animal + ", which " + 
pronoun + " named " + adj3 + " " + obj3 + " and it was the most " + adj4 + " " + animal + " " + pronoun + " had/have ever seen! " + name + 
" couldn't find any potion starter" + " base - especially not the " + num3 * measurement + " ounces needed, but luckily found a textbook that " + 
action + "ed. \n\n" + "Despite the struggles, " + pronoun + " made friends with other witches, wizards, " + typeOfPerson1 + "s, and " + 
typeOfPerson2 + "s and" + " excelled in school.");
}
```

The output looks like this:

> One manic and shiny dusk, Bartholowmew was delivered a\(n\) orb by an owl and attached was an acceptance letter to Hogwarts School of Witchcraft and Wizardry. This seemed weird to Bartholowmew, not only because the orb could have been sent through the regular mail, but because they was/were 21.1 years old.
>
> The letter said classes start in 19 days and that they has/have to go to Diagon Ally to pick up three things: a set of textbooks that burst, a pet owl, and 4007 potion bottles of 2.6-ounce of potion starter base \(also known as Razzwheat Gaterade\). Tupperwares are provided. Bartholowmew was unfamiliar with Diagon Ally and wandered the town of Wandville. They easily found a stray owl, which they named uncomfortable flying car and it was the most rainy owl they had/have ever seen! Bartholowmew couldn't find any potion starter base - especially not the 10418.199 ounces needed, but luckily found a textbook that bursted.
>
> Despite the struggles, they made friends with other witches, wizards, Half man half snakes, and Clones and excelled in school.



You can also turn large numbers into strings that properly format the number with commas and rounding.

For this example, we can use the Processing function _nfc\(number, number of decimals\)_.

```java
"...not the " + num3 * measurement + " ounces needed..."
```

becomes

```java
"...not the " + nfc(num3 * measurement, 2) + " ounces needed..."
```

## Final Code

```java
/* Variables needed:
- 4 adjectives
- time of day
- name
- pronoun
- 3 objects
- animal
- number higher than 20
- 2 whole numbers
- measurement number
- action
- liquid
- 2 types of people
*/

String adj1 = "manic";
String adj2 = "shiny";
String adj3 = "uncomfortable";
String adj4 = "rainy";
String timeOfDay = "dusk";
String name = "Bartholowmew";
String pronoun = "they";
String obj1 = "orb";
String obj2 = "wand";
String obj3 = "flying car";
String animal = "owl";
float num1 = 21.1;
int num2 = 19;
int num3 = 4007;
float measurement = 2.6;
String action = "burst";
String liquid = "Razzwheat Gaterade";
String typeOfPerson1 = "Half man half snake";
String typeOfPerson2 = "Clone";
String typeOfContainer1 = "potion bottle";
String typeOfContainer2 = "tupperware";

void setup() {
  println("One " + adj1 + " and " + adj2 + " " + timeOfDay + ", " + name + " was delivered a(n) " + obj1 + " by an owl" +
" and attached was an acceptance letter to Hogwarts School of Witchcraft and Wizardry. This seemed weird to " + name + "," +
" not only because the " + obj1 + " could have been sent through the regular mail, but because " + pronoun + " was/were " + 
num1 +
" years old. \n\n"  +
"The letter said classes start in " + num2 + " days and that " + pronoun + " has/have to go to Diagon Ally to pick up three things:" + 
" a set of textbooks that " + action + ", a pet " + animal + ", and " + num3 + " " + typeOfContainer1 + "s of " + measurement + "-ounce" +
" of potion starter base (also known as " + liquid + "). " + typeOfContainer2.substring(0,1).toUpperCase() + typeOfContainer2.substring(1) + 
"s are provided. " + name + " was unfamiliar with Diagon Ally" + " and wandered the town of " + obj2.substring(0,1).toUpperCase() + 
obj2.substring(1) + "ville. " + pronoun.substring(0,1).toUpperCase() + pronoun.substring(1) + " easily found a stray " + animal + ", which " + 
pronoun + " named " + adj3 + " " + obj3 + " and it was the most " + adj4 + " " + animal + " " + pronoun + " had/have ever seen! " + name + 
" couldn't find any potion starter" + " base - especially not the " + nfc(num3 * measurement, 2) + " ounces needed, but luckily found a textbook that " + 
action + "ed. \n\n" + "Despite the struggles, " + pronoun + " made friends with other witches, wizards, " + typeOfPerson1 + "s, and " + 
typeOfPerson2 + "s and" + " excelled in school.");
}
```

Output:

> One manic and shiny dusk, Bartholowmew was delivered a\(n\) orb by an owl and attached was an acceptance letter to Hogwarts School of Witchcraft and Wizardry. This seemed weird to Bartholowmew, not only because the orb could have been sent through the regular mail, but because they was/were 21.1 years old.
>
> The letter said classes start in 19 days and that they has/have to go to Diagon Ally to pick up three things: a set of textbooks that burst, a pet owl, and 4007 potion bottles of 2.6-ounce of potion starter base \(also known as Razzwheat Gaterade\). Tupperwares are provided. Bartholowmew was unfamiliar with Diagon Ally and wandered the town of Wandville. They easily found a stray owl, which they named uncomfortable flying car and it was the most rainy owl they had/have ever seen! Bartholowmew couldn't find any potion starter base - especially not the 10,418.20 ounces needed, but luckily found a textbook that bursted.
>
> Despite the struggles, they made friends with other witches, wizards, Half man half snakes, and Clones and excelled in school.

