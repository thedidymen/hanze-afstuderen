Docenten en regisseurs mogen evenementen aanmaken en stellen de beschikbaarheidsperiodes vast voor één of meerdere dagen. Deze periodes worden opgedeeld in tijdslots met een configureerbare duur en capaciteit.

Het planningsproces ondersteunt pauzes en optionele lunchpauzes. De minimale groepsgrootte is niet verplicht, maar de maximale groepsgrootte is een strikte eis voor studenten.

Studenten registreren zich individueel en kunnen normaal gesproken maar één tijdslot per event reserveren. De openings- en sluitingstijd van de registratie en de annuleringsdeadline zijn onafhankelijk in te stellen. Studenten mogen hun tijdslot wijzigen zolang de registratie openstaat, ook na de annuleringsdeadline. Na de annuleringsdeadline kan er niet meer geannuleerd worden.

Docenten en regisseurs kunnen inschrijvingen van deelnemers beheren en indien nodig handmatig de capaciteit van een tijdslot overschrijden. Dit vraagt om een expliciete bevestiging.

De applicatie beschermt persoonlijke informatie door dataminimalisatie, role-based access control (RBAC) en course-gebaseerde autorisatie. Studenten mogen geen toegang hebben tot de identiteit of registraties van andere studenten (NF-PS-01, NF-PS-02, NF-PS-08).

De tool waarborgt de data-integriteit wanneer meerdere gebruikers tegelijkertijd registreren. Registratiewijzigingen worden atomair verwerkt om inconsistente data en onbedoelde overboeking van een tijdslot te voorkomen (NF-BDI-01).

De tool is uitbreidbaar en onderhoudbaar. De componenten hebben ieder een eigen en duidelijke verantwoordelijkheid, waardoor het mogelijk is om deze onafhankelijk te testen en te vervangen (NF-MA-01, NF-MA-04).

# Funtioneel ontwerp

Dit hoofdstuk beschrijft de hoofdfunctionaliteti van de Sign-Up Tool. Het ontwerp is gebaseerd op de requirements die zijn vast gesteld in het analyseverslag en de ontwerp principen uit het vorige hoofdstuk. 

De focus ligt op de interactie tussen studenten, docenten/regisseur, evenementen, tijdslots en registraties. Het ontwerp beschrijft ook de bedrijfregels en uitzonderingen. De volgende hoofstukken beschrijven de technische implementatie en het datamodel.

## Gebruikersrollen en autorisaties

De applicatie maakt onderscheid tussen twee functionele rollen: studenten en docent/regisseur. Docenten en regisseurs hebben dezelfde rechten binnen de tool. Regisseurs hebben een overkoepelende rol binnen de organisatie. Zoals weergegeven in @tbl:autorisatiematrix beschikken studenten en docenten/regisseurs over verschillende rechten binnen de Sign-Up Tool.

| Functionaliteit | Student | Medewerker |
|---|---|---|
| Relevante evenementen bekijken | Ja | Ja |
| Beschikbare tijdslots bekijken | Ja | Ja |
| Registreren voor een tijdslot | Eigen registratie | Handmatig registreren |
| Registraties wijzigen of annuleren | Eigen registratie | Registraties binnen de geautoriseerde context |
| Evenementen aanmaken en configureren | Nee | Ja |
| Deelnemersinformatie bekijken | Alleen eigen gegevens | Ja |
| Deelnemerslijsten genereren | Nee | Ja |
| Maximale capaciteit van een tijdslot overschrijden | Nee | Ja, na bevestiging |

: Autorisatiematrix voor studenten en medewerkers {#tbl:autorisatiematrix}

De gebruikers' rol en course context worden verkregen door de Brightspace integratie. De tool verifieerd de permissies voordat toegang wordt verkregen tot functionaliteit en persoonlijke informatie. 

Binnen de POC zal elk evenement gekoppeld zijn aan een enkele course binnen Brightspace. Toegang tot het opzetten van een evenement is voorbehouden aan geautoriseerde gebruikers binnen de Brigthspace-course. 

## Usecases en gebruikersscenario's

Het functioneel ontwerp focust zich op de registratie workflow, van het opzetten van een evenement tot de student registratie en het verkrijgen van de deelnemerlijsten. 

### Aanmaken en beheren van evenementen

Geautoriseerde gebruikers kunnen een nieuwe evenement aanmaken binnen de hun Brightspace-courses. 

Een evenement bevat informatie zoals een naam, beschrijving, course context, locatie en docent. De docent/regisseur stelt ook een openingstijd voor de registratie, een sluitingstijd en een annulerings deadline. Evenementen hebben een of meer beschikbaarheids periodes. Deze periodes geven de tijdsvlakken waarvoor een student zich kan registreren voor de activiteit. 

De tool laat docenten/regisseurs een evenement aanmaken en instellen voordat deze beschikbaar wordt voor de studenten. Een evenement kan gepubliceerd worden zodra de configuratie compleet is. Een evenement zonder registraties kan verwijdert of bewerkt worden. Zodra registraties bestaan, kunnen wijzigingen of verwijdering ongewenste effecten hebben (TO DO: is dat erg?).

De beschreven functionaliteit ligt in deze requirement: FN-ETM-01, FN-ETM-02, FN-DRO-04 and FN-DRO-09.

### Tijdslotbeheer en capaciteitsmanagement



### Studentregistratie, wijzigen en annuleren



### Deelnemeroverzichten en exports



### Uitzonderingen en foutscenario's



## Acceptatiecriteria

