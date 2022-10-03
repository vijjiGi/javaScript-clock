In this Images.html program we make some interesting functions like increase font-size,flex like that
firstly We take some images and add some lines on them then we make them some fnctions.
In this program we use a css event called flex.
         
         display:flex;
         align-items:center;
         justify-content: center;
         flex:1;
         
 To make increment of flex value we create a sepecial class css.
 
           .panel.open{
                flex:5;
                font-size:40px;
       
to make this valuable we add some JavaScriptcode.For this we create a consonant class to track the images.

               const pannels= document.querySelector('.panel');.
               
to make flex increment 
               
               panel.forEach(panel=>panel.addEventListener('click',toggleOpen))
               
               function toggleOpen(e){
                          this.classList.toggle('open');
                          
                          
 To make data invisibel and visuable to add some css data.
 
                .panel > *:first-child(transform:translatey(-100%);} For invisible
                .panel.open-active > *:first-child(transform:translatey(0);} for visible
                It is also for last-child and differnece is 100%,0.
                              
To make data invicible and when we click the image then show the data on image.

                 panel.forEach(panel=>panel.addEventListner('transitionend',toogleActive));
                 
                 function toggleActive(e){
                                if(e.propertyName.includes('flex')){
                                this.classList.toggle('open-active');
                                }
