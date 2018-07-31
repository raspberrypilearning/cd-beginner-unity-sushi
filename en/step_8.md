## Moving properly

MazeRobo moves, but it's a little...weird. It doesn't turn around to see where it's going. You can fix that! 

+ Go back into the `RoboMover` script and add this new line below `rb.MovePosition`:

```cs
rb.MoveRotation (Quaternion.LookRotation (desiredDirection, Vector3.up));
```

This line makes MazeRobo look where it's going.

+ Run the game and check it out!

MazeRobo does look where it's going, but as soon as you release the controls it springs back to looking in its original direction. You can fix that too!

--- collapse ---
---
title: Why does the robot spring back to facing the other way?
---

The problem is that Unity understands MazeRobo's original direction as the default value `0`, and so when there's no active input from the player, the input is `0`.

You need to make it so that MazeRobo will only turn based on active player input.

The check you'll use for this in the code is: **if** the player's input is bigger than a very small number \(`0.01`\), **then** move and turn. So nothing will happen for that default `0`.

--- /collapse ---

+ The first thing you'll need to do is wrap all your existing direction change code in an `if` statement, which only runs the code inside it if the condition in the brackets is `true`.

```cs
// Update is called once per frame
void Update () {

    if (true) {
      Vector3 desiredDirection = new Vector3 (Input.GetAxis ("Horizontal"), 0.0f, Input.GetAxis ("Vertical"));
      desiredDirection = moveSpeed * desiredDirection;
      desiredDirection = Time.deltaTime * desiredDirection;
      rb.MovePosition (rb.position + desiredDirection);
      rb.MoveRotation (Quaternion.LookRotation (desiredDirection, Vector3.up));
    }
}
```

--- collapse ---
---
title: What does the new code do?
---

Right now, you're forcing the `if` statement to be **true** by actually passing it `true` as the condition. This means the code will run exactly as it did before. You'll change that in a moment.

--- /collapse ---

+ Run the game and check it's all still working.

Now you need to create your test conditions.

+ Above the `if` statement but still inside the `Update` function, you'll need to collect the inputs from the user and get their **absolute** values like this:

```cs
    void Update () {

    float inputHorizontal = Mathf.Abs (Input.GetAxis ("Horizontal"));
    float inputVertical = Mathf.Abs (Input.GetAxis ("Vertical"));

    if (true) {
```

--- collapse ---
---
title: What is an absolute value, and what does it do?
---

When you tell MazeRobo to go forward, Unity sees that as a positive number \(e.g. `1`\), and when you tell it to go backwards, Unity sees that as a negative number \(e.g. `-1`\).

You just want to test for the **size** of the number, regardless of its sign, which is why you're using the absolute value of the number.

The **absolute value** is the value of the number without the sign and it's always a positive number or zero.

--- /collapse ---
 
Now it's time to update the `if` statement so it actually tests something! You'll need to change what's in the brackets after  the`if` so that it checks if `inputHorizontal` is **greater** than `0.01` **or** if `inputVertical` is **greater** than `0.01` and gives a **true** result in either case. 

To do this, you'll need to use an 'or' between your conditions that your computer can understand. In C\# \(the language you're writing your Unity scripts in\) we represent 'or' with two pipe characters, like this: `conditionA || conditionB`. There are also other ways of joining two or more conditions, for example the 'and' operator \(`&&`\), and you can look those up online if you need them.  

+ To write the 'or' condition you need, just update your `if` statement like this:

```cs
  if (inputHorizontal > 0.01f || inputVertical > 0.01f) {
```

Now MazeRobo should stay facing the direction it's just moved in! If you're having any problems, check that your `Update` function matches this:

```cs
void Update () {

  float inputHorizontal = Mathf.Abs (Input.GetAxis ("Horizontal"));
  float inputVertical = Mathf.Abs (Input.GetAxis ("Vertical"));

  if (inputHorizontal > 0.01f || inputVertical > 0.01f) {
    Vector3 desiredDirection = new Vector3 (Input.GetAxis ("Horizontal"), 0.0f, Input.GetAxis ("Vertical"));
    desiredDirection = moveSpeed * desiredDirection;
    desiredDirection = Time.deltaTime * desiredDirection;
    rb.MovePosition (rb.position + desiredDirection);
    rb.MoveRotation (Quaternion.LookRotation (desiredDirection, Vector3.up));
    }
```

![MazeRobo facing towards us](images/step8_RoboFacingCamera.png)
