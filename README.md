# flappyBird-basic
A dead-simple recreaction of flappy bird. 

### how is time handled? 
  Time is counted using the window.requestAnimationFrame() object method. This method tells the browser that you wish to perform an animation and requests that the browser calls a specified function to update an animation before the next repaint. The method takes a callback as an argument to be invoked before the repaint. In this case, the specified callback is updateLoop, which sets the delta as the difference between the number of frames passed between the last time it was called. 
  
  Time stops when checkLose() is true. 
  
### how is bird motion handled? 
  A difficult question to answer as motion is made of a couple things: the logic to calculate how much and where, and the logic to display the updated position of the bird on the screen. 

  A variable birdElem is created to track the position of the bird. In index.html, a data-bird class is created to handle state. Global variables are declared for bird speed and jump duration. The setTop helper function takes this initial value as a parameter.The bird setup function also adds an event listener for jump. 
  
   Updating the position of the bird in the browser is achieved by getting and setting the "top" pseudo-element value, ("--bird-top"). Counter-intuively, CSS plays a role in setting the intial values for the bird's position. When the game repaints the browser, the bird's top is calculated by recalculating the computed style of the bird-top pseudoelement. 
  
  Updating the value of this computed style is achieved by taking in the delta **see above section**  indicating the change in the passage of time since the updateLoop function last ran (and the browser was last repainted), and decides whether to move the bird up or down. If the time since the last jump is less than arbitrary Jump_duration, it moves up, if it is more, it moves down. 

### how is pipe motion handled? 

### how are collisons handled? 
