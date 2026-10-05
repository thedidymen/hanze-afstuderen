# Vergelijken oplossingen

## Inleiding

In het voorgaande hoofdstuk zijn er verschillende oplossingen voor de Sign-Up tool onderzocht. Gebaseerd op de initiële selectie tegen de Must-requirements, zijn er drie oplossingen uitgekomen voor verder onderzoek: Academy Attendance, RegisterBlast en een maatwerkoplossing. 

Binnen dit hoofdstuk worden de drie oplossingen in meer detail vergeleken. Waar eerder gekeken werd naar mogelijke oplossingen, wordt nu gekeken voor deze oplossingen naar de complete set requirements. Het doel van de vergelijking is om de sterke kanten, de beperkingen en de onzekerheden in kaart te brengen, zodat we bij een voorkeursoplossing uitkomen.

## Criteria voor vergelijken

De requirements zijn vastgelegd in het requirmenthoofdstuk, deze vormen de primaire basis voor het vergelijken van de oplossingen. Hiermee wordt de uiteindelijke keuze traceerbaar naar de behoeften van de stakeholders. 

De Must-requirements vormen een hard minimum waar een product aan moet voldoen. Bij onvoldoende bewijs voor een Must, wordt de onzekerheid aangegeven en verder onderzocht. Een oplossing die aantoonbaar niet aan een Must-requirement kan voldoen, valt af als geschikte eindoplossing. Voor de Should- en Could-requirements worden de scores gecombineerd met de eerder vastgestelde requirementprioriteiten. Hiermee ontstaat per oplossing een gewogen totaalscore. De exacte scoringsschaal en berekening worden voorafgaand aan de beoordeling vastgelegd. Hierbij hebben requirements met een hogere prioriteit een grotere invloed. Won't-requirements vallen buiten de scope van het project. 

De analyse maakt onderscheid tussen functionaliteit die aantoonbaar aanwezig is, gedeeltelijk aanwezig is en waar onvoldoende bewijs voor is. Waar mogelijk is de assessment gebaseerd op documentatie van de leverancier, technische documentatie, interviews en informatie over de bestaand Hanzeomgeving. Functionaliteit waarvoor onvoldoende bewijs beschikbaar is, wordt als niet geverifieerd beschouwd. Alleen wanneer uit de beschikbare informatie blijkt dat functionaliteit niet wordt ondersteund, wordt deze als niet ondersteund beoordeeld. 

Voor de maatwerkoplossing vereist een andere interpretatie dan die voor bestaande producten. Academy Attendance en RegisterBlast worden geëvalueerd op aantoonbare functionaliteit. Bij de maatwerkoplossing wordt gekeken naar of het reëel haalbaar is om de requirement te implementeren binnen de technische oplossing. De oplossing bestaat dus nog niet, maar kan reëel worden toegevoegd aan het ontwerp en de implementatie. 

## Multi-Criteria Analyse

Een Multi-Criteria Analyse (MCA) wordt gebruikt om systematisch de drie oplossingenen te vergelijken. Deze MCA is gebaseerd op gevestigde Multi-Criteria Decision Analysis methoden. Binnen een MCDA worden alternatieven systematisch vergeleken tegen een gedefinieerde set criteria [@belton2002mcda; @dodgson2009mca]. De requirements vormen de criteria voor de vergelijking, waarbij Must-requirements als harde voorwaarden worden behandeld en Should- en Could-requirements onderdeel zijn van de gewogen vergelijking. Dit maakt de vergelijking transparant en laat zien op welke criteria de oplossingen van elkaar verschillen. De exacte beoordelingsschaal en de wijze waarop de requirementprioriteiten als weging worden gebruikt, worden binnen de MCA vastgelegd voordat de oplossingen worden gescoord. Voor de gewogen vergelijking van de Should- en Could-requirements wordt een lineair additief model gebruikt, waarbij de score per criterium wordt vermenigvuldigd met het bijbehorende gewicht en de gewogen scores worden opgeteld tot een totaalscore. Voorafgaand aan de scoring worden de criteria gecontroleerd op inhoudelijke overlap, zodat dezelfde eigenschap niet onbedoeld meerdere keren wordt meegewogen.

Naast de requirement-gebaseerde vergelijking, wordt het laatste oordeel ook gebaseerd op praktische verschillen tussen oplossingen. Denk hierbij aan implementatie-inspanning, vereiste integraties, technisch onderhoud, functioneel beheer en eigenaarschap voor de lange termijn. Waar mogelijk zijn deze ook gevangen in de requirements. Waar deze aspecten al door requirements worden afgedekt, worden ze niet opnieuw als afzonderlijk criterium meegewogen. Overige praktische consequenties worden aanvullend kwalitatief besproken.

## Conclusie

