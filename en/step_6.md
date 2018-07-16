## Making the ground

Now you're going to create a ground plane for MazeRobo to move about on!

+ Start by adding a **Quad** to be the ground (**GameObject > 3D Object > Quad**). Change the name of this object from `Quad` to `Ground` using the **inspector**.
 
+ In the **inspector** for this object under **transform** set the **X** **rotation** to 90. In the **transform**'s **scale** section, enter the values of: 
  X=40.96
  Y=40.96
  Z=1

  ![Setting the transform properties for the ground](images/step6_groundTransform.png)

Gah! MazeRobo’s stuck halfway into the ground! Let's move her up by one meter.

+ Select MazeRobo and, in the **inspector** under **transform** set the following **position** coordinates: 

  X=0
  Y=1
  Z=0

  ![Positioning MazeRobo onto the ground](images/step6_MazeRoboOnGround.png)
 
Now you’ll add a wall to start your maze!

+ Create a Cube (**GameObject > 3D Object > Cube**) and set its **transform position** to:

  X=-2
  Y=1.5
  Z=0 

+ Make the Y **scale** `3` and rename the object to `Wall`.
 
+ Now make a new material for "Wall" (**Assets > Create > Materials**), rename it `WallBlue` and give it a (surprise!) blue colour.

+ Assign the "WallBlue" material to "Wall" using the **MeshRender > Materials** section of the **inspector** (you can also drag the colour straight onto the object).

Later on, you’ll turn this wall into a maze for MazeRobo to explore!

![MazeRobo next to the Wall object](images/step6_Wall.png)
