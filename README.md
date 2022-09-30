# javaScript-clock
we create divs to create a clock



<div class='clock'>
  <div class='clock-face'>
      <div class='hand min-hand'></div>
      <div class='hand second-hand'></div>
      <div class='hand hour-hand'></div>
    </div>
    </div>
    
    then we style the divs using classnames.
    
    
    .clock{
          height:30rem;
          width:30rem;
          border:20px solid white;
          border-radius:75%;
          margin:25px auto;
          position:relative;
          padding:2rem;
          box shadow:
                  0 0  0 0px rgba(0,0,0,0.2),
                  inset 0 0 3px #fefefe;
                  inset 0 0 10px red;
                  0 0 10px rgba(0,24,4,0.3);
          }
     .clock-face{
          position:realtive;
          width:100%;
          height:100%;
          transform:translatey(-3px);
          }
       .hand{
              widht:50%;
              height:8px;
              background:black;
              position:absolute;
              top:50%;
              transform-origin:100%;
              transform:rotate(90deg);
              transition-timing-function:cubic-bezier(0.75,0.82,0.165,1);
              }
              
              
This style we use for clock dimesions,width,height,radius all of which we are using for Clock dimension.
Then we write the javaScript code for clock Functions.



const seconHand=document.querySelector('.second-hand');
const minHand=document.querySelector('.min-hand');
const hourHand=document.querySelector('hour-hand');


function newDate(){

    const now=new Date();
    const seconds=now.getSeconds();
    const secondDegree=((seconds/60)*360)+90;
    secondHand.style.tranform=`rotate(${secondDegree}deg)`;
    
    const mins=now.getMinutes();
    const minDegree=((mins/60)*360)+90;
    minDegree.style.transform=`rotate(${minDegree}deg}`;
    
    const hours=now.getHours();
    const hourDegree=((hours/12)*360)+90;
    hourHand.style.transform= `rotate(${hourDegree}deg)`;
    }
    
 In this we manage seconds,minutes,hours transitions.we have the values of those from newDate()..we can access them using getSeconds,getMinutes,getHours.then we can manage the direction updates with timeIntreval function.we set the time in this function using 1 second..then it will display the time now. 
    
