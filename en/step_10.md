## Give MazeRobo something to play with

Now that you've got your character and it's moving around properly, it's time to give it something to play with! You're going to add a ball for the robot to push around.

+ Start by creating a **Sphere** (**GameObject > 3D Object > Sphere**). Rename it to `Ball`. 

+ Set the **Transform** of Ball so as the **position** is:

  X: 0
  Y: 1
  Z: 2
 
+ Make another material (see the **Adding colour** step if you don't remember how!) and make it green. Call it BallGreen and drag it onto "Ball"!

![The sphere and the green material](images/step10_AddGreenBall.png)

If you test the game now and walk MazeRobo into the sphere, you'll notice it behaves just like the wall: It doesn't move. You want this to be a rolling ball, though, so you'll need to give it some rules for moving, like MazeRobo has.

+ Select "Ball" and give it a **Rigidbody** component (**Component > Physics > Rigidbody**).

+ Now try playing!

![Gameplay now with a ball that rolls](images/step10_RollingBall.png)