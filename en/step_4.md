## Making a Robot

+ Now create your first object! Make a **Capsule** object \(**GameObjects &gt; 3D Object &gt; Capsule**\): this will be the body of MazeRobo, your robot!

+ Select the **Capsule** by clicking on it. Look to the right and you should see loads of options and menus. This is called the **Inspector** and it's where you setup most of the objects in your game.

+ You can rename an object by typing a new name in at the top of the inspector. Change the name of the **Capsule** to `MazeRoboBody` now.

+ Next, to be sure that MazeRobo is right at the middle of the game world, look in the **Transform** section of the **Inspector**, click on the cog icon and choose "Reset".

+ You need a couple more objects to make your robot, so create a **Cube** \(**GameObjects &gt; 3D Object &gt; Cube**\) and a **Sphere** \(**GameObjects &gt; 3D Object &gt; Sphere**\).

+ Rename the **Cube** to "Shades" and the **Sphere** to "Nose".

+ Look at the left of the screen. You should see a list of the objects in your game, including "MazeRoboBody", "Shades" and "Nose". Click on "Shades" and drag it onto "MazeRobo". Now drag "Nose" onto "MazeRobo" in the same way.

--- collapse ---
---
title: Dragging pieces together
---

This puts "Shades" and "Nose" "inside" the "MazeRobo" object, so when they move, they move together. 

This lets you build complex objects \(like a game character!\) from simple ones like **Cubes**, **Spheres**, **Capsules**, etc.

--- /collapse ---

+ Now select "Shades" and look at the **Inspector**'s **Transform** section. You will see a set of three **coordinates**  \(X, Y, Z\) that control the object's **position**. Try changing each of their values to see which direction they control. Try putting a `-` in front of some of the numbers too! Finally, set them to these values:

   X: 0
   Y: 0.64
   Z: 0.42

+ Do the same for "Nose", setting them like this:

   X: 0
   Y: 0.5
   Z: 0.5

+ It doesn't quite look like anything yet, does it? Staying in the **Inspector** look at the **scale** controls. They control the shape of the object. Set "Shades" **scale** to these values:

   X: 0.64
   Y: 0.16
   Z: 0.16

+ Now set "Nose" **scale** to:

   X: 0.16
   Y: 0.16
   Z: 0.16

That's starting to look like a robot! Time to add some colour!



