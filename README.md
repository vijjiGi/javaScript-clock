In this program we can change the values of color,border spacing,image bluring
we are using css variables those are spacing,base,blur.
we give some values in styles to those


        :root{
                  --base:#ffc600;{-- is used to point them as variables}
                  --spacing:10px;
                  --blur:50px;}
                  
                  
 we assigning these variables to image and text values.
 
 
          img{
                padding:var(--spacing);
                background:var(--base);
                filter:blur(var(--blur));}
            .h2{
                  color:var(--base);}
                }
                
                
 we change the values of variables using JavaScript function.
 we can change the input values using
           
           inputs.forEach(input=>input.addEventLisstner('change',handleUpdate));
 handleUpdate is a function define the changes.
     
     
     function handleUpdate(){
           const suffix=this.dataset.sizing || "";.in this statement we create a const suffix to describe the dataset values.
we can setProperty of name of varibles to value of those variables using
            document.documentElement.style.setProperty(`--${tis.name}`,this.value+suffix)
            }
                
