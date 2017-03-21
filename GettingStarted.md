# Teaching Students How to Build Virtuality Reality Content for the Web

## Introduction
WebVR is still in its early stages and provides access to Virtual Reality devices, such as the Oculus Rift, HTC Vive, Samsug Gear VR, or Google Cardboard, in your browser. 

[A-Frame](http://aframe.io "A-Frame Homepage") is an open-source web framework for building virtual reality experiences for the browser. We can build VR web pages that users can walk into with just HTML.

## Why Use A-Frame

A-Frame makes VR more accessible since you can develop and render VR experiences in the browser as opposed to needing resource heavy platforms such as Unity. This is especially important for schools with limited technology where student devices have limited graphics capabilities or inexpensive devices, like Chromebooks, are not only more common but necessary to fit budget constraints ([you can't install Unity on Chromebooks](https://unity3d.com/unity/system-requirements "Unity System Requirements")).

A-Frame is also an easy leap for students who have already been introduced to basic HTML. There are definitely a number of other WebVR frameworks and tools to use, but my teacher personal preference is to get kids to write code and A-Frame currently fits that need.

## Getting Started with Your Coding Environment

### Selecting an IDE
For the purpose of getting started, we will be using 2 different Interactive Development Environments (IDEs). We chose these IDE's specifically because they are web based which means that no installation of software is necessary; this is useful for schols were Chromebooks are since since they are one of the most affordable options for schools. You can still use code editors like Atom or Sublime, but you'll need set up a Web Development Environment on your computer which can be a little more complicated for beginners.

#### Thimble by Mozilla
Though this isn't a true IDE, [Thimble by Mozilla](https://thimble.mozilla.org) is an online code editor that makes it easy to create and publish web pages while learning HTML, CSS & JavaScript. It is great for beginners wanting to learn a web design/webVR workflow which provides a good scaffold to then transition to “real-life” tools such as Cloud 9.

![Mozilla Logo](https://pbs.twimg.com/media/CP8Qhl3XAAA1uRH.png)

In terms of our experience with WebVR, the biggest limitation of Thimble is that it doesn't work really well with file uploads:

1. You can't upload mass files into folders. Thimble lets you upload files into the root directory, but then you have to move them one by one into their respective folders. It's a mess for organization.
2. It only supportes a limited number of file types. This especially becomes troublesome when you want to import 3D object files because Thimble doesn't recognize .mtl files.

As such, when we get deeper into our A-Frame tutorials, we will transition into using Cloud 9 exclusively.

#### Cloud 9
[Cloud 9](https://c9.io) is an online development environment. It supports hundreds of programming languages and enables developers to get started with coding immediately with pre-configured workspaces and other development features. 

![Cloud 9 Logo](http://nethusiastic.com/wp-content/uploads/2013/12/c9.jpg)

[Cloud 9 has various tiered pricing options](https://c9.io/pricing) to include free indivual options, but also an Education plan at $1/month for unlimited students. I recommend the Education Plan because it allows students to create accounts without needing to provide Credit Card information, but also because it houses all the accounts into one Team Subscription, allowing teachers to view students' work.

### Setting Up Your Coding Space
You start by setting up your basic HTML page. This file is normally called `index.html`.

Inside your `index.html` file, write the following:

```html
	<!DOCTYPE html>
	<html>
		<head>
			<script src="https://aframe.io/releases/0.5.0/aframe.min.js"></script>
		</head>
		<body>
			<a-scene>
			
			</a-scene>
		</body>
	</html>
```

The line `<script src="https://aframe.io/releases/0.5.0/aframe.min.js"></script>` links your html file to the A-Frame library giving you access to all the VR components. In between the `<a-scene>` `</a-scene>` tags is where all your A-Frame coding will go in.

## Creating Your First WebVR World

Let's add a sphere to our `index.html` file by adding the following line inside he `<a-scene>` `</a-scene>` tags:

```html
<a-sphere position="0 1.25 -5" radius="1.25" color="#EF2D5E"></a-sphere>
```

Your `index.html` file should look like so:

```html
	<!DOCTYPE html>
	<html>
		<head>
			<script src="https://aframe.io/releases/0.5.0/aframe.min.js"></script>
		</head>
		<body>
			<a-scene>
				<a-sphere position="0 1.25 -5" radius="1.25" color="#EF2D5E"></a-sphere>
			</a-scene>
		</body>
	</html>
```

When you preview your webpage you should see a single sphere. On desktop computer you can look around with a click and drag of the mouse. You can also walk around with the WASD keys. 

If you play around with the attributes, you'll notice that the position attribute, `position="0 1.25 -5" `, controls where the object is placed in the canvas based of an x, y, z coordinate system.

The radius attribute `radius="1.25"` controls the size of the sphere, and the `color='#EF2D5E'` controls the color which takes a hex-value, color name (such as `color='green'`), or rgb value such as `color='rgb(0,255,0)'`. 

Add the `<a-box>`, `<a-cylinder>`, `<a-plane>` elements inside the same `<a-box>` as shown below. 


```html
	<!DOCTYPE html>
	<html>
		<head>
			<script src="https://aframe.io/releases/0.5.0/aframe.min.js"></script>
		</head>
		<body>
			<a-scene>
				<a-sphere position="0 1.25 -5" radius="1.25" color="#EF2D5E"></a-sphere>
				<a-box position="-1 0.5 -3" rotation="0 45 0" width="1" height="1" depth="1" color="#4CC3D9"></a-box>
				<a-cylinder position="1 0.75 -3" radius="0.5" height="1.5" color="#FFC65D"></a-cylinder>
				<a-plane position="0 0 -4" rotation="-90 0 0" width="4" height="4" color="#7BC8A4"></a-plane>
			</a-scene>
		</body>
	</html>
```

Play around with the attributes to learn more about how they are used. 

