---
Title: Redovisning - Kursmoment 07-10: Projekt
Description: Min redovisningstext för kursmoment 07-10: Projekt
Template: kmom
KmomId: kmom10
MenuTitle: Projekt
---

Kursmoment 07-10: Projekt
-----------

####1.1 Implementerade uppdrag

**Uppdrag 1: Webbplats**

Jag valde att börja med en ny installation från example-mappen. Det kändes bäst att börja från scratch, och dessutom bra att repetera hur man t.ex. initierar package.json och lägger in scripten för SASS. Min kod utgår från dbwebb-temat, men jag rensade ut rejält i Twig- och CSS-filerna för att få bort oanvänd kod.

Bland kunderna kändes artistalternativet mest inspirerande, och jag började uppgiften med att försöka hitta en grafisk profil. Jag hittade på artistnamnet “SYSTEMKOMMANDO”, och efter att ha hittat ett snyggt typsnitt som jag byggde en logotyp utifrån, så ordnade jag ett par passande herobilder (en för varje tema). För varje tema ordnade jag också en favicon. Nästa steg blev att skissa upp en webbplatsdesign i Gimp.

Jag satte tidigt sidbredden till 960 pixlar. Det kändes vettigt att ha en ram att utgå ifrån, och 960 px ger många alternativ för att dela upp sidan i mindre delar. Jag valde att satsa på en trekolumnersgrid, vilket kändes som att det gav bra möjligheter för att skapa en dynamisk design. Menyn fungerar bra både i desktop och mobil: vid < 600 pixlars bredd övergår menyalternativen från att stå i bredd till att stå på varandra i höjdled.

Jag försökte hitta lite variation i utformningen av de tre sidorna (förstasida = “News”, about = “Bio” och highlights = “Music”), och fick bland annat till en “splash” och en tabell på förstasidan, och lite olika knappar och varierande bildstorlekar på de övriga sidorna. Bilderna laddas in via Cimage, med undantag för den stora bakgrundsbilden samt tre bilder för stiliserade linjer och ramar som istället laddas in via CSS. Cimage-bilderna använder sourceset för att ladda in rätt storlek för rätt skärmbredd.

Sidorna har också fyllts med texter om artistens historia, musik och nyheter. På about (eller “Bio”)-sidan finns information om kundens tanke med hemsidan - mer ingående om detta finns på den “dolda” aboutsidan. Längst ner på varje sida finns en footer med kontaktinformation, länkar till musikströmningstjänster samt en ikon för att byta tema.

**Uppdrag 2: Tema**

Med tanke på kundens profil som ett alternativt syntband, kändes svart som ett självklart färgval. Jag ville bygga ut färgschemat, men inte satsa på ett alltför färgglatt (t.ex. triadiskt eller tetriadiskt) schema. Kunden har ändå ambitionen att vilja sticka ut, och jag landade därför i ett analogt färgschema med tre färger mellan rosa och blått. Dessa färger passar väldigt bra ihop med det svarta, och jag använder den rosa färgen för att t.ex. highlighta länkar.

Schemat använder SASS, vilket bland annat gett möjlighet att t.ex. nästla regler. Färger och andra designregler bestäms via variabler. Variablerna för temat ligger i en separat SASS-fil, så att det enkelt går att hitta den kod som påverkar det aktuella temat. SASS-koden är uppdelad ytterligare, med separat moduler för globala regler, segmentspecifika regler, och regler för responsivitet.

En ledstjärna i arbetet med temat har varit enhetlighet. Redan från början hade jag en tanke kring hur designen och temat skulle se ut, och jag utgick t.ex. från ett specifikt typsnitt när jag skissade fram webbplatsen. Resultatet visar sig i t.ex. ett enhetligt utseende på alla skivomslag, och att jag återanvände logotypen och typsnittet för både skivomslag och trycken på flexskiva och t-shirt.

Jag har också sett till att upprepa vissa detaljer och designelement, t.ex. den lilla blixten som förekommer i logotyp, i en linje och i typsnittet.

Textur förekommer i form av kopplingsschemat som utgör bakgrundsbild för webbplatsen. Att bakgrundsbilden är fixerad, och shadow-effekten från webbplatsens huvudinnehåll gör att den tycks sväva över kopplingsschemat, vilket ger en känsla av djup.

