---
Title: Om
Description: Om sidan
---

TEKNIKER BAKOM SIDAN
-----------
CSS-filen som styr sidans style genereras av preprocessorn Sass utifrån ett
antal moduler skrivna i CSS och SCSS. CSS-filen är en minifierad version som
därmed är lite mindre tung för browsern att läsa in.

Jag utgick från CSS-filen för grunddesignen (dbwebb), och skapade där först en
design som jag är nöjd med. Sedan gick jag igenom koden i CSS-filen och tog
bort eller slog samman överflödiga regler. Dessutom har jag utnyttjat SCSS-kod
för att göra koden tydligare och smidigare att underhålla.

Slutligen flyttade jag ut regler för typografi till en separat modul som heter
__typography.scss__.

För t.ex. färger som återkommer i flera olika element och klasser använder jag
__variabler__ som definieras i __variables.scss__. Det gör det lättare att
underhålla/ändra koden längre fram.

Ur mappen "shared" läser jag in SCSS-filer för FontAwesome-fonter (ikoner)
samt fonten Alata som jag laddat hem från Google. Övriga SCSS-filer
ligger i mappen för detta tema. Det kändes mest logiskt att göra så, innan jag
vet hur eventuella framtida teman kommer att kunna se ut.

Förutom ovan nämnda moduler läser jag även in en __normalize.css__ som
nollställer browserspecifika egenheter och gör designen mer förutsägbar.

__Nästlade regler__ är tillämpade där det varit möjligt, t.ex. för nav-,
fieldset-, footer- och header-elementen.
