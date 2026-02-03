<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body style="background-color: pink; overflow: hidden;">
    <div>
        <h1>Will you be my valentine?❤️</h1>
        <button id="Yes">Yes!</button>
        <button id="No">No</button>
    </div>

    <style>
        h1 {
            font-size: 50px;
        }

        button {
            color: black;
            font-size: 15px;
            padding: 5px;

        }

        div {
            
            margin-top: 200px;
            text-align: center;
            vertical-align: middle;
            position: relative;
        }

        #No {
            background-color: red;
            margin-left: 5px;
            position: fixed;
        }

        #Yes:hover {
            background-color: green;
            animation: pulse 0.5s infinite;
        }

        #Yes {
            animation: pulse 0.5s infinite;
            background-color: green;
            
        }

        @keyframes pulse {
            0% {
                transform: scale(1);
            }

            50% {
                transform: scale(1.1);
            }

            100% {
                transform: scale(1);
            }
        }
    </style>
    <script>
        document.getElementById("Yes").addEventListener("click", function () {
            alert("I love you! See you soon ❤️");
        });
        var b = document.getElementById("No")
        b.addEventListener("mouseenter", change);
        function change() {

            
            var maxX = window.innerWidth - b.offsetWidth;
            var maxY = window.innerHeight - b.offsetHeight;

            
            if (maxX < 0) maxX = 0;
            if (maxY < 0) maxY = 0;

            var i = Math.random() * maxX;
            var j = Math.random() * maxY;

            b.style.left = i + "px";
            b.style.top = j + "px";
        }
    </script>

</body>

</html>
