---
Title: Redovisning - Kmom03
Description: Min redovisningstext för kursmoment 03
Template: kmom
KmomId: kmom03
MenuTitle: Kmom03
---

Kursmoment 03
-----------
#####Hur har det gått att jobba med CSS-Grid/Flexbox?
Det har både gått bra och stundtals varit lite frustrerande. Griden kändes till
en början intuitiv, men jag behövde krångla ett tag med att få griden att hamna
centrerat på sidan (istället för att täcka hela skärmens bredd). Flexboxen
jag använder på sidan för redovisningstexterna är ganska enkelt utformad så den
gick väldigt smidigt att få till. Det är mycket regler att tänka på, och det
var till stor hjälp att använda Firefox developer tools, där man enklare ser
griden (även om jag i Chrome gillar att man ser exakt fönsterstorlek när man
drar i developer-tools-fönstret).

#####Har du jobbat med dessa tekniker sedan tidigare? Vad anser du om det?
Både flexbox och grid använde jag under htmlphp-kursen tidigare under terminen,
och som självlärd i att göra all layout med tabeller för ca 20 år sedan så är
detta något som är mycket bättre såklart, men det är också många fler
aspekter att tänka på: många olika regler, där man behöver förstå om det är
child- eller parent-elementet som ska ändras, och vilken av alla regler det
är som påverkar ett elements position.

#####Har du försökt dela upp din SASS-kod i olika moduler? Kanske har du skapat en ny modul som är din layout?
Förutom de olika moduler jag redan skapat skapade jag denna vecka en scss-modul
vardera för grid-sidan och sidan med redovisningstexterna. Jag flyttade också
ut reglerna för responsivitet (media-queries) till en separat modul som jag
läser in allra sist.

#####Valde du att göra om din sidas layout eller nöjde du dig med report sidan?
Sidan har hittills inte särskilt mycket mer innehåll än just redovisningstexter
så det kändes inte aktuellt att ändra något på de andra sidorna. Jag ordnade
annars en automatiserad meny med twig-kod, där länkarna i menyn här till
vänster genereras baserat på de filer som ligger i min "reports"-mapp, med
hjälp av en loop som stegar igenom innehållet. Twig-kod testar också om
nuvarande sida är aktiv och tilldelar i så fall en klass som ger en röd länk.
Denna vecka ordnade jag också några småsaker med designen, t.ex. en ny logga.

#####Vilken är din TIL för detta kmom?
Jag har fått lite mer struktur och en förbättrad förståelse för hur grid och
flexbox fungerar. Mer specifikt har jag lärt mig hur man med hjälp av en
media query som ställer om span till 1 ordnar ett väldigt smidigt sätt att
göra en grid-sida responsiv. Justify-content har tidigare känts lite suddigt
men där har jag nu fått lite bättre koll.
