---
Title: Rapport - Färganalys
Description: Utvärdering av webbplatsers färgval
Template: analysis
KmomId: 01_colors
MenuTitle: Färganalys
---

Färganalys
------------
Följande text är en jämförelse av typografi och färgpalett för tre webbplatser.
Texten innehåller en analys av vilka färger företagen valt att använda på sina
webbplatser, och vad som kan tänkas ligga bakom besluten.

###Urval
Jag har valt att undersöka tre europeiska flygbolags webbplatser:
Lufthansa.com, Ryanair.com och Wizzair.com. De verkar inom samma bransch, men
deras målgrupp och grafiska profiler skiljer sig åt en del. Dessa upplevda
skillnader gjorde att jag valde ut just dessa tre.

###Metod
Berätta kort om din "metod", hur du gör för att utföra undersökningen. Berätta
om du använder något speciellt verktyg.

Jag tittade i första hand på webbplatserna startsidor, men klickade även runt
lite för att se hur färger återkom i t.ex. brödtext och bokningsprocess. Sedan
lät Adobe Colors analysera färgpaletten utifrån ett screenshot jag tagit på
above-the-fold-delen av startsidan. I vissa fall ändrade jag Adobe Colors
urval av färger för att hitta de färger som bäst representerade sidans
färgschema. För att på egen hand plocka ut färgkoder ur webbplatserna använde
jag pluginen Colorzilla. Färghjulen nedan är genererade av Adobe Colors.

