In this program we have to create agame called mole and hole.
in this game we have some certain of time.In this time we have tap maximum no.of moles.how many moles we
can tap thats our score

For this we get that moles and holes images from brower and add them some styles.
we access som attributes like lasthole,timeUp=0,score=0,
In this program we assign some time and random Holes..For that we create functions

        function randomTine(min,max){
                return Math.round(Math.random()*(max-min)+min;
                }
                
For select random holes we create a function called randomHole()
           
           function randomHole(holes){
                const idx=Math.floor(Math.random()*holes.length);
                const hole=holes[idx];
                if(hole===lastHole){
                        return randomHole(holes);
                       }
                       lastHole=hole;
                       return hole;
                       }
   
  when we run the game then moles are coming up from randomHoles to functioning this we create a 
  function called peep()
  
                function peep(){
                        const time=randomTime(200,1000);
                        const hole=randomHole(holes);
                        hole.classList.add('up');
                        setTimeout(()=>{
                                hole.classList.remove('up');->when the mole came up and down in with 
                                                        some fraction of seconds
                                if(!timeUp)
                                peep();
                               },time)
                               }
                               
 To start the game we create a button called start
 
                function startGame(){
                        scoreBoard.textContent=0;
                        timeUp=0;
                        score=0;
                        peep();
                        setTimeout(()=>timeUp=true,20000)
                        }
                        
  To functioning the score when we touch the mole we create a function calles bunk()
                        
                        function bunk(e){
                                if(!isTrusted)return;
                                score++;
                                this.classlist.remove('up');
                                scoreBoard.textContent=score;
                                }
                         
                         
                       mole.forEach(mole=>mole.addEventListemer('click',bunk));
                       
 Then we start the game by click on start button and have 20seconds of game..
