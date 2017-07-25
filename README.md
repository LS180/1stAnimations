<!DOCTYPE HTML>
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
  background: red;
}
</style>
<body>

<p>
<button onclick="myMove()">Click Me</button>            
</p>



<h1>My First JavaScript Animation</h1>

<div id="myContainer">                      
<div id="myAnimation"></div>                
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
