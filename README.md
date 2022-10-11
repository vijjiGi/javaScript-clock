In this program we add some properites to screen when we press a specific word what we are create.

For this we create an array and a constant

        const pressed=[];
        const secret='ing';->when we enter this word on screen it will show some magic.
        
Then to show the magic we create an eventListener

        window.addEventListener('keyup',(e)=>{
             console.log(e.key);
             pressed.push(e.key);->everyTime we pushing the keys they store in the pressed array.
             pressed.splice(-secret.length-1,pressed.length-secret.length);->divide the with secret 
                                                                                length
              if(pressed.join('').includes(secret)){
                        console.log('tring tring');->when we press the secret word it will display
                        cornify_add();->it will show the magic;
                    }
                    console.log(pressed);
                    })
                    
 Then we can see the magic
