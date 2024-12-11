---
Title: Load time
Description: This is a page about load.
template: analys
---

# Utvärdera webbplatsers laddningstid och användbarhet

I denna rapport analyseras och utvärderas webbplatsers laddningstid och användbarhet. Syftet med analysen är att mäta hur snabbt de laddas samt undersöka om de innehåller faktorer som kan förbättras kopplat till laddningstid och användbarhet.

## Urval

De tre webbplatser som har valts ut är XXL, Stadium och Intersport. Samtliga webbplatser hör till kategorin e-handel och verkar inom segmentet tränings- och sportprodukter.

Urvalet är intressant då e-handlar ofta är omfattande webbplatser som består av många sidor och produkter, mycket bilder och eventuella videos. Även en stor mängd script som behövs köras för att webbplatsen ska fungera.

Analysmaterialet har begränsats till webbplatsens startsida, landningssida för allt inom dam samt landningssida för kampanjer och erbjudanden. Delvis för att analysen inte ska blir för omfattande, men även för att få fler mätvärden att analysera.

## Metod

För att analysera en webbplats laddningstid används verktyget _DevTools_ och fliken _Network_ i Google Chrome, vilket ger mätvärden för laddningsprestanda. Mätvärdena visar hur resurser laddas på webbplatsen i realtid.

Finish är svår att läsa av och därför har mätvärdena _DOMContentLoaded_ och _Load_ används istället. DOMContentLoaded sker när HTML-dokumentet är färdigladdat och parsat och DOM är uppbyggt. Mätvärdet markerar hur snabbt användarna kan börja interagera med innehållet, även om sidan inte helt är klar. _Load_ sker när hela sidan inklusive alla externa resursers som bilder, CSS, script etc. är färdigladdat. Mätvärdet markerar när alla nödvändiga resurser som hör till sidans initiala rendering har laddats och mäter en tidpunkt när sidan anses ”klar” för användaren att använda.

För antalet resurser dokumenteras värdet på ”requests” och för sidans totala storlek värdet på ”transferred”. "Transferred" visar den totala mängden data som överförs från servern till webbläsaren och anses vara det mest korrekta värdet för den totala storleken.

När mätvärdena i _DevTool_ mäts görs en så kallad hard refresh av webbplatsen för att webbläsaren inte ska använda en cachad version. För en hard refresh används kommandot ”Shift+Option+R” (Mac).

För att analysera webbplatsens användbarhet används verktyget _PageSpeed Insights_ som analyserar prestanda på både mobile och stationära enheter. Verktyget genererar en prestandapoäng som baseras på laddningstider och användarupplevelse. Verktyget ger även specifika rekommendationer för förbättringar.

Samtliga mätvärden förs in i ett kalkylark i en tabell per webbplats och för mätvärdena i _DevTools_ används tre värden för samma mätvärde och sedan räknas snittet ut för mer pålitliga mätvärden att analysera. Kombinationen av de båda verktygen ger en översiktlig bild av webbplatsens prestanda och insikterna hjälper till att optimera webbplatserna.

## Resultat

<div class="embed-container">
	<iframe src="https://docs.google.com/spreadsheets/d/e/2PACX-1vTkED8nVkCTLk9hpJM5eOCMaSGzZJiXY8LZxAIAeOWBb4fO2eBUf5JI7vTJ9VuAD22beaDWtLb-DOna/pubhtml?gid=0&amp;single=true&amp;widget=true&amp;headers=false"></iframe>
</div>

### XXL Sports

![XXL](%assets_url%/img/xxl.png)

Prestandan når en poäng mellan 44-67 för desktop och 37-63 för mobile. Poängen är mycket låga för båda enheterna och har helt klart förbättringspotential.

Tillgängligheten ligger på mellan 83-92 för desktop och 85-92 för mobile, vilket ändå är relativt höga poäng då samtliga värden gränsar till 90 eller över. Självklart finns förbättringspotential även här, men det är mycket bättre poäng än prestanda.

Användningen av bästa metoder briljerar däremot med toppoäng 100 eller nära 100 på både desktop och mobile. SEO-optimeringen av webbplatsen får en genomgående poäng på 92, vilket är mycket bra men går att optimera ytterligare.

Ser vi till laddningstiderna varierar tiderna kraftigt mellan de olika försöken, webbplatsen är dock snabb på att konstruera DOM men tar betydligt längre tid på sig att ladda fullständiga resurser. Snittvärdet för antalet förfrågningar som skickas till servern är 202 stycken för startsidan och 110-125 stycken för undersidorna. Det stora antalet förfrågningar till servern kan mycket troligt hänga ihop med den långsamma laddningstiden samt låga poängen för prestandan.

De mest kritiska förbättringsåtgärdena för XXL's hemsida är att undvika ett onödigt stort DOM-träd, undvika stora layoutförskjutningar och optimera de script som används. Att reducera, optimera och minifiera de JavaScript som körs kommer att minska arbetsbelastningen på modertråden, minska tiden det tar för scripten att exekveras samt undvika att script som inte används tar onödiga resurser. Genom att använda bilder i rätt storlek och filformat, att kritiska bilder laddas in i förväg samt se till att alla bildelement har attributen height och width, kan vara det som krävs för att höja poängen för tillgängligheten.

### Stadium

![Stadium](%assets_url%/img/stadium.png)

Prestandan når en poäng mellan 91-93 för desktop och 57-73 för mobile. Prestandan för desktop är väl godkänd, medan prestandan för mobile är låg och kräver förbättringsarbete.

Tillgängligheten ligger på mellan 80-93 för desktop och 80-89 för mobile, vilket har förbättringspotential för båda enheterna men det är inte katastrof.

