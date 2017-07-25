<!DOCTYPE html>
<html>
<style>
#myContainer {                   /*#myContainer=background*/
  width: 400px;
  height: 400px;
  position: relative;
  background: yellow;
}
#myAnimation {                  /*#myAnimation=object that moves*/
  width: 50px;
  height: 50px;
  position: absolute;
  background: red;
}
</style>
<body>

<p>
<button onclick="myMove()">Click Me</button>            /*button--<button onclick="myMove()">[defines what happens when button is                                                                 clicked]-->Click Me<[writing inside button]--</button>[closes button tag:<button                                                         onclick="myMove()">]*/
</p>



<h1>My First JavaScript Animation</h1>

<div id="myContainer">                      /*vital for background to work*/
<div id="myAnimation"></div>                /*vital for object to work*/
</div>

<script>                                                      //starts/contains the moving function for the object
function myMove() {                                           // defines myMove used for button
  var elem = document.getElementById("myAnimation");          //names the variable element; tells element to call out the id myAnimation
  var pos = 0;                                                //names the variable pos; tells pos to = 0
  var id = setInterval(frame, 10);                            //names the variable id; tells id to set the interval/timing as (frame, 10)
  function frame() {                                          //defines frame;frame is used to set the interval/timing of object's motion
    if (pos == 350) {                                         //if variable pos changes to 350, interval will be cleared
      clearInterval(id);
    } else {//,but if interval is != 350, var pos will increment by 1 px/pixel up & 1 px L, making elem/myAnimation move 1 px L & 1 px up
      pos++;
      elem.style.top = pos + 'px';
      elem.style.left = pos + 'px';
    }
  }
}
</script>

</body>
</html>
