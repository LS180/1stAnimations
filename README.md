<!Doctype html>
<html>
<style>
#myContainer {                   //#myContainer=background
  width: 400px;
  height: 400px;
  position: relative;
  background: yellow;
}
#myAnimation {                  //#myAnimation=object that moves
  width: 50px;
  height: 50px;
  position: absolute;
  background: red;
}
</style>
<body>

<h1>My First JavaScript Animation</h1>

<div id="myContainer">                      //vital for background to work
<div id="myAnimation"></div>                //vital for object to work
</div>

</body>
</html>
************THE ANIMATION CODE****************************
************TIME INTERVAL*****************************
var id = setInterval(frame, 5);

function frame() {
    if (/* test for finished */) {
        clearInterval(id);
    } else {
        /* code to change the element style */
    }
}
***************CREATING THE ANIMATION WITH JAVASCRIPT*******
<!DOCTYPE html>
<html>
<style>
#myContainer {
  width: 400px;
  height: 400px;
  position: relative;
  background: yellow;
}
#myAnimation {
  width: 50px;
  height: 50px;
  position: absolute;
  background-color: red;
}
</style>
<body>

<p>
<button onclick="myMove()">Click Me</button>
</p>

<div id ="myContainer">
<div id ="myAnimation"></div>
</div>

<script>
function myMove() {
  var elem = document.getElementById("myAnimation");
  var pos = 0;
  var id = setInterval(frame, 10);
  function frame() {
    if (pos == 350) {
      clearInterval(id);
    } else {
      pos++;
      elem.style.top = pos + 'px';
      elem.style.left = pos + 'px';
    }
  }
}
</script>

</body>
</html>
