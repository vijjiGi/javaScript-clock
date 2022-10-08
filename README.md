In this program we access some cities,states information from link.
And then we access that information from link to json.

        
         let cities=[];
         fetch(endpoint)
         .then(blob=>blob.json())
         .then(data=>cities.push(...data))


In this we access the data of the link toinderstandable view using json.and add the information to  class called"data".
We access the information using classes with querySelsctor,and classes are search,suggestions.and store them in a constant called serachInput,suggestion.

        const searchInput=document.querySelector('.search');
        const suggestions=document.querySelector('.sugggestions');
        
And then we use some keyBoard functions like 'change','keyup'.

        searchInput.addEventListener('change',displayMatches);in this displayMatches is a function.
        
        function displayMatches(){
        const matchArray=findMatches(this.value,cities);
        const html=matchArray.map(place=>{
                const regex=new RegExp(this.value,'gi');
                const cityName=place.city.replace(regex,`<span class='h1'>${this.value}</span>`);
                const stateName=pllacce.state.replace(regex,`<span class='h1>${this.value}</span>`);
                return `
                        <li>
                                <span class='name'>${cityName}, ${stateName}</span>
                                <span class='population'>${numberWithCommas(place.population)}</span>
                                </li> }).join(' ');
                                suggestions.innerHtml=html; }
                                
 In the displayMatches function we have another function to find the matches cities,states called findMatches() and another function called numberWithCommas
 
        function findMatches(wordToMatch,cities){
                 return cities.filter(place=>{
                        const regex=new RegExp(wordToMatch,'gi');
                        return place.city.match(regex) || place.state.match(regex) });
                       
          function numberWithCommas(x){
                return x.toString().replace(/\B(?=(\d{3})+(?!\d))/g,','); }
                
  In the input column we enter some place name then it display the matching places cities or states.
          
                        
        
