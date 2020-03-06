---
title: Code
description: Snippets of some well-implemented code
---

<br>

>> "Talk is cheap. Show me the code."
>>
>> -Linus Torvalds

---

<h2>🌙Phase Pharmer</h2>
<div class="gridwrap">
    <div class="gridright"> 
      <p class="redlist">Calculating the Julian day</p>        
      <p class="blocktext">The commonly-used Gregorian calendar is woefully-inadequate for use in
        astronomy and developing software: Try calculating the difference between two arbitrary times/dates 
        in the Gregorian calendar. It isn't a simple subtraction operation, now is it?</p>        
      <p class="blocktext">We require a linear time scale, one that can be expressed as a large (but simple) 
        number rather than an aggregate of the year/month/day/hours/minutes/seconds. The Julian calendar has
        such properties, but we must first find the Julian Day (JD) using the Gregorian date and some math...</p>
        <p class="blocktext">
          <ul>
            <li>First we adjust the month and year for January and February such that they
            occur in the previous year as hypothetical months 13 and 14.</li>
          </ul>
              <code> 
                // Gregorian time/date values as input
                function julianDay(year, mon, day, hour, min) {
                  mon += 1; // adjust month numbers from 0-11 to 1-12
                  if (mon < 3) { // Jan and Feb are months 13 and 14, respectively, 
                    year -= 1;   // from the previous Julian year
                    mon += 12;
                  }
            </code>
                <ul>
                  <li>Next we convert the hours and minutes to fractional days for better accuracy,
                    and add them to the current day value.</li>
                </ul>
                <code> 
                  let minToDay = min / 1440; // minutes expressed as fractional days
                  let hourToDay = hour / 24; // hours expressed " " 
                  let adjDay = day + hourToDay + minToDay; // adjust day to include hours and minutes
                </code>
                <ul>
                <li>Lastly we perform some seemingly-arbitrary calculations involving floor 
                  division, including the adjusted day, and return that value as the number of
                  Julian days since the year -4712 (or 2693 BCE).</li>
                </ul>
                <code>
                  let a = Math.floor(year / 100);
                  let b = 2 - a + Math.floor(a / 4);
                  let JD = Math.floor(365.25 * (year + 4716)) 
                              + Math.floor(30.6001 * (month + 1)) 
                              + adjDay + b - 1524.5; // calculate Julian Day from previous values
                  return JD;
                </code>
        </p>
    </div>
</div>
