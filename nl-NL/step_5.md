## Maak de grond van je spelwereld

Nu ga je een grondvlak maken voor MazeRobo om verder te gaan!

+ Begin met het toevoegen van een ** Quad ** object om de grond te zijn (** GameObject > 3D Object > Quad ** ). Verander de naam van dit object van ` Quad ` naar ` Ground ` in de Inspector.

+ In de Inspector voor dit nieuwe object onder ** Transform **, stel de ** X-rotatie in ** tot ` 90 `, en voor ** Scale **, voer deze waarden in:
```
  X = 40.96
Y = 40.96
Z = 1
```

  ![De transform properties voor de grond instellen](images/step6_groundTransform.png)

Oei! MazeRobo's zit halverwege de grond vast! Laten we haar een meter opschuiven.

+ Selecteer MazeRobo en in de Inspector onder ** Transformeren **, stel de volgende ** positie in ** coördinaten:
```
  X = 0
Y = 1
Z = 0
```
  ![MazeRobo op de grond plaatsen](images/step6_MazeRoboOnGround.png)

Nu voeg je een muur toe om je doolhof te starten!

+ Maak een kubus (** GameObject > 3D Object > Cube **) en stel de ** Transform Position ** in naar:
```
  X = -2
Y = 1.5
Z = 0 
```
+ Stel de Y ** schaal in ** tot ` 3 ` en hernoem het object naar ` Muur `.

+ Maak nu een nieuw materiaal voor ` Wall ` (** Activa > Creëer > materialen **), hernoem het ` WallBlue `, en verander het albedo om het een (verrassing!) blauwe kleur te geven.

+ Wijs de ` WallBlue toe ` materiaal aan ` Muur ` met behulp van de ** MeshRender > materialen ** sectie van de Inspector (je kunt het materiaal ook rechtstreeks naar het object slepen).

Later verander je deze muur in een doolhof, zodat MazeRobo deze kan verkennen!

![MazeRobo naast het Wall-object](images/step6_Wall.png)
