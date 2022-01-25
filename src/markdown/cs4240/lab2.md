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

## Player Locomotion

To add physical properties to this ball and make it be able to move, we need to add Rigidbody to it. You need to choose Player at Hierarchy panel and click Add Component at Inspector panel. Search for Ridigbody and click it to add it to your Player.

<p align="center">
  <img alt="" style="margin: 0 auto; object-fit:fill; max-width:400px" src="/img/unity-tut/lab2/roll-locomotion-img.png" width="90%" height="auto" />
</p>

A Rigidbody component adds control of Unity's Physics Engine to the GameObject. Even without adding any code, a Rigidbody object will be pulled downward by gravity and will react to collisions with incoming objects if the right Collider component is also present.

The Rigidbody also has a scripting API that lets you apply forces to the object and control it in a physically realistic way. For example, a car's behaviour can be specified in terms of the forces applied by the wheels. Given this information, the physics engine can handle most other aspects of the car's motion, so it will accelerate realistically and respond correctly to collisions.

Next, let's add a custom C# Script so that we can take in Player Input and allow us to move our player ball.

<p align="center">
  <img alt="" style="margin: 0 auto; object-fit:fill; max-width:300px" src="/img/unity-tut/lab2/roll-locomotion2-img.png" width="90%" height="auto" />
</p>

We can do so by clicking on Add Component in the Inspector panel of Player, type in the name of our C# class script, hit New Script > Create and Add. This creates a PlayerLocomotion.cs file that we can edit in VSCode/Visual Studio.

Note that scripts can always be dragged in from your project folder. You can also choose to create the C# script within a separate folder in Project for better organization as adding scripts via the Inspector places the script in the root Assets folder by default.

After creating the PlayerLocomotion.cs script, double click it to edit it in VSCode/Visual Studio.
