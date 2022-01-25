<h1 align="center">Lab 2 - Scripting with C# in Unity</h1>

## Preface

Great! Now that you have mastered the Unity Engine. It's time to code and have a small running game! This time, we will do a “Roll a Ball” game. You can either use the same project from Lab 1 or create a new one, just make sure that you use a different scene this time!

## Building the Surface

Before we place our player in the game, let's first define the ground in which our player will roll on. Click on the + sign next to Hierarchy (or from GameObject above) > 3D Object > Plane to create a plane in your scene. You may rename it as Ground.

<p align="center">
  <img alt="" style="margin: 0 auto; object-fit:fill; max-width:400px" src="/img/unity-tut/lab2/roll-ground-img.png" width="90%" height="auto" />
</p>

Next, set its position as (0, 0, 0) and its scale as (2, 1, 2) in the Inspector Panel under the Transform Component.

<p align="center">
  <img alt="" style="margin: 0 auto; object-fit:fill; max-width:300px" src="/img/unity-tut/lab2/roll-plane-img.png" width="90%" height="auto" />
</p>

<p align="center">
  <img alt="" style="margin: 0 auto; object-fit:fill; max-width:500px" src="/img/unity-tut/lab2/roll-plane2-img.png" width="90%" height="auto" />
</p>

After you have created the ground, let's create our Player! You can click GameObject > 3D Object > Sphere to create a ball in your scene and rename it as “Player”.

<p align="center">
  <img alt="" style="margin: 0 auto; object-fit:fill; max-width:600px" src="/img/unity-tut/lab2/roll-player-img.png" width="90%" height="auto" />
</p>

You should set the position of this ball as (0, 0.5, 0) in the Inspector to make this ball perfectly stand on the plane.

<p align="center">
  <img alt="" style="margin: 0 auto; object-fit:fill; max-width:300px" src="/img/unity-tut/lab2/roll-player2-img.png" width="90%" height="auto" />
</p>

At Project panel, right click and choose Create > Folder. You can name this folder as “Materials”. Then right click this folder and choose Create > Material to create a new material, named as “Background”. You can choose your favorite color at Albedo to set this material color. Afterwards, drag it to the plane within the Scene to colour it. Alternatively, you can change the materials in the Mesh Renderer component in the Ground GameObject.

<p align="center">
  <img alt="" style="margin: 0 auto; object-fit:fill; max-width:800px" src="/img/unity-tut/lab2/roll-ground2-img.png" width="90%" height="auto" />
</p>
