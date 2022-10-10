In this Program we create print like what we want to draw on screen
For this we create two constants called 'canvas','ctx'.

      use These we manage the screen line and width
                canvas.length=window.innerlength;
                canvas.width=widows.innerWidth;
        
        and some designs to help to draw are
        
                ctx.strokeStyle='#BADA55';
                ctx.linejoin='round';
                ctx.linecap='round';
                ctx.lineWdth=100;
For drawing we manage some outfits like isDrawing,lastX,lastY,hue,direction and give them some values false,0,0,0,true.

For this functioning we use mouseEvent mousedown,mousemove,mouseup,mouseout.
we add to canvas addEventListener();in this a function define 

        isDrawing=true;
        [lastX,lastY]=[e.offsetX,e.offsetY];
        
        
this mouse event we access in a function called draw.

        function draw(e){->in this function we check some conditions to show as we like.
        
                if(!isDrawing)return
                console.log(e);
                ctx.strokeStyle=`hsl(${hue},100%,50%)`;
                ctx.beginPath();->start
                ctx.moveTo(lastX,lastY);->go to
                ctx.lineTo(e.offsetX,e.offsetY);
                ctx.stroke();
                [lastX,lastY]=[e.offsetX,e.offsetY];
                hue++
                
              then we chheck the hue and line width,length values.
                if(hue>=360){
                    hue=0;
                    }
                 if(ctx.lineWidth=100||ctx.lineWidth<=1){
                        direction=!direction
                        }
                  if(direction){
                        ctx.linelength++;
                        }else{
                        ctx.linelength--;
                        }}
                        
In this function we add the mouseEvent also to functioning the drawing.
                        
                        
             
                
                    

        
                
