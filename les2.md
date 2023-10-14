# Les 3: Python - werken met Socket en Scapy

Dit activiteitslogboek beschrijft het experiment dat is voorgesteld voor week 3. In dit experiment wordt een tool ontwikkeld met behulp van Scapy om de volgende functionaliteiten uit te voeren: Host Discovery, Service Discovery, Remote OS Detection en PCAP Analysis. Het doel is om een interactieve tool te maken die kan worden bediend via de terminal en met behulp van command-line argumenten.

## 1. Aanmaken van het Programma

*Datum: [3 oktober]*

Het ontwikkelingsproces van de "Ethisch Hacking Toolkit" begon in de les. Dit omvatte het opzetten van de projectstructuur en het maken van de eerste versie van de code. Ook zocht ik ook een aantal dingen op.

## 2. Implementatie van Functionaliteit

*Datum: [7 oktober]*

- Functionaliteit voor hostontdekking & serviceontdekking.
- Het verwerken van opdrachtregelargumenten werd toegevoegd.

*Datum: [14 oktober]*

- OS-detectie en PCAP-analyse werd geïmplementeerd.
- Een loggerklasse werd geïntegreerd om resultaten en fouten te registreren.

## 3. Uitvoeren van Tests

*Datum: [14 oktober]*

Er werden tests uitgevoerd om de werking van het programma te controleren. Dit omvatte:

- Het uitvoeren van het programma met verschillende opdrachtregelargumenten om ervoor te zorgen dat de functionaliteit correct werkte.
- Testen met verschillende doel-IP-adressen om de serviceontdekking, OS-detectie en PCAP-analyse te valideren.

## 4. Problemen en Uitdagingen

*Datum: [14 oktober]*

Tijdens het ontwikkelingsproces werden enkele problemen en uitdagingen geïdentificeerd:

- **PCAP liep vast**: Het programma liep vast wanneer geen Windows-machine werd opgegeven voor PCAP-analyse. Er is geen oplossing gevonden voor dit probleem.

- **Logboekregistratieprobleem**: Er waren problemen met het logboekregistratieproces. Het programma probeerde een lijst aan een string toe te voegen, wat resulteerde in een fout.

- **Uitvoer versus Logboek**: De uitvoer op het scherm was niet identiek aan wat in het logboek werd geregistreerd. Dit zou kunnen leiden tot inconsistenties in de vastgelegde gegevens.

## 5. Oplossingen

*Datum: [14 oktober]*

Om met de geïdentificeerde problemen om te gaan, werden de volgende oplossingen voorgesteld en geïmplementeerd:

- **PCAP liep vast**: Er is geen oplossing gevonden voor het probleem van vastlopen wanneer geen Windows-machine wordt opgegeven voor PCAP-analyse. Dit blijft een beperking van het programma.

- **Logboekregistratieprobleem**: Het logboekregistratieprobleem is opgelost door te appenden i.p.v. te extenden.

- **Uitvoer versus Logboek**: Het is van belang om ervoor te zorgen dat de gegevens die op het scherm worden weergegeven exact overeenkomen met wat in het logboek wordt vastgelegd, zodat er geen inconsistenties zijn.
