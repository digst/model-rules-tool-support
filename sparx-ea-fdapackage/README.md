FDAprofil Sparx EA-pakke
=======

Modelsekretariatet har udviklet en FDAprofil-pakke af værktøjer der letter modellering efter Modelreglerne med Sparx Enterprise Architect. Pakken indeholder UML-profilen, der specificerer stereotyper og tags-definitioner.  Derudover tilpasses layout og indtastningsmuligheder, der tilføjes rapportskabeloner mm. Vi har udarbejdet 3 vejledninger til installation af Sparx EA samt til konfigurering med og brug af FDAprofil-pakken.

FDAprofil Sparx EA-pakken indholder 5 komponenter

1. Begrebslisteskabelon til csv-import (xlsx-fil)
2. MDG-teknologi (xml-fil) https://data.gov.dk/tool/SparxMDG/FDAprofil-MDG_v0.7.0.xml
3. Referencedata (xml-fil)
4. Projektskabelon (eap-fil)
5. Dialogboks (msi-fil)

Du kan hente pakken samt tilhørende vejedninger ovenfor og gå i gang eller du kan læse mere om de enkelte komponenter herunder.

Bemærk: I forhold til generel vejledning til Sparx EA henviser Modelsekretariatet til deres samling af brugermanualer her: https://sparxsystems.com.au/resources/user-guides/. Vi kan dog supplere med små tips og tricks til UML-modellering i Sparx EA her: https://docs.google.com/document/d/14oSR_QnLja8LuUbpsNE2FnV-22CK-TzNG1xqwIlp6Jo/edit#
 

## Begrebslisteskabelon til csv-import

Regnearksfil der er forberedt til at blive konverteret til csv, som kan importeres til Sparx EA, såfremt MDG-teknologi og tilhørende referencedata er installeret. Detaljerede instruktioner til dette finder du i Vejledning til brug af Plusprofil-pakken i Sparx EA.

Skabelonen ligner meget den generelle begrebslisteskabelon, (så kopiering af data fra den ene til den anden er ligetil), men har noget ekstra data, der gør at tags bliver udfyldt korrekt og mangler forretningsmetadata, som man selv er nødt til at indtaste.

 

## Plusprofil-MDG-teknologi

En MDG-teknologi er en konfiguration af Sparx Enterprise Architect (Sparx EA) som udvider funktionaliteten af værktøjet til et specifikt behov.

Plusprofil-MDG-teknologien indeholder udover selve UML-Plusprofilen yderligere funktionaliteter der tilpasser Sparx EA til begrebs- og datamodellering efter de fællesoffentlige regler.

Den består af følgende komponenter:

* Profildefinition: Modelreglernes stereotyper og tags (selve UML-profilen)
* Diagramdefinition: Modelreglernes diagramtyper
* Toolboxdefinition: Værktøjskasser tilpasset diagramtyperne hvorfra elementer kanhentes ind i diagrammet med de tags, der hører til de relevante stereotyper
* Datatyper: Modelreglernes XSD datatyper
* Workspace-layout: Placering af vinduer som letter adgang til værktøj og tags.

Konfigurering og brug af FDAprofil-MDG-teknologien er beskrevet i vejledningerne nedenfor.

 

## Plusprofilreferencedata

Til MDG-teknologien hører en fil med referencedata der yderligere udvider de begrebs- og datamodelleringsorienterede funktionaliteter i Sparx EA.

Den indeholder:

* CSV-import specifikation: Specifikation til import af begrebsliste i tabelformat
* Scripts: Diverse scripts til masseopdatering af modelelementer og tags
* Rapportskabeloner: Rapportskabeloner til begrebsmodeller og logiske modeller
 

## Projektskabelon

Projektskabelon i Sparx EAs eget filformat (eap), der automatisk knytter Plusprofil-MDG-teknologien og tilhørende referencedata til projektet.

Du kan også vælge selv at knytte MDG-teknologi og referencedata til et projekt, der ikke bruger projektskabelonen. Du kan få hjælp til dette i Vejledning til brug af FDAprofil Sparx EA-pakken.

 

## Dialogboks

Installation af dialogboksen gør det muligt at åbne et vindue, hvor netop de tagged values der skal udfyldes ifølge modelreglerne samles og vises på en nemt overskuelig måde. Desuden giver dialogboksen mulighed for at indtaste mere end en Accepterede termer (altLabel) og Frarådede termer (deprecatedLabel).

Dialogboksen ligger i en msi-installationsfil installationen går i gang ved dobbeltklik. Hvis du har spørgsmål om installationen, er der yderligere information i Vejledning til konfigurering af Sparx EA med FDAprofil-pakken.

Efter installation kan du aktiverer dialogboksen på to måder. I begge tilfælde skal du markere den pakke eller det modelelement, du ønsker at se tags for. Dernæst TRYK:

* Ctrl+R (for dansk version af dialogboksen) eller 
* Ctrl+Q (for version med de standardiserede engelske betegnelser), 

eller åbn Extend-menuen, og klik Plusprofil Editing Window, og dernæst enten Open Danish Editing Window Eller Open English Editing Window
 
