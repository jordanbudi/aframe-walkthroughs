# Shapes


**Example 1**
```html
<!DOCTYPE html>
<html>
    <head>
        <title>
            Making Shapes
        </title>
        <script src="https://aframe.io/releases/0.5.0/aframe.min.js"></script>
    </head>
    <body>
        <a-scene>
            <a-sphere position="-1 2 -4" radius="1" color="lightblue"></a-sphere>
            <a-box position="1 2 -3" width="1" height="1" 
            depth="1" color="pink"></a-box>
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
            Forrest
        </title>
        <script src="https://aframe.io/releases/0.5.0/aframe.min.js"></script>
    </head>
    <body>
        <a-scene>
            <a-plane position="0 0 -3.8" rotation="-90 0 0" width="6" height="6" color="lightblue"></a-plane>
            <a-box position="0 .5 -3" width="1" height="1" depth="1" color="green"></a-box>
            <a-sphere position="0 1.5 -3" radius=".5" color="yellow"></a-sphere>
        
            <!--To Make a Tree Copy the Next 2 lines-->
            <a-cylinder position="2 1.5 -5" radius=".25" height="3" color="brown"></a-cylinder>
            <a-sphere position="2 3 -5" radius="1.25" color="green"></a-sphere>
            
            <a-cylinder position="-2 1.5 -5" radius=".25" height="3" color="brown"></a-cylinder>
            <a-sphere position="-2 3 -5" radius="1.25" color="green"></a-sphere>
            
            <a-cylinder position="-2.5 1.5 -3" radius=".25" height="3" color="brown"></a-cylinder>
            <a-sphere position="-2.5 3 -3" radius="1.25" color="green"></a-sphere>
            
            <a-cylinder position="2 1.5 -6.5" radius=".25" height="3" color="brown"></a-cylinder>
            <a-sphere position="2 3 -6.5" radius="1.25" color="green"></a-sphere>
            
            <a-cylinder position="-2 1.5 -6.5" radius=".25" height="3" color="brown"></a-cylinder>
            <a-sphere position="-2 3 -6.5" radius="1.25" color="green"></a-sphere>
            
            <a-cylinder position="2 1.5 -8" radius=".25" height="3" color="brown"></a-cylinder>
            <a-sphere position="2 3 -8" radius="1.25" color="green"></a-sphere>
            
            <a-cylinder position="-2 1.5 -8" radius=".25" height="3" color="brown"></a-cylinder>
            <a-sphere position="-2 3 -8" radius="1.25" color="green"></a-sphere>
            
            <a-cylinder position="2 1.5 -9.5" radius=".25" height="3" color="brown"></a-cylinder>
            <a-sphere position="2 3 -9.5" radius="1.25" color="green"></a-sphere>
            
            <a-cylinder position="-2 1.5 -11" radius=".25" height="3" color="brown"></a-cylinder>
            <a-sphere position="-2 3 -11" radius="1.25" color="green"></a-sphere>
            
            <a-cylinder position="2 1.5 -12.5" radius=".25" height="3" color="brown"></a-cylinder>
            <a-sphere position="2 3 -12.5" radius="1.25" color="green"></a-sphere>
            
            <a-cylinder position="-2 1.5 -14" radius=".25" height="3" color="brown"></a-cylinder>
            <a-sphere position="-2 3 -14" radius="1.25" color="green"></a-sphere>
            
            <a-cone position="0 1 -2" radius-bottom=".2" radius-top=".01" color="red" rotation="45 0 ds0"></a-cone>
        </a-scene>
    </body>
</html>

```