För att se om webbplatsernas text höll det standardiserade kontrastvärdet
på 1:4.5 körde jag dem genom
[Color Contrast Accessibility Validator](https://color.a11y.com/Contrast/).

För att hitta vilka typsnitt som användes har jag använt developer tools i
Chrome, och sökt i CSS-koden efter h1-h3, samt letat fram ett brödtextstycke
och inspekterat motsvarande element. Vid ett tillfälle lyckades jag inte hitta
information om typsnitt i koden, och jag installerade då pluginen WhatFont, som
hjälpt mig ta reda på WizzAirs brödtexttypsnitt.

###Resultat

####Lufthansa.com
<a href="../assets/img/analysis/analysis_01_lufthansa.png" target="_blank">
<img src="../assets/img/analysis/analysis_01_lufthansa_thumb.png" alt="Lufthansa.com">
</a>

#####Färger

Lufthansas webbplats har väldigt sparsmakat med färger och använder sig av ett
färgschema med en mörkblå (#05154d) och en gul (#ffad01) färg. De två färgerna
är nästan varandras exakta motpoler i färghjulet, och schemat kan därför sägas
vara ett komplementerande färgschema. Den gula färgen används som accentfärg
för call-to-action-knappar och för att visa på t.ex. låga priser. Utöver det
förekommer olika grånyanser och mörka blå nyanser i menyer och textblock.

<div class="report-analysis-inline-wrap">
    <img src="../assets/img/analysis/analysis_01_lufthansa_wheel.png" class="report-analysis-inline-img" alt="Färghjul Lufthansa.com">
    <table class="color-table">
        <tr><td class="color-box" style="background-color: #05154d"></td><td class="color-code">#05154d</td></tr>
        <tr><td class="color-box" style="background-color: #ffad01"></td><td class="color-code">#ffad01</td></tr>
        <tr><td class="color-box" style="background-color: #414e63"></td><td class="color-code">#414e63</td></tr>
        <tr><td class="color-box" style="background-color: #f5f5f5"></td><td class="color-code">#f5f5f5</td></tr>
        <tr><td class="color-box" style="background-color: #000036"></td><td class="color-code">#000036</td></tr>
    </table>
</div>

#####Typografi

Lufthansa.com använder sig genomgående av egna typsnitt som alla är sans-serifer.
Texten är aldrig helt svart, utan använder en väldigt mörkt blå (#000036). Ljusa
områden är ibland inte helt vita, vissa menyer har t.ex. en väldigt ljust grå
nyans (#f5f5f5). Det gör kontrasterna något mjukare.

- h1: LufthansaHead
- h2: LufthansaHead
- h3: LufthansaText
- Brödtext: LufthansaText

Lufthansas val av färger och typsnitt stämmer väl med det intryck jag tror att
webbplatsen vill ge. De har valt stiliga, mörka nyanser som andas kvalitet och
tradition.


####Ryanair.com

<a href="../assets/img/analysis/analysis_01_ryanair.png" target="_blank">
<img src="../assets/img/analysis/analysis_01_ryanair_thumb.png" alt="Ryanair.com">
</a>

#####Färger

Webbplatsens dominerande färger är mörkblå färg (#08428c) samt en gul färg
(#f2c335) som hämtats från logotypen. De är (nästan) varandras
komplementfärger. Den gula färgen används också genomgående, t.ex. som
accentfärg för call-to-action-knappar i boknings- och sökprocessen.

Även de gröna (#48bf11) och röda (#f21d1d) färgerna används som accentfärger,
t.ex. för att markera låga priser och specialerbjudanden. Tillsammans med den
mörkblå färgen skapar dessa två accentfärger ett triadiskt färgschema.

Dessutom förekommer på hela webbplatsen flera olika nyanser av
blått. T.ex. på webbplatsens hero-image som skiftar från mörkare till
ljusare blått, samt en ljus blå nyans (#2091eb) i t.ex. många ikoner och
sökrutor.

<div class="report-analysis-inline-wrap">
    <img src="../assets/img/analysis/analysis_01_ryanair_wheel.png" class="report-analysis-inline-img" alt="Färghjul Ryanair.com">
    <table class="color-table">
        <tr><td class="color-box" style="background-color: #08428c"></td><td class="color-code">#08428c</td></tr>
        <tr><td class="color-box" style="background-color: #2091eb"></td><td class="color-code">#2091eb</td></tr>
        <tr><td class="color-box" style="background-color: #48bf11"></td><td class="color-code">#48bf11</td></tr>
        <tr><td class="color-box" style="background-color: #f2c335"></td><td class="color-code">#f2c335</td></tr>
        <tr><td class="color-box" style="background-color: #f21d1d"></td><td class="color-code">#f21d1d</td></tr>
    </table>
</div>

#####Typografi

Ryanair använder sig av typsnittet Roboto i både rubriker och brödtext. Det är
ett mycket vanligt sans-serif-typsnitt. Textbakgrund är ofta vit, och när den
är det så är texten inte helt svart, utan har ofta en mörkgrå nyans (#2e2e2e).
Detta ger mjukare kontrast. Color Contrast Accessibility Validator gav ett
negativt utslag på en rubrik, där en ljusblå (#1976db) länk på framsidan ansågs
aningen för ljus (1:4.1) mot den ljusgrå (#f4f4f4) bakgrunden.

- h1: Roboto
- h2: Roboto
- h3: Roboto
- Brödtext: Roboto

Val av färger passar bra med det jag tror är Ryanairs syfte: man vill ge ett
intryck av att man här kan boka riktigt billiga flygresor. Typsnittet bryter
inte av mot detta, utan är väldigt neutralt.

####Wizzair.com

<a href="../assets/img/analysis/analysis_01_wizzair.png" target="_blank">
<img src="../assets/img/analysis/analysis_01_wizzair_thumb.png" alt="Wizzair.com">
</a>

#####Färger

De dominerande färgerna på Wizzair.com är de lila (#5c166e) och rosa (#c6007e)
färger som förekommer i företagets logotyp, samt en mörkblå färg (#06038d). På
vissa ställen på webbplatsen, t.ex. i ikoner, förekommer också ljusare eller
mörkare nyanser av de blå och lila färgerna. För att highlighta t.ex. vissa
rabatter används en ljusblå (#00a0Df) accentfärg.

De ovan nämnda färgerna skapar ett analogt färgschema som sträcker sig från
varma till kalla färger. De kontrasterar mot den gula färg (#ffed24) som
används som accentfärg för viktig information. Denna bryter av mot det analoga
färgschemat och ligger nästan på motsatt sida i färghjulet från webbplatsens
vanligaste mörkblå nyans, och som därmed nästan är dess komplementfärg.

<div class="report-analysis-inline-wrap">
    <img src="../assets/img/analysis/analysis_01_wizzair_wheel.png" class="report-analysis-inline-img" alt="Färghjul Wizzair.com">
    <table class="color-table">
        <tr><td class="color-box" style="background-color: #5c166e"></td><td class="color-code">#5c166e</td></tr>
        <tr><td class="color-box" style="background-color: #c6007e"></td><td class="color-code">#c6007e</td></tr>
        <tr><td class="color-box" style="background-color: #06038d"></td><td class="color-code">#06038d</td></tr>
        <tr><td class="color-box" style="background-color: #00a0Df"></td><td class="color-code">#00a0df</td></tr>
        <tr><td class="color-box" style="background-color: #ffed24"></td><td class="color-code">#ffed24</td></tr>
    </table>
</div>

#####Typografi

Wizzair.com använder P22 Underground Pro för rubriker. Typsnittet är ett
sans-serif (och känns igen från bl.a. Londons tunnelbana). Även typsnittet för
brödtexten är ett sans-serif-typsnitt: Source Sans Pro.

- h1: P22 Underground Pro
- h2: P22 Underground Pro
- h3: P22 Underground Pro
- Brödtext: Source Sans Pro

Färgerna stämmer bra med den profil jag tror att WizzAir vill ha. Färgerna är
ganska djärva och passar snarare en ungdomligare än en traditionsmedveten
målgrupp. Om Ryanair är low-cost-flygens Coca-Cola så är WizzAir Pepsi, och de
nya uppstickarna. Färgerna förstärker det intrycket.

###Analys
Min analys är att företagen verkar ha varit noga med att låta deras respektive
målgrupp och identitet genomsyra hur webbplatsen ser ut. Det visar sig i att
de tre webbplatsernas val av färgpalett och typografi skiljer sig åt ganska
markant, även om produkten skulle kunna sägas vara nästan densamma. Störst är
skillnaden mellan Lufthansa och de två lågprisbolagen Ryanair och WizzAir.

Lufthansas webbplats domineras av en lugn, mörkblå färg som kan förknippas med
traditionalism. Accentfärgen sticker ut, men är inte särskilt ettrig, (särskilt
inte om man jämför med den gula accentfärg som WizzAir använder). Om man utgår
från att deras målgrupp i större utsträckning än lågprisbolagens snarare
värdesätter service än låga priser så verkar färgvalet logiskt.

WizzAirs färger gör att de sticker ut från mängden: lila är ett ovanligt
färgval för webbplatser. Kanske var det ett medvetet val att sticka ut för att
profilera sig som den unga uppstickaren och kunna konkurrera med redan
etablerade low-cost-flygbolag som t.ex. Ryanair. WizzAirs webbplats är den som
valt mest ungdomliga färger, och de har också unga passagerare.

På Ryanairs webbplats signalerar färgvalet och de olika accenfärgerna rött och
grönt att man kan göra riktiga klipp. Det är antagligen väl uttänkt och rimmar
bra med företagets lågprisprofil.

Genomgående har webbplatserna valt sans-serif-typsnitt, och inte särskilt
djärva sådana. Sans-serifer anses vara mer lättlästa än typsnitt med serifer,
vilket gör att valet känns rimligt. Webbplatserna vill slutligen sälja något,
och användbarheten går före eventuella konstnärliga ambitioner som man kanske
hade väntat sig på webbplatser för t.ex. ett rockband eller en festival.
Lättlästheten hjälps också av att alla tre webbplatser undviker alltför stora
kontraster mellan text och bakgrund genom att istället för svart text använda
mörkgrå. Color Contrast Accessibility Validator gav utslag för en länk på
Ryanairs webbplats som hade marginellt för lite kontrast, i övrigt fick
webbplatserna godkänt.

Jag slogs av att alla tre webbplatser använder färgpaletter som passar en
vedertagen modell, men med ett par mindre finjusteringar (t.ex. är inte
färger varandras exakta komplementfärger). Även om det ganska generösa
användandet av olika färger på Ryanair.com och Wizzair.com skulle kunna riskera
att bli rörigt så gör de, tack vare det uttänkta färgschemat, ett rent intryck.

###Referenser

<i>The other demographic shows that Wizz is a young person's airline, with an
average passenger age of 36.</i>
TheTimes.co.uk, 2020-07-20:
[https://www.thetimes.co.uk/article/an-airline-full-of-eastern-promise-gmxrctw90]

<i>According to Patrick McNeil, author of "The Web Designer's Idea Book",
purple is one of the least-used colors in web design.</i>
Beaird, George, Walker 2020:
The Principles of Beautiful Web Design, 4th Edition (s. 88)

###Övrigt
Vid tangentbordet: Richard Axelsson
