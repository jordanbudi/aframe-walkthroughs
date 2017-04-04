# Adding Physics

This is a basic example of applyng physics. Notice the only change to the head is a diferent script that incorporates the pyhsics. We then create a player similar to how we created a cursor and objects similar to how we created them before. The main change is to assign each object as either a static body or a dynamic body.

Play around with the different objects and feel free to create your own.

As a challenge, see if you can push the ball us the ramp!

```html
<!DOCTYPE html>
<html>
    <head>
        <title>
            Physics
        </title>
        <script src="https://sandbox.donmccurdy.com/vr/aframe-extras.js"></script>
    </head>
    <body>
    <a-scene>
      
      <!-- Ground The default is 75 by 75-->
      <a-grid static-body></a-grid>
      
      <!-- Walls -->
      <a-box color="#39BB82"
             width="75" height="2" depth="2"
             position="0 1 -36.5"
             static-body></a-box>
      <a-box color="#39BB82"
             width="75" height="2" depth="2"
             position="0 1 36.5"
             static-body></a-box>
      <a-box color="#39BBBB"
             width="2" height="2" depth="71"
             position="36.5 1 0"
             static-body></a-box>
      <a-box color="#39BBBB"
             width="2" height="2" depth="71"
             position="-36.5 1 0"
             static-body></a-box>

    <!-- Ojects you can push are lightblue -->
      <a-box color="lightblue"
             position="8 2.5 0"
             dynamic-body></a-box>
      <a-sphere color="lightblue"
             roughness="0.2"
             position="-2 1 -5"
             dynamic-body></a-sphere>
      <a-sphere color="lightblue"
             roughness="0.9"
             position="1 2 20"
             radius="0.5"
             dynamic-body></a-sphere>
             
    <!-- Stationary objects are red  -->
      <a-box color="#b2260e"
             position="1 1.5 -10"
             width="2"
             depth ="2"
             height="3"
             static-body></a-box>
      <a-box color="#b2260e"
             position="1 1 20"
             width="4"
             depth ="4"
             height="2"
             static-body></a-box>
      <a-box color="#b2260e"
             position="7.2 0.5 20"
             rotation="71 -90 0"
             width="4"
             depth="0.1"
             height="9"
             static-body></a-box>
    
    <!-- Player -->
      <a-entity camera
                universal-controls
                kinematic-body
                position="0 1.764 0"
                jump-ability>
      </a-entity>
             
      <!-- Lighting -->
      <a-light type="ambient" color="#bbb"></a-light>
      <a-light color="#ccc" position="0 30 0" distance="100" intensity="0.4" type="point"></a-light>
      <a-light color="#ccc" position="3 10 -10" distance="50" intensity="0.4" type="point"></a-light>
    </a-scene>
    </body>
</html>
```