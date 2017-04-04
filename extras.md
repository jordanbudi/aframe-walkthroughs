# A-Fram 3rd Party Extras
In this example, we are exploring some basic add ons, while still using the physics property.

This example uses a simple command to create an ocean. Feel free to play with some of the variables such as density, speed, and opacity.

The example also uses a box with a sand texture that is repeated to create a beach and some simple objects to create a pier.

Use the jump ability (space bar) to try and jump from post to post at the end of the sphere.


**Example 1**
```html
    <!DOCTYPE html>
<html>
    <head>
        <title>
            Using extras
        </title>
        <script src="https://sandbox.donmccurdy.com/vr/aframe-extras.js"></script>
    </head>
    <body>
    <a-scene fog="type: exponential; color: #FFF; density: 0.02;">
    <a-assets>
                <img id="sand" src="http://mycode.zone/res/sand.jpg">
    </a-assets>
      <!-- Player -->
      <a-entity camera
                universal-controls
                kinematic-body
                position="0 1.764 0"
                jump-ability>
      </a-entity>

      <!-- Ocean and Beach -->
      <a-ocean width="75" depth="50" density="40" position="0 0 -25" static-body></a-ocean>
      <a-box material="src: #sand; repeat: 25 25" width="75" depth="0.1" height="75" rotation="85 0 0"
            position="0 0 0" static-body></a-box>
      
      <!-- Pier -->
      <a-box position="13 1 -9" width="3" height="0.25" depth="30" color="#562c01" static-body></a-box>
      <a-cylinder position="12 -24 -1" color="#562c01" radius=".25" height="50"></a-cylinder>
      <a-cylinder position="14 -24 -1" color="#562c01" radius=".25" height="50"></a-cylinder>
      <a-cylinder position="12 -24 -9" color="#562c01" radius=".25" height="50"></a-cylinder>
      <a-cylinder position="14 -24 -9" color="#562c01" radius=".25" height="50"></a-cylinder>
      <a-cylinder position="12 -24 -23" color="#562c01" radius=".25" height="50"></a-cylinder>
      <a-cylinder position="14 -24 -23" color="#562c01" radius=".25" height="50"></a-cylinder>
      
      <!-- posts -->
      <a-cylinder position="13 -24 -28" color="#562c01" height="50" static-body></a-cylinder>
      <a-cylinder position="10 -24 -33" color="#562c01" height="50" static-body></a-cylinder>
      <a-cylinder position="9 -24 -37" color="#562c01" height="50" static-body></a-cylinder>
      <a-cylinder position="9 -24 -42" color="#562c01" height="50" static-body></a-cylinder>
     
     
      <!-- Lighting -->
      <a-entity light="type: hemisphere; color: #AAA; groundColor: #000000; intensity: 0.9;"></a-entity>
      <a-entity light="type: ambient; color: #DC8874; intensity: 0.5;"></a-entity>
    </a-scene>
    </body>
</html>
```

**Example 2**

```html
<!DOCTYPE html>
<html>
    <head>
        <title>
            Maze
        </title>
        <script src="https://sandbox.donmccurdy.com/vr/aframe-extras.js"></script>
    </head>
    <body>
    <a-scene>
     <!-- Create a dynamic sphere here.
     Radius should be 0.5 -->
     
      <a-sphere color="lightblue"
             position="0 1 0"
             radius="0.5"
             dynamic-body></a-sphere>
     
     <!-- Player -->
      <a-entity camera
                universal-controls
                kinematic-body
                position="0 1.764 2"
                jump-ability>
      </a-entity>
      
      <!-- Ground The default is 75 by 75-->
      <a-grid static-body></a-grid>
      
      <!-- Walls -->
      <a-box color="#39BB82"
             width="40" height="2" depth="2"
             position="0 1 -19"
             static-body></a-box>
      <a-box color="#39BB82"
             width="40" height="2" depth="2"
             position="0 1 19"
             static-body></a-box>
      <a-box color="#39BBBB"
             width="2" height="2" depth="36"
             position="19 1 0"
             static-body></a-box>
      <a-box color="#39BBBB"
             width="2" height="2" depth="32"
             position="-19 1 -2"
             static-body></a-box>
       <a-box color="#39BBBB"
             width="1" height="2" depth="32"
             position="-11 1 -2"
             static-body></a-box>
      <a-box color="#39BBBB"
             width="1" height="2" depth="20"
             position="-3 1 -2"
             static-body></a-box>
      <a-box color="#39BBBB"
             width="1" height="2" depth="26"
             position="3 1 5"
             static-body></a-box>
      <a-box color="#39BBBB"
             width="22" height="2" depth="1"
             position="8.5 1 4"
             static-body></a-box>
      <a-box color="#39BBBB"
             width="17" height="2" depth="1"
             position="6 1 -11.5"
             static-body></a-box>
      <a-box color="#39BBBB"
             width="1" height="2" depth="12"
             position="7 1 -2"
             static-body></a-box>
      <a-box color="#39BBBB"
             width="1" height="2" depth="12"
             position="11 1 -5"
             static-body></a-box>
       <a-box color="#39BBBB"
             width="1" height="2" depth="12"
             position="14 1 -5"
             static-body></a-box>
       <a-box color="#39BBBB"
             width="10" height="2" depth="1"
             position="-5.5 1 13.5"
             static-body></a-box>
             
      <!-- Lighting -->
      <a-light type="ambient" color="#bbb"></a-light>
      <a-light color="#ccc" position="0 30 0" distance="100" intensity="0.4" type="point"></a-light>
      <a-light color="#ccc" position="3 10 -10" distance="50" intensity="0.4" type="point"></a-light>
    </a-scene>
    </body>
</html>
```