---
Title: Rapport - Projekt: Laddningstid
Description: Laddningstid och användbarhet
Template: analysis
KmomId: 11_design-och-webbplatser
MenuTitle: Projekt: Laddningstid
---

Projekt: Design och webbplatser: Laddningstid och användbarhet
-------------------
__Denna rapport är min analys av laddningstider och användbarhet för tre
sidor på webbplatsen för projektet (defaulttemat). Rapporten
omfattar också tankar om vad som kan förbättras för att sänka laddningstiden
och öka användbarheten.__

###Urval

Urvalet begränsas till de tre sidor som utgör projektets webbplats:

* <u><a href="http://www.student.bth.se/~riax20/dbwebb-kurser/design/me/kmom10/" target="_blank" class="inline-link">Startsida ("News")</a></u>
* <u><a href="http://www.student.bth.se/~riax20/dbwebb-kurser/design/me/kmom10/about" target="_blank" class="inline-link">Aboutsida ("Bio")</a></u>
* <u><a href="http://www.student.bth.se/~riax20/dbwebb-kurser/design/me/kmom10/music" target="_blank" class="inline-link">Highlightssida ("Music")</a></u>

<div class="report-analysis-inline-wrap">
    <a href="../image/analysis/analysis_11_systemkommando.jpg" target="_blank">
        <img src="../image/analysis/analysis_11_systemkommando.jpg?h=220" class="report-analysis-inline-img" alt="Desktopversion SYSTEMKOMMANDO">
    </a>
    <a href="../image/analysis/analysis_11_systemkommando_mobile.jpg" target="_blank">
        <img src="../image/analysis/analysis_11_systemkommando_mobile.jpg?h=220" class="report-analysis-inline-img" alt="Mobilversion SYSTEMKOMMANDO">
    </a>
</div>

###Metod
Datan som ligger till grund för min analys är inhämtad från två olika verktyg:
Dels kommer den från Google PageSpeed Insights, som tillhandahåller data för
laddningstid, och ett Performance Score. Det sistnämnda är en sorts
sammanslaget betyg för datan som genererats vid mättillfället.

För många webbplatser tillhandahåller Google PageSpeed Insights det de kallar för
"Field Data", som är ett sammanvägt värde av många olika användares laddningstider.
Denna data saknas för webbplatsen på studentservern. Enligt Google kan detta ha
två orsaker: antingen saknas det tillräckligt många samples för att
kunna ge ett representativt anonymiserat resultat. (Google är beroende av att
användare väljer att göra denna data tillgänglig). Om studentservern inte är
indexerad hos Google så skulle det kunna vara den andra möjlga orsaken. Det är
en förutsättning för att "Field Data" ska kunna tas fram.

Mina data grundar sig därför helt på det som kallas "Lab data". Det vill säga
den data som genererats vid just mitt mättillfälle. Jag har gjort fem mätningar
per sida och tagit ut medelvärdet för dessa mätningar. På så vis hoppas
jag ha undvikikt eventuella tillfälligheter som gjort att mätvärdet inte är
representativt. Mätningarna har gjorts fem gånger vardera för mobil och för
desktop.

De värden Google tycker är viktigast ingår i deras "Core Web Vitals", där en
webbplats kan anges som godkänd eller inte. Områdena som bedöms är
laddningstid, interaktivitet och visuell stabilitet. Eftersom "Field Data" krävs för
att göra den bedömningen så kan det betyget inte delas ut. Jag har ändå tagit
fasta på det Google berättar om kriterierna för betyget, och fokuserat på
motsvarande områden ur den "Lab Data" jag fått ut vid mättillfället, nämligen:

* "Largest Contenful Paint" för laddningstid
* "Time to Interactive" för interaktivitet
* "Cumulative Layout Shift" för visuell stabilitet

PageSpeed Insights ger vid varje mätning också indikationer på möjliga
förbättringsområden. Även här har jag sammanställt resulten av fem mätningar,
och använder datan i min analys gällande vad som kan förbättras för att sänka
laddningstiden och öka användbarheten.

Det andra verktyget från vilket jag hämtat data för min analys är Chrome
Developer Tools, där jag ur fliken "Network" hämtat ut data för dels
laddningstid (fram till att sidan kan användas = "load", respektive har laddat
helt klart = "finish"), och dels mängden nedladdad data (okomprimerat resp.
komprimerat).


