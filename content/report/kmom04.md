---
Title: Redovisning - Kmom04
Description: Min redovisningstext för kursmoment 04
Template: kmom
KmomId: kmom04
MenuTitle: Kmom04
---

Kursmoment 04
-----------
#####Kommentera kort om skrivuppgiften, något som är värt att nämna från arbetet med den?
Det var intressant att se hur teorierna från kursen och kurslitteraturen
användes i praktiken av stora webbplatser. Att analysera webbplatser var ett
bra sätt att få kunskaperna att sätta sig. Det visade sig lättare än jag
trodde att hitta ett mönster och logik i vilka färger respektive webbplats
arbetade med.

#####Vilket färgschema valde du till ditt tema och hur valde du att använda färgerna (mer eller mindre eller lika mycket av alla färger)?
Jag hade ursprungligen ett akromatiskt färgschema, d.v.s. gråskala, med
inslag av en mörkröd accentfärg, och valde att föra in ytterligare två röda
färger i andra nyanser, så att jag nu har ett monokromatiskt färgschema. Totalt
utgörs sidans färger därmed av en gråskala samt följande tre röda nyanser:

<table class="color-table">
    <tr><td class="color-box" style="background-color: #330000"></td><td class="color-code">#330000</td></tr>
    <tr><td class="color-box" style="background-color: #9a0000"></td><td class="color-code">#9a0000</td></tr>
    <tr><td class="color-box" style="background-color: #cc0000"></td><td class="color-code">#cc0000</td></tr>
</table>

Eftersom jag ursprungligen byggt designen kring tanken att vara sparsam med
färger blev det en liten utmaning att försöka få in fler färger utan att det
såg konstigt ut.

Alla tre röda nyanser förekommer i sidans logga samt i flash-image-baren
mellan headern och sidans huvudinnehåll. 9a0000 finns också i en detalj i
footer-bilden (med ca 50 % opacitet), där ett fönster lyser rött.

#####Valde du att jobba med accentfärg och isåfall hur?
Utöver ovanstående så använder jag de klaraste röda nyanserna som accentfärger
för länkar: markerade länkar är mörkröda, och vid hover blir de klarröda.

#####Hur valde du att lösa ditt dark theme? Gjorde du en kopia på ditt vanliga tema? Eller löste du det med imports?
För det mörka temat valde jag att dra ner på både ljuset och kontrasten. Jag
ersatte header- och footerbilder med mörkare varianter och i stora drag
inverterade jag text och bakgrundsfärg. Texten är dock inte helt vit utan en
ljus grå, för mjukare kontrast. Alla bildfiler har fått ett mörkt filter,
eller så ligger en div med en opacitet på för att göra dem mörkare.

Jag har via SASS genererat två separata CSS-filer. Grunden i dessa filer är densamma. Den enda skillnaden är att jag gjort varsin variabelfil för det ljusa respektive det mörka temat. Filerna innehåller både färgvariabler och variabler för t.ex. bild-URL:er och effekter. På så sätt var det mycket enklare att göra uppdateringar och se hur designen påverkades.


#####Vilken är din TIL för detta kmom?
Under detta kursmoment lärde jag mig en hel del. Färgteori med olika
färgscheman, hur man kan få till skugga på element, hur man ska tänka med
kontraster, och att man kan lägga filter på bildelement, t.ex. Det var också
intressant att se hur stora webbplatser valt att arbeta med färger,
accentfärger o.s.v.
