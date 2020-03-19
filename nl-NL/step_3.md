## Maak een robot

Tijd om je eerste object te maken!

+ Maak een ** Capsule ** object \ (** GameObject > 3D Object > Capsule ** \): dit wordt het lichaam van MazeRobo, jouw robot!

  ![Het nieuwe capsule-object](images/step4_capsule.png)

+ Selecteer de capsule door erop te klikken. Aan de rechterkant zou je heel veel opties en menu's moeten zien. Dit heet de ** Inspector **, en hier stel je de meeste objecten in je spel in.

U kunt de naam van een object wijzigen door bovenaan de Inspector een nieuwe naam in te voeren.

+ Verander nu de naam van de Capsule in `MazeRobo`.

  ![](images/step4_rename.png)

+ Om er zeker van te zijn dat MazeRobo midden in de gamewereld staat, kijk je in de ** Transform ** sectie van de Inspector, klik op het tandwielpictogram en kies ** Reset **.

  ![](images/step4_Transform.png)

+ Je hebt nog een paar objecten nodig om je robot te maken, dus maak een **Cube** \ (** GameObject > 3D Object > Cube ** \) en een ** Sphere ** \ (** GameObjects > 3D Object > Sphere ** \).

+ Wijzig de naam van de kubus in ` zonnebril `, en de naam van de bol naar ` neus `.

+ Kijk aan de linkerkant van het scherm. Je zou een lijst met de objecten in je game moeten zien, inclusief ` MazeRobo `, ` Zonnebril `, en ` Neus `. Klik op ` Zonnebril ` en sleep het naar ` MazeRobo `. Sleep vervolgens ` Neus ` op ` MazeRobo ` op dezelfde manier.

  ![The objects list](images/step4_moveObjects.png) ![The objects list after moving Shades and Nose onto MazeRobo](images/step4_afterMove.png)

--- collapse ---
---
title: Dragging objects together
---

This puts the `Shades` and `Nose` objects 'inside' the `MazeRobo` object, so when they move, they move together.

Putting objects 'inside' other objects lets you build up complex objects \(like a game character!\) from simple ones like Cubes, Spheres, Capsules, etc.

--- /collapse ---

+ Now select the `Shades` object and look at the Inspector's **Transform** section. You will see a set of three **coordinates**  \(X, Y, Z\) that control the object's **Position**.

+ Try changing each of the coordinates' value to see which direction they control. Try putting a `-` in front of some of the numbers too! Finally, set them to these values:
```
   X = 0
   Y = 0.64
   Z = 0.42
```
  ![Changing the position coordinates](images/step4_TransformPosition.png)

+ Do the same for `Nose`, setting them like this:
```
    X = 0
    Y = 0.5
    Z = 0.5
```
This doesn't quite look like anything yet, does it? Om MazeRobo op een robot te laten lijken, pas je de ` Zonnebril ` aan en ` neus ` ziet eruit als. You can control the shape of objects with the **Scale** controls.

+ Kijk nog even in de ** Inspector **, en bekijk daar de scale control (schaal bediening) voor ` Schaduwen `. Set its scale to these values:
```
    X = 0.64
    Y = 0.16
    Z = 0.16
```
  ![Changing the scale values](images/step4_TransformScale.png)

+ Now set the `Nose` scale to:
```
    X = 0.16
    Y = 0.16
    Z = 0.16
```
Now it's starting to look like a robot!

  ![The robot character](images/step4_robot.png)

In the next step, it's time to add some colour!
