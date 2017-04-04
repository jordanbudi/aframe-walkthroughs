# Embedding Media (Audio/Video)

Take time to explore this example using images. The first image is a special 360 degree image (like one that might be taken with a Theta S camera) and it is used as a background.

The second image is a 360 image of the Earth and bent around a sphere object as a texture. This gives the sphere the sense that it is a globe. Notice the size and position as well. By putting it far away and bigger, it makes it more fixed in the sky as you move around.

The third image is a flat texture applied to a box. Notice how the pattern repeats.


```html
<!DOCTYPE html>
<html>
    <head>
        <title>
            Embedding Media
        </title>
        <script src="https://aframe.io/releases/0.5.0/aframe.min.js"></script>
    </head>
    <body>
        <a-scene>
            <a-assets>
                <img id="planet" src="http://mycode.zone/res/spaceGirl.png">
                <img id="globe" src="http://mycode.zone/res/earth.gif">
                <img id="texture" src="http://mycode.zone/res/texture.jpg">
            </a-assets>
            <!-- Try switching the images around on different objects -->
            <a-sphere src="#globe" 
                rotation="0 0 -23.5" 
                position="-800 600 -200"
                radius="100">
                    <a-animation
                        attribute="rotation"
                        from="0 0 -23.5"
                        to="0 360 -23.5"
                        dur="10000"
                        easing="linear"
                        repeat="indefinitely"
                    >
                    </a-animation>
            </a-sphere>
            <a-box src="#texture"
                position="0 0 -2">
            </a-box>
            <a-sky src="#planet"></a-sky>
            <!-- The camera is put in an entity and rotated to
                change the starting position. Try changing this. -->
            <a-entity rotation = "15 75 0">
                <!-- Try setting wasd controls to true and see what happens -->
                <a-camera wasd-controls-enabled="false"></a-camera>
            </a-entity>
    </a-scene>
    </body>
</html>
```