Griddesignen utgör basen för layouten och hur elementen positioneras på sidan, och tycker mig ha hittat en balans mellan de olika designelementen.. För att bryta av mot balansen valde jag att lägga en “splash” på förstasidan, med lite extra whitespace och en skev, rosa ram runt. Det får den att sticka ut. Den snedställda flexskivan i bilden i splashen ger en känsla av rörelse och dynamik och drar uppmärksamheten till sig


**Uppdrag 3: Responsivitet och tillgänglighet**

Sidan har ett trekolumnersgrid som löper över hela huvudinnehållet. Ibland upptar bilder eller texter hela bredden, ibland endast 1 eller 2 tredjedelar. Med hjälp av griden kan man därmed visa webbplatsens innehåll på ett dynamiskt men ordnat sätt. Även flexbox används flitigt. Bland annat förekommer det i den stora textlogotypen i herobilden, i huvudmenyn och i “splashen” på startsidan.

Webbplatsen är anpassad för att dynamiskt kunna hantera olika skärmstorlekar. Mitt mål var att sidan skulle kunna användas på enheter ned till 320 pixlars viewport ( = iPhone 3). Följande regler är definierade i modulen responsive.scss:

Vid 980 pixlars bredd ( = 960 px sidbredd + 20 px scrollbar) övergår griden till ett enkolumnersgrid som upptar hela skärmbredden. Alla grid-, bild- och flexelement får bredden 100 % och anpassar sig dynamiskt efter skärmbredden. Via srcset-taggar sätter CImage storleken för bildkällan till 900px.

Splashens flex-direction ändras från row till column-reverse, så att bilden hamnar över texten. På about-sidan ( = “Bio”) beskär CImage den avlånga bilden till en kvadratisk bild som passar bättre när alla element ligger i en kolumn.

Nästa breaking point är 768px. För att undvika scrollbars bryts textlogotypen i herobilden upp i två rader genom att flex-direction ändras till column. Den kvadratiska logotypen försvinner från herobilden. Menyn får större bokstäver så att det är lättare att klicka rätt i en mobil.

Vid 600 px minskar textlogotypens textstorlek och navigeringen får flex-direction column istället för row. Via srcset-taggar sätter CImage storleken för bildkällan till 600px.

För att göra webbplatsen användbar även för gamla mobiler med en skärmbredd på mindre än 360px finns ytterligare en breakingpoint, vid just 360px. Där döljs en av kolumnerna i tabellen på startsidan och textlogotypens textstorlek minskas ytterligare. Därmed ser sidan bra ut i skärmbredder på ända ned till 250px.

Alla sidor får 100 i accessibility i Lighthouse. För att nå dit behövde jag ändra html-lang till sv och lägga till alt-taggar på alla bilder. Jag behövde också välja något mörkare nyanser av blått och lila i mitt defaulttema så att kontrasten mellan för- och bakgrundsfärg på två actionbuttons fick godkänt.
Båda mina teman ser OK ut i Toptals filter för färgblindhet. Även om man går miste om en viss highlighteffekt för vissa färger är det inga problem att navigera på sidorna, och det finns ingen risk för missförstånd p.g.a. felaktig färgåtergivning.

**Uppdrag 4: Alternativt tema**

I mitt alternativa tema tog jag fasta på kundens önskemål om att få med datornostalgi och teknik i designen, och jag valde därför att låta färgerna bestämmas av färgschemat för den dator (ABC 80) kunden använder i sin musik. Det blev ett analogt färgschema med varma färger, som jag kompletterade med ljusare bruna nyanser för att få fler möjliga kontrastnivåer. Resultatet blev varmare än defaulttemat, vilket känns rimligt med tanke på nostalgitanken. Den rosa highlightfärgen från defulttemat har här ersatts av orange, som är en bra signalfärg.

Bilder påverkas också av det nya temat. Alla bilder har ett CSS-filter som ger dem en sepiaton som passar bra in i färgschemat. Sepiatonen återkommer också i de textelement som har en mörk bakgrund, vilket sänker kontrasten och gör webbplatsen skonsammare mot ögat. Bakgrundstexturen i form av kopplingsschemat är en varmare variant än i defaulttemat, också detta i sepiaton.

