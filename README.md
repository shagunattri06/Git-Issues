#  Animated cube

##  Description
This HTML and CSS code creates a 3D rotating cube using CSS 3D transformations and keyframe animations. The cube consists of six colored faces (div elements) positioned using rotateX(), rotateY(), and translateZ() for a proper 3D effect. The perspective: 1000px; in the body ensures depth, and transform-style: preserve-3d; maintains the cube's 3D structure. The @keyframes rotate animation continuously rotates the cube around both the X and Y axes, creating a smooth infinite spinning effect. The result is a visually appealing 3D animated cube without using JavaScript.

##  Demo Preview (HTML & CSS)
Here is a simple **HTML & CSS** snippet from the project:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>3D Rotating Cube</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f0f0f0;
            margin: 0;
            perspective: 1000px;
        }

        .cube {
            width: 200px;
            height: 200px;
            position: relative;
            transform-style: preserve-3d;
            animation: rotate 5s infinite linear;
        }

        .cube div {
            position: absolute;
            width: 200px;
            height: 200px;
            border: 1px solid #ccc;
        }

        .front  { transform: rotateY(  0deg) translateZ(100px); background-color: red; }
        .back   { transform: rotateY(180deg) translateZ(100px); background-color: blue; }
        .right  { transform: rotateY( 90deg) translateZ(100px); background-color: green; }
        .left   { transform: rotateY(-90deg) translateZ(100px); background-color: yellow; }
        .top    { transform: rotateX( 90deg) translateZ(100px); background-color: cyan; }
        .bottom { transform: rotateX(-90deg) translateZ(100px); background-color: magenta; }

        @keyframes rotate {
            from {
                transform: rotateX(0deg) rotateY(0deg);
            }
            to {
                transform: rotateX(360deg) rotateY(360deg);
            }
        }
    </style>
</head>
<body>
    <div class="cube">
        <div class="front"></div>
        <div class="back"></div>
        <div class="right"></div>
        <div class="left"></div>
        <div class="top"></div>
        <div class="bottom"></div>
    </div>
</body>
</html>
