Vejledning i brug af FDAprofil-pakken
======

Følgende forudsætter at du har installeret Sparx Enterprise Architect, hentet FDAprofil Sparx EA-pakken og konfigureret Sparx EA med FDAprofil-MDG-teknologien. Illustrationer her passer til Sparx EA version 13, men der gives instruktioner til både version 13, 14 og 16. 

Vejledningen indeholder 4 dele:
1.	Trin-for-trin vejledning til modellering med MDG-teknologien
2.	Trin-for-trin vejledning til import af data fra begrebslisteskabelon
3.	Vejledning til brug af dialogboks-udvidelsen
4.	Vejledning til brug af Vocabulary Tools-udvidelsen

# 1) Trin-for-trin vejledning til modellering med MDG-teknologien
Følg disse trin for at oprette en ny projektfil 

Version 13:
* Klik New File i fanen "start page"
* Angiv filnavn
* Klik Gem

Version 14 og 16:
* Klik på Sparx-logoet øverst til højre
* Klik New Project…
* Angiv filnavn og placering 
* Klik Gem

## Opret modelprojekt (med Model Wizard)
Følg disse trin for at oprette en samlet projektpakke med forskellige FDA-modelskabeloner

Version 13:
* Klik Design
* Klik Model Wizard
* Klik Others (under Technology)
* Sæt flueben "FDAprofil (UML): Opret samlet FDAprofilpakke"

Version 14:
* Klik Design
* Klik på pilen ved Insert ▼
* Vælg Insert Using Model Wizard
* Scroll ned til FDAprofilen
* Vælg "FDAprofil (UML): Opret samlet FDAprofilpakke"
* Klik Create Pattern(s)
* Luk evt Model Wizard

Version 16
* Klik Design
* Klik Model Wizard
* Scroll ned til FDAprofilen og klik derpå
* Vælg "FDAprofil (UML): Opret samlet FDAprofilpakke"
* Klik Create Model(s)

(Der oprettes en ny skabelonpakke med vejledningsdiagram og to forskellige modeltyper)

Uanset om du anvender projektskabelonen eller opretter et nyt projekt, anbefales det at ekstrafunktionerne (rapportskabeloner, importspecifikationer og scripts) importeres i projektet. Se vejledning nedenfor.

## Importér ekstrafunktioner som referencedata i projektet (anbefales):
Version 13 og 14:
1.	Klik CONFIGURE | Transfer | Import Reference Data
2.	Klik Select File og vælg <a
href="https://github.com/digst/model-rules-tool-support/blob/master/sparx-ea-fdapackage/referencedata.xml">Referencedata.xml-filen</a> fra FDAprofil-pakken.
3.	Vælg begge dataset: Automation Scripts og CSV (Vælg flere ved at holde Ctrl nede)
4.	Klik på Import og funktionerne er nu tilgængelige

Version 16
1. 	Klik Settings | Transfer | Import Reference Data
2. 	Klik Select File og vælg <a
href="https://github.com/digst/model-rules-tool-support/blob/master/sparx-ea-fdapackage/referencedata.xml">Referencedata.xml-filen</a> fra FDAprofil-pakken.
3. 	Vælg begge dataset: Automation Scripts og CSV (Vælg flere ved at holde Ctrl nede)
4.	Klik på Import og funktionerne er nu tilgængelige
   
Nu er du klar til at tilføje modelelementer og angive metadata

## Tilføj modelelementer og tilføj metadata (tags)
1.	Dobbeltklik på modeldiagrammet og træk elementer og relationer fra værktøjskassen til diagrammet 
2.	Udfyld de nødvendige tags på elementerne (klasser, associationsender, attributter, og objekter). <br>
	1.	I version 13 og 14: Klik på det pågældende element og udfyld de relevante tag values i ‘Tagged Values’-vinduet <br>
	2.	I version 16: Klik på det pågældende element og udfyld de relevante tag values i ‘Properties’-vinduet under fanen Elements, hvor tag values findes under Concept-fanen <br>	 	
