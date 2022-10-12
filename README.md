In this program we can add images to paragraphs.And when we scroll the page images are add to the pages where we store them.
For this we want paragrapghs and images with classes names are 'align-left slide-in','align-right slide-in','active slide-in', 
All images have a same classname called slide-in.
Then we access a function called debounce();It is used for set the timing to run the data

        function debounce(func,wait=50,immediate=true){
                 var timeout;
                 return function(){
                        var context=this, args=arguments->for this we create two variables..another                                                                       variable with function is 'later'
                        var later=function(){
                                timeout=null;
                                if(!immediate) func.apply(context,args);
                                }
                         var callNow=immediate && !timeout;
                                clearTimeout(timeout);
                                timeout=setTimeout(later,wait);
                                if(callNow) func.apply(context,args);
                                }
                                };
This function we can use as with eventListener
                window.addEventListener('scroll',debounce(checkSlide));
                
Then we implement the checkSlide()

                function checkSlide(e){
                        sliderImages=forEach(sliderImage=>{
                                const sliderInAt=(window.sccrollY+window.innerHeight)-                                                                                  sliderImage.height/2;
                       /*halfway through the image*/
                                  const imageBottom=sliderImage.offsetTop+sliderImage.height;
                       /*bottom of the Image*/
                                   const isHalfShown=sliderInAt>sliderImage.offsetTop;
                                   const isNotScrolledPast=window.srollY<imageBottom;
                                   
                               if(isHalfShown && isNotScrolledPast){
                                        sliderImage.classList.add('active');
                                     }else{
                                          sliderImage.classList.remove('active');
                                          }
                                          })
                                          }
                                   

        
