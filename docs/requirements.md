## Doel
Ik wil een live score app hebben waarmee ik data van tenniswedstrijden kan bijhouden en streamen naar vrienden.

## Gebruikers
Ik, mijn vrouw, mijn familie en vrienden.

## Kernfunctionaliteit
1. Wedstrijden aanmaken met namen spelers, type spel (dubbel single), score methode (best of three sets, twee sets super tiebreak, open format), locatie wedstrijd obv geolocatie.
2. Score automatisch berekenen. Score moet worden ingevoerd door het drukken van de knop wie het punt gescoord heeft. De score functionaliteit van tennis moet werken. Zie score systeem.
3. De bediening van de webapp moet op een smartphone kunnen. Stel dat je voor dat je naast de kant een wedstrijd kijkt dan moet je de score simpelweg kunnen invoeren door op de knop te drukken van de speler. Het mooiste zou zijn als de spelers op het scherm mee wisselen met de wedstrijd. Zie kantwissel.
4. De wedstrijd moet live te volgen zijn voor familie en vrienden. Het liefst door het delen van een link via bijvoorbeeld WhatsApp. Het moet echt live zijn via websocket.
5. Statistieken,wedstrijden en scores moeten bijgehouden worden in een sqlite database. Ook wil ik spelers kunnen toevoegen om die eventueel later her te gebruiken.
6. Optioneel zou ik het leuk vinden om de volgende statistieken kunnen bijhouden. Dubbele fout dropshot winner unforced error smash volley
7. De ui moet eenvoudig zijn. Ik wil als score invoerde twee knoppen en een score zien. Een undo en redo optie zou erg handig zijn voor als ik een fout maak.
8. Het zou leuk zijn als ik een lijst zie van wedstrijden die gespeeld zijn. Wedstrijden die live zijn moeten een groen lampje hebben.
9. 

## Score systeem
Game: punten tellen als 0 (love), 15, 30, 40, game. Je moet minimaal 4 punten halen én 2 punten voorsprong hebben. Bij 40-40 (deuce) moet je dus twee punten op rij winnen: eerst "voordeel" (advantage), dan game.
Set: wie als eerste 6 games wint met minimaal 2 games verschil, wint de set (6-4, 6-3, enz.). Bij 5-5 speel je door tot 7-5. Bij 6-6 volgt meestal een tiebreak.
Tiebreak: hier tel je gewoon 1, 2, 3, enz. Wie als eerste 7 punten haalt met 2 punten verschil wint de set (7-6). Serveerbeurten wisselen na het eerste punt en daarna elke twee punten.
Wedstrijd: meestal best-of-three (eerste tot 2 sets), bij grand slams voor mannen best-of-five (eerste tot 3 sets). In de beslissende set gelden soms afwijkende regels, zoals een supertiebreak tot 10 punten.

## Kantwissel
Kantwissel gebeurt bij oneven aantal games dus. Bij 1-0 2-1 etc. Let op bij een set wissel kan het zijn dat van kant gewisseld wordt bijvoorbeeld 6-3 bij de nieuwe set wordt dan weer gewisseld bij 1-0.

Bij een tiebreak is er een kantwissel als het aantal punten in de tiebreak bij elkaar opgeteld deelbaar is door 6. dus bijv 4-2 of 3-3 of 6-6