3.	Udfyld de nødvendige tags på modellen (pakken). Klik på den pågældende pakke og udfyld de relevante tag values i ‘Tagged Values’-vinduet (i v.16 under Properties-Elements-Concept som ved forrige trin). <br>
Har du installeret FDAprofil-dialogboks-tilføjelsen anvender man blot genvejen Ctrl+Q for at åbne en mere brugervenlig dialogboks til indtastning af tagged values.

Har man hverken installeret FDAprofil Workspace-layoutet eller FDA-profildialogboksen
skal man dobbeltklikke på elementet/modellen for at tilføje indhold til taggene. Her findes de under fanen FDAprofil.

## Udskriv modelrapport vha. rapportskabeloner
Version 13 & 14:
1)	Tryk på F8
2)	I valglisten Generate angiv filplacering under ”Output to File” (Klik ”…”)
3)	Åbn valglisten Template (i v. 16: Templates)
4)	Dobbeltklik på den relevante rapportskabelon (Eks. FDAprofil Begrebsliste under Technology Templates/User Templates)

## Udskriv HTML-modelrapport
Denne metode danner et HTML-dokument der viser metadata for modellen og dens elementer. Der indgår ikke diagrammer, så disse bør vedlægges seperat. Rapporten udskriver udelukkede felter der er udfyldte. Den kræver at stereotyperne 'Modelelement' eller 'Concept' fra FDA-profilen er anvendt. Fordelen ift. at anvende rapportskabeloner er at tomme felter ikke udskrives, hvilket øger rapportens læsevenlighed.

Version 13:
1)	Højreklik på pakken (modellen) i Project Browser
2)	Vælg Import/Export og vælg Export package to xmi…
3)	 Klik på Publish
		under XML Type: vælg UML 2.5 (XMI 2.5.1)
		under Stylesheet: vælg FDA-Modelrapport-HTML
4)	Angiv filnavn (af typen .html) og placering
5)	Klik Export

Version 16:
1)	Klik på pakken (modellen) i Project Browser
2)	Klik på fanen Publish | Publish As...
   		under XML Type: vælg UML 2.5 (XMI 2.5.1)
  		under Stylesheet: vælg FDA-Modelrapport-HTML
4)	Angiv filnavn (af typen .html) og placering
5)	Klik Export
	
### Udskriv diagrammer til billedfiler

1)	Åben diagrammet
2)	Klik på fanen Publish
3)	Klik Save Image (i v. 16: Save) | Save to File
4)	Angiv filnavn og placering 
5)	Klik Gem
 
## Eksporter UML-model (til xmi-format)
Følg disse trin for at eksportere en UML-model (til xmi-format)

Version 13:
1)	Højreklik på pakken (modellen) i Project Browser
2)	Vælg Import/Export og vælg Export package to xmi…
3)	Klik på Publish og vælg UML 2.5 (XMI 2.5.1)
4)	Angiv filnavn og placering
5)	Klik Export

Version 14:
1)	Vælg pakken (modellen) i Project Browser
2)	Klik Publish|Export XMI|Export XMI for Current Package
3)	Klik på Publish og vælg UML 2.5 (XMI 2.5.1)
4)	Angiv filnavn og placering
5)	Klik Export

Version 16:
1)	Klik på pakken (modellen) i Project Browser
2)	Klik på fanen Publish | Publish As...
   		under XML Type: vælg UML 2.5 (XMI 2.5.1)
4)	Angiv filnavn og placering
5)	Klik Export

## Importer UML-model (i xmi-format)
Følg disse trin for at importere en UML-model (i xmi-format) til et eksisterende EA-projekt

Version 13:
1)	Højreklik på den pakke i Project Browser vinduet, som du gerne vil have modellen placeret i.
2)	Klik på Import Model from xmi…
3)	Naviger hen til den pågældende xmi-fil der skal importeres (ud for Filename)
4)	(sæt evt. flueben i Strip GUIDs – hvis root node fejlbesked forekommer)
5)	Klik på Import

Version 14:
1)	Klik Publish|Import XMI|Import Model XMI
2)	Vælg placering af modellen (ud for Package)
3)	Naviger hen til den pågældende xmi-fil der skal importeres (ud for Filename)
4)	(sæt evt. flueben i Strip GUIDs – hvis root node fejlbesked forekommer)
5)	Klik på Import

Version 16:
1)	Klik Publish|Import XMI|Import XMI File
2)	Vælg placering af modellen (ud for Package)
3)	Naviger hen til den pågældende xmi-fil der skal importeres (ud for Filename)
4)	(sæt evt. flueben i Strip GUIDs – hvis root node fejlbesked forekommer)
5)	Klik på Import

## Genbrug modelelementer
Følg disse trin for at genbruge et eller flere elementer fra en importeret UML-model
1.	Naviger hen til den relevante model (pakke) i Project Browseren der skal genbruges fra
2.	Marker den eller de klasser der skal genbruges i Project Browseren
3.	Højreklik på de valgte elementer og vælg: 

Version 13:
Copy / Paste > Paste Element(s) from Clipboard 

Version 16
Copy to Clipboard > Full Structure for Duplication 

Elementet duplikeres og kan genbruges til en bestemt anvendelse, men identifikatoren (URIen) gør det muligt at opnå sporbarhed på tværs af organisationer og anvendte modelleringsværktøjer.

## Masseopdatering af elementer
Man kan tilføje yderligere funktionalitet til Sparx Enterprise Architect ved at importere en fil med funktioner der kan masseopdatere modellens indhold og deres tilhørende tags, dvs. klasser, objekter, attributter og associationsender.

Herefter har man flere muligheder:
* Kopier UML-navn til prefLabel (da) - Copy UML name to prefLabel (da)
* Kopier UML-navn til prefLabel (en) - Copy UML name to prefLabel (en)
* Kopier Alias til prefLabel (da)  - Copy UML Alias to prefLabel (da)
* Kopier Alias til prefLabel (en)  - Copy UML Alias to prefLabel (en)
* Kopier Notes til definition (da) - Copy UML Notes to definition (da) 
* Kopier Notes til definition (en) - Copy UML Notes to definition (en) 
* Kopier tags fra ét element til et andet -Copy tags from one element to another
* Generer identifikatorer og tildel præfikses -: Autofill URI and assign prefixes 
* Autoudfyld subClassOf-tag: - Autofill subClassOf-tag

Sådan anvendes masseopdateringsfunktionerne:
1)	Højreklik på den relevante model (som skal have en stereotype fra Plusprofilen)
2)	Vælg <BR>  a)	I EA 13: menupunktet Scripts <BR>  b)	I EA 14: Specialize|Scripts <BR>
4)	Klik på det relevante script og elementerne opdateres
 
# 2) Vejledning til csv-import af begrebsliste til Sparx Enterprise Architect
Følgende vejledning forudsætter at Projektskabelonen anvendes, eller at du har tilknyttet MDG-teknologien og referencedata til dit projekt. 
Anvend skabelon til csv-import. Indholdet af Begrebsliste DA eller Begrebsliste DA+EN kopieres med copy+paste ind i skabelonen. Det er ok, hvis der er felter der er uudfyldte og/eller det kun er den danske del (og den sprogneutrale proveniensdel) der er udfyldte.  Evt. uudfyldte rækker slettes dog, da de eller bliver til elementer (uden) data i Sparx EA.
Begrebslisten skalt gemmes i en fil af typen CSV (semikolonsepareret), som skal have UTF-8 kodning for at de danske specialtegn ‘æøå’ kan bibeholdes. Da regnearksprogrammer (oftest) ikke kan gemme i denne kodning, er det være nødvendigt at ændre kodning i en teksteditor.

Bruger du Microsoft Excel (version 2010) gør du det således:
1.	Klik Filer
2.	Klik Gem som..
3.	Vælg filtype CSV (semikolonsepareret) (*.csv) (OBS Excel kan gemme i tre forskellige .csv-formater, vælg semikolonsepareret)
4.	Klik Gem (og efterfølgende Ja i dialogboksen)

