## Voeg een kleur toe

+ Maak een nieuwe map door op **Assets > Create > Folder** te klikken en noem het `Materials (materialen)`.

+ Maak nu twee **materials** (**Assets > Create > Material**) genaamd `EyeBlack (oog zwart)` en `NoseRed (neus rood)`.

+ De twee nieuwe materialen moeten in de `Materials` map staan die je zojuist hebt gemaakt in het **Project** deelvenster onder aan het scherm. Als ze er niet zijn, sleep ze dan naar de `Materials` map om ze erin te plaatsen.

![De materialen map met de twee nieuwe materialen](images/step5_materialsFolder.png)

--- collapse ---
---
title: Dingen hernoemen
---

Je kunt de naam van een materiaal of map wijzigen door er met de rechtermuisknop op te klikken en **Rename** te selecteren.

![Rename selecteren in het rechtermuisklik-menu](images/step5_rename.png)

--- /collapse ---

+ Je kunt de kleur van een materiaal instellen door de **albedo** waarde te wijzigen in de Inspector. Klik op de rechthoek naast het pipetpictogram en een kleurkiezer zou moeten openen.

![De kleurenkiezer](images/colour_picker.png)

+ Maak `EyeBlack`'s albedo-waarde zwart en `NoseRed`'s albedo waarde rood.

+ Selecteer het `Shades` object, kijk naar de **Mesh Renderer** sectie van de Inspector en vouw de **Materials** subsectie uit. Klik op de kleine cirkel rechts van **Element 0** en selecteer `EyeBlack`. Nu heeft MazeRobo een zwarte zonnebril!

![Het Mesh Renderer-gedeelte van de inspector](images/step5_chooseMaterial.png)

+ Doe hetzelfde voor het `Nose` object zoals je deed voor het `Shades` object, selecteer nu alleen het `NoseRed` materiaal. Nu heb je MazeRobo een rode neus gegeven!

![MazeRobo met kleur toegevoegd](images/step5_mazeRoboInColour.png)

### Je robot regels geven

MazeRobo heeft een **Rigidbody (onbuigbaar lichaam)** component nodig zodat je haar kunt verplaatsen en haar met de wereld kunt laten communiceren.

+ Selecteer MazeRobo en klik op **Component > Physics > Rigidbody**. Hiermee kun je regels instellen voor hoe MazeRobo zich gedraagt in het spel.

+ Je zult nu zien dat wanneer je MazeRobo hebt geselecteerd, er een **Rigidbody** sectie is in de Inspector. Open de **Constraints (beperkingen)** subsectie van de **Rigidbody** sectie en stel **Freeze Rotation (bevries rotatie) X, Y en Z** in op **True (waar)** door in alle vakjes te klikken. In **Freeze Position (bevries positie)**, stel **Y** in op **True** door op dat vakje te klikken.

![De Rigidbody-constraints instellen](images/step5_RigidbodyConstraints.png)

+ Nu heb je een basis robotkarakter dat je in je spel kunt gebruiken. Je kunt het echt je eigen maken door een paar kleuren te veranderen of er misschien extra stukken aan toe te voegen met meer **3D-Objects** die je kunt positioneren, zoals je deed in de laatste stap! Als je eenmaal tevreden bent met je robot, ga je verder met de volgende stap.
