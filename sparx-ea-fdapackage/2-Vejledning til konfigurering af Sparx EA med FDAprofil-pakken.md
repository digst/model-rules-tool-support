Konfigurering af Sparx Enterprise Architect med FDAprofil-pakken
=======

Følgende forudsætter at Sparx EA version 13 er installeret på maskinen . Se evt. Vejledning til installation af Sparx Enterprise Architect via Statens IT eller køb det på http://www.sparxsystems.eu/. Desuden forudsættes at du har hentet FDAprofil Sparx EA-pakken.

# Trin-for-trin konfigurering af Sparx EA med MDG-teknologi 
Sådan konfigurerer du Sparx Enterprise Architect med MDG-teknologi samt anbefalede indstillinger

## Aktivering af MDG-teknologi (fjern evt. tidligere version først - se note) 
1.	Åbn Sparx Enterprise Architect (Luk evt. startmenu)
2.	Åbn menuen for MDG Technolgies
      1.	I version 13: Klik CONFIGURE | Manage Technology | Advanced...
      2.	I version 14: Klik Manage (under SPECIALIZE | Technologies) | Advanced
      3.    I version 15: Klik Manage-Tech (under SPECIALIZE | Technologies) | Advanced
3.	Klik Add  
4.	Vælg Add URL...
5.	Indsæt denne sti: https://data.gov.dk/tool/SparxMDG/FDAprofil-MDG.xml  
6.	Klik Ok (Og tjek at FDAprofil MDG-teknologien nu har fået et flueben i oversigten)
7.	Klik OK og teknologien aktiveres

NOTE: MDG-filer gemmes lokalt på maskinen her (og kan slettes manuelt herfra også): C:\Users\BRUGERNAVN\AppData\Roaming\Sparx Systems\EA\MDGTechnologies

## Deaktivér MDG-teknologier som ikke anvendes (anbefales):
1.	Åbn menuen for MDG Technologies
      1.	I version 13: Klik CONFIGURE | Manage Technology | Advanced...
      2.	I version 14: Klik Manage (under SPECIALIZE | Technologies) | Advanced
2.	Klik None og sæt et flueben ud for teknologierne FDAprofil,  samt evt. Basic UML 2 Technology og andre teknologier der anvendes 
3.	Klik OK

Nu er opsætningen af MDGen fuldført. 

Den tilhørende referencedatafil skal importeres specifik til hvert projekt.
Se derudover eventuelt dokumentet Tips og tricks til UML-modellering i Sparx Enterprise Architect:
https://docs.google.com/document/d/14oSR_QnLja8LuUbpsNE2FnV-22CK-TzNG1xqwIlp6Jo/edit?usp=sharing
 
# Import af stylesheet til HTML-modelrapport
1. Hent stylesheet ([FDA-Modelrapport-HTML.xsl](https://github.com/digst/model-rules-tool-support/blob/master/sparx-ea-fdapackage/FDA-Modelrapport-HTML.xsl)) fra dette repositorie
2. I Sparx: Find Resources-vinduet (ofte bag Project Browser, eller kan vælges Window-manue øverst til venstre)
3. Højreklik på Stylesheets
4. Vælg Import Stylesheet og finde den hentede .xsl-fil
5. Giv stylesheetet et sigende navn, fx FDA-Modelrapport-HTML (den angivne max-grænse på 12 tegn kan godt overskrides)

Stylesheet er nu tilgengængligt i forbindelse med eksport af xmi-filer. Se mere i Vejledning til brug af FDAprofil-pakken i Sparx EA.

# Trin-for-trin installation/afinstallation af Plusprofil-dialogboksen:

## Vejledning til installation af dialogboks
1.	Afinstaller evt. tidligere versioner af Plus/FDAprofil-dialogboksen – se separat vejledning herunder
2.	Dobbeltklik på dialogboks-filen. (Windows kan finde på at give en advarsel fordi udgiveren er ukendt - det betyder ikke at der er noget galt med filen)
3.	Klik på Kør. Læs licensaftalen og sæt flueben ud for ’I accept the terms in the License Agreement’ og Klik på Install
4.	Vent og tilføjelsen installeres…
  
## Vejledning til afinstallation af dialogboks
*	Åbn Kontrolpanelet/Control Panel  
*	Vælg”Fjern et program/Remove program”
*	Marker ”Enterprise architect – FDAprofil Add-In” på programlisten og klik ”Fjern/Uninstall”
 
N.B. Det er også muligt at fjerne dialogboks-tilføjelsen ved at slette .dll-filen direkte i AppData-mappen
C:\Users\BRUGERNAVN\AppData\Roaming\Sparx Systems\EA\MDGTechnologies


