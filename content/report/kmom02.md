---
Title: Redovisning - Kmom02
Description: Min redovisningstext för kursmoment 02
Template: kmom
KmomId: kmom02
MenuTitle: Kmom02
---

Kursmoment 02
-----------
**Vad tycker du om SASS än så länge?**

SASS verkar väldigt smart och smidigt. Jag skrev reglerna med SCSS (d.v.s. inte
SASS), så övergången från CSS var inte så dramatisk. Ju större ett projekt
växer, desto större blir fördelarna med att kunna definiera t.ex. textstorlek
och färger med hjälp av variabler istället för att behöva gå in och ändra i
varje enskilt element. Att nästla regler har jag också använt mig av. Ännu har
jag bara snuddat vid att kunna använta matematiska operatorer i koden, men det
verkar också väldigt smidigt, t.ex. för att kunna skala upp text utan att behöva
ändra varje enskilt elements teckenstorlek.

**Är du bekant med Node, npm eller npm scripts (t.ex. npm run lint) sedan tidigare? Vad anser du om det?**

Nej, det här är min första erfarenhet. Det verkar smidigt att kunna göra egna
scripts, t.ex. det script som visades i föreläsningen för att automatiskt
kompilera till SASS.

**Hur kändes det att kompilera SASS till CSS, var det något du reflekterade över?**

Det blev väldigt många rader, delvis på grund av CSS:en som läses in för
Font-Awesome-fonterna, gissningsvis. Den minifierade CSS-filen ser inte
särskilt rolig ut, men den tar nästan 25% mindre plats.

**Kommentera ditt tema, hur kan man beskriva dess design och hade du några planer på “design” när du byggde ditt tema?**

Jag gillar modernism och brutalism och satsade på att försöka få till ett tema
på det. På Google Fonts hittade jag ett teckensnitt som liknade ett jag sett på
en gammal filmposter. Jag hade även ett par egna foton på futuristisk
arkitektur och har försökt väva in dem i designen. Känslan jag ville få till
var konsthall/betong. Med en vinröd highlightfärg kan jag highlighta t.ex.
markerade länkar och ge lite liv åt sidan.

**Valde du att dela upp din kod? Vilka uppdelningar valde du att göra?**

Jag valde att lyfta ut typografiregler till en separat modul, och dessutom la
jag alla variabler i en egen modul. I övrigt kände jag inte att det fanns någon
vettig uppdelning att göra, och lät koden vara kvar i samma modul. Tack vare
nästlade regler blev koden ändå ganska bra strukturerad.

**Vilken är din TIL för detta kmom?**

Detta kursmoment var ganska massivt för min del. Det var min första
erfarenhet av SASS och Node Package Manager, och dessutom känns både Git och
Pico fortfarande väldigt nytt. En stor del av pluggtiden gick åt till att
försöka hänga med i föreläsning och i guidetext på dbwebb. Till slut vågar jag
säga att jag nu i alla fall fått en grund att stå på i SASS, och vet vilka
fördelar det ger gentemot vanlig CSS. Eftersom vi jobbat vidare på samma
Portfolio som vi började med förra veckan har jag långsamt fått bättre koll på
strukturen i Pico och hur de olika filerna samspelar med varandra. Detsamma
gäller även Git, där de vanligaste funktionerna så sakteliga börjar sätta sig.

Jag läste också de aktuella kapitlen ur kursboken, och tog med mig en
del därifrån, bland annat gyllene snittet och hur man kan jobba med text för
få till det snyggt.