Dernæst gør du følgende i Notesblok (eller anden plain text-editor):
1.	Åbn den gemte csv-fil i Notesblok (under "Programmer | Tilbehør i Startmenuen)
2.	Vælg Gem som… og klik valglisten “Kodning” nederst i dialogboksen og vælg UTF-8. 
3.	Giv filen et nyt navn

Til sidst gør du følgende i Sparx EA (version 13 & 14):
1.	Åbn projektskabelonen
2.	Vælg den pakke hvortil begreberne skal importeres i Project Browseren
3.	Klik PUBLISH | CSV
4.	Klik CSV Import/Export
5.	Ved Specification vælg den begrebslisteskabelon du bruger, fx Begrebslisteskabelon_v0.10.0
6.	Ved file vælg den gemte csv-fil (i UFT8-formatet)
7.	Klik Run og begreberne importeres som klasser i modellen

Bemærk at der vil optræde to 'kendte fejl', som skyldes at overskrifterne ikke fjernes, men dette har ingen betydningen for importen
 
# 3) Vejledning til brug af FDAprofil-dialogboksudvidelsen
Dialogboksen giver mere brugervenlig dialogboks til indtastning af tagged values for modeller og modelelementer. Se evt. Vejledning til konfigurering af Sparx Enterprise Architect med FDAprofil-pakken for information om hvordan du installerer dialogboksen.
 
Der er to udgaver af dialogboksen. De indeholder begge de samme felter og giver mulighed for redigering af samme data. Den ene version, som ses ovenfor, anvender danske betegnelser for felterne, svarende til dem der er anvendt i Begrebslisteskabelonen. Den anden anvender standardiserede UML-tags, som også anvendes internationalt. Disse betegnelser er på engelsk. <BR>  
Aktivering af dialogboksen:

Dialogboksen kan aktiveres på to måder. I begge tilfælde skal du markere relevante pakke eller modelelement, dernæst kan du enten:
* bruge genvejstaster: Ctrl+R for den danske version, Ctrl+Q for den engelske, eller
* bruge menubåndet foroven og klikke Extend (v 14: Specialize) | Plusprofil Editing Window og vælge Open Danish Editing Window eller Open English Editing Window, som vist nedenfor
 
Bemærk: Vi anbefaler at du kun har en instans af Sparx EA åben når du bruger dialogboksen, da den kan opføre sig uforudsigeligt ved flere instanser. 
 
# 4) Vejledning til brug af Plusprofil-Vocabulary Tools- udvidelsen
Ved anvendelse af Vocabulary Tools udvidelsen kan man:
* Importere en OWL/RDF fil
* Eksportere et vokabular på niveau 3 til en OWL/RDF Fil
* Tilføje en værktøjskasse med en oversigt over samtlige genbrugelige RDF elementer
* Aktivere en RDF-guide oprettelse og genbrug af egenskaber (datatype- og objektegenskaber)

Disse funktioner kan tilgås ved at 
1.	Højreklikke på en model, 
2.	Vælge menupunktet
      1.	EA 13: Extensions
      2.	EA 14: Specialize
3.	Vælge Vocabulary Tools og den relevante funktion

(Nærmere vejledning til brug af de forskellige funktioner herunder følger)

(N.B. Det er også muligt at aktivere funktionerne via den øverste højre fane med navnet ’Extend’)
'Vocabulary Tools' funktionaliteten har sine begrænsninger ift. de mange forskellige måder hvorpå et vokabular kan udtrykkes i RDF/XML på, men de fleste internationale vokabularer kan importeres. Det anbefales at at lade importfilen validere af W3Cs RDF Validator for at udelukke eventuelle mangler i inputfilen. Ift. eksport skal man angive prefix, namespace og navn for de vokabularer man eventuelt importerer/anvender i sin model i et notesfelt på diagrammet, da eksportfunktionaliteten anvender disse til genereringen af RDF/XML'en. Derfor bør vokabularskabelon-pakken anvendes, da der her ligger et eksempel på hvorledes noten skal struktureres.
 
