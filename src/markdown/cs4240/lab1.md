<h1 align="center">Lab 1 - Intro to Unity</h1>

## Preface

Great! Now that you have installed Unity Hub, let's start with creating a project. For this lab, our main focus is to introduce you to the Unity Editor as well as to build a simple environment!

## How To Create A Project

To create a project, click the "New Project" button under the Projects tab.

<p align="center">
  <img alt="" style="margin: 0 auto; object-fit:fill; max-width:700px" src="/img/unity-tut/lab1/add-project-img.png" width="90%" height="auto" />
</p>

After you clicked on New Project. Turn your attention to the Editor Version situated at the top. Ensure that you select the correct version as different Unity Versions may affect compatibility with future assets and SDKs.

It is recommended that you decide on a version early as trying to change the version in the midst of your project might actually break things!

<p align="center">
  <img alt="" style="margin: 0 auto; object-fit:fill; max-width:700px" src="/img/unity-tut/lab1/project-unity-ver-img.png" width="90%" height="auto" />
</p>

Now I have 2020.3.8f1 selected. However, for this project, let's select 2021.2.8f1 for Silicon as that's the platform I am using.

<p align="center">
  <img alt="" style="margin: 0 auto; object-fit:fill; max-width:700px" src="/img/unity-tut/lab1/project-2021-unity-ver-img.png" width="90%" height="auto" />
</p>

After that is done, let me explain a bit of what's going on below. For Unity, there are quite a number of templates that you can choose from to get started. These templates come with presets for you that is configured to the platform/setting that you are trying to build for. For this lab (Lab 1 & 2), we are going to start with the basic 3D template.

<p align="center">
  <img alt="" style="margin: 0 auto; object-fit:fill; max-width:700px" src="/img/unity-tut/lab1/project-unity-template-img.png" width="90%" height="auto" />
</p>

After selecting the template, you can give your project a name and then choose the location that you are going to store your project in, and then click on 'Create Project'!

Psst, you can now go for a quick coffee break if you want because the first-time setup might take a while (especially if your computer is slow).

Once the project has been set up. You should see this rather complicated screen that is the Unity Editor.

<p align="center">
  <img alt="" style="margin: 0 auto; object-fit:fill; max-width:700px" src="/img/unity-tut/lab1/unity-editor-img.png" width="90%" height="auto" />
</p>

Not to worry if you don't understand what's going on! For now, we'll use the default layout as it is in the image above. However, if you want to change the layout, you can always drag them as you see fit! There are also other built-in layouts that you can use by going to <code>Window -> Layout</code>.

<p align="center">
  <img alt="" style="margin: 0 auto; object-fit:fill; max-width:700px" src="/img/unity-tut/lab1/unity-layout-img.png" width="90%" height="auto" />
</p>

## Unity Editor Basics

Okay, now let's run through some of the things that you see on the screen.

### Scene

First up, let me introduce to you what is the Scene tab. But before knowing what the tab does, it is important for you to understand the concept of a Scene in Unity.

<p align="center">
  <img alt="" style="margin: 0 auto; object-fit:fill; max-width:700px" src="/img/unity-tut/lab1/unity-scene-tab-img.png" width="90%" height="auto" />
</p>

A scene is basically an asset that contains all or part of a game or application in Unity. Imagine a game where you have the Main Menu, Game World with two areas. This game can be divided into 3 scenes (or all in 1 if you choose to do so).

1. Main Menu Scene
2. Game World - Area A
3. Game World - Area B

Generally, we try to create separate scenes so that we are able to separate all the concerns of the game. The Main Menu scene for example should only be handling what the user/player sees as he loads into the game such as starting a new game, changing settings, loading a saved file or exiting the game.

This idea of having different scenes to handle different parts of the game or application is not too different from having different web pages or components in a website or a mobile app. Most game engines have a similar concept as well.

Now that you have understood what is a Scene. The Scene tab is basically the "Game World" in which you can interact and build with. All of your assets in the scene (that are in Hierarchy) will be visible in the Scene Tab and you can interact with them by clicking on them within the world.

Within the scene tab, there are various options such as turning the perspective into 2D, turning on and off different Gizmos that you don't want to see and more. Feel free to explore how they work!

Now turn your attention to this widget on the top right.

<p align="center">
  <img alt="" style="margin: 0 auto; object-fit:fill; max-width:700px" src="/img/unity-tut/lab1/unity-perspective-widget-img.png" width="90%" height="auto" />
</p>

This widget is probably the most helpful within the scene tab as it shows you the 3 dimensions (x, y, z) which will help you visualize what perspective of the scene are you looking from.
