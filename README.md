In this program we create a nav and when we scroll the screen we set that nav stable and highlight a logo
what is hidden
For this we add screen an image some text area and the nav we add some hyperLinks..
And give them some styles to look beautifull and the logo we hidden that to when we scroll we can see that 
log..

we give nav "id=main" and logo "class=logo" and div "class=site-wrap" and the middle of the text we add 
some images..
Then we write a program for that..

        const nav=document.querySelector('#main');
        const topOfNav=nav.offsetTop;
        
 Then we add an EventListener for screen and implement the function
 
         window.addEvenetListener('scroll',fixNav);
         
         function fixNav(){
                if(winodw.scrollY>=offsetTop){
                        document.body.style.paddingTop=nav.offsetHeight+'px';
                        document.body.classlist.add('fixed-nav');
                   }else{
                        document.body,style.paddingTop=0;
                        document.body.classList.remove('fixed-nav');
                      }
                      
And we add some style for fixed-nav

                .fixed-nav .site-wrap{
                        transform:scale(1);
                        }
                  .fixed-nav nav{
                        poosition:fixed;
                        box-shadow:0 5px rgba(0,0,0,0.1);
                  }
                  .fixed-nav li.logo{
                        max-width:500px;
                        }
                        
Then we see the logo when we scroll the screen..
