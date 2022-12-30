---
title: "Fluid Simulation - 1"
date: 2022-12-30T15:07:48+05:30
slug: "Fluid Simulation"
description: "Introduction to Fluid Simulation in JavaScript"
keywords: []
draft: false
tags: []
math: false
toc: false
---

## Initial Setup 
To do anything fun with ```HTML```, you need the ```canvas``` tag. 
In this post, we will setup the following. 

    1. Files 
    2. Folders 
    3. Basic boiler-plate code for each file. 
    4. Basics of HTML canvas

### File & Folders 

Fire up whatever code-editor or IDE you use for web development, create a ```index.html``` file. This will be the index point for our canvas.  
<br>
The HTML file doesn't have to be elaborate with a lot of styling. We will create a simple HTML file and, essentialy we won't have the need to look back at it.
The content of your HTML file should like this:

```
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Fluid Simulation - Element JS</title>
</head>
<body>
    <canvas id="c"></canvas>
</body>
</html>
```
In the code above the, most important component is the ```canvas``` tag.
The ```canvas``` element, is essentially used to render animations and graphics on the webpage.
The canvas element has ```height``` & ```width``` properties, giving you the ability to set the ```canvas``` element to desired height and widht; much like every other ```HTML``` component.

***Why canvas?***

```Canvas``` allows you to render scriptable graphics. 
```HTML5 canvas``` allows you render bitmaps as well as 2D shapes using it's own ```API``` and ```WebGL```. Canvas is the central element that is used to make web-games using JavaScript.    

The element ```canvas``` is just an empty whiteboard and the element itself doesn't render any objects on the screen, nor can you render objects inside the Canvas using raw `HTML` & `CSS`. In order to make use the `canvas`, and render anything - you have to use JavaScript to render anything.

<br>

With that said, let's add a JavaScript file to our project.
Let's create a JavaScript file named `fluid.js`. You can name it whatever you want, but for better understanding lets call it `fluid.js` only.

Do not forget to import this script into your `HTML` file.

>Like this:

`<script defer type="text/javascript" src="/fluid.js"></script>`


The last file we need to add is the `CSS` file. There is not much to explain in the `CSS` file. 
The rules we will describe are only going to there to setup the stage for the `canvas`.

These are the contents for the `CSS` file:

```
* {
    margin: 0;
    padding: 0;
}

body{
    margin: 0;
    background: #272727;
    font-family: "Raleway";
}

canvas{
    background-color: #131313;
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    margin: auto;
    border: 5px solid white;
}
```

We are adding the backgroung color to the canvas here, along with the border to make sure it is visible and stands out from rest of the objects on the screen.