###Resultat

Fullständigt resultat från alla mätningar finns i detta Google sheets-dokument:<br>
<u><a href="https://docs.google.com/spreadsheets/d/1kMQfD3RbW6wvTkgPhCZr4dnDrw2Op1HL-zV0brPkjMU/edit?usp=sharing" target="_blank" class="inline-link">Google Sheets</a></u>

####News

<h5 class="pagespeed-header">Google PageSpeed Insights</h5>

<table class="pagespeed-table">

    <tr><td></td><td class="bold">Desktop</td><td class="bold">Mobil</td></tr>

    <tr><td class="right">Performance score</td>
    <td class="green">92</td>
    <td class="yellow">80,2</td></tr>

    <tr><td class="right">Largest Contentful Paint (sek)</td>
    <td class="green">1,2</td>
    <td class="red">4,1</td></tr>

    <tr><td class="right">Time to Interactive (sek)</td>
    <td class="green">0,6</td>
    <td class="green">2,7</td></tr>

    <tr><td class="right">Cumulative layout shift</td>
    <td class="red">0,28</td>
    <td class="red">0,40</td></tr>
</table>

<h5 class="pagespeed-header">Developer Tools (Chrome)</h5>

<table class="pagespeed-table">

    <tr><td></td><td class="bold">Desktop</td><td class="bold">Mobil</td></tr>

    <tr><td class="right">Laddningstid (sek)</td>
    <td class="light">1,04</td>
    <td class="light">1,31</td></tr>

    <tr><td class="right">Transferred data (MB)</td>
    <td class="light">1,1</td>
    <td class="light">1,6</td></tr>

</table>

####Bio

<h5 class="pagespeed-header">Google PageSpeed Insights</h5>

<table class="pagespeed-table">

    <tr><td></td><td class="bold">Desktop</td><td class="bold">Mobil</td></tr>

    <tr><td class="right">Performance score</td>
    <td class="green">96</td>
    <td class="yellow">81</td></tr>

    <tr><td class="right">Largest Contentful Paint (sek)</td>
    <td class="green">1,0</td>
    <td class="yellow">3,4</td></tr>

    <tr><td class="right">Time to Interactive (sek)</td>
    <td class="green">0,7</td>
    <td class="green">1,5</td></tr>

    <tr><td class="right">Cumulative layout shift</td>
    <td class="red">0,34</td>
    <td class="red">0,34</td></tr>
</table>

<h5 class="pagespeed-header">Developer Tools (Chrome)</h5>

<table class="pagespeed-table">

    <tr><td></td><td class="bold">Desktop</td><td class="bold">Mobil</td></tr>

    <tr><td class="right">Laddningstid (sek)</td>
    <td class="light">1,04</td>
    <td class="light">1,31</td></tr>

    <tr><td class="right">Transferred data (MB)</td>
    <td class="light">1,1</td>
    <td class="light">1,6</td></tr>

</table>

####Music

<h5 class="pagespeed-header">Google PageSpeed Insights</h5>

<table class="pagespeed-table">

    <tr><td></td><td class="bold">Desktop</td><td class="bold">Mobil</td></tr>

    <tr><td class="right">Performance score</td>
    <td class="green">95,6</td>
    <td class="yellow">83,6</td></tr>

    <tr><td class="right">Largest Contentful Paint (sek)</td>
    <td class="green">1,0</td>
    <td class="yellow">3,3</td></tr>

    <tr><td class="right">Time to Interactive (sek)</td>
    <td class="green">0,5</td>
    <td class="green">1,8</td></tr>

    <tr><td class="right">Cumulative layout shift</td>
    <td class="red">0,30</td>
    <td class="red">0,267</td></tr>
</table>

<h5 class="pagespeed-header">Developer Tools (Chrome)</h5>

<table class="pagespeed-table">

    <tr><td></td><td class="bold">Desktop</td><td class="bold">Mobil</td></tr>

    <tr><td class="right">Laddningstid (sek)</td>
    <td class="light">1,21</td>
    <td class="light">2,17</td></tr>

    <tr><td class="right">Transferred data (MB)</td>
    <td class="light">0,81</td>
    <td class="light">1,77</td></tr>

</table>

###Analys

