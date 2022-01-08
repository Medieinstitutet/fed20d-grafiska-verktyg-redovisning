# 👏 Feedback
Hej, här kommer feedback till alla grupper! Jag tänker att det är nyttigt att också ta del av andras feedback, så därför kommer den samlad.

**Har jag missat att säga att något** ni/du har gjort är bra, som jag kommenterat på någon annans projekt, så ta till dig av det. Samma sak, om det finns förbättringspotential i något, som ett annat projekt fått kommentarer på, men du/ni kanske inte tänkt på.

- [ ] Ett tips är att samla på sig en egen "[launch checklist](https://www.websitelaunchchecklist.com/)", t.ex. som ett privat repo på GitHub, där man går igenom sådant som är bra att tänka på inför en lansering av ett projekt. t.ex. dubbelkolla färgkontraster, aria labels, SEO, osv. Det är omöjligt att hålla allt i huvudet.

## 😡 Generell feedback
Några vanliga issues, som nästan uteslutande alla projekt har haft problem med (lägg till på era launch checklists).

### Font size i en tillgänglig enhet
[Sätt gärna font-size i en tillgänglig enhet](https://css-tricks.com/is-it-better-to-use-ems-rems-than-px-for-font-size/), såsom `rem` eller `em` istället för `px`. [Använd en smidig Sass-funktion](https://gist.github.com/garystorey/5920051), så slipper man tänka mer på det :) Mer om rem nedan 👇

> In most browsers, a user can set their default browser font-size to be a different size to the default (typically 16px). If the user sets their default to 20px, all font-sizes should scale accordingly.
> However, if the website explicitly sets font-sizes in pixels, a heading set at 30px will always be 30px. That might sound great from a designer/developer point of view - but you’re not the user, stop making websites for yourself.
> Thankfully, setting font-sizes in pixels doesn’t completely ruin accessibility. The user can still zoom in and out with ctrl plus +/- (cmd instead of ctrl on OS X). However, we can do better. [Källa](https://engageinteractive.co.uk/blog/em-vs-rem-vs-px)

### Sätt width och height på bilder
Bilder skulle kunna ha attributen `width` & `height` för att påskynda sidladdningen och [undvika layout shift](https://www.smashingmagazine.com/2020/03/setting-height-width-images-important-again/).

### Använd normalize.css
Använd gärna [normalize.css](https://necolas.github.io/normalize.css/) för att få sidorna att se enhetliga ut i samtliga webbläsare.

### gitignore
Lägg till `.DS_STORE` (och andra systemfiler) i `.gitignore`, de behövs inte i repot.
Det gäller också t.ex. `.map`-filer som genereras för CSS.

### Lägg till en README
Lägg gärna in en README på projektet, särskilt om ni planerar att visa det för t.ex. framtida arbetsgivare. Ser snyggare ut!

[Inspo](https://readme.so/)

## 🦄 Projekt-baserad feedback

- [hers.](#hers)
- [Save the Bees](#Save-the-Bees)
- [Ge Blod](#Ge-Blod)
- [Blue Recycle](#Blue-Recycle)
- [Santa's workshop](#Santas-workshop)
- [Red Bull](#Red-Bull)
- [Poké Queen](#Poké-Queen)
- [Circus Citrus](#Circus-Citrus)
- [Årets Glöggsmaker](#Årets-Glöggsmaker)
- [Raptor](#Raptor)
- [Fiskarium](#Fiskarium)
- [Breakfast Club](#Breakfast-Club)

### hers
[Live](https://kimmiich.github.io/Mathildas-webshop/) | [Repo](https://github.com/Kimmiich/Mathildas-webshop)

#### 🤗 Grymt jobbat med…

- SEO-aspekten av sidan, t.ex. meta-taggen, title, länkar, rubriker, semantiska element.
- Följt best practices och framför allt när det gäller tillgänglighet. Exempelvis semantiska element, använt `ul` för att skapa en navigation.
- Sidan fungerar bra responsivt, och inte ens i små upplösningar försvinner någon text.
- Knappar får en `cursor: pointer;` som gör det tydligt att det är en knapp, även för personer som använder mus.
- Snyggt med den avklippta produktkarusellen!
- Ingen overflow-x på sidan (side scroll)
- Bra README som förklarar uppgiften och även länkar tydligt till designern liksom live-sidan.
- Tydliga och små "commits"
- Bra och tydligt strukturuppdelning av koden i mappar. Lätt att läsa, hitta och pluspoäng för [innehållsförteckningen i style.scss](https://github.com/Kimmiich/Mathildas-webshop/blob/main/scss/style.scss) liksom namngivningen av variabler.
- Bra att du lagt till en favicon!

#### 🤔 Förbättringspotential:

- Hover-effekten på menyikonerna gör att det blir lite väl blekt/transparent, utifrån ett tillgänglighetsperspektiv.
- Bra val av HTML-element på sidan, då sidan går att tabba sig igenom. Produktkarusellen saknar tabb-möjlighet, men i och med att detta är en "prototyp" så spelar det ingen roll.
- Detalj: $-symbolen brukar stå före priset, medan "kr" ofta står efter priset.
- Bilderna bör minskas rejält i storlek. Det skulle snabba på laddningstiden på sidan. T.ex. är [bakgrundsbilden 8 MB](https://github.com/Kimmiich/Mathildas-webshop/blob/main/imgs/background.png), vilket är mycket, framför allt på en långsam mobiluppkoppling. Hela sidan är nu nästan 14 MB. Eftersträva (för onepagers) någonstans mellan 1-2 MB, om det går. Spara t.ex. bilder i `JPG`-format, så blir det hårdare komprimerat (kvalitet 8 i Photoshop brukar räcka), än `PNG`.
- Login-knappens kontrastvärde på texten är inte tillräcklig utifrån ett tillgänglighetsperspektiv.
- Hjärtat och varukorgen har inte beskrivande text, för den som navigerar utan att se.
- Rubrikerna är inte i en logisk ordning, från h1 --> h6.
- Meny-knappen hade kunnat vara ett annat element än en `div`. Den går nu inte att tabba till med tangentbordet i mobilläget.
- [Sätt font-size i en tillgänglig enhet](#font-size-i-en-tillgänglig-enhet)
- [Sätt width & height på bilder](#sätt-width-och-height-på-bilder)

### Save the Bees
[Live](https://cutlasskiwi.github.io/save-the-bees/) | [Repo](https://github.com/tovebratt/save-the-bees)

#### 🤗 Grymt jobbat med…
- Performance på sidan, den är snabbladdad på under 1 sekund!
- Många SVG-bilder, bra.
- Kul att ni jobbat i samma repo som själva designen/projektet var i!
- Bra med olika bilder för olika upplösningar 👍 
- 100 i score på tillgänglighet i den automatiska checkern - mycket bra, men det finns en del issues att ta itu med.
- Texten får alltid plats på sidan, även i små fönsterstorlekar och generellt skalar sidan riktigt bra. I vissa lägen ser det dock ut som att "mitten-biet" får lite konstiga proportioner (sätt bara `width`, och `height: auto;`), och ibland lägger sig bakgrundsbilden under sista biet. Bakgrundsbilden hade kanske behövt vara en separat container som haft `position: absolute; top: 0; right: 0px;` för att hänga med i alla tänkbara upplösningar.
- Grymt resultat, _särskilt_ med tanke på att ni bara var två!

#### 🤔 Förbättringspotential…
- Vissa bilder skulle gå att skala ner i storlek ytterligare, typ [hero-tablet.png](https://github.com/tovebratt/save-the-bees/blob/main/img/tablet/hero-tablet.png).
- Hela sidans "laddningsstorlek" är nu nästan 11 MB, så försök att dra ner bilderna så mycket som möjligt i storlek.
- [Undvik mellanslag i filnamn](https://github.com/tovebratt/save-the-bees/blob/main/img/tablet/Bees%20Flying%20Around%20Beehive.png), så att det är "web safe" med namngivningen.
- [Lägg till `.DS_STORE` i `.gitignore`](#gitignore)
- [Sätt width & height på bilder](#sätt-width-och-height-på-bilder)
- Minifiera gärna CSS:en & använd Sass för att förenkla denna process.
- Cookie-banner skulle kunna ha `position: fixed` så att den hänger med även om man scrollar.
- Klickabara element (knappar, länkar, bilder) skulle kunna ha `cursor: pointer,` för att förtydliga interaktionen.
- Meta saknas i header för SEO.
- Typsnittet är fel på sektionen med bilder/text (ej bin).
- Använd ett element som går att navigera till, när ni skapar en meny, typ en `button` istället för `div`, eller sätt åtminstone `tabindex="0"` på div:en, så den blir tillgänglig :) Det går t.ex. inte att öppna menyn i mobilen med tangentbordet.
- Beskriv gärna bilderna i alt-texten, och håll er till ett språk. Nu är det blandat med "rädda bina logga" och "Icon for bee-app"
- Använd gärna semantiska element, typ `footer` och `header`, liksom en `nav` och `ul` för att bygga menyn.
- [Sätt font-size i en tillgänglig enhet](#font-size-i-en-tillgänglig-enhet)

### Ge Blod
[Live](https://mathildap.github.io/GEBLOD/) | [Repo](https://github.com/Mathildap/GEBLOD)

#### 🤗 Grymt jobbat med…
- Performance på sidan!! "Time to interactive" är 0,5 s vilket är fantastiskt bra! Således också bra med bildkomprimeringen.
- Vissa knappar har `cursor: pointer;`, bra!
- Ingen overflow-x scroll, bra!
- Responsiviteten på sidan funkar kanon!
- Kul att du lagt in en animation på hjärtat, det ger sidan lite extra känsla!
- Bra jobbat med local storage & cookies, skönt att slippa den varje gång sidan öppnas. Tydlig JavaScript-kod som är lätt att läsa.
- Tydlig struktur på Sass-filen!
- Bra små commits.


#### 🤔 Förbättringspotential…
- Det finns en del tillgänglighetsissues på sidan, t.ex. kontrasten mellan text- och bakgrundsfärg, och formulärens input-fält saknar labels. Det är också lite otydligt var någonstans jag befinner mig på sidan, om jag tabbar igenom den. Menyn går inte heller att öppna med hjälp av tangentbordet i mobilläget.
- Bilder skulle kunna ha attributen width & height för att påskynda sidladdningen och undvika layout shift.
- Meta-taggar skulle kunna läggas till för SEO.
- Gör menyknappen till ett interaktivt element istället för en div.
- Använd semantiska taggar i hela dokumentet - du har ju bevisligen koll på dessa! Och lägg t.ex. menyn inuti en `nav` för tydlighet :)
- [Lägg till `.DS_STORE` i `.gitignore`](#gitignore)

### Blue Recycle
[Live](https://smaristeinar.github.io/blue-recycle/) | [Repo](https://github.com/smaristeinar/blue-recycle)

#### 🤗 Grymt jobbat med…
- Time to interactive på 0,4 s, mycket bra! Användarna gillar. Däremot är laddningstiden för bilderna långsam. Krymp jeans1.png från ≈ 9 MB till någonting mindre, och spara som en JPG med kvalitet 8 så får ni upp sidans hastighet ytterligare.
- Snyggt implementerad design, och att ni fixat det med CSS i stor utsträckning.
- SÅ BRA att mobilmenyn går att öppna med tangentbordet 👏 
- Också tydligt var jag är, om jag tabbar igenom sidan.
- Toppen att ni använt rätt `type` på input-element.
- Bra att ni använt Sass, men minifiera också [output-CSS-filen](https://github.com/smaristeinar/blue-recycle/blob/main/style.css) för maximal prestandaoptimering :)
- Bra projektstruktur över lag.


#### 🤔 Förbättringspotential…
- Se till så att texten har en fallback-font medan webfonten laddas, så att det finns text på sidan om font load skulle misslyckas.
- [Sätt width & height på bilder](#sätt-width-och-height-på-bilder)
- Sidans totala storlek är 9 MB, det kan ni dra ner (och räcker nästan med att få ner bakgrundsbilden i storlek, då den i sig är 9 MB).
- Tillgänglighet: dubbelkolla kontrasten på textfärgen mot bakgrundsfärgen, och se till att form-element har labels.
- Fick en security warning på sidan, för att ett typsnitt inte laddas över HTTPS.
- Lägg till meta-taggar för SEO.
- I små upplösningar får texten inte plats på sidan. Förvisso ett extremfall, men värt att ha i åtanke. Sätt en `min-height` för att komma runt problemet.
- Skriv bättre commit-meddelanden än "Update script.js" och "fix", så slipper man leta i historiken om något har blivit fel.
- Ur ett SEO-perspektiv, fundera på om det hade gått att använda text och/eller ha en fallback till SVG-bilderna, för sökmotorerna kommer inte kunna läsa av innehållet i en bild ännu, på ett tag. Så att ha texten tillgänglig på sidan, skulle vara ett lyft.
- Lite [inkonsekvent](https://github.com/smaristeinar/blue-recycle/blob/c712eb44526cbbf2191e7cd863ff722db5c775f7/index.html#L65) kodstil stundtals, t.ex. dubbelfnutt och enkelfnutt. Välj en stil.
- "[Image that says](https://github.com/smaristeinar/blue-recycle/blob/c712eb44526cbbf2191e7cd863ff722db5c775f7/index.html#L67)" är onödig för skärmläsare i alt-texten, stryk och behåll sista delen. De flesta kommer läsa upp "Image: alt-texten", så "Image: Image that says Join our newsletter" blir kaka på kaka.
- [HTML kan inte samtidigt vara ett XML-dokument](https://github.com/smaristeinar/blue-recycle/blob/c712eb44526cbbf2191e7cd863ff722db5c775f7/index.html#L89), så ta bort det om ni lägger in en SVG-bild direkt i HTML-koden.
- [Varifrån kommer denna font](https://github.com/smaristeinar/blue-recycle/blob/c712eb44526cbbf2191e7cd863ff722db5c775f7/style.css#L9)? Tror ev. Microsoft blockar resursanvändningen på externa sidor 🤔 
- En del bilder ligger i roten på projektet, andra i img-mappen.

<img width="1344" alt="image" src="https://user-images.githubusercontent.com/18628999/148645263-7a8f750f-b570-45e9-a6d1-ef6ce3dfaef5.png">

### Santa's workshop
[Live](https://tonihalmetoja.github.io/santas-workshop/) | [Repo](https://github.com/ToniHalmetoja/santas-workshop)

#### 🤗 Grymt jobbat med…
- Time to interactive är 0,6 s - mycket bra! 👏 
- Bilderna är hårt komprimerade och sidan således också snabbladdad, toppen!
- Det går att tabba sig igenom sidan och det är tydligt (fram till slutet) var någonstans jag är på sidan.
- Kul att ni provat Tailwind i projektet! 👍 
- Responsiviteten på sidan funkar kanon!
- Så roligt med ljudet & animationen, jag dör 😂 Made my day!
- Bra alt-texter (👏 ), även om det är lite svenska och lite engelska.

#### 🤔 Förbättringspotential…
- Se till att det finns en fallback-font medan webfonten laddas, så att texten är synlig.
- [Sätt width & height på bilder](#sätt-width-och-height-på-bilder)
- Kontrast mellan text och bakgrund är inte alltid tillräcklig utifrån ett tillgänglighetsperspektiv; våga ifrågasätta/ändra designerns färgval så att det blir det.
- Menyn går inte att öppna med tangentbordet i mobil-läget.
- Glöm inte att lägga till meta-taggar för att opta för SEO.
- [Lägg till `.DS_STORE` i `.gitignore`](#gitignore)
- [Undvik mellanslag i filnamn](https://github.com/ToniHalmetoja/santas-workshop/blob/main/public/Buffalo%20Plaid%20Christmas%20Tree.svg) för säkerhets skull!
- Rensa bort mergade branches, och döp till något vettigare än `margins` och `margins-2` 😂 

#### 💭  Vet inte vilken åsikt jag ska ha
- Kanske hade sett en mer detaljerad mappstruktur med separata mappar för bilder, om projektet hade växt (vilket det ofta gör i verkligheten, så kanske en bra vana). Däremot var ju detta scope begränsat.

### Red Bull
[Live](https://gabriellekamph.github.io/tootsie-rolls/) | [Repo](https://github.com/gabriellekamph/tootsie-rolls)

#### 🤗 Grymt jobbat med…
- Så bra med laddningstiden på sidan!
- Bra att knapparna har `cursor: pointer;`
- Riktigt bra responsivitet på sidan, och inget sidroscrollande.
- [Bra kommentar i CSS:en om färgändringen](https://github.com/gabriellekamph/tootsie-rolls/blob/f2c43eaaee05b65753271ef4400b1e00a19d6036/style.css#L12), riktigt snyggt och väldokumenterat för framtiden 👍 
- Bra och tydlig struktur i CSS:en. Bra användning av variabler och kommentarer.
- Toppen med menyn som går att öppna med tangentbordet.
- Bra semantiska taggar och best practice. Tydlig kod.

#### 🤔 Förbättringspotential…
- Saknar en README i repot, även om ni satt det skulle finnas en 😭 
- [Sätt width & height på bilder](#sätt-width-och-height-på-bilder)
- Hittills har jag mest kommenterat att bilder ska bli mindre, men här kan jag tycka att bakgrundsbilden är aningens för hårt komprimerad (den första med Red Bull), den är något oskarp på min skärm.
- Bilder saknar alt-attribut. Om det är en dekorativ bild, lämna attributets värde tomt.
- Lägg till meta-taggar på sidan för ökad SEO.
- Menyn går inte att öppna med tangentbordet.
- Ingredienslistan sitter ganska tight till vänster på skärmen, kanske mer padding?
- [Sätt font-size i en tillgänglig enhet](#font-size-i-en-tillgänglig-enhet)
- [Sätt en "timeout"-funktion i resize](https://github.com/gabriellekamph/tootsie-rolls/blob/f2c43eaaee05b65753271ef4400b1e00a19d6036/index.js#L23), annars byts bilden ut kontinuerligt. Så att den istället byts ut när timeouten är klar, t.ex. efter 500 ms.
- [Lägg till `.DS_STORE` i `.gitignore`](#gitignore)

💭 Vet inte vilken åsikt jag ska ha
- Ingredienslistans "chevron neråt"-ikon är förvirrande, för det händer inget vid klick. Oavsett om det är ett designbeslut eller kod-beslut; ta bort så slipper det bli förvirrande.
- Kort-elementen i "burkens kretslopp" har en pointer-pekare, men inget händer vid klick. Future-proof, eller bara förvirrande?

<img width="1900" alt="image" src="https://user-images.githubusercontent.com/18628999/148646379-aa0dd003-5cd1-4259-9089-0c4fea9b2281.png">

### Poké Queen
[Live](https://nifty-blackwell-8beed5.netlify.app/) | [Repo](https://github.com/rebecka-oscarsson/lollipop)

#### 🤗 Grymt jobbat med…
- Knapparna med rätt sorts cursor på sidan
- Rolig (om än något störig, efter 2 min) animation med pilen
- Snabbladdad sida - wow! 0.3 s, mycket bra! Hårt komprimerade bilder utan att storleken/kvaliteten påverkas.
- SEO & tillgänglighet, ➕  för att mobilmenyn går att öppna med tangentbordet.
- Responsiviteten på sidan! 👍  Mycket bra.
- Bra och tydlig readme.
- [GitRules](https://github.com/rebecka-oscarsson/lollipop/blob/main/LillipopGitRules.md) 🤩 
- Användning av normalize.css & prettier
- Bra mappstruktur, tydlig komponentuppdelning & lätt att hitta i koden för den oinvigde - skulle vara enkelt att ta över om det behövdes.
- Tydlig och konsekvent kod.
- Bra commit messages (för det mesta), tydligt vad som hänt i vilken commit 👌 
- Imponerad av användningen av issues, även om ni har massor så verkar inget ha fallit mellan stolarna.

#### 🤔 Förbättringspotential…
- Vid hover på knapparna så blir färgkontrasten alldeles för blek.
- Precis vid breakpointen mellan tablet och mobil så blir det side-scroll på sidan, för att texten inte riktigt får plats på sidan där de tre bowlsen presenteras.
- [Sätt font-size i en tillgänglig enhet](#font-size-i-en-tillgänglig-enhet)

### Circus Citrus
[Live](https://rebeckaalsterlind.github.io/circus_citrus/) | [Repo](https://github.com/rebeckaalsterlind/circus_citrus)

#### 🤗 Grymt jobbat med…
- Sidan är snabbladdad, time to interactive är 0.5 s! Mycket bra 💪 
- Tangentbordsnavigation funkar, inkl. öppna & stänga menyn
- Knappar har `cursor: pointer;`
- Gillar den subtila blob-animationen som knappt är märkbar, men något litet händer på sidan.
- Responsiviteten funkar & ingen side-scroll på sidan. Även när skärmen är pytte på höjden, så funkar menyn. Kanon!
- Bra readme
- Bra användning av semantiska taggar
- Bra att även fotografen creddats i alt-texten! 📸 
- Tydlig kod- och projektstruktur.
- ➕  för 404-sidan
- Bra med komprimerad CSS-kod för optad laddning
- [BRA namngivning av bild](https://github.com/rebeckaalsterlind/circus_citrus/blob/main/dist/img/man-in-red-coat-on-stage-mark-williams-unsplash.jpg).


#### 🤔 Förbättringspotential…
- Färgkontrasten är inte tillräcklig i cookie-bannern på själva texten (och den följer inte designen för den med bakgrundsfärg 😉 )
- Headings är i fel ordning och meny-knappen saknar en [aria label](https://web.dev/button-name)
- [Lägg till `.DS_STORE` i `.gitignore`](#gitignore)
- Dessa filer gör ingen nytta i ["other"-mappen](https://github.com/rebeckaalsterlind/circus_citrus/tree/main/dist/other), ta bort. Syftet med samtliga ([humans](https://www.google.com/humans.txt), [robots](https://developers.google.com/search/docs/advanced/robots/intro)) är att ligga direkt under roten på det publicerade projektet.

### Årets Glöggsmaker
[Live](https://brave-turing-b1d1be.netlify.app/) | [Repo](https://github.com/MatsHaby/GV_Design-Sprint)

#### 🤗 Grymt jobbat med…
- Bra med SEO-aspekten
- Fint med menyanimationen!
- Bra projektstruktur och mappstruktur, tydlig uppdelning i komponenter; lätt för någon annan att jobba vidare om det skulle behövas.
- Bra användning av semantiska element
- Tydlig uppdelning av koden i komponentfilerna, lätt att läsa och följa med i den.
- Bra använding av "git flow"-principer i branches.
- ➕  för snyggt [commit-meddelande](https://github.com/MatsHaby/GV_Design-Sprint/commit/107231fe7987e7306ff7f10b6092357864aee301) med bra beskriving, väldigt tydligt snabbt vad som ingår i det.
- Bra användning av [issues](https://github.com/MatsHaby/GV_Design-Sprint/issues?q=is%3Aissue+is%3Aclosed) & uppdelning i projektet. Lätt att [se historiken](https://github.com/MatsHaby/GV_Design-Sprint/pulls?q=is%3Apr+is%3Aclosed).

#### 🤔 Förbättringspotential…
- Byt title & favicon på sidan från "React App" till "Glögga", eller motsv.
- Saknar en README i själva repot.
- Time to interactive var på 2 s, vilket är lite på gränsen för en snabbladdad sida (3 brukar sägas vara max).
- Dra ner filstorleken på bilder. Om en bild aldrig visas bredare än 300 px t.ex., så finns det ingen anledning att serva den i storleken 4696 px eller 3 MB :)
- [Sätt width & height på bilder](#sätt-width-och-height-på-bilder)
- Sidan har lite side-scroll. Går det inte att få bort annars, sätt t.ex. `max-width: 100%; overflow-x: hidden;` på `body`
- Dubbelkolla så även menyn går att öppna med tangentbordet i mobilläget.
- Det är lite overflow och overlap i responsiviteten. Ett tips är att inte sätta `height` på elementet, utan låta text- och innehållsmängden styra. Behövs det en viss höjd (t.ex. för den röda ribbon-grejen), så sätt hellre `min-height`, så slipper ni problemet med överflödet.
- Responsiviteten på sidan hade behövt en "touch-up" och lite mer kärlek :)
- [Lägg till `.DS_STORE` i `.gitignore`](#gitignore)
- Använd rätt "type" [på input-fält](https://github.com/MatsHaby/GV_Design-Sprint/blob/5bb6dd31b11157a0ad14cbd11ecf48e74d622255/design/src/components/Form.jsx#L19) för att underlätta för användare

<img width="1079" alt="image" src="https://user-images.githubusercontent.com/18628999/148647656-0fc76c1c-854f-4a3b-8168-223a2eba09f7.png">

### Raptor
[Live](https://ant1n.github.io/Chupa-Chups/) | [Repo](https://github.com/Ant1N/Chupa-Chups)

#### 🤗 Grymt jobbat med…
- Time to interactive är 0,7 s, mycket bra 👏 
- Roligt med roterande R:et (även om lite av det försvinner utanför viewboxen) :) Bra att animationen upprepas vid resize av sidan, om man skulle råkat missa den.
- På det stora hela funkar responsiviteten bra, några "minor glitches" (se nedan) men det tar inte ifrån helhetsintrycket ändå. Bra t.ex. att stora bilden (hero) får plats även om skärmhöjden är smal!
- Plus för tillgängliga font-storlekar med em/rem.
- Tydlig CSS-kod!
- Bra att ni fått in en video!
- Bra med aria labels! 👏 
- Bra commit-meddelanden mestadels!


#### 🤔 Förbättringspotential…
- [Sätt width & height på bilder](#sätt-width-och-height-på-bilder)
- Sätt labels till form-element för att bättra på tillgängligheten ytterligare
- Lägg till meta-taggar för att maxa SEO
- Jag har svårt att komma åt menyalternativen med tangentbordet. Sätt i alla fall `tabindex` på den & en keyboard listener, men helst även ett semantiskt korrekt element, typ `button`.
- Cookie-popupen hade kanske behövt ha `position: fixed` för att inte hamna så långt ner på sidan, även om det hade varit ett drömscenario att slippa dessa. Även texten i själva knappen hade kunnat vara centrerad i desktop-läget 🤔 
- Menyalternativen överlappar logotypen i vissa skärmbredder.
- Saknar `cursor: pointer;` på knappar och t.ex. menyn.
- I CSS:en hade ni haft nytta av fler kommentarer för att "bryta ner" det i sektioner som är lättare att hitta, och av en linter för att hålla en konsekvent kodstil. Ni hade också vunnit lite prestanda på att baka ihop CSS-filerna till en, istället för att ladda in 3 st, eller åtminstone [sätta media queryn då på själva link-taggen](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-blocking-css).
- Sätt rätt "type" på [input-element,](https://github.com/Ant1N/Chupa-Chups/blob/8be28a5d9082367e1ba79596562e5adb8eb1a7b1/index.html#L144) t.ex. "email" för bästa användarupplevelse.
- En tydligare README & länk till projektet, saknar det :)

### Fiskarium
[Live](https://aahland.github.io/fiskarium/) | [Repo](https://github.com/aahland/fiskarium)

#### 🤗 Grymt jobbat med…
- Performance score, mycket bra!
- Gillar också att sidan inte blir ultra-bred, utan att innehållet håller sig läsvänligt även på en enormt bred skärm.
- Bra och roligt med blubben från fisken 😍 
- Bra med `cursor: pointer;` på knapparna.
- Bra responsivitet på sidan, även om jag tycker att bakgrunden/innehållet hade kunnat gå hela vägen ut på de mindre storlekarna. Nu ser det lite konstigt ut då det inte är "design man är van vid".
- Fint att animationen hänger med i det responsiva läget!
- Härligt att slippa hamburgarmenyn i mobilen för en gångs skull!
- Snyggt skriven CSS, även om filen är mastig med sina 1248 rader, så kanske dela upp den i mindre komponenter för att lättare hålla koll på vad man ska rota och ändra.
- Bra med den komprimerade CSS-koden!
- Bra semantiska taggar!
- Bra commit-meddelanden, och bra användning av issues.


#### 🤔 Förbättringspotential…
- Lägg gärna in en README på projektet, särskilt om ni planerar att visa det för t.ex. framtida arbetsgivare. Ser snyggare ut!
- [Sätt width & height på bilder](#sätt-width-och-height-på-bilder)
- Eftersom att sidan har en blå färg, hade kanske focus color vid tabbning behövt vara en annan än webbläsarens default (ofta blå). Det hade räckt med en generisk regel, typ `:focus { outline: 3px solid yellow; }` för hela dokumentet.
- Se över några tillgänglighetsaspekter, t.ex.: input-element bör ha en label, kontrasten mellan text och bakgrund och vissa element har ett tabindex högre än 0.
- Lägg till meta för att förbättra SEO.
- [Sätt font-size i en tillgänglig enhet](#font-size-i-en-tillgänglig-enhet)

En mycket mega-petig detalj, men [följande rad](https://github.com/aahland/fiskarium/blob/8a2a4829f6f85c0282f29b52fffddb2bc4499885/index.html#L151) hade kunnat ändras till:
```
if (cookie.style.display !== "none")
```
För om någon ändrar från `grid` till t.ex. `flex` eller `block` så slutar JavaScriptet fungera :) Så future-proofing-tips bara!

### Breakfast Club
[Live](https://jgammelli.github.io/Breakfastclub/) | [Repo](https://github.com/JGammelli/Breakfastclub)

#### 🤗 Grymt jobbat med…
- Bra performance score på 0,5 s! 👏 
- Roliga animationer, som ändå inte är för påträngande.
- Bra jobbat med SEO!
- Bra att musen indikerar att knapparna är klickbara (cursor: pointer)
- Fin design!
- Bra alt-texter, och användning av semantiska taggar.
- Bra att du använt Sass! Du behöver dock inte importera variablerna i varje fil, eftersom att du gör det en gång i själva huvudfilen :)
- Bra projekt- och mappstruktur. Bra commit-meddelanden, och bra projekt, särskilt bra då du jobbade själv!

#### 🤔 Förbättringspotential…
- Om det går att dra ner storleken på PNG-bilderna från 1,7 MB, så överväg det, särskilt om det går att bibehålla kvaliteten. Ibland är det svårt, men värt ett försök. Hela sidan är nästan 9 MB, så en del bilder kan nog vara värt att dra ner i storlek, om det går.
- [Sätt width & height på bilder](#sätt-width-och-height-på-bilder)
- På något enstaka ställe var kontrasten mellan bakgrund & text inte tillräcklig utifrån ett tillgänglighetsperspektiv.
- Menytexten är megaliten i mobilvyn och det går inte att zooma in sidan. eller i alla fall så skalas ingenting upp (typ texten) 😱 
- En del innehåll får inte alltid plats i vissa fönsterstorlekar, och/eller täcks av andra element.
- Sätt font-storleken i `rem` eller `em`. Nu är den i `vw` vilket gör att det inte går att skala upp (eller ner) texten, om jag skulle ha behov av det. Se [Sätt font-size i en tillgänglig enhet](#font-size-i-en-tillgänglig-enhet)
- Den slutgiltiga CSS-filen skulle kunna ha output-style compressed, för att spara ytterligare lite storlek :)
