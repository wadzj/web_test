<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1 id="demo">Test</h1>
    <button onclick="javascript:getLocation()">Get Loc</button>
    <button onclick="javascript:showPosition()">Show Loc</button>
</body>

<script>
   var x = document.getElementById("demo");
    function getLocation() {
    if (navigator.geolocation) {
        navigator.geolocation.watchPosition(showPosition);
    } else {
        x.innerHTML = "Geolocation is not supported by this browser.";
    }
    }
    function showPosition(position) {
    x.innerHTML = "Latitude: " + position.coords.latitude +
    "<br>Longitude: " + position.coords.longitude +
    "<br>Speed: " + position.coords.speed;
    }
    </script> 


</html>
