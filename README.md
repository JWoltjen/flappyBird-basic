# flappyBird-basic
A dead-simple recreaction of flappy bird. 

### how is time handled? 
  Time is counted using the window.requestAnimationFrame() object method. This method tells the browser that you wish to perform an animation and requests that the browser calls a specified function to update an animation before the next repaint. The method takes a callback as an argument to be invoked before the repaint. In this case, the specified callback is updateLoop, which sets the delta as the difference between the number of frames passed between the last time it was called. 
  
  Time stops when checkLose() is true. 
  
### how is motion handled? 

### how are collisons handled? 
