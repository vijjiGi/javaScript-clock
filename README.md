In this program we are learning about Bubblibg, propagation,capturing

Bubbling:

For thid we create three divs with diff colors..Then check the bubbling
Fot that we access the divs and add an evnetListener to check if click them what willl display.

        const divs=document.querySelectorAll('div');
        
        div.forEach(div=>div.addEventListener('click',logText);
        
        function logText(){
                console.log(this.classList.value);
                
                }
                
 Then we click on third div it will display three,two,one...it is called bubbling we can access the all 
 the divs what we can touch
 
 propagation:
 
 Propagation means it will display the divs bottom to top(three,two,one).
 
 Capture:
 
 when propagation false and capture true then display one,two,three(top to bottom)..
        
        function logText(e){
                console.log(this.classList.value);
                //e.stopPropagation();
                }
                
        div.forEach(div=>div.addEventListener('click',logText,{capture:true});
        
Another property in evenListener is once..

Once:

         div.forEach(div=>div.addEventListener('click',logText,{capture:true},{once:true});

Then when we click it will display result only one time.. 
     
