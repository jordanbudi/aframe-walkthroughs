# Interactivity (Cursor/Onclick)

In this example, you will see several new concepts. The first is the cursor on the screen. Notice that the cursor is set as part of the camera entity. This is done so that it is always directly in front of the user in the VR exerience.

The next idea is the concept of interacting with the environment. On the desktop, we can interact with a mouse click. Position the cursor over an element and click on it to trigger the animation.

In a emersive VR world such as google cardboard, we may not have a button to click, so the concept of a fuse is introduced. Set the fuse to true and then move the cursor over the object to see what happens.

**Example 1**

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Interaction</title>
      <script src="https://aframe.io/releases/0.5.0/aframe.min.js"></script>
  </head>
  <body>
    <a-scene>
        <!-- Use the cursor to position it over the box and click -->
        <a-box position="1 0 -4" height="1" 
                width="1" depth="1" color="#b79f03">
            <a-animation
                attribute="rotation"
                from="0 0 0"
                to="180 180 0"
                dur="3000"
                begin="click">
            </a-animation>
        </a-box>
        <a-sphere position="-1 0 -4" radius="0.5" color="#803d8c">
            <a-animation
                attribute="scale"
                from="1 1 1"
                to="4 4 4"
                dur="2000"
                begin="click"
                easing="ease-out"
                fill="none">
            </a-animation>
        </a-sphere>
        <a-camera>
            <!-- Try changing the fuse to true and see what happens -->
            <a-cursor fuse="false" fuse-timeout="1500"></a-cursor>
        </a-camera>
        <a-sky color="#AAB"></a-sky>
    </a-scene>
  </body>
</html>

```

**Example 2**

```html

<!DOCTYPE html>
<html>
  <head>
    <title>Basic Interaction</title>
      <script src="https://aframe.io/releases/0.5.0/aframe.min.js"></script>
  </head>
  <body>
    <a-scene>
        <!-- Use the cursor to position it over the box and click -->
        <a-box position="-1 0 -4" height="2" 
                width="1" depth="1" color="#586c8c">
            <a-animation
                attribute="position"
                from="-1 0 -4"
                to="1 0 -4"
                dur="2000"
                begin="click"
                direction="alternate">
            </a-animation>
        </a-box>
        <a-camera>
            <a-cursor></a-cursor>
        </a-camera>
        <a-sky color="#efd6b8"></a-sky>
    </a-scene>
  </body>
</html>
```

**Example 3**

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Interaction</title>
      <script src="https://aframe.io/releases/0.5.0/aframe.min.js"></script>
  </head>
  <body>
    <a-scene>
        <!-- Use the cursor to position it over the box and click -->
        <a-cone position="2 1 -4" height="1" 
                radius-bottom="0" radius-top="1" color="tomato">
            <a-animation
                attribute="rotation"
                from="0 0 0"
                to="0 0 180"
                dur="1000"
                begin="click"
                direction="alternate">
            </a-animation>
        </a-cone>
        <a-sphere position="-2 1 -4" radius="1.5" color="gold">
            <a-animation
                attribute="position"
                from="-2 1 -4"
                to="-2 1 -12"
                dur="2000"
                begin="click"
                direction="alternate">
            </a-animation>
        </a-sphere>
        <a-camera>
            <!-- Try changing the fuse to true and see what happens -->
            <a-cursor fuse="false" fuse-timeout="1500"></a-cursor>
        </a-camera>
        <a-sky color="#AAB"></a-sky>
    </a-scene>
  </body>
</html>

```