---
layout: layouts/page.njk
title: Information
excerpt: Who I am

---

<img class="profile" src="/img/profile_250.jpg" alt="profile picture">
<script>
currentTime=new Date();
//getHour() function will retrieve the hour from current time
if(currentTime.getHours()<13)
document.write("Good morning! I hope you're having a great ");
else if(currentTime.getHours()<17)
document.write("Good afternoon! I hope you're having a great ");
else if(currentTime.getHours()<20)
document.write("Good evening! I hope you're having a great ");
else if(currentTime.getHours()<6)
document.write("Good night! I hope you had a great ");
else 
document.write("Good night! I hope you had a great ");
var weekday = new Array(7)
weekday[0] = " Sunday"
weekday[1] = " Monday"
weekday[2] = " Tuesday"
weekday[3] = " Wednesday"
weekday[4] = " Thursday"
weekday[5] = " Friday"
weekday[6] = " Saturday"
var currentDate = new Date()
weekdayValue = currentDate.getDay()
document.write(
weekday[weekdayValue] + "."
)
</script>

<p>I am lucky to be a husband to Mar, a father to Lucas and Nico, and a friend to Pancho.</p>
<p>I live in Madrid and work at Técnica y Avance.</p>



<h3>1. Personal</h3>
<p>By day, I solve complex problems with data; by night. My mission to shape the life I want.</p>

<p>My interests are data, data driven decision making, AI, webdesign, internet, biomimicry, spreadsheets, EVs, evolution, industrial design, science, history, speeches, philosophy, poetry (wordsmithing), data visualization, space, sci-fi and cooking...  
</p>

<p>I was born at 345.73 ppm CO2</p>

<p>My full name is Carlos Roberto Rodrigo Turner.</p>
<h3>2. Contact</h3>
<p><a href="mailto:email@carlosrodrigo.com">email@carlosrodrigo.com →</a></p>


<h3 id="professional">3. Professional</h3>
<p>
I'm a data specialist with 7+ years of experience in leveraging data to drive businesses forward. I am passionate about helping make data-driven decisions that lead to growth and success. 
</p>
<p>
I have worked in architecture studios, big energy companies, luxury brands, and small companies. I currently work at <a href="http://tecnicayavance.com">Técnica y Avance</a> My background is intentionally diverse—spanning architecture, energy, luxury brands, and startups—giving me a unique perspective on how data impacts different sectors. Whether I’m optimising back-office operations or resolving intricate inventory issues, I maintain a process-driven approach and a keen eye for detail to ensure every workflow is seamless and results-oriented.</p>

<h3>4. More about me</h3>
<ul>
<li><a href="/blog/2026-02-04-questions-about-me.md">Questions to know me better</a></li>
<li><a href="/blog/2026-02-04-geek-code.md">Geek code</a></li>
<li><a href="/blog/2026-02-04-colophon.md">Colophon</a></li>
</ul>