Även i detta tema har jag låtit enhetlighet vara ett ledord. Jag tog fasta på datornostalgitanken och lät ett återkommande designelement vara grova pixlar. De förekommer som ett rutnät i skärmen på herobilden och i linjer: linjen mellan herobilden och menyn samt linjerna som omsluter sidans huvudinnehåll. Även splashen på startsidan har markant ändrats i sitt utseende: den skeva ramen har ersatts med en grovpixlig inramning över och under.

Typografin går också i pixlighetens tecken. Typsnittet för menyn och rubriker är ett som liknar det typsnitt som finns på text-tv och i datorer från tidigt 80-tal. De har fått en liten shadow-effekt för att ge en varmare framtoning.

**Uppdrag 6: Analys valfri**

I den valfria analysen valde jag att analysera min webbplats utifrån laddningstid och användbarhet. Färganalys har jag på många sätt redan gjort i texten som beskriver mina två teman, så det kändes mer naturligt att välja ett annat område.

Jag använde Developer Tools Network och gjorde flera mätningar för varje sida. Precis som i kmom05 gjorde jag även flera mätningar via PageSpeed Insights. I båda verktygen gav mätningarna lite olika utfall varje gång, så det kändes bra att istället få till ett medelvärde.

Något som skilde sig från min analys inom ramen för kmom05 var att ingen “Field Data” fanns tillgänglig för min webbplats. Jag fick istället basera analysen helt på den data som genererades vid mina mätningar. Datan samlade jag i ett Google Sheets-dokument, och på Portfoliosidan skrev jag sedan en analys utifrån resultaten.

####1.2 Projektets genomförande

Från början var jag orolig för att jag skulle behöva krångla mycket med ramverket, med Pico, SASS och npm – det kändes inte som att jag hade fått så bra grepp om det i kursen, men jag verkar ha fått bättre koll på det än vad jag trodde, och de bitarna löste sig snabbt.

Överlag rullade projektet på som jag ville, men jag märker att designen tagit mycket mer tid i anspråk än jag ursprungligen hade tänkt. Det tog mig t.ex. mycket längre tid än jag trodde att få min grid att fungera som jag ville. Just kombinationen av grid, flex och responsivitet var den stora utmaningen programmeringsmässigt. För att få koll på det behövs en del trial and error, och jag lärde mig mycket under projektets gång. Med hjälp av guider från dbwebb.se, MDN och w3schools löste det sig till slut.

Ett självförvållat “problem” tidsmässigt var att jag tyckte projektet var så roligt att jag möjligen la ner orimligt mycket tid på att redigera bilder i Gimp och att ändra smådetaljer i sidans utseende. Jag fotade till och med en gammal dator och disketter för att få exakt rätt bilder till webbplatsen. Saker som kanske inte nödvändigtvis påverkar betyget. Å andra sidan var mitt mål med kursen att lära sig bra design, så tiden var kanske ändå värt det.

Som ett av de optionella kraven valde jag att analysera laddningstid och användbarhet. Uppgiften gick bra, men krävde att jag tänkte till för att förstå samband mellan hur webbplatsen ser ut och vilka resultat det ger i Googles verktyg. Sammantaget gick uppgiften ganska smidigt att lösa.

Jag uppskattade verkligen projektet och ser det som en väldigt bra examinationsform. Man får använda de kunskaper man fått i kursen, vilket både är bra repetition och ett sätt att kolla att man faktiskt fått med sig det man ville från kursen.


####1.3 Tankar om kursen

Kursen gav en hel del aha-upplevelser designmässigt, och jag känner att jag tagit med mig en del. Till en början kändes det ganska tungrott att lära sig flera olika tekniker och ramverk på samma gång, och samtidigt försöka lära sig bra design, men jag gissar på att t.ex. Pico eller liknande ramverk kan förekomma ute i arbetslivet och är bra att kunna.

Jag förstår poängen med att utgå från en redan fungerande webbplats, så att man kan fokusera på designaspekter istället för kodande, men på ett sätt hade det också varit skönt börja helt från scratch, och slippa kastas in i kod som någon annan skrivit.

Kursboken var bra, och jag gillade att den hade en ganska lättsam stil och språk, och visade på många exempel. Även handledningen har jag varit nöjd med, även om jag inte sett till att utnyttja den särskilt mycket. Om någon skulle vilja lära sig om design inom ramen för webbprogrammering skulle jag absolut kunna rekommendera kursen. Mitt betyg för kursen är 7 av 10.
