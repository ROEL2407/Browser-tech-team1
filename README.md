# Team Dikdik

## Inhoudsopgave
- [Team Dikdik](#team-dikdik)
  - [Inhoudsopgave](#inhoudsopgave)
  - [Opdracht 2](#opdracht-2)
    - [1. Afbeeldingen (door Farrahton)](#1-afbeeldingen-door-farrahton)
    - [2. Custom fonts (door Marloes)](#2-custom-fonts-door-marloes)
    - [3. Kleur & kleurenblindheid (door Marloes)](#3-kleur--kleurenblindheid-door-marloes)
    - [4. Muis/trackpad (door Roel)](#4-muistrackpad-door-roel)
    - [5. Breedband internet uitzetten (door Roel)](#5-breedband-internet-uitzetten-door-roel)
    - [6. JavaScript (door Farrahton)](#6-javascript-door-farrahton)
    - [7. Cookies (door Lisanne)](#7-cookies-door-lisanne)
    - [8. localStorage (door Lisanne)](#8-localstorage-door-lisanne)
    - [B. Ad blockers (door Jorn)](#b-ad-blockers-door-jorn)
    - [C. Browser detect (door Jorn)](#c-browser-detect-door-jorn)

## Opdracht 2
De website die wij hebben onderzocht is https://www.vegan-store.eu.

### 1. Afbeeldingen (door Farrahton)
In Chrome ga je naar preferences -> security & settings -> site setting -> content -> images 

Nu de foto's eenmaal uit staan, ziet de website er als volgt uit. Opvallend is dat de productafbeeldingen lazy worden geload en een styling hebben die de 'placeholder' voor een ongevonden foto wazig maakt. De foto bovenin de navigatiebalk heeft wel de 'placeholder'. 
<img src="https://user-images.githubusercontent.com/92303930/159916272-66a80e3f-d919-443e-9b63-e046779f25b0.png">

Hieruit kunnen we opmerken dat ze geen ALT-tekst hebben toegevoegd, terwijl ze wel een alt tag hebben. 
<img width="1228" alt="altTag" src="https://user-images.githubusercontent.com/92303930/159916367-9c604698-26d9-4a7e-ba7d-0434d017498b.png">

### 2. Custom fonts (door Marloes)
Het probleem met custom fonts zijn dat deze soms niet geladen worden of dat de gebruiker ervoor kiest om deze niet te gebruiken.
Via uBlock origin, dit is een adblocker die ook extra functionaliteiten heeft zoals het uitzetten van JavaScript of grote media bloken te blokkeren. via uBlock origin kan je externe lettertypes blokkeren, de website veranderd verder niet dus ze maken geen gebruik van externe letertypes. Een optie om dit op te lossen zou zijn om altijd een fallback font te gebruiken die de meeste browsers kent.

De zoekbalk en winkelmandje maken gebruik van een icon font. Zodra dit font er niet is het icoon niet meer zichtbaar, er blijft nog wel plek voor deze iconen gereserveerd door een vierkant. Echter wordt deze niet opgevuld met een fallback waardoor je nu als gebruiker niet weet wat er hoort te staan.

Ervoor

<img width="250" alt="Met iconen" src="https://user-images.githubusercontent.com/24413936/159945711-e6315fa7-fee2-43a9-b8a8-e14c0e62bf3d.png">

Erna

<img width="250" alt="Zonder iconen" src="https://user-images.githubusercontent.com/24413936/159945896-84ad259b-9c74-43db-930d-2093410ff88d.png">

### 3. Kleur & kleurenblindheid (door Marloes)
Via de instellingen van je Mac kan je kiezen voor grijswaarden om zo geen kleuren te zien, de website is al erg zwart wit en hierdoor is deze zonder kleur ook prima te gebruiken.

<img width="720" alt="Zwart wit website" src="https://user-images.githubusercontent.com/24413936/159946373-b5fad3b0-630d-4e0e-a178-8166e13a3420.png">

De website is wit met zwarte tekst waardoor het voor iedereen leesbaar is. Via een contrast checker kan je zien dat het contrast bij een aantal elementen niet goed genoeg is zoals bij de tekst in de button en het jaar in de footer.

Contrast button

<img width="250" alt="contrastknop" src="https://user-images.githubusercontent.com/24413936/159946515-d8d3cb7c-e6c2-4f9b-a181-9d47f5512667.png">


Contrast jaar in footer

<img width="250" alt="contrastjaar" src="https://user-images.githubusercontent.com/24413936/159946531-66395e0d-0ee1-42f3-bfbb-d67d10bdf17a.png">

Met de contrast checker kan je ook meteen kijken hoe de website eruit ziet voor iemand die kleurenblind is. Met deze extensie aan ben ik door de site heen gegaan. 
De roze accenten veranderen wel van kleur maar de iconen blijven leesbaar.


<img width="343" alt="Contrast checker" src="https://user-images.githubusercontent.com/24413936/159946711-332c492a-1293-460f-a399-e11ce528f383.png">


<img width="720" alt="Kleurenblind" src="https://user-images.githubusercontent.com/24413936/159946771-86285012-22b5-476e-8add-3ac5637ccdfa.png">


### 4. Muis/trackpad (door Roel)
Bij mensen die geen muis of trackpad kunnen gebruiken kan je denken aan mensen met cognitieve problemen, fysieke problemen en mensen met problemen met de zintuigen. 
Hierbij kan je bijvoorbeeld denken aan blinde mensen.

In mijn ervaring bij de website gaat het door de pagina heen tabben niet goed. Ik heb hiervoor gekozen om bij de login pagina te gaan tabben. Allereerst begin je gelijk bij het loginform. Hierna krijg je een aantal set tabs die niet zichtbaar zijn.
Daarna ga je langs de bovenste header. In deze header staat een language preference die uitklapt, hier tab je overigens niet door heen als je terug tabt. Focus state is voor sommige dingen wel anders vormgegeven dus hier kan een kleine verwarring van ontstaan.

Als je enige tijd door tabt kom je bij de forgot password en signup links. Deze had ik persoonlijk bij het formulier zelf verwacht. 

Je zou dit laatste probleem kunnen oplossen door de links binnen de form in de HTML te zetten of ten minste deze eronder.

Hulpbron: [https://www.abilitynet.org.uk/factsheets/keyboard-and-mouse-alternatives-and-adaptations](https://www.abilitynet.org.uk/factsheets/keyboard-and-mouse-alternatives-and-adaptations)

### 5. Breedband internet uitzetten (door Roel)
Door middel van throttling binnen de chrome browser heb ik getest hoe de ervaring is op een langzame 3g verbinding.

Dit kan je doen door de volgende stappen te volgen:
Inspecteren > netwerk > dropdown waar standaard geen throttling in staat

Hierbij zie ik geen erge fouten. De website wordt ingeladen, enkele blokken verschijnen eerst over elkaar maar dat wordt later opgelost. Afbeeldingen worden ook na de tekst pas ingeladen en worden eerst als onscherpe afbeelding ingeladen waarna deze scherper wordt.

Je zou rekening kunnen houden met mensen die reizen, bijvoorbeeld die reizen met de trein. Deze wifi is niet geheel sterk en ook open dus er kunnen extra problemen hiermee doorkomen zoals het aantal gebruikers op de verbinding. In mijn is dit een probleem die verschilt per situatie. 

In mijn ogen zijn zullen de verschillen tussen landen zonder (100%) 4G en tijdelijke problemen niet heel veel verschillen met elkaar. De pagina laadt namelijk goed in op zowel langzaam als snel 3G.

<img src="https://user-images.githubusercontent.com/90243819/159915105-53e3f3fc-0e94-4d3c-bc76-c08a21c06b90.png">

### 6. JavaScript (door Farrahton)

In Chrome ga je naar preferences -> security & settings -> site setting -> content -> JavaScript

Opmerkelijk is dat in combinatie met het uitzetten van de afbeeldingen, er niets meer in de plaats komt van de afbeeldingen. Het is dan helemaal leeg. 
<img width="1223" alt="geenImages+Java" src="https://user-images.githubusercontent.com/92303930/159916618-77c0c167-6d14-492d-9c57-ffd5afc94d9e.png">


Alleen JavaScript uitzetten zorgt voor een resultaat waarin de doorklik carousel niet meer werkt en de productfoto's daardoor allemaal onder elkaar staan. 
<img width="1227" alt="javaUit" src="https://user-images.githubusercontent.com/92303930/159916673-ba971349-fc99-43f8-aeef-f1329bcc8fbf.png">


Je kan zonder JavaScript nog wel klikken op de dropdown menu linkjes en doorverwezen worden naar een nieuwe path. Echter, als je daar aankomt is de pagina helemaal leeg op de navigatie balk en de footer na.
<img width="1280" alt="navMenShoes" src="https://user-images.githubusercontent.com/92303930/159916733-47f6f6d9-1700-49c5-98cb-96c72e0c191c.png">

Hetzelfde geldt voor de zoekbalk. Er komen geen resultaten uit. 
<img width="1280" alt="zoeken" src="https://user-images.githubusercontent.com/92303930/159916786-e9027e17-6e8c-4382-b14d-0604c551f8d1.png">


Je kan nog op login klikken en het formulier invullen en submitten, maar eenmaal op de volgende pagina is de Captcha gebroken. Je kan niet laten weten dat je geen robot bent en kan daarom niet met de submit knop doorgaan. 
<img width="1280" alt="captcha" src="https://user-images.githubusercontent.com/92303930/159916838-f1021d2c-bd82-4df1-83b4-5913c3615f23.png">

De taal veranderen kan ook niet meer. 
Het is ook nog mogelijk om de betaalvaluta te veranderen. 
Informatie die volgt na het klikken op help doet het nog wel. 

Helaas als je een bestelling wilt volgen heb je weer pech, want alleen de path in de url verandert. Er komt geen informatie in beeld, zoals met JavaScript wel gebeurd.
<img width="1224" alt="orderTrack" src="https://user-images.githubusercontent.com/92303930/159916903-dc86aa94-3bad-443a-a9f1-3bfae22b4216.png">
<img width="1222" alt="orderWelGetracked" src="https://user-images.githubusercontent.com/92303930/159916933-90dbf3cc-84d7-480c-9f32-42748f59ca95.png">

Op basis van deze ervaring je je kunnen afvragen waarom iemand überhaupt JavaScript uit zou zetten. Aangezien het doel van bijvorbeeld deze webshop niet meer te bereiken is. Daarom zet ik even de voor- en nadelen van JavaScript uitschakelen op een rijtje. 

Voordelen van uitschakelen. 

* Beveiliging: het grootste probleem met JavaScript zijn verdachte webpagina's. Bovendien kunnen clientbrowsers schadelijke code invoegen die rechtstreeks van invloed is op jouw computer.

* Browserondersteuning: niet elke browser is in staat om JavaScript effectief uit te voeren, omdat elke browser de code anders interpreteert. Dit kan leiden tot inconsistenties als het gaat om functionaliteit en de interface.

* Door de programmeertaal uit te schakelen, zorg je ervoor dat jouw browser pagina's nauwkeurig kan lezen en laden, zeker als je graag oudere websites bezoekt.

* Uitgeschakelde plug-ins en cookies: een belangrijk punt van zorg voor veel computergebruikers is dat bedrijven internetgebruik kunnen volgen en die gegevens vervolgens aan andere bedrijven kunnen verkopen. Wanneer JavaScript is uitgeschakeld, werken veel van de cookies die verantwoordelijk zijn voor het bewaken van jouw persoonlijke gebruikersinformatie niet meer. Dit vermindert hoeveel bedrijven jouw kunnen volgen en verbetert zeker de gemoedsrust voor de gemiddelde gebruiker.

Bron: https://anonymania.com/disabling-javascript-browser-cons-pros/#disabling-pros

Nadelen van uitschakelen

* Verwarrende presentatie: een nadeel van het uitschakelen van JavaScript is dat alle snelkoppelingen, opsommingstekens en andere organiserende informatie verdwijnen. Dit kan webpagina's verwarrend of moeilijk leesbaar maken.

* Minder toegang tot media: een ander probleem is dat u de toegang tot de afbeeldingen, video's, kaarten en afbeeldingen op webpagina's kunt verliezen, wat mogelijk de toegang tot en de zichtbaarheid van media beperkt.

* Minder wendbaarheid: JavaScript vernieuwt websites en zoekopdrachten altijd om het gemakkelijker te maken om door de informatie te bladeren. Als het eenmaal is uitgeschakeld, moet je door tonnen "Volgende" -links bladeren om afbeeldingen of inhoud te zien.


### 7. Cookies (door Lisanne)
Op de voorpagina komt er een pop-up in beeld, die met cookies in één klik te verbergen is. Zonder cookies blijft de pop-up een keer of vijf terugkomen, voordat het verdwijnt. Als de pagina herladen wordt, verschijnt de pop-up weer, evenals de "Visiting from outside Europe?" pop-up.

![](https://user-images.githubusercontent.com/90243819/159908306-3bb654cf-a9d1-4882-9be3-4f2b2d0437aa.png)

Op de pagina waarop klanten kunnen inloggen, kom ik erachter dat het probleem met de pop-up websitebreed is. Na de inloggegevens te hebben ingevuld en te hebben geklikt op "Login", kom ik op een 404 Not Found pagina. Na een seconde verschijnt de pop-up uiteraard weer (niet te zien in de screenshot).

![](https://user-images.githubusercontent.com/90243819/159909533-3dde424d-5689-4ef0-a82f-7c866f16cfac.png)

Na het aanzetten van de cookies en het inloggen op de website, zijn de onderstaande cookies aangemaakt voor het domein https://www.vegan-store.eu.

![](https://user-images.githubusercontent.com/90243819/159912493-5ca97dcc-363c-4cbd-ac98-18e32aa4723c.png)

### 8. localStorage (door Lisanne)
Omdat localStorage alleen uitgeschakeld kan worden samen met de cookies, is het niet mogelijk om erachter te komen wat er zou gebeuren als enkel de localStorage uitstaat. Het pop-up probleem lijkt enkel te liggen aan de cookies, omdat er in de localStorage geen data staat die hier invloed op zou kunnen hebben. Het niet kunnen inloggen zou hier wel te maken mee kunnen hebben, omdat mijn e-mailadres in de key "swym-authn" staat.

![](https://user-images.githubusercontent.com/90243819/159914159-7d35bd9a-7907-4abe-9a6a-4e0dbfee50c6.png)



### B. Ad blockers (door Jorn)
<img width="317" alt="Schermafbeelding 2022-03-24 om 23 08 06" src="https://user-images.githubusercontent.com/74248007/160018507-4c7926d5-60a7-451c-8549-9851010180bb.png">

Ad blockers zijn steeds populairder. 42,7% van de internet gebruikers wereldwijd zeggen een ad blocker te gebruiken. Deze ad blockers blokkeren automatisch advertentie sectie's op sites, maar ook facebook trackers en andere analytics. Dit gebeurt voordat deze geladen kunnen worden op een site, erg handig dus qua privacy en performance. Een site wordt namelijk aanzienlijk sneller als het niet alle advertenties en trackers hoeft te laden.

Naast het verliezen van een (soms) belangrijke inkomsten bron die advertenties de websites brengen, zijn er nog andere nadelen.

Er zit een nadeel in de statistieken van je site, omdat adblockers de trackers voor deze statistieken blokkeren. Dit geeft dus een vertekend beeld van je statistieken.

<img width="884" alt="Schermafbeelding 2022-03-24 om 23 07 55" src="https://user-images.githubusercontent.com/74248007/160018683-2aa8538c-5247-438f-bb57-aad23ecc832f.png">

Een ander nadeel is dat het kan zijn dat het adblockers filter systeem per ongeluk delen van je site ziet als advertenties en deze onterecht volledig weghaalt van je site. Dit is vooral iets om op te letten bij e-commerce sites. Deze sites bevatten namelijk producten met product beschrijvingen en call to actions die verkeerd geanalyseerd kunnen worden door de adblockers.

Dit kan er voor zorgen dat de bezoeker van de site bepaalde items niet ziet. Het grote nadeel hiervan is dat de bezoeker van een site niet door heeft wat een adblocker weghaalt, want ... het is weg. 

Als web developer kun je hier rekening mee houden door:
- Pop-ups te vermijden 
- Veel testen 
- Aan elementen die weggehaald worden duidelijk maken dat het geen advertenties zijn.

*Bronnen:* 

[https://www.ionos.com/digitalguide/websites/web-design/adblockers-impact-on-web-development/](https://www.ionos.com/digitalguide/websites/web-design/adblockers-impact-on-web-development/)

[https://backlinko.com/ad-blockers-users](https://backlinko.com/ad-blockers-users)


### C. Browser detect (door Jorn)
Browser detect of ook wel Browser sniffing wordt gebruikt om te achterhalen welke browser wordt gebruikt door de bezoeker van je site. Dit zou je kunnen gebruiken om speciale styling te laten zien, informatie te verzamelen over je bezoekers of om te checken of de browser een bepaalde feature support.

Welke browser gebruikt wordt kun je (in theorie) achterhalen door te kijken naar de 'User agent string'. Deze string wordt meegegeven in de HTTP Headers.

<img width="70%" alt="Schema HTTP Header User Agent" src="https://user-images.githubusercontent.com/74248007/159980616-e6d28ad5-f02a-40e1-83e2-3a1b64c74bca.png">

Er zitten alleen een hoop haken en ogen aan Browser sniffing:

1. Als je je code aanpast op specifieke browsers kan je site niet makkelijk aangepast worden en zal hij wellicht breken wanneer er een nieuwe browser gereleased wordt. Niet erg fijn te onderhouden dus.

2. Browser Opera deed onderzoek naar browser sniffing en zegt dat het sommige browser blokkeerden van sites, terwijl deze prima zouden functioneren. 

3. Browser willen helemaal niet gedetecteerd kunnen worden. De user agent string kan dan ook makkelijk worden veranderd in veel browsers. Zo geeft mijn eigen Chrome een string mee met bijna alle browser namen:

<img width="375" alt="User Agent Jorn" src="https://user-images.githubusercontent.com/74248007/159980577-9d7ab1a9-e5e4-43a4-95bb-05854433787c.png">

4. Als je dan eenmaal tóch een browser gedetecteerd hebt, kan het nog steeds zo zijn dat dit een hele oude versie is van de browser. Zo weet je dus nog niet of een feature wel of niet wordt ondersteund.

*Oplossingen en alternatieven* hiervoor zijn:
- [Progressive enhancement](https://roel2407.github.io/Browser-tech-team1/) 
- [Feature detection](https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Cross_browser_testing/Feature_detection) ipv. browser detection


*Bronnen:*

[https://medium.com/@markevan100/browser-sniffing-with-user-agent-is-it-always-bad-a420c172ea06](https://medium.com/@markevan100/browser-sniffing-with-user-agent-is-it-always-bad-a420c172ea06)

[https://developer.mozilla.org/en-US/docs/Web/HTTP/Browser_detection_using_the_user_agent](https://developer.mozilla.org/en-US/docs/Web/HTTP/Browser_detection_using_the_user_agent)

[https://www.sitepoint.com/why-browser-sniffing-stinks/](https://www.sitepoint.com/why-browser-sniffing-stinks/)

[https://dev.opera.com/blog/perils-browser-sniffing/](https://dev.opera.com/blog/perils-browser-sniffing/)
