In this program we have some videos and thier timevallue.we have know the time value of all videos in hours,mins,seconds
For this we use the reduce function to know the time value.
Firstly we access the time values of all videos and combine them.
        
        const timeNodes=Array.from(document.querySelectorAll('[data-time]'));
       
In this constnat we access all the time values in an array from nodeList.
then convert minutes to seconds with use of map function.

        const seconds=timeNodes.map(node=>node.dataset.time)
                               .map(timeCode=>{
                                        const[mins,secs]=timeCode.split(':').map(parseFloat);
                                        return (mins*60)+secs;
                                       })->It will give the time value in seconds.
                                       
Then we add the all seconds with the help of reduce function.

                                 .reduce((total, videSeconds)=>total+videSeconds);
                                 
                                 
Then we know the time value in HOURS,MINUTES,SECONDS format.

        let secondLeft=seconds;
        const hours=Math.floor(secondsLeft/3600);->floor value show the accurate Hours value
        secondsLeft=secondsLeft%3600->It will show the minutes with seconds also
        
        const mins=Math.floor(secondsLefft/60);->it will show the accurate minutes
        secondsLeft=secondsLeft%60;->It will show seconds value
        
        console.log(hours, mis, secondsLeft);
        
It will show the HOURS,MINUTES,SECONDS value the all videos time..
