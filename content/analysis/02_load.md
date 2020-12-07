---
Title: Rapport - Laddningstid
Description: Laddningstid och användbarhet
Template: analysis
KmomId: 02_load
MenuTitle: Laddningstid
---

Laddningstid och användbarhet
-------------------
Denna rapport är en analys av laddningstid och användbarhet för tre webbplatser.
I min analys ska jag också försöka peka ut vad som kan förbättras för att
sänka webbplatsernas laddningstid och öka användbarheten.

###Urval
Jag har valt att undersöka webbplatserna för tre av de största europeiska
museerna för modern konst. Det kändes som en intressant kategori av
webbplatser, då de kanske inte är lika konkurrensutsatta och
optimerade som t.ex. e-handelswebbplatser. Samtidigt borde de vilja ha visuellt
tilltalande webbplatser.

###Metod
Med hjälp av Googles PageSpeed Insights samt Network-funktionen i Google Chromes
Developer Tools har jag tagit fram data av olika slag för de tre webbplatsernas
laddningstider och användbarhet. För båda verktygen såg jag till att göra
separata sökningar för desktop och mobil. Eftersom mätresultaten skilde sig
åt något mellan varje mättillfälle så gjorde jag göra flera mätningar från vilka
jag räknade ut ett medelvärde.

