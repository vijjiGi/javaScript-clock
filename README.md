In this program we make a timer to show the balcnce time of what we set.
For this we ad some extra feature like we add 20secs,5min,15mins,20mins,60mins,and a textbox to show 
what tie we want..
For this we use some attributes like seconds,countdown...

First we access all the classes..

        const timerDisplay=document.querySelector('.display__time-left');
        const endTime=document.querselector('.display__end-time');
        const buttons=document.querySelectorAll('[data-time']);
        
        
And then we make a function called timer();

              funtion timer(seconds){
                        //clear existing timer
                        clearInterval(countdown);
                        
                        const now=Date.now();
                        const then=now+seconds*1000;
                        displayTimeLeft(seconds);->to show the how much time left 
                        displayEndTime();->to show ending time of the time
                        
                        countdown=setInterval(()=>{
                                const secondsleft=math.round((then-Date.now())/1000);
                              //check if we should stop it;
                                if(secondsLeft<=0){
                                        clearInterval(countdown);
                                        return;
                                    {
                                    //display it
                                    displayTimeLeft(secondsLeft);
                                    },1000);
                                    }
    
To know how much time is left we make funtction called displayTimeLeft(seconds)


                function displayTimeLeft(seconds){
                                const minutes=Math.floor(seconds/60);
                                const reminderSeconds=seconds/60;
                                const display=`${minutes}:${remiderSeconds<10 ? '0' : 
                                                        ''}${remiderSeconds}`;
                                 document.title=display;->to display the time on title bar also
                                 timerDisplay.textContent=display;
                               }
To know the ending of the time we create a function called displayEndTime()
                
                function displayEndTime(timestamp){
                                const end=new Date(timestamp);
                                const hours=end.getHours();
                                const adjustHour=hours >12 ?hours-12 :hours;
                                const minutes=end.getMinutes();
                                endTime.textCpontent=`Be Back at${adjustHour}:${minutes<10 ?'0' : 
                                                        ''}${minutes}`;
                                 }
                                 

After that we have to add the buttons evnets

                buttons.forEach(button=>button.addEventListener('click',startTimer);
                
                        function startTimer(){
                                const seconds=parseInt(this.dataset.time);
                                timer(seconds);
                                }
                                
And then we add the text time functioning

                document.customForm.addEventListener('submit',function(e){
                                e.preventDefault();
                                const mins=this.minutes.value;
                                console.log(mins);
                                timer(mins*60);
                                this.reset();
                               })
                               
                               
Then we add the timer using buttons and text time



                                   
                        
                        
