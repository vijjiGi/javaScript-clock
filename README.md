in this program we can translate text to speech..

For this we create an option(voices),rate(range),pitch(range),textarea,stop(stop) button and speak(speak) 
buttons.And we access them with constants

        const msg=new speechSythesisUtterance();->used for speech recognize and translator
        let voices=[];
        const voicesDropdown=document.querySelector('[name="voice"]');
        const options=document.querySelectorAll('[type="range"],[name="text"]');
        const speakButton=document.querySelector('#speak');
        const stopButton=document.querySelector('#stop');
        
We add the text to msg constant using querySelector;

        msg.text=document.querySelector('[name="text"]').value;
        
        
We add eventListeners to every inputs, voices,and buttons.

        speechSythesis.addEventListener('voiceschanged',popilatedVoice);
        voicesDropdown.addEventListener('change',setVoice);
        options.forEach(option=>option.addEventListener('change',setOption);
        speakButton.addEventListener('click',toggle);
        stopButton.addEventListener('click',()=>toggle(false));
        
        
And we implement the functions
                
             function populatedVoices(){
                        voices=this.getVoices();
                        voicesDropdown.innerHtml=voices
                        .map(voice=>`<option value="${voice.name}">${voice.name}(${voice.lang})
                        </option>`);

this function implement voices of different languages..


                function setVoice(){
                        mag.voice=voices.find(voice=>voice.name===this.value);
                        toggle();
                        
this function when we change the text then voice can changed for that text..

                function toggle(speechOver=true){
                        speechSynthesis.cancel();
                        if(startOver){
                                speechSynthsis.speak(msg);
                }}
                
 this function can make the changes when we stop then it will stop or it will run;;
 
                function setOption(){
                        console.log(this.name, this.value);
                        msg[this.name]=this.value;
                        toggle();
                        }
                       
 This will display hte value of options like range,pitch,text..
 

                
