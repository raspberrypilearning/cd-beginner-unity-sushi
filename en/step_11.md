## Winning!

You've got a robot, you've got a ball... now in order for it to be a game, there's got to be a way to win! You'll be adding that now!

+ First, add another cube and call it `WinZone`. Maybe give it a new, noticeable colour (yellow? orange? pink?).

+ Make sure you have "WinZone" selected in the **Hierarchy** and then in the **Inspector**, under **Box Collider** check the **Is Trigger** option. Set the Transform of "WinZone" so as the **position** is:
  X: -5
  Y: 1
  Z: -2

You're going to write another **script** to let "WinZone" detect when the "Ball" touches it. In order to do that, the ball needs to be **tagged**.

+ Select "Ball" in the **Hierarchy** and then select the **Tag** field just under its name in the **Inspector**. Choose "Add Tag" then click on the "+" icon and create the tag "Ball".

+ Re-select "Ball" in the **Hierarchy**, check the **Tag** list again and choose the "Ball" tag you just created.

While you're at it, why not add some celebration to let the player know when they've won! 

+ Create a **Particle System** (**Create > GameObject > Particle System**) and call it `Fireworks`. Select it and untick the checkbox beside its name in the **Inspector**. This hides the object, so you can make it appear with your **script** once you're ready to set off the fireworks!

+ Now look in the list of settings in the **Inspector**, find "Start Color" and set it to yellow... or green... or whatever you like really! Oh, and make the **Position** of the "Fireworks" match the **Position** of "WinZone".

+ Now create a **C# Script** (in the "scripts" folder) called `WinZone`. Open it up and remove the `Start()` and `Update()` functions. Put this code inside it instead:

```cs
public GameObject fireworks;

void OnTriggerEnter (Collider col) {
  if (col.transform.CompareTag ("Ball")) {
    fireworks.SetActive (true);
  }
}
```

--- collapse ---
---
title: What does the new code do?
---  

What's happening here is a **GameObject** called "fireworks" is created (you'll connect it to your fireworks in a moment) and this **script** then waits for any **Rigidbody** to touch the **collider** it's attached to (whichever one you drag it on to, in this case it'll be "WinZone").

If the thing that collided with it, which it will automatically assign to the **Collider** variable "col", happens to have the tag "Ball" then the "fireworks" object will be made to appear.

--- /collapse ---

+ Save the changes to the **script** and go back into Unity.

+ Drag the **script** onto the "WinZone" in the **Hierarchy** and then, with "WinZone" selected, drag the "Fireworks" object from the **Hierarchy** into the "Fireworks" field in the "Win Zone (Script)" section of the **Inspector**.

+ Save the game, run it and put the "Ball" in the "WinZone". See what happens!

That's all the basic pieces of the game! 

--- challenge ---

## Challenge: Make a maze for the robot

Now, this is called "MazeRobo", so there should probably be a maze... 

+ You've got one wall, so add some more cubes, play with the **Position** and **Scale** of them and build a few walls! 

+ Move the "WinZone" around a little, so it's harder to get to and give your player a real challenge!

+ If you know someone else who is making this game, try doing a swap, to see if you can beat each other's mazes!

--- /challenge ---