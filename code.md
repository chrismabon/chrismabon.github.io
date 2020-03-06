---
title: Code
description: Snippets of logic
---

<br>

>> "Talk is cheap. Show me the code."
>>
>> -Linus Torvalds

---

<div class="gridwrap">
    <div class="gridright"> 
        <h2>Calculating the Julian Day</h2>     
        <p class="blocktext">The common Gregorian calendar is woefully-inadequate for use in
        astronomy and developing software: Try calculating the difference between two arbitrary times/dates 
        in the Gregorian calendar. It isn't a simple subtraction operation, now is it?</p>        
        <p class="blocktext">We require a linear time scale, one that can be expressed as a large (but simple) 
        number rather than an aggregate of the year/month/day/hours/minutes/seconds. The Julian calendar has
        such properties, but we must first find the Julian Day (JD) using the Gregorian date and some math...</p>
<ul>
<li>First we adjust the month and year for January and February such that they
occur in the previous year as hypothetical months 13 and 14</li>
</ul>      
<code> 
    
                // Gregorian time/date values as input
                function julianDay(year, mon, day, hour, min) {
                  
                  // adjust month numbers from 0-11 to 1-12
                  mon += 1; 
                  
                  // Jan and Feb are months 13 and 14, respectively, 
                  // from the previous year
                  if (mon < 3) { 
                    year -= 1;   
                    mon += 12;
                  }
                  
</code>                          
<ul>
  <li>Next we convert the hours and minutes to fractional days for better accuracy,
    and add them to the current day value</li>
</ul>
<code>                 
                
                  // minutes expressed as fractional days
                  let minToDay = min / 1440; 
                  
                  // hours expressed " " 
                  let hourToDay = hour / 24; 
                  
                  // adjust day to include hours and minutes
                  let adjDay = day + hourToDay + minToDay; 

</code> 
<ul>
<li>Lastly we perform some seemingly-arbitrary calculations involving floor 
  division, including the adjusted day, and return that value as the number of
  Julian days since the year -4712 (or 2693 BCE)</li>
</ul>
<code> 
                  
                  // find intermediate values
                  let a = Math.floor(year / 100);
                  let b = 2 - a + Math.floor(a / 4);
                  
                  // calculate Julian Day from previous values
                  let JD = Math.floor(365.25 * (year + 4716)) 
                              + Math.floor(30.6001 * (month + 1)) 
                              + adjDay + b - 1524.5; 
                  return JD;               

<code> 
   </div>
</div>
