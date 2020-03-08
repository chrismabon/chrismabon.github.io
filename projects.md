---
title: Projects
description: Various activities of mine
---

<br>

>> "The package system was not designed to manage software. It was designed to facilitate collaboration."
>> 
>> -Ian Murdock

---

<h2>🌙Phase Pharmer</h2>
<div class="gridwrap">
    <div class="gridleft">
        <p class="redlist">JavaScript</p> 
        <p class="blocktext">Beginning as a simple spreadsheet, 
            <a href="https://github.com/chrismabon/PhasePharmer">🌙Phase Pharmer</a>
            is a web app that organizes and displays information about
            the mushroom farming skill in Project: Gorgon (an online fantasy 
            role-playing game). </p>
        <p class="blocktext">The app is hosted live and available to any 
            player to use at their convenience. It gives the time for 
            each mushroom to grow, which substrate is best, and handily
            displays information about various grow boxes.</p>
        <p class="blocktext">Calculating the moon phase to the minute requires some 
            trigonometry! For example, to find the "local hour angle", 
            one takes the arctangent of:</p> 
        <code>
            <ul>
                <li>sin(A)</li>
                <li>➗</li>
                <li>cos(A) sin(φ) + tan(h) cos(φ)</li>
            </ul>
        </code>
            <p class="blocktext">where:</p>
        <code>
            <ul>
                <li>A ⇒ azimuth from the south</li>
                <li>φ ⇒ observer's latitude</li>
                <li>h ⇒ altitude</li>
            </ul>
        </code>
        <p class="blocktext">Etc.</p>
    </div>
    <div class="gridright">
        <img class="rounded" src="assets/images/phase-pharmer3.png" alt="Phase Pharmer">
        <img class="rounded" src="assets/images/phase-pharmer2.png" alt="Phase Pharmer">
        <img class="rounded" src="assets/images/phase-pharmer1.png" alt="Phase Pharmer">
    </div>
    <div class="gridcenter">
        <img class="rounded" src="assets/images/phase-pharmer5.gif" alt="Phase Pharmer">
    </div>
</div>
<h2>Guild Website</h2>
<div class="gridwrap">
    <div class="gridleft">
        <p class="redlist">Python & JavaScript</p> 
        <p class="blocktext">What modern gaming guild would be 
            complete without a website? After initially using only pure 
            HTML/CSS and Apache2, I ported the site to the Flask
            web microframework.</p>
        <p class="blocktext">Heavy use of CSS gradients, 
            transparency, and special background image effects 
            characterize the site. Exotic fonts add to the inherent 
            mystical feel.</p>
    </div>
    <div class="gridcenter">
        <img class="rounded" src="assets/images/dragon2.png" alt="Dragon Moon Clan">
        <p class="blocktext">A useful trick using JavaScript is to 
            force the navigation area to "stick" to the top of the page
            after scrolling down far enough.
            As one can see from the screenshots, the 
            navigation bar seems to not scroll down past a certain point, 
            keeping navigation items in visual range at all times.</p>
        <p class="blocktext">This makes the site more accessible to
            mobile users who lack the large screen experience of the 
            desktop.</p>
        <img class="rounded" src="assets/images/stickynav.gif" alt="Sticky navbar">
    </div>
</div>
<h2>Encryption Machine</h2>
<div class="gridwrap">
    <div class="gridleft">
        <p class="redlist">Java</p> 
    </div>
    <div class="gridright">
    </div>
    <div class="gridcenter">
        <p class="blocktext">One of my past projects was a program
            that could utilize multiple types of ciphers to encrypt
            and decrypt text and files.</p>
        <p class="blocktext">The transpositional cipher 
            randomly picks a swap between two letter in the text and 
            saves that information in a text key. The key is then used
            to decrypt the message or file.</p>
        <p class="blocktext">There are also two other ciphers available,
            both of which are substitution ciphers and which operate 
            similarly to one another within the program.</p>
        <img class="rounded" src="assets/images/encrypt.png" alt="Encryption Machine">
    </div>
</div>