I Google Chrome Developer Tools hämtade jag ut värden för nedladdad datamängd,
komprimerat ("transferred") respektive okomprimerat ("resources"). Dessutom
hämtade jag ut antal filer som laddas in ("requests) samt tiden det tar att
ladda in sidan för att kunna användas ("load"), och tiden fram till att sidan
helt laddat klart ("finish").

Från PageSpeed Insights hämtade jag ut "field data", det vill säga ackumulerade
resultat från en mängd användare över en längre tid, för varje webbplats. De
viktigaste kriterierna utgör det som Google kallar "Core Web Vitals", som är
en sammanvägning av data för laddningstid, interaktivitet och visuell
stabilitet. De tre områdena representeras (för tillfället) av data som Google
kallar "Largest Contentful Paint" (laddningstid), "First Input Delay"
(interaktivitet) och "Cumulative Layout Shift" (visuell stabilitet).

Jag hämtade även ut "lab data" i form av "Time to Interactive". Lab data är
mer av en ögonblicksskildring: det är data som genererats av just mina
mätningar (kanske blir den därmed mindre tillförlitlig?). PageSpeeds
"Performance score" (som visas längst upp på Pagespeed-sidan) är en
sammanvägning av just lab-data.

Slutligen tittade jag också på de fem översta (sorterat på potentiell vinst i
laddningstid som åtgärden skulle resultera i) förbättringsåtgärder som Google
föreslagit för respektive webbplats.

###Resultat

####Astrup Fearnley Museet - afmuseet.no

<div class="report-analysis-inline-wrap">
    <a href="../image/analysis/analysis_02_afmuseet.png" target="_blank">
        <img src="../image/analysis/analysis_02_afmuseet.png?h=220" class="report-analysis-inline-img" alt="Desktopversion afmuseet.no">
    </a>
    <a href="../image/analysis/analysis_02_afmuseet_mobile.png" target="_blank">
        <img src="../image/analysis/analysis_02_afmuseet_mobile.png?h=220" class="report-analysis-inline-img" alt="Mobilversion afmuseet.no">
    </a>
</div>

<h5 class="pagespeed-header">Google PageSpeed Insights</h5>

<table class="pagespeed-table">

    <tr><td></td><td class="bold">Desktop</td><td class="bold">Mobil</td></tr>

    <tr><td class="right">Performance score</td>
    <td class="yellow">76,8</td>
    <td class="red">39,2</td></tr>

    <tr><td class="right">Core Web Vitals passed</td>
    <td class="red">Nej</td>
    <td class="red">Nej</td></tr>

    <tr><td class="right">Largest Contentful Paint (sek)</td>
    <td class="red">2,7</td>
    <td class="red">3,5</td></tr>

    <tr><td class="right">First input delay (ms)</td>
    <td class="green">3</td>
    <td class="green">17</td></tr>

    <tr><td class="right">Cumulative layout shift</td>
    <td class="red">0,48</td>
    <td class="red">1,13</td></tr>
</table>

<h5 class="pagespeed-header">Developer Tools (Chrome)</h5>

<table class="pagespeed-table">

    <tr><td></td><td class="bold">Desktop</td><td class="bold">Mobil</td></tr>

    <tr><td class="right">Laddningstid (sek)</td>
    <td class="light">1,09</td>
    <td class="light">1,91</td></tr>

    <tr><td class="right">Transferred data (MB)</td>
    <td class="light">0,92</td>
    <td class="light">0,91</td></tr>

</table>

Sidan får ett genomsnittligt performance score för desktopversionen, och ett
ganska lågt score för mobilversionen. Sidan verkar inte vara så tung, men
mobilversionen verkar vara ganska långsam att ladda in. Både desktop- och
mobilversionen får höga värden (dåligt) på Cumulative Layout Shift, d.v.s. hur
sidan ändras medan den laddas in.

Webbplatsens största förbättringspotential ligger i att förbättra
mobilversionen. På startsidan finns två bilder där bildstorlekarna inte är
optimerade, och det finns också oanvänd CSS och JavaScript som kan rensas bort.

####Stedelijk Museum voor Actuele Kunst - smak.be

<div class="report-analysis-inline-wrap">
    <a href="../image/analysis/analysis_02_smak.png" target="_blank">
        <img src="../image/analysis/analysis_02_smak.png?h=220" class="report-analysis-inline-img" alt="Desktopversion smak.be">
    </a>
    <a href="../image/analysis/analysis_02_smak_mobile.png" target="_blank">
        <img src="../image/analysis/analysis_02_smak_mobile.png?h=220" class="report-analysis-inline-img" alt="Mobilversion smak.be">
    </a>
</div>

<h5 class="pagespeed-header">Google PageSpeed Insights</h5>

<table class="pagespeed-table">

    <tr><td></td><td class="bold">Desktop</td><td class="bold">Mobil</td></tr>

    <tr><td class="right">Performance score</td>
    <td class="yellow">64,6</td>
    <td class="red">23,8</td></tr>

    <tr><td class="right">Core Web Vitals passed</td>
    <td class="red">Nej</td>
    <td class="red">Nej</td></tr>

    <tr><td class="right">Largest Contentful Paint (sek)</td>
    <td class="red">3,6</td>
    <td class="red">2,6</td></tr>

    <tr><td class="right">First input delay (ms)</td>
    <td class="green">6</td>
    <td class="green">25</td></tr>

    <tr><td class="right">Cumulative layout shift</td>
    <td class="green">0,01</td>
    <td class="red">0,12</td></tr>
</table>

<h5 class="pagespeed-header">Developer Tools (Chrome)</h5>

<table class="pagespeed-table">

    <tr><td></td><td class="bold">Desktop</td><td class="bold">Mobil</td></tr>

    <tr><td class="right">Laddningstid (sek)</td>
    <td class="light">2,97</td>
    <td class="light">3,27</td></tr>

    <tr><td class="right">Transferred data (MB)</td>
    <td class="light">3,5</td>
    <td class="light">3,53</td></tr>

</table>

Webbplatsens desktopversion hamnar i Googles gula performance score, medan
mobilversionen får ett mycket lågt betyg. Ingen av versionerna klarar av
Core Web Vitals-testet. Det är en ganska stor skillnad i Cumulative
Layout Shift mellan desktop och mobil - ett tecken på att mobilversionen inte
är så genomtänkt. Sidan är ganska tung, med en total storlek på ca 3,5 MB.

Den stora potentialen ligger i att förbättra hur bilder presenteras.
Bildstorlekar kan optimeras för att spara totalt nästan en sekund, och också
genom att växla från JPEG till WebP kan man spara resurser.

####Tate - tate.org.uk

<div class="report-analysis-inline-wrap">
    <a href="../image/analysis/analysis_02_tate.png" target="_blank">
        <img src="../image/analysis/analysis_02_tate.png?h=220" class="report-analysis-inline-img" alt="Desktopversion tate.org.uk">
    </a>
    <a href="../image/analysis/analysis_02_tate_mobile.png" target="_blank">
        <img src="../image/analysis/analysis_02_tate_mobile.png?h=220" class="report-analysis-inline-img" alt="Mobilversion tate.org.uk">
    </a>
</div>

<h5 class="pagespeed-header">Google PageSpeed Insights</h5>

<table class="pagespeed-table">

    <tr><td></td><td class="bold">Desktop</td><td class="bold">Mobil</td></tr>

    <tr><td class="right">Performance score</td>
    <td class="yellow">78,8</td>
    <td class="red">36,2</td></tr>

    <tr><td class="right">Core Web Vitals passed</td>
    <td class="red">Ja</td>
    <td class="red">Nej</td></tr>

    <tr><td class="right">Largest Contentful Paint (sek)</td>
    <td class="red">2,2</td>
    <td class="red">2,4</td></tr>

    <tr><td class="right">First input delay (ms)</td>
    <td class="green">5</td>
    <td class="green">16</td></tr>

    <tr><td class="right">Cumulative layout shift</td>
    <td class="red">0,04</td>
    <td class="red">1,16</td></tr>
</table>

<h5 class="pagespeed-header">Developer Tools (Chrome)</h5>

<table class="pagespeed-table">

    <tr><td></td><td class="bold">Desktop</td><td class="bold">Mobil</td></tr>

    <tr><td class="right">Laddningstid (sek)</td>
    <td class="light">4,82</td>
    <td class="light">5,79</td></tr>

    <tr><td class="right">Transferred data (MB)</td>
    <td class="light">3,20</td>
    <td class="light">2,80</td></tr>

</table>

Webbplatsen är ganska tung, ca 3 MB, och tar ca 5 sekunder att ladda in. Google
ger den ändå ett ganska högt betyg (desktopversionen). Kanske på grund av att
Largest Contentful Paint får ett godkänt värde? Även Cumulative Layout Shift
får ett bra värde.

Startsidan har flera stora bildfiler som har potential att optimeras,
framförallt den stora gröna målningen som är "above the fold". Där används
samma version av bilden både för desktop och mobil.

###Analys
Delvis får jag säga att mina fördomar om hur webbplatser för museum skulle
klara sig i testet besannades. Jag tänker att museiwebbplatser inte i lika hög
grad som t.ex. prisjämförelseportaler eller nyhetssajter har ett tryck på sig
att göra sin webbplats snabb och lättåtkomlig. Konkurrensen är rimligen inte
lika hård som om man skulle vara i t.ex. hemelektronikbranschen. Kanske
har man därför satsat på stora, attraktiva bilder utan att se till att
optimera dem tekniskt.

Även om ovanstående skulle vara sant, så är det givetvis viktigt även för ett
museum att hemsidan är smidig och lättnavigerad. Besökare ska kunna hitta
museets öppettider, vilja handla i museets webbshop och bli inspirerade att
göra ett besök. Dessutom påverkas SEO-rankingen av Googles PageSpeed-index, och
det är självklart viktigt för alla typer av webbplatser.

Alla tre webbplatser har fått låga betyg för mobilversionerna, och alla har ett
sämre Cumulative Layout Shift-värde än respektive desktopvariant. Webbplatserna
är överlag ganska röriga och svårnavigerade, och det är såklart inget plus om
sidorna dessutom oväntat hoppar till medan man vill klicka på något. Även "Time
to Interactive" har ett mycket högre värde (dåligt) i mobilversionen än för
desktop. Sammanfattningsvis verkar det inte ha satsats så mycket på att
optimera upplevelsen för mobilanvändare. Där finns alltså en del att jobba på
i strukturen för koden, så att sidorna blir mer användarvänliga.

Något som slår mig är att laddningstiden enligt dev tools genomgående är längre
för mobilsidorna än desktopsidorna, och att nedladdad datamängd är ungefär
lika stor i båda versionerna. Det skulle kännas rimligt om mobilversionen vore
mer lightweight, och alltså gå snabbare att ladda in än desktopversionen.

Två av de tre webbplatserna har stor förbättringspotential i hur
bilder laddas in och presenteras. För varje webbplats hämtade jag en topp-5
"opportunities" för förbättring som Google såg. Fem av de totalt åtta
opportunities som jag fick upp hade med bilder att göra. Bland möjligheterna
till förbättring finns att komprimera filerna mer och att använda andra
format, t.ex. WebP.

Annars sticker "unused Javascript" ut. Där ser Google förbättringspotential på
alla sidor (med undantag för det norska museets desktopsida). Google flaggar
för detta när mer än 20 kB i en JavaScript-fil inte används. Man skulle med
andra ord kunna titta på att dela upp koden och endast läsa in den kod som
faktiskt används.

Baserat på datan i testet ser min rangordning ut så här:

1. afmuseet.no
2. tate.org.uk
3. smak.be

Förstaplatsen var ganska enkel att dela ut, men plats 2 och 3 var svårare.
Mätvärdena från dev tools respektive PageSpeed Insights verkar motsäga varandra
lite. Tate får bättre värden hos den senare, medan Smak.be får bättre värden
, d.v.s. snabbare laddningstid, i dev tools. Eftersom jag själv inte upplevde
Tate som så långsam, så får det fälla avgörandet.

Beroende på vilken typ av webbplats jag besöker så är jag mer eller mindre
känslig för långa laddningstider. Vid shopping är det väldigt frustrerande om
det blir någon sekunds fördröjning när man håller på och jämför produkter. Om
jag besöker en sida för att läsa en längre artikel så är jag inte lika känslig.
Det är dessutom värre om sidan "hoppar till" när man redan upplevt att den
är klar, än att sidan är lite långsam. För att säga något generellt så märker
jag av att något är långsamt när laddningstiden börjar närma sig 3-4 sekunder.

Jag upplever faktiskt ingen av webbplatserna som särskilt långsam, trots de
dåliga värden de fått i testen. Det går helt klart att få sidorna att ladda
snabbare, men jag har kanske ännu inte blivit så känslig. Kanske ändras det och
jag märker skillnaden mer när jag lärt mig mer om hur man optimerar
laddningstid.

###Referenser

Rådata från Chrome Development Tools och PageSpeed Insights:<br>
<a href="https://docs.google.com/spreadsheets/d/1I26gzh9foqO9T_6mpbCl_hPEwWmskS8pcooJnMqfxUs/edit?usp=sharing" target="_blank" class="inline-link">Google Sheets (öppnas i ny flik)</a>

###Övrigt

Vid tangentbordet: Richard Axelsson