Användningen av bästa metoder ligger statiskt på 81 för desktop och 82 för mobile, vilket inte är dåligt men det finns helt klart optimeringsmöjlgiheter även här. SEO-optimeringen ligger på 92 för desktop och mobile får båda sidorna förutom kampanjsidan. 92 är en hög poäng och det visar att Stadium jobbar aktivt med SEO för att driva in trafik och nå bra plaeringar i sökresultaten.

Ser vi till laddningstiderna varierar tiderna även kraftigt mellan försöken och den genomsnittliga tiden tyder på att det tar väldigt lång tid att både att konstruera DOM samt ladda webbplatsens fullständiga resurser. Snittvärdet för antalet förfrågningar som görs till servern är 174 stycken för startsidan och 121-162 för stycken för undersidorna. Webbplatsens totala storlek på 2,8 MB för startsidan och hela 4,6 MB för landningssidan för dam i kombination med det stora antaler förfrågningar hänger troligt ihop med de långa laddningstiderna.

För Stadium’s webbplats påverkas laddningstiden mycket av att bildinläsningen blir förskjuten som i sin tur fördröjer tiden för den största uppritningen av innehåll. Detta fördröjer renderingen av hela webbplatsen. Andra optimeringar att göra är att rensa, optimera och minifiera JavaScript samt optimering av de bilder som används. Flera av bilderna är onödigt stora och kan med fördel anpassas när de läses in.

För att nå en högre poäng för tillgänglighet behöver länkar få title-attribut och vissa knappar saknar namn som kan tydas av skärmläsare. Kontrasten mellan Stadiums orangea färg i text mot vit bakgrund samt vit text mot exempelvis knappar i orange är för låg. Även klickytan för länkar på vissa element är för små och gör det svårt för användare att klicka.

### Intersport

![Intersport](%assets_url%/img/intersport.png)

Prestandan för desktop når en poäng på 37-76 och 37-65 för mobile, poängen är extremt låga för de båda enheterna.

Tillgängligheten är inte heller något att hurra för med en poäng på 77-87 för desktop och 84-92, med det är inte lika katastrofalt som prestandan. Poängen för användandet av bästa metoder ligger på 93-100 för båda desktop och mobile, vilket är mycket bra. SEO-optimeringen för Intersport når en poäng på 92-100 med övervägande mätvärden på 100.

Laddningstiderna överlag är jämnare mellan försöken men tiderna för både konstruktion av DOM och för att rendera alla resurser är inte jättesnabba. Antalet förfågningar som skickas till servern är 108-154 stycken bland sidorna med flest förfrågningar på startsidan.

Laddningstiden och prestandan på Intersport's webbplats påverkas av flera faktoren men det som ser ut att påverka allra mest är lång körningstid för JavaScript och stor arbetsbelastning på modertråden med ett ondödigt stort DOM-träd. Genom att använda anpassade bilder när det handlar om både storlek och filformat kan prestandad säkerligen förbättras, och sen ett optimeringsarbete för script- och stilfiler.

Poängen för tillgänglighet är redan höga men går att förbättra, bland annat genom att vissa länkar saknar title-attribut och en del knappar saknar namn som kan tydas av skärmläsare.

## Analys

Tittar man på resultaten för de tre webbplatserna upptäcks en rad gemensamma förbättringsåtgärder. Samtliga sidor har långa laddningstider, undermålig prestanda i stor utsträckning, många serverförfrågningar och omfattande DOM-träd. Detta hänger sannolikt ihop med att mitt urval består av e-handelssidor, som på grund av sitt innehåll, omfattning och funktioner ofta är tunga i både skript och filer. Dessa faktorer påverkar prestandan negativt, särskilt för mobila enheter. Det framgår tydligt i mätvärdena att prestandan generellt är bättre på desktop än på mobile, vilket är problematiskt då det minst borde vara tvärtom, med tanke på att majoriteten av användarna besöker via mobila enheter.

För att möta användarnas förväntningar och förbättra upplevelsen måste e-handelssidorna fokusera på att minska laddningstider, särskilt för mobila enheter. Här är XXL och Stadium bättre än Intersport, men alla tre behöver ytterligare optimering. Genom att reducera sidstorlek, minimera antalet serverförfrågningar och implementera bättre cachingstrategier kan samtliga sidor förbättra sin användarupplevelse och konverteringsgrad. Samtliga webbplatser visar bra resultat inom SEO, vilket är avgörande för synlighet i sökresultat och för att driva trafik till sidorna. Poängen för SEO ligger nära toppoäng på alla sidor och även toppoäng på vissa sidor, vilket är positivt och visar på att dessa webbplatser är väloptimerade för sökmotorer.

Tillgängligheten på webbplatserna är inte katastrofalt dålig, men det finns definitivt förbättringspotential för att nå toppoäng på både desktop och mobile. Särskilt i förhållande till de kommande kraven på tillgänglighetsanpassade webbplatser som träder i kraft 2025. Att genomföra dessa förbättringar skulle inte bara göra webbplatserna snabbare utan även mer tillgängliga och användarvänliga, vilket i sin tur kan leda till bättre kundupplevelse och ökad konvertering.

När det gäller laddningstider är Intersport generellt bäst, då den både klarar gränsvärdet för snabb laddning (under 500 ms) och de godkända nivåerna (under 1000 ms). Intersport har också lägst antal förfrågningar till servern med ungefär lika stor total storlek som XXL. Stadium har visserligen bäst prestanda men längre laddningstider och underkänns helt, medan XXL ligger nära underkänt med för höga snittvärden för både desktop och mobile. Laddningstider över 1000 ms räknas som långsamma och påverkar användarupplevelsen negativt, vilket tydligt framgår i resultaten. Ingen bör egentligen vinna, men "vinnaren" i detta minitest blir därför Intersport med snabbast laddad sida.
