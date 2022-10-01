In this program we show the functions of Array
Those are filter,map,sort,reduce.For check these functions we create two constant classes like "Auditors","people".
Array.Filter().this function use to konw the auditors who are born in 1400.For these we Filter the auditor class.to know this we create a constant fourteen

            const fourteen=auditors.filter(auditor=>(auditor.year>=1400 &&                                        auditor.year<=1900))

Array.map().this functon used for mapping the attributes and give them what we want.we want to know the first and lastName of the auditor,

            const fullName=auditors.map(auditor=>(`${auditor.first} ${auditor.last}`))
     
Array.Sort().this function used for sortOut the auditors class and display what we want.

##First we know the auditors birthDate which come to oldest to youngest.to know that we use objects like a,b.

            const birth=auditors.sort((a,b)=>(a.year>b.year ? 1 : -1))
            
Array.reduce().this function used for reducing the attributes or combining what we want.
      to know the years of did all the auditors live
            
            const totalYears=auditors.reduce((total,auditor)={
               return total+(auditor.passed-auditor.year);
               ),0}
               
               
   
            
            
          
    
