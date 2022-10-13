In this program we do speech recognition and place that speech on screen.
For this we use our system micrphone and give permision to that..
Lets start..
        
          window.SpeechRecognition=window.SpeecchRecognition || wnidow.webkitSpeechRecognition;
      
In this we do the recognition from our system,or web which we are using with microphone.

        const recognition=new SpeechRecognition();
        recognition.interimResults=true;
        
recognition is store the recognised data

        let p=document.createElement('p');
        const words=document.querySelector('.words');
        words.appendChild(p);
        
Then add the data to paragraph..

        recognition.addEventListener('result',e=>{
                        const transcript=Array.from(e.results)
                        .map(result=>result[0])
                        .map(result=>result.transcript)
                        .join('')
                        
Then add the recognized data on the screen..

        p.textContent=transcript;
        if(e.results[0].isFinal){
                p=document.createElement('p');
                words.appendChild(p);
                }
                
             console.log(transcript)
             });
             
        recognition.addEventListener('end',recognition,start);
        recognition.start();
        
 when we talk with gap then a new paragraph is made automatically..
