in this program we design some hyperLinks in the text and highlight them when curser reach them
For this we add some text and middle of them add some hyperLinks and add some styles to them..

In the style of the hyperlinks and text have margin:0 importantly
We add nav with some hyperlinks and ther "class=menu" and the text div "class=wrapper" and mixing with 
some hyperlinks

And we  acces them and make them hignlight..

        const triggers=document.querySelector('a');
        const highlight=document.createElement('span');
        highlight.classList.add('highlight');
        documnet.body.append(highlight);
        
        
        
For highlight we add some styles

        .highlight{
                transition:all 0.2s;
                border-bottom:2px solid white;
                positon:absolute;
                top:0;
                background:white;
                left:0;
                z-index:1;
                border-radius:20px;
                display:block;
                box-shadow:0 0 10px rgba(0,0,0,0.2);
                }
                
Then we add triggers an EventListener then we implement the funtioning of triggers..

        triggers.forEach(a=>a.addeventListener('mouseenter',highlightLink);
                
                
           function highlightLink(){
                const linkCoords=this.getBoundingClientRect();
                console.log(linkCoords);
                const cords={
                        width:linkCoords.width,
                        height:linkCoords.height,
                        Top:linkCoords.top+winodow.scrollY,
                        left:linkCoords.left+window.scrollX,
                        }
                 highlight.style.width=`${cords.width}px`;
                 hightlight.style.height=`${cords.height}px`;
                 highlight.style.transform=`translate(${cords.left}px,${cords.top}px)`;
                 }
                 
 Then we will hightlight what we want in the screen..
