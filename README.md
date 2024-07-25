# Example2

import React, {useState, useEffect} from 'react';

function Clock(){
   
      const [time, setTime] = useState(new Date());

      useEffect(() => {
        const intervalId = setInterval(() => { 
            setTime(new Date()); 
        }, 1000);
      })

      function Time(){
        let hours = time.getHours();
        const minutes = time.getMinutes();
        const seconds = time.getSeconds();
        const meridiem = hours >= 12 ? "PM" : "AM";

         return `${hours}:${minutes}:${seconds}:${meridiem}`
      } 

     return(
     <div>
        <div>
            <span>{Time()}</span>
        </div>
     </div>

     );


}

export default Clock;
