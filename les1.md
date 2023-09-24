# Week 1: De Basis + Experimenten Reconnaissance

## Inhoudelijk

- **Wat is ethical / white-hat hacking?**

  - Het gebruik van hacking-technieken met toestemming om de beveiliging van computersystemen en netwerken te testen en te verbeteren.

- **In welke context gebeurt dit?**

  - Om de beveiliging van een systeem te verbeteren en te beschermen tegen criminele hackers. In bug bounty platformen voor bedrijven.

- **Wat zijn de basis-voorwaarden om aan ethical hacking te doen?**

  - Wettelijke toestemming, technische vaardigheden en ethische richtlijnen.

- **Wat is pentesting?**

  - Bij pentesten worden cyberaanvallen gesimuleerd om de beveiliging van een systeem om te zien of het wel veilig is.

- **Wat zijn de verschillende fasen die in de literatuur worden beschreven? Meer bepaald: wat wordt begrepen onder "reconnaissance"? Beschrijf!**

  - Reconnaissance is de initiële fase van pentesting, waarbij informatie over het doelsysteem wordt verzameld, zoals IP-adressen en open poorten. Het is een soort scouting/verkenningsfase.
  - Scanning
  - Gaining Access
  - Maintaining Access
  - Enumeration (zo veel mogelijk informatie verzamelen)
  - Pilfering and Data Extraction (gegevens stelen)
  - Reporting
  - Cleanup (backdoors enz. verwijderen)

- **Wat is bug bounty? Welke zijn de mogelijkheden om aan bug bounty te doen?**

  - Het is een beloningsprogramma waarbij organisaties geld of andere beloningen aanbieden aan ethische hackers en beveiligingsonderzoekers voor het vinden en melden van beveiligingskwetsbaarheden in hun systemen of software.

- **Hoe verhoudt het Belgische Intigriti (intigriti.com) platform zich hiertoe?**

  - Ze hosten bug bounty-programma’s en verbinden onderzoekers met organisaties.

- **Hoe ga je te werk bij bug bounty? Wat is de beste aanpak voor een beginnend bounty hunter?**
  - Leer de basisprincipes van ethical hacking en webbeveiliging (verschillende soorten aanvallen).
  - Oefen in gecontroleerde omgevingen zoals TryHackMe en Hack The Box.
  - Lees en begrijp de regels van bug bounty-programma's.
  - Kies geschikte doelwitten voor beginners met lage of gemiddelde prioriteit.
  - Gebruik hulpmiddelen zoals Burp Suite en OWASP ZAP.
  - Meld kwetsbaarheden volgens het programma en wees geduldig.
  - Documenteer: bouw een portfolio van je bevindingen.
  - Blijf leren en blijf op de hoogte van nieuwe ontwikkelingen, leer van anderen, gebruik online bronnen.

## Demo 1: Informatie Inwinnen Via Request en Socket

- **In welke context kan dit nuttig zijn?**

  - Om informatie te verzamelen van een website en het bijbehorende IP-adres, verkenning of monitoring.

- **Kan je dit algemener uitbreiden naar een pure IP-context?**

  - Ja, in plaats van een URL kun je het via een IP-adres doen.

- **Kan je specifieke informatie verkrijgen naargang de context?**
  - Ja, je kunt bijvoorbeeld een poortscan doen om te zien welke poorten open zijn, kijken naar het type tijdszone, postcode, enz.

## Demo 2: Poort Scannen met Nmap in Python

`Nmap uitgetest.
  $ py portscan.py
  <class 'dict'>
  {'nmap': {'command*line': 'nmap -oX - -p 80 -v --version-all pcwijs.live', 'scaninfo': {'tcp': {'method': 'syn', 'services': '80'}}, 'scanstats': {'timestr': 'Tue Sep 19 10:59:16 2023', 'elapsed': '0.84', 'uphosts': '1', 'downhosts': '0', 'totalhosts': '1'}}, 'scan': {'172.67.129.117': {'hostnames': [{'name': 'pcwijs.live', 'type': 'user'}], 'addresses': {'ipv4': '172.67.129.117'}, 'vendor': {}, 'status': {'state': 'up', 'reason': 'syn-ack'}, 'tcp': {80: {'state': 'open', 'reason': 'syn-ack', 'name': 'http', 'product': '', 'version': '', 'extrainfo': '', 'conf': '3', 'cpe': ''}}}}}
  nmap -sVC -O -T4 scanme.nmap.org
  Starting Nmap 7.94 ( https://nmap.org ) at 2023-09-19 10:34 Romance Summer Time
  Nmap scan report for scanme.nmap.org (45.33.32.156)
  Host is up (0.16s latency).
  Not shown: 923 closed tcp ports (reset), 68 filtered tcp ports (no-response)
  PORT STATE SERVICE VERSION
  21/tcp open tcpwrapped
  22/tcp open tcpwrapped
  | ssh-hostkey:
  | 1024 ac:00:a0:1a:82:ff:cc:55:99:dc:67:2b:34:97:6b:75 (DSA)
  | 2048 20:3d:2d:44:62:2a:b0:5a:9d:b5:b3:05:14:c2:a6:b2 (RSA)
  | 256 96:02:bb:5e:57:54:1c:4e:45:2f:56:4c:4a:24:b2:57 (ECDSA)
  |* 256 33:fa:91:0f:e0:e1:7b:1f:6d:05:a2:b0:f1:54:41:56 (ED25519)
  80/tcp open tcpwrapped
  |\_http-server-header: Apache/2.4.7 (Ubuntu)
  |\_http-favicon: Nmap Project
  110/tcp open tcpwrapped
  143/tcp open tcpwrapped
  443/tcp open tcpwrapped
  8010/tcp open tcpwrapped
  9929/tcp open tcpwrapped
  31337/tcp open tcpwrapped
  Device type: general purpose|storage-misc|firewall|WAP|webcam
  Running (JUST GUESSING): Linux 4.X|2.6.X|3.X|2.4.X (88%), Synology DiskStation Manager 5.X (86%), WatchGuard Fireware 11.X (86%), Tandberg embedded (85%)
  OS CPE: cpe:/o:linux:linux_kernel:4.0 cpe:/o:linux:linux_kernel:2.6.39 cpe:/o:linux:linux_kernel:3 cpe:/o:linux:linux_kernel cpe:/a:synology:diskstation_manager:5.1 cpe:/o:watchguard:fireware:11.8 cpe:/o:linux:linux_kernel:2.4 cpe:/h:tandberg:vcs
  Aggressive OS guesses: Linux 4.0 (88%), Linux 2.6.39 (87%), Linux 3.10 - 3.16 (87%), Linux 3.10 (86%), Linux 2.6.32 (86%), Linux 2.6.32 or 3.10 (86%), Linux 3.4 (86%), Linux 3.5 (86%), Linux 4.2 (86%), Linux 4.4 (86%)
  No exact OS matches for host (test conditions non-ideal).
  Network Distance: 15 hops

  OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
  Nmap done: 1 IP address (1 host up) scanned in 45.88 seconds
`

## Demo 4: Screenshots Nemen (en indien gewenst via FTP Opladen)

- **Bedenk zelf enkele mogelijke use cases voor het maken van screenshots**

  - Screenshot naar anderen sturen voor ondersteuning op afstand, testing, momentopname, om informatie te onderscheppen op het moment van het uitvoeren.

- **Een FTP-ophaal- en afzetplek voor informatie gebruiken heeft voor- en nadelen. Wat zijn alternatieven?**
  - E-mail, cloudopslag, sociale media, fysieke schijven, delen via VPN, WeTransfer.
