In this program we create a program to make checcked between two checked checkboxes.
For this we create two variables called lastChecked,inBetween
For this we create a constant called checkboxes

        const checkboxes=document.querySelectorAll('.inbox input[type="checkbox"]');
        
 To show the checked boxes we have a mouseEvent called 'click'.
 
        checkboxes.forEach(checkbox=>checkbox.addEventListener('click',handleCheck));
        
  Then we fullfill the function handleCheck
        function handleCheck(e){
                let inBetween=false;
            /*then check if they have shift key AND check if they checked*/
                if(e.shiftKey && this.checked){
                        checkboxes.forEach(checkbox=>{
                                        console.log(checkbox);
               /*Then we checked the checkbox and last checked box*/
                                     if(checkbox===this || chackbox===lastCheked){
                                              inBetween=!inBetween;
                                              console.log('checked between them');
                                           }
                  /*then if inBetween them are true then clicked them automatically.
                                       if(inBetween){
                                               checkbox.checked=true;
                                               }
                                               
                                       })
                                       }
                                       lastChecked=this;
                                     }
this will show the first and last checked boxes and between them checkboxes

        
