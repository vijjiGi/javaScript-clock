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
               

In ArrayFunction2.html we know about some(),every(),find(),findIndex(),splice(),slice().

For this we create 2class constants people,comments.

Array.some().This function we can check altleast some are suitable for our condition.We want to know if altest some of people have 27years.

               const current=(new Date()).getFullYear().it is used for know current year
               const isYounger=people.some(person=>(cureent-person.year)>=27;
           
Array.every().To know every person of people have 27years.

            const isOlder=people.every(person=>(current-person.year)===27
            
Array.find().to find out description of variables.In this we know the Id using '583921'

            const comment=comments.find(com=>com.id===583921))
            
Array.findIndex().to find the index of the id using '583921'.

            const comm=comments.findIndex(comment=>comment.id===583921)
            
Array.slice().to know the data of b/w two indexes.

              const newComment=[
                        ...comments.slice(comm,o),
                        ...comments.slice(comm+1)
                        ]
                        
Array.splice().to delete the data from class

            comments.splice(comm,2);
            
               
   
            
            
          
    
