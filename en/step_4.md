## Making a Robot

Time to create your first object!

+ Make a **Capsule** object \(**GameObject &gt; 3D Object &gt; Capsule**\): this will be the body of MazeRobo, your robot!

  ![The new capsule object](images/step4_capsule.png)

+ Select the **Capsule** by clicking on it. Look to the right and you should see loads of options and menus. This is called the **Inspector** and it's where you setup most of the objects in your game.

You can rename an object by typing a new name in at the top of the inspector.

+ Change the name of the **Capsule** to `MazeRobo` now.

  ![](images/step4_rename.png)

+ Next, to be sure that MazeRobo is right at the middle of the game world, look in the **Transform** section of the **Inspector**, click on the cog icon and choose "Reset".

  ![](images/step4_Transform.png)
  
+ You need a couple more objects to make your robot, so create a **Cube** \(**GameObject &gt; 3D Object &gt; Cube**\) and a **Sphere** \(**GameObjects &gt; 3D Object &gt; Sphere**\).

+ Rename the **Cube** to "Shades" and the **Sphere** to "Nose".

+ Look at the left of the screen. You should see a list of the objects in your game, including "MazeRobo", "Shades" and "Nose". Click on "Shades" and drag it onto "MazeRobo". Now drag "Nose" onto "MazeRobo" in the same way.

  ![The objects list](images/step4_moveObjects.png)
  ![The objects list after moving Shades and Nose onto MazeRobo](images/step4_afterMove.png)

--- collapse ---
---
title: Dragging pieces together
---

This puts "Shades" and "Nose" "inside" the "MazeRobo" object, so when they move, they move together. 

This lets you build complex objects \(like a game character!\) from simple ones like **Cubes**, **Spheres**, **Capsules**, etc.

--- /collapse ---

+ Now select "Shades" and look at the **Inspector**'s **Transform** section. You will see a set of three **coordinates**  \(X, Y, Z\) that control the object's **position**.

+ Try changing each of their values to see which direction they control. Try putting a `-` in front of some of the numbers too! Finally, set them to these values:

   X: 0
   Y: 0.64
   Z: 0.42

  ![Changing the position coordinates](images/step4_TransformPosition.png)

+ Do the same for "Nose", setting them like this:

    X: 0
    Y: 0.5
    Z: 0.5

It doesn't quite look like anything yet, does it? You can control the shape of an object with the **scale** controls.

+ Staying in the **Inspector** look at the **scale** controls for "Shades". Set **scale** to these values:

    X: 0.64
    Y: 0.16
    Z: 0.16

  ![Changing the scale values](images/step4_TransformScale.png)

+ Now set the "Nose" **scale** to:

    X: 0.16
    Y: 0.16
    Z: 0.16

That's starting to look like a robot! Time to add some colour!

  ![The robot character](images/step4_robot.png)



