In this Program we learning about the clock directions,and how it works.

minsHand.style.transform= `rotate(${minDegree)deg}`;

In this statement we assign the directions,transformation to minuteHand.For that we create a function called newDate();.
      
      {const now=new Date();}
Firstly we create a constant which is define the Date.It will show the what time,date is now.
       

     const mins=now.getMinutes();.
Then we get the minutes value from new Date().

     {const minDegree=((mins/60)*360)+90}.
Then we change and know the direction of minute-hand,for that we create a constant to know it is          

    {const minsHand=document.querySelector('.min-hand')}.
To know the changes in directions of minute-hand we style the minuteHand.For the firstly we create a constant to know the minute-hand value.

With this we know the minuitValue and direction changes of minut-hand.

This process is work seconds and hours also..
      secondsHand.style.transform=`rotate(${minDegree}deg)`;
      hourHand.style.transform=`rotate(${hourHand}deg)`;


          
    
