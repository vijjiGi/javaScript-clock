In this program we sort the Array values in alphabetc order and place on the screen in list items
First we create an with some words with staring an,the,a.
Firstlywe sortout and display with alphabetcal order with sort function

        const sortedBands=bands.sort((a,b)=>strip(a)>strip(b) ? 1 : -1);
        
In this we sortout the values in alphabetcally and avoid the an,the,a with help of strip function
Then we implement the strip funtion

        function strip(bandName){
                return bandName.replace(/^(a |the |an )/i, '').trim();
                
Lastly we add the array items to list on screen

        document.querySelector('#bands').innerHtml=sortedBands
                        .map(band=>`<li>${band}</li>`)
                        .join('');
