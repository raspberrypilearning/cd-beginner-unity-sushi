## Making MazeRobo move

+ Go to the Project pane and create a new folder \(**Assets &gt; Create &gt; Folder**\) inside the `Assets` folder \(you may need to click on the `Assets` folder first\). Call the new folder `Scripts`.  

![](images/step7_ScriptsFolder.png)
   
+ Create a new C\# script \(**Assets &gt; Create &gt;  C\# Script**\) in this folder, and call it `RoboMover`.

![The RoboMover script inside the Scripts folder](images/step7_NewScript.png)

+ Double-click on `RoboMover` to open it in your editor (which is a separate program from Unity). You should see code like this:

```cs
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class RoboMover : MonoBehaviour {

  // Use this for initialization
  void Start () {

  }

  // Update is called once per frame
  void Update () {

  }
}
```

--- collapse ---
---
title: Understanding the code
---
Let's look at what you've got here. You can ignore the first three lines, for now. They're just the program setting up things it needs. Then you've got this:

```cs
public class RoboMover : MonoBehaviour {
```

This is the start of a **class** \(a blueprint of code\) called `RoboMover`. Don't worry about the `: MonoBehaviour` bit right now. Everything between this first `{` and the last `}` is inside the `RoboMover` class.

Then below that, you have two **function declarations** for **functions** named `Start` and `Update`. A function declaration is where a function gets defined in your code. Right now, the functions are both empty, so their only difference is their names, so let's just look at one quickly:

```cs
void Update() {

}
```

A function is a set of instructions for a computer to do something, wrapped up with a label for the task that makes it easy to remember. For example, for a human, "Make me a cup of tea" is a function. We know there are lots of steps to it and, at the end, you have a cup of tea. It would be silly to have to tell someone every step every time you wanted them to make you some tea. The same is true of asking the computer to do something. Much easier to teach it once, in one place, and then get it to do it over and over again just by using the name of the function!

The first word in these function declarations here is `void`. That shows you that the functions don't **return** anything. That means they give nothing back at the end of running. For example, the human function "Make me a cup of tea" **returns** a cup of tea once all the instructions are done, but "Add milk" doesn't return anything, it just changes the cup of tea that already exists. So "Add milk" would be a `void` function!

Next comes the name of the **function**, that easy label you can use to **call** the function from elsewhere in your code to use it. Notice the round brackets `()` beside it though. They're empty now, but they can be used to **pass** information into the function. For example: "Make me a cup of tea \(two sugars\)".

Finally, you have the curly brackets `{}`. Everything inside them is the set of instructions the program will follow when the **function** is called. For "Make me a cup of tea" that would be things like:

* Boil water
* Put water in teapot
* Add teabag
* ...and so on

--- /collapse ---

Now that you've got some code to work with, it's time to start adding to it!

+ First, you need to add some **variables**, inside the class but before the functions, like this:

```cs
public class RoboMover : MonoBehaviour {

  public float moveSpeed = 4.0f;
  public Rigidbody rb;
  public Transform tf;

  // Use this for initialization
  void Start () {
```

--- collapse ---
---
title: What does the new code do?
---

   These variables are labels on values, or things. In this case we've got:

   * `moveSpeed` — a **f**loat \(decimal\) number, in this case `4.0`
   * `rb` — a variable you'll use to refer to the **Rigidbody** component \(which is MazeRobo itself, remember?\)
   * `tf` — a variable you'll use to refer to the **Transform** component

--- /collapse ---

+ You don't actually need the `Start` function in this program, so you can delete these lines:

```cs
// Use this for initialization
void Start () {

}
```

+ Now you need to fill out the `Update` function with this code:

```cs
// Update is called once per frame
void Update () {
  Vector3 desiredDirection = new Vector3 (Input.GetAxis ("Horizontal"), 0.0f, Input.GetAxis ("Vertical"));
  desiredDirection = moveSpeed * desiredDirection;
  desiredDirection = Time.deltaTime * desiredDirection;
  rb.MovePosition (rb.position + desiredDirection);
}
```

--- collapse ---
---
title: What does the new code do?
---

The first line of the function creates `desiredDirection`, which is a  set of three coordinates. Two of them are taken from `Input`, which is the direction the game receives from the player. The last is the depth of the character, which you're not changing, so it's set to `0.0`.  

You then multiply the `desiredDirection` by `moveSpeed`, the variable you set earlier that controls the speed at which MazeRobo moves.  

Next, you multiply `desiredDirection` again by `Time.deltaTime` which is the amount of time since the last time `Update` ran. This means the direction changes correctly no matter the type of computer it's on.  

Finally, you change the position of the `rb`, the **Rigidbody**, by the amount you've calculated.  

What all this adds up to is that the character moves a tiny bit in the direction the player is sending it with the controls every time the screen is updated. 

--- /collapse ---

+ Be sure to save your code (**File > Save**).

That should do it! You're close to getting MazeRobo moving now!

+ Back in Unity, drag and drop your `RoboMover` script from the `Scripts` folder and onto the MazeRobo **gameobject** in the **Hierarchy**.

![Drag the script onto MazeRobo](images/step7_dragScript.png)

+ You'll see that a field for the script is now visible in MazeRobo’s Inspector, below **Rigidbody**.  

![The script appears in the inspector for MazeRobo](images/MazeRobo_Inspector.png)

+ There are two empty fields in the `RoboMover` field:`rb` and `tf`. As you know, these stand for **Rigidbody** and **Transform**, and if you click and drag the names of these components from their places in the Inspector and into their respective fields, `RoboMover` \(the script\) will have all the info it needs to move MazeRobo! 

![Drag the names onto the script](images/step7_DragOntoScript.png)
![The Rb and Tf variables now have the values of Rigidbody and Transform](images/Script_Vars.png)

+ Now click on the big **Play** button at the top centre of the Unity interface...

MazeRobo is moving!

+ Use the arrow keys to control MazeRobo. When you're done, press the **Play** button again to stop the game.



