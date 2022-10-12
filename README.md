In this program we know the diff b/w refereance and copy of string,arrays,objects.

Strings,bool,numberrs

        let a=100;
        let b=a;
        console.log(a,b)->it will display the same value 100
        let word='hi';
        let text=word;
        console.log(word,text)->it will show ('hi','hi')
        let text='big';->then it will show('hi','big')
In numbers it will not copy the value when we change the variable value

Arrays

Let's check the Array reference and copy values
        
        let vir=['sir', 'hlo', 'hi'];
        let big=vir
        console.log(vir,big)->It will print the same values.
        Then 
                let big[3]='wes';
Then we see print same values also.This is called reference.
If we want to copy the values of one array to another array we have some methods.

        copy with slice operator
                var bag=big.slice();
        copy with concat operator
                var wes=[].concat(bag);
        copy with Array.from operator
                var nav=Array.from(wes);
        copy with spread operator 
                var vig=[...nav];
                
Objects

Lets see the objects reference and copy values

        let avg={name:'vig',num:12,nil:{na:'gif',div:23};
        let cap=avg
        cap.num=14
 It will change the main object num also.it is called reference 
 To avoid this problem we have a 'assign' function to copy Objects
 
        let fin=Object.assign({},cap,{num:12});->it will not change the main num value
        
We dont have spread operator in bjects
if we want to copy the 1 level values we use the json stingify function

        const wesi=JSON.parse(JSON.stringfy(cap));
        wesi.nil.div=54;
        console.log(wesi.nil);
        JSON.stringyfy(cap);


then it will not copy the values.

        
 
 