Webbplatsen får sammantaget ett ok till bra "Performance score" av PageSpeed
Insight. Desktopversion lyckas bättre i testet än mobilversionen, och framförallt
för den senare verkar det finnas förbättringspotential. Ungefär samma värden
får båda versionerna för "Cumulative layout shift", det vill säga hur layouten
ändras medan sidan laddas in. En potentiell orsak till detta skulle kunna vara
att bilder i vissa fall styr hur stor plats ett element ska uppta, och att det
därmed kan uppstå "hopp", om omkringliggande element laddats in innan bilden
gjort det. Där finns alltså möjlighet att kanske koda om sidan för att undvika
"hoppande" design, och därmed förbättra användbarheten.

Tittar man på sammanlagd datamängd som läses in för att ladda sidan ser man att
mobilversionen där ligger ca 50-100 % högre än desktopversionen
("Transferred data", från Developer Tools).

Denna skillnad verkar kunna vara orsaken till skillnaden i betyg mellan mobil
och desktop för "Largest Contentful Paint" och "Time to Interactive".

PageSpeed Insight föreslår i mätningarna totalt sex olika förbättringar, och
i tre fall handlar dessa om hur man kan optimera bildstorlekar och ändra
bildformat för att öka snabbheten. En möjlig lösning för att öka snabbheten
skulle kunna vara att erbjuda fler srcset-nivåer för bilderna, så att fler
olika skärmbreddar läser in bilder som är optimerade för just den skärmbredden.

Högst potential att spara in laddningstid verkar finnas i det som PageSpeed
Insights kallar "Serve images in next gen formats", d.v.s. att använda de nyare
bildformaten JPEG 2000, JPEG XR eller WebP istället för JPEG eller PNG. För två
av sidorna ger detta en potentiell besparing av laddningstid på runt 5 sekunder.

Ikonerna längst ner laddas in i ett större format än det i
vilket de visas på webbplatsen, vilket är ytterligare en punkt som anges
som förbättringsmöjlighet. Dessutom skulle vissa bilder kunna komprimeras mer
än de gjort.

Övriga förbättringsförslag verkar inte kunna göra så stor skillnad, men det
verkar kunna finnas möjlighet att optimera ordningen i vilken resurser för sidan
läses in: PageSpeed Insight föreslår "Eliminate render-blocking resources" och
"Preload key requests", där stylesheetet respektive ett typsnitt väntar ca 180
ms med att laddas in. För att riktigt förstå hur man skulle kunna göra detta
behöver jag mer kunskap, men det verkar finnas möjlighet att använda ett
"link rel=preload"-element i HTML-filen.

####Sammanfattning

Jag är nöjd med testresultaten, och ser också hur jag skulle kunna förbättra
betyget. Min gissning innan testet var att just bilderna skulle kunna optimeras
ytterligare. Det verkar dessutom kunna vara en bra idé att testa andra
bildformat, kanske framförallt för PNG-bilderna med transparens. Även
användbarheten skulle kunna förbättras genom att se över hur sidan ritas ut, och
om storleken på vissa bilder kanske kan fördefinieras för att slippa vänta in att
bilden laddas.

Webbplatsen upplever jag som snabb och smidig. Skulle en webbplats ta 4+
sekunder att ladda in så skulle jag uppleva den som märkbart långsam. Något som
slog mig är att Googles angivna förbättringspotential i tid faktiskt överstiger
den tid som sidan verkar ta att ladda in. Värdena går inte helt ihop, men kanske
ska ses som en grov fingervisning istället för ett exakt värde.

###Referenser

Data från alla mätningar<br>
<u><a href="https://docs.google.com/spreadsheets/d/1kMQfD3RbW6wvTkgPhCZr4dnDrw2Op1HL-zV0brPkjMU/edit?usp=sharing" target="_blank" class="inline-link">Google Sheets (öppnas i ny flik)</a></u>

Om Field Data hos PageSpeed Insights:<br>
<u><a href="https://developers.google.com/speed/docs/insights/v5/about#faq" target="_blank" class="inline-link">About PageSpeed Insight (öppnas i ny flik)</a></u>

Om Core Web Vitals hos Google Developers:<br>
<u><a href="https://web.dev/vitals/" target="_blank" class="inline-link">Web Vitals (öppnas i ny flik)</a></u>
