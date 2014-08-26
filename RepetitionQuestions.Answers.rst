=======================================
FS14 InfSi3 Repetitionsfragen Antworten
=======================================

Dieses Dokument wird vorzu erweitert. Ergänzungen und Antworten sind herzlich willkommen.
Repetitionsfragen: https://github.com/moonline/HSR.modules.InfSi3/blob/master/RepetitionQuestions.rst


.. contents:: Inhaltsverzeichnis


1 Information Security Management
=================================

**1.0.1. Thread Model**

.. image:: img/rq-1.0.1.1.jpg
   :width: 50 %


**1.0.2. Effiziente Massnahmen**

Mit organisatorischen Massnahmen (M2 Organisationsmanagement).


**1.0.3. Risikomodell**

::

	Risiko = Schaden ◆ Eintrittswahrscheinlichkeit
	       = Schaden ◆ Bedrohung ◆ Verletzlichkeit der Schutzmassnahmen
	
	Es muss eine Bedrohung existieren, damit ein Risiko da ist!


.. image:: img/rq-1.0.3.1.jpg
   :width: 50 %


**1.0.4. Grund für Sicherheitsmassnahmen**

Unternehmen fürchten sich vor Gesetzesverstössen


1.1 Anforderungen an Informationssicherheit
-------------------------------------------

**1.1.1 Schadensindikatoren**

.. figure:: img/1.3.jpg

   Der Indikator gibt an, um was für einen Schaden es sich handelt. Die Skala definiert, in welcher Grössenordnung Bagatellen, Unfälle, Störfälle und Katastrophen für die jeweiligen Schäden liegen.


**1.1.2. Gesetzliche Anforderungen**

* Datenschutz (Bearbeiten von Personendaten)
* Vorschriften für Finanzinstitute
* Fernmeldegesetz
* Allgemeines Controlling


**1.1.3. Gesetze & Artikel**

DSG
	Datenschutzgesetz, regelt Bearbeitung von Personendaten, Schutz von Systemen gegen bestimmte Risiken
Stgb Art. 179
	Vorsätzlicher Missbrauch von Fernmeldeanlagen, Unbefugtes Beschaffen von Personendaten
HIPAA / TARMED
	Schutz von Gesundheitdaten
BankG Art 47
	Bankgeheimnis, Umgang mit Finanzdaten / Kundendaten
VSB 08
	Vereinbarung zwischen den Bankiervereinigung und Banken über Sorgfaltspflicht
PCI
	Payment Card Industry Data Security Standard Anforderungen, Schutz von Daten und Hardware
Fernmeldegesetz
	Regelt Telekommunikationsdienstleistungen sowie den Schutz übertragener Daten
SOX
	Allgemeines Controlling für US-börsenkotierte Unternehmen
FISA 1978
	Regelt Vorgehen bei Aufklärung und Spionageabwehr un den USA
PATRICOT ACT 2001
	Anti Terror Bestimungen zur vereinfachten Überwachung von Bürgern


1.2 Threads
-----------

**1.2.1. Bedrohung, Motivation, Mittel**

Die Bedrohung steigt sowohl mit zunehmender Motivation und zunehmenden Mitteln (Zeit/Finanzen) und den technischen Fähigkeiten.

Jedermann
	Ausprobieren, wenig Know How, Schaden gering, geringe Motivation
IT-Freak
	Persönliche Profilierung, gutes Know How, Schaden gering
Professioneller Hacker / Hacktivismus
	Gezielte Angriffe, gutes Know How, persönlicher oder politischer Gewinn
Spione
	Gezielte, mit viel Mitteln gestützte Angriffe, grosses Know How, Nationale Interesse, Schaden gross
	

**1.2.2. NSA**

* Nationale Sicherheitsagentur mit weltweiten Standorten
* Verarbeitet und überwacht riesige Datenmengen
* 30'000 MA / 8Mia Jahresbudget


**1.2.3. Quantum**

Computer werden hardware oder Softwareseitig infiziert und anschliessend Daten zur NSA umgeleitet.
Z.B. Leitet die NSA Trafic an Internet Routern um, um sich in ein login einzuhängen und das Target zu kompromitieren.



2 Location Based Services
=========================

**2.0.1. Typen von LSB**

Map/Navigation
	* Standort
	* Bewegung
Local Information/Search
	* Standort
	* User generated content
Tracker
	* Standort
	* Bewegung
Special (Friend finder, Augmented Reality, Gaming, ...)
	* Standort


**2.0.2. Standort bezogene Dienste (Beispiele)**

* Google Maps -> Aktuelle Position, ermittelt über IP, GPS, Wlan, Mobilfunk
* Trafic Info -> Aktuelle Position/Verkehrsweg
* Wetter App -> Aktuelle Position
* SBB Fahrplan (indirekt)
* Google Now
* Google Buzz (Around Me)
* Google Glass


**2.0.3. Datenschutzgesetz**

DSG Art3 Begriffe
	Personendaten
		Daten, die sich auf eine Person beziehen
	Besonders Schützenswerte Personendaten
		* Religiöse/politische Ausrichtung
		* Gesundheitsdaten
		* Soziale Hilfe
		* Strafverfolgung
	Persönlichkeitsprofil
		Erlaubt die Beurteilung der Persönlichkeit
DSG Art4 Grundsätze
	Bearbeiten von Personendaten
		Nur für vorgesehen Zweck verwenden
	Beschaffung von PD
		Zweck und Zweck ihrer Bearbeitung muss ersichtlich sein
	Einwilligung zur Bearbeitung
		* Betroffener muss angemessen Informiert werden
		* ausdrückliche Einwilligung für besonders Schützenswerte Daten
DSG Art5 Datensicherheit
	Personendaten müssen angemessen (organisatorisch/technisch) geschützt werden
DSG Art6 Auskunfstrecht
	Betroffene haben das Recht auf Auskunft über die Bearbeitung ihrer Daten
DSG Art14 Tracking/Persönlichkeitsprofile
	* Betroffene Person muss informiert werden
	* Angegeben werden müssen: 
		* Inhaber der Datensammlung
		* Zweck
		* Kategorien der Empfänger bei Datenweitergabe
		
**2.0.4. Google Analytics/Facebook Social Buttons auf Webseiten**

a) Gesammelte Informationen
	Google
		* Aufrufzeitpunkt, Dauer des Besuches jeder Seite
		* Ungefährer Standort, Land, Region, Ort, Provider, Down-/Uploadrate
		* Betriebsystem, Sprache, eingestellte Lokalisierung, Bildschirmauflösung, Gerätetyp
		* Browser Footprint, Unterstützte Plugins/API's
		* Neuer Benutzer oder wiederkehrender
	Facebook
		* Selbe Informationen wie Google Analytics +/-
		* Identität (z.B: Facebook login)
		* Mit Identität verknüpfte Informationen (Freunde, Familie, Vorlieben)
		* Was dem Benutzer gefällt oder nicht (Like)
	Anwaltskanzlei
		* Selbe Informationen wie Google Analytics
		
b) Zu Beachten
	* Facebook verfügt über Persönlichkeitsprofile der Benutzer -> DSG Art.14
	* Die Anwaltskanzlei muss in der Lage sein, Benutzern Auskunft darüber zu geben, welche Daten gesammelt wurden
	
	
2.1 Methoden zur Lokalisierung von Objekten
-------------------------------------------

**2.1.1. Passive Standortpreisgabe Beispiele**

* Online Fahrplan
* Google Maps
* Navi
* Wetter Apps


**2.1.2. Standortbekanntgabe bei Browsern**

Der Browser schickt alles, was er hat:

* Sichtbare WLAN Netzwerke
* IP


**2.1.3. Lokationsdaten**

Lokationsdaten, die mit einer Person verknüpft sind (auch IP Adressen) sind in CH Personendaten.


**2.1.4. IP Lokalisierung**

Über IP wird zugeteilter Provider ermittelt -> Zugangsknoten von ISP ist genauste mögliche Location.


**2.1.5. IP Adresse als Personendatum**

Da die IP mit der Identität eines Benutzers verknüpft ist sie das und unterliegt damit dem DSG.


**2.1.6. Cell Tower Localization**

* Provider weiss, in welcher Zelle sich ein Benutzer befindet
* Handy sieht jedoch mehrere Antennen und kann über einen Antennenstandortdatenbank mittels Triangulation ziemlich genau seine Position orten


**2.1.7. GSM Netz**

Ein Mobiltelefon gibt folgende Daten in einem GSM Netz preis:

* Identität, TeilnehmeriID+Verschlüsselungskeys auf SIM (GSM besitzt eine Authentisierung)
* Zelle (Standort auf weniger als eine Zelle genau da mit den Signallaufzeiten gearbeitet wird)
	* Location Area ID
	* Cell ID
	* Timing Advance
* Die weltweit eindeutige TeilnehmeriID wird auf der Luftschnittstelle verborgen und stattdessen eine temporäre verwendet, um Mithörer diese nicht preiszugeben


**2.1.8. Wlan Ortung**

* Nutzer gibt seine Mac Adresse Preis (Weltweit eindeutig)
* Ortung erfolgt über WLAN Datenbanken

**2.1.9. Beacons**

* Kurz- und Langdistanz RFID/Bluetooth Tags Zur Identifikation von Fahrzeugen (langdistanz) oder Personen in Gebäuden (Kurzdistanz)
* Smartphones verbinden sich mit Beacons an Messen


**2.1.10. E-Plate Long Range Tags**

Aktive RFID Tags in Kennzeichen, auslesbar auch 100m Entfernung und bis 320 Km/h


**2.1.11. Genauigkeit der Lokalisierung**

* Bluetooth/Beacons Kurzdistanz: Bis 2m
* GPS: Bis 15m, mit Korrekturdaten bis im cm Bereich


**2.1.12. GSP zur Flottenüberwachung**

Der Arbeitgeber überwacht damit den Mitarbeiter und trackt diesen Kontinuierlich. Der MA muss darüber informiert werden und sein Einverständnis geben.


**2.1.13. bewusste Bekanntgabe von Lokationsdaten**

Der Benutzer tätigt eine Handlung, mit der er seine Position bekannt gibt. Z.B:

* Hochladen eines Bildes mit GPS Daten
* Friends Finder (Standort Sharen)
* Facebook Places (An einem Ort "einchecken")
* Flicker Foto Upload: Standort auf Karte einzeichnen


**2.1.14. unbewusste Bekanntgabe von Lokationsdaten**

Die Bekanntgabe des Standortes ist ein Nebeneffekt eines genutzten Dienstes, z.B.:

* Wetter Apps
* Activity Tracker
* Google Suche (Browser Footprint, IP)
* CDN Abrufe
* Proxy


**2.1.15. Google**

Google hat ziemliche Umfangreiche Informationen über Benutzer, da sie auf sehr vielen Webseiten mit Google Analytics drinhangen und sehr viele Dienst betreiben, auf denen User breitwillig Informationenpreisgeben:

* Surfverhalten / Vorlieben (Suche)
* Freunde / Familie (Google+)
* Standort (Google Maps, Google Buzz, Google Glass, Autonome Fahrzeuge)
* Reisen (Flugvergleiche, Fahrpläne)
* Informationen über benutzes Gerät sowie online-Zeiten (Schalfverhalten)


**2.1.16. Browser Fingerprint**

* Browser / Device / BS / Auflösung / Sprache / Lokalisierung
* Standort / ISP
* Unterstützte JS Schnittstellen / Aktivierte Plugins / Addons / Media Support
* Browsereinstellungen wie "Do Not Track" / JS ein/aus / Cookie settings
* Local Storage / Flash Storage

Die Kombination dieser Merkmale ist einmahlig und damit der Benutzer eindeutig zuortbar/idenitifizierbar.


3 Software Security
===================

**3.0.1. Potentiell gefährliche Funktionen**

* Auffinden mit Blacklist (Tool)
* Massnahme gegen erneuten Fehler später: Tests


**3.0.2. Connectivity, Extensibility, Complexity**

Connectivity
	Jede Software ist mittlerweile über das Netz verbunden und somit einem grossen Angriffsrisiko ausgesetzt -> müsste sich entsprechend verteidigen
Extensibility
	Software selbst ist ausgereift und sicher aber Erweiterungen bringen wieder Schwachstellen ein
Complexity
	Zunehmende Komplexität erhöht die Fehlerwahrscheinlichkeit und somit die Wahrscheinlichkeit, das ein Security Problem vorliegt.
	

**3.0.3. Bugs, Flaws, Defects**

Bugs
	* Fehler im Code (Falschbenutzung von Schnittstellen)
	* Implementation Level Fehler
	* Maschinell auffindbar
	* z.B. Buffer Overflow, Race Condition, Unsave system call
Flaws
	* Falscher Programmfluss, Nicht behandeln von Spezialfällen
	* Design Level Fehler
	* Mit Code Analyse Tools nicht auffindbar
	* z.B: Method Overriding, error handling, type save confusion
Defect
	Überbegriff für Bugs und Flaws
	

**3.0.4. Bug oder Flaw?**


1) Rückgabewert von Read() ignored
   -> Bug
2) Verwendung von strlen() auf einem Wert, der nicht garantiert mit einem 0-Byte terminiert
   -> Bug
3) Speicherung von Benutzerpasswörtern als Klartext in der Datenbank
   -> Flaw
4) Passwort des Users mit memcmp mit Passwort in der DB vergleichen. Wenn der Rückgabewert von memcmp != 0 wird der Zugriff geblockt (memcamp("", password) gibt auch 0 zurück).
   -> Bug (Ja nach Definition könnte es auch ein Flaw sein)


**3.0.5. Software Security Basics**

* Risk management
	* Business and technical risk
	* Risk priorisation
	* Mitigation strategies
* Best practices
	* Code Review
	* Risk analysis
	* Penetration testing
* Knowledge
	* Prescriptive Knowledge(Principles/Guidelines)
	* Diagnostics (Vulnerabilitis, Exploits, Attacks)
	* Historical risks
	
	
**3.0.6. Risiko**

Setzt sich zusammen aus Schaden (Schadensausmass) und Eintrittswahrscheinlichkeit (Verletzlichkeiten, Bedrohung)

.. image:: img/rq-1.0.3.1.jpg
   :width: 50 %


Es sollte so viel Geld in Security investiert werden, das die Gesammtkosten (Schaden + Massnahmen) minimal sind.


**3.0.7a. Best Practises**

1) Code Review
2) Risiko Analysen
3) Penetration Testing


**3.0.7b. Massnahmen & Artefakte**

i) Requirements & Use Cases
	* 7 Abuse Cases
	* 4 Security Requirements
	* 3 Risk Analysis
ii) Architecture & Design
	* 3 Risk Analysis
iii) Test Plans
	* 6 Risk based Security Testing
iv) Code
	* 2 Code Reviews
v) Tests & Test Results
	* 5 Penetration testing
	* 3 Risk Analysis
vi) Feedback from the Field
	* 5 Penetration testing
	* 1 Security Operation
	
	
**3.0.8. Barry Boehms Cost of Change Law**

Mit jeder Phase im SW-Entstehungsprozess steigen die Kosten, wobei sie exponentiell steigen.
Bugs, die während der Entwicklung gefunden werden, sind um Faktoren günstiger, als Bugs, die beim Kunden gefixt werdne müssen.


**3.0.9. Software Security Knowledge**

* Prescriptive Knowledge
	* Principles
	* Guidelines
	* Rules
* Diagnostic Knowledge
	* Vulnerabilitis
	* Attacks
	* Exploits
* Historical Knowledge
	* Historical risks
	

**3.0.10. Security Knowledge Architecture**

.. figure:: img/3.8.jpg
   :width: 75 %

   Exploits sind erkannte Verletzlichkeiten. Aus diesen ergeben sich Angriffsmuster und Historische Risikodaten. Zum Verhindern von Verletzlichkeiten kommen Prinzipien (Guidelines, Rules) zum Einsatz.


**3.0.11 Code Review Tools**

1) Code Scanners: Scannen den Code nach Patterns (Regex)
2) Advanced Source Code Analysis Tools: Führen den Code aus und analysieren den Code Fluss. Diese finden auch falsch Verwendete Schnittstellen etc. die nicht auf den ersten Blick ersichtlich sind.


**3.0.12. Architectural Risk Analysis**

* Analyse über die Attenresistenz (Checklisten zum Finden von bekannten Problemen)
* Mehrdeutigkeitsanalyse (Unklarheiten in den Architekturdokumentationen)
* Schwächenanalyse (Analyse von Abhängigkeiten von externen Tools und Frameworks und dadurch entstehende Schwächen)



4 Microsoft Security Livecylce
==============================

**4.0.1. Continious Process Improvement & Accountability**

Continious Process Improvement
	* Ständiger Verbesserungsprozess des Security Livecylce
		* Vier Levels: Basic, Standardized, Advanced, Dynamic
	* Disciplines (In jeder Discipline wird Kontinuierlich versucht, ein höheres Level zu erreichen)
		* Schulungen, Policy, organisatorische Fähigkeiten
		* Anforderungen & Design
		* Implementierung
		* Verifizierung
		* Release & Response
Accountability
	* Definierte Verantwortlichkeiten für den Fall eines Vorfalls
	* Wenn was passiert, schnell rausfinden, was passiert ist (Release and Response)
	* Zugriff für alle Beteiligten (Public Repo)
	* Im Falle eines Vorfalles soll schnell und richtig reagiert werden
	
	
**4.0.2. Security Livecylce**

::

	.-------------------+-------------------------------------------------------------.
	| 1) Training       | Core Security training                                      |
	'---------------------------------------v-----------------------------------------'
	.-------------------+-------------------------------------------------------------.
	| 2) Requirements   | * Establish Security Requirements                           |
	|                   | '-> Experten einbeziehen                                    |
	|                   | * Create Quality gates / Bug bars                           |
	|                   | '-> Produkt erst freigeben, wenn Bug/w Rate unterschritten  |
	|                   | * Security & Privacy Risk Assessment (R. minimieren/tragen) |
	'---------------------------------------v-----------------------------------------'
	.-------------------+-------------------------------------------------------------.
	| 3) Design         | * Establish Design Requirements                             |
	|                   | * Analyse Attack Surface                                    |
	|                   | '-> z.B. einhalten von "Least Priviledge"                   |
	|                   | * Threat Modelling                                          |
	|                   | '-> Checklisten/Regeln (z.B. BSI Handbuch)                  |
	'---------------------------------------v-----------------------------------------'
	.-------------------+-------------------------------------------------------------.
	| 4) Implementation | * Use Aprooved Tools (z.B. Code analysis tools)             |
	|                   | * Deprecate Unsafe Functions                                |
	|                   | * Static Analysis (Bugs finden)                             |
	'---------------------------------------v-----------------------------------------'
	.-------------------+-------------------------------------------------------------.
	| 5) Verification   | * Dynamic Analysis                                          |
	|                   | '-> Flaws finden, korrekte Implementierung überprüfen       |
	|                   | * Fuzzy Testing (Mit randoom input fluten)                  |
	|                   | * Attack Surface Review                                     |
	'---------------------------------------v-----------------------------------------'
	.-------------------+-------------------------------------------------------------.
	| 6) Release        | * Incident Response Plan                                    |
	|                   | * Final Security Review                                     |
	|                   | * Release Archive                                           |
	'---------------------------------------v-----------------------------------------'
	.-------------------+-------------------------------------------------------------.
	| 7) Response       | Execute Incident Response Plan                              |
	|                   | '-> Verfügbarkeit von Personen für Ernstfall                |
	'---------------------------------------------------------------------------------'


**4.0.3. Begriffe**

Quality gates / bug bars
	Gefundene Bugs/Woche muss best. Rate unterschreiten, damit das Release freigegeben wird
Risk Assessment
	Risiken minimieren, kleine Risiken tragen
Analyse Attack Surface
	Angriffsmöglichkeiten untersuchen, einhalten von Regeln wie z.B. "Least Priviledge"
Threat Modelling
	Mit Checklisten/Regeln Angriffsmöglichkeiten untersuchen (z.B. BSI Handbuch)
Fuzzy Testing
	Fluten mit Randoom Input
Dynamic Analysis
	Verhalten analysieren, macht das Programm, was es soll
Static Analyis
	Bugs finden
Response Plan
	Verantwirtlichkeiten, Verfügbarkeiten von Personen für Ernstfall
	

	
5 Web Application Security
==========================

**5.0.1. Web Applications**

* Über das Netz erreichbare Services (Zugriff von überall)
* Meisst Client/Server Architektur, Multi Tier Architektur
* Universellen Client (Browser), der nicht kontrolliert werden kann
* Direkter Zugriff zu Backend Data


**5.0.2. Web Application Architecture**

::

	.----------------------------------------------------------.
	|                          Client                          |
	'----------------------------------------------------------'
	                             ^ |
	                             | | Internet
	                             | |
	.----------------------------------------------------------.
	|              Server Network / Company Network            |
	|                            | |                           |
	|                            | v                           |
	| .------------------------------------------------------. |
	| |              Router, Firewall, Switching             | |
	| '------------------------------------------------------' |
	|                            ^ |                           |
	|                            | v                           |
	| .----------------..------------------..----------------. |
	| |                ||    Web Servers   ||                | |
	| '----------------''------------------''----------------' |
	|                             |                            |
	| .------------------------------------------------------. |
	| |                Web Application Server                | |
	| '------------------------------------------------------' |
	|          .------------------'------------------.         |
	| .---------------. .------------------. .---------------. |
	| |               |-| Database Servers |-|               | |
	| '---------------' '------------------' '---------------' |
	'----------------------------------------------------------'


**5.0.3. Cookies**

* Textdateien, die im Browser abgelegt werden (Speicherung von Requestübergreifender Information Clientseitig)
* Nur Scripts der Domain, die das Cookie gesetzt haben, dürfen es auch wieder lesen

.. code-block:: HTTP

	// scheme ame=value; name2=value2
	Cookie: LSID=DQAAAK…Eaem_vYg; Path=/accounts; Expires=Wed, 13 Jan 2021 22:23:01 GMT; Secure; HttpOnly; Domain=hsr.ch;
	
	
**5.0.4. Session Management**

1) Benutzer verbindet sich mit Server, loggt sich ein falls nötig
2) Server erzeugt eindeutige, nicht erratbare Session ID
3) Server speichert Session zu ID bei sich ab und schickt Session ID an Client
4) Client sendet Session ID bei jedem Request wieder mit, sodass der Server weiss, wer er ist

::

	                   Client              Web Server           App Server           DB Server
	                  
	Application Session  |<---------------------------------------->|
	
	HTTP Session         |<------------------->|
	
	Internal Session                           |<------------------>|
	
	Db Session                                                      |<------------------>|
	
	TCP Session         |<------------------->|<------------------->|<------------------>|
	

**5.0.5. Arten von Cookies**

Session Cookie
	* Speichert Session ID
	* Nicht persistent (Browser Memory)
	* Keine "expire time"
Persistent Cookie
	* In File abgelegt
	* Expire time
Secure Cookie
	* Darf nur über SSL/TLS Verbindungen transportiert werden
3rd Party Cookie
	* Wurde nicht von der ursprünglichen Seite gesetzt
HTTP Only Cookie
	* Nur durch HTTP auslesbar (Nicht durch JS)

**Supercookie**

* z.B. Flash Cookies
* Schwieriger zu finden und entfernen, Cookie-Remove Mechanismen von Browser finden sie nicht
* Werden an unterschiedlichen Orten gespeichert, z.B. in einem durch ein Flash Plugin angelegten File
* Erweiterte Funktionen, wie z.B. reguläre Cookies reaktivieren/verlängern


**5.0.6. E-Tags**

* Information, ob sich Seite beim Browser im Cache befunden hatte (Caching Kontrolle)
* Kann als Seitencookie gentzt werden, da zu jeder aufgerufenen Seite eine eindeutige ID gespeichert wird


**5.0.7. Cookie read/write access**

* Same Origin Policy: Nur Scripts vom gleichen Ursprung dürfen ein Cookie lesen


**5.0.8. Same Origin Policy**

* Port+Host+Protocoll stimmen überrein
* IP =! URL
* ABER gleiche Domain mit unterschiedlichen IP's (mehrere Web-Server) = Same Origin


**5.0.9. 3rd Party Cookie Data Mining**

1) Geladene Seite bindet über Skript ein Werbebanner eines Werbeanbieters ein und übermittelt Info über Domain (Damit die Werbeanbieter den Zugriff einem Werbekunden zuordnen können)
	.. code-block:: HTML
	
		<script>
			// create banner image from remote
			var bannerImage = document.createElement('img');
			bannerImage.outerHTML = '<img src="http://www.adtech.com/ad/?page=20min" />';
			
			document.getElementByTagName('body')[0].appendChild(bannerImage);
		</scipt>
		
2) Browser lädt eingebundenes Element. Dadurch erhält der Werbeanbierter die gleichen Informationen über den Client, die der Anbieter der ursprünglichen Seite auch hat (Browser, BS, Auflösung, Plugins, IP, Location, ...). Durch einen Parameter im Aufruf des Elements erfährt der Werbeanbieter, wessen von seinen Werbekunden (im Beispiel 20min.ch) er den Aufruf zuordnen muss.
3) Der Werbeanbieter setzt ein Cookie oder Supercookie um die Client beim nächsten Mal wiedererkennen zu können. Diese Wiedererkennung funktioniert aber auch über den Browser Footprint.
4) Wird die Werbung dieses Werbeanbieters von ganz vielen Seiten eingebunden (wie z.B. Google Analytics), so kann der Werbeanbierter Clients über Webseiten hinweg verfolgen und Persönlichkeitsprofile erstellen.


**5.0.10. P3P**

* Privacy Policy
* Deklaration der Seite, was mit welchen Daten geschieht
* Matcht die Policy nicht, wird die Seite nicht geladen
* Problem: Selbstdeklaration


**5.0.11. Sandboxing**

* Code wird in einem Container ausgeführt, aus dem er nicht ausbrechen kann
* Code hat beschränkten Ressourcen und API Zugriff
* Dem Code wird grundsätzlich nicht vertraut


**5.0.12. Rechte und Möglichkeiten**

JavaScript
	* Ohne Warnung
		* Remote Verbindungen
		* Video/Audio
		* Local Storage
		* Local DB
	* Mit Nachfrage
		* GeoLocation
		* File Access
		* Camera/Microphone Access

Flash
	* Remote Verbindungen
	* File Access
	* Camera/Microphone
ActiveX
	* Remote Verbindungen
	* File Access
Java Plugin
	* Remote Verbindungen
	* File Access


5.1 OWASP
---------

**5.1.1. OWASP**

Open Web App Security Project


**5.1.2. Häufigste Vulnerabilitis**

1) Injection
2) Broken Authentication and Session Management
3) Cross Site Scripting


**5.1.3. Injection Flaws**

* Einschleusen von Code über Benutzereingaben
* Aämmtliche Benutzereingaben müssen validiert werden
	* Whitelisting (allow none, allow some)
	* Blacklisting (allow all, disallow some)
	* Escaping (Replace bad data)
	
* Massnahmen gegen Injection
	* Review
	* Avoid external params
	* limit priviledges of app
	* validate ALL input
	* use system functions instead of own (e.g. prepared statements)


**5.1.4. Broken Authentication & Session Management**

* Umgehen von Authentication
* Login attacks (user/pw enumeration)
* Stehlen von Session/Session fixation
* Fehlende Verschlüsselung/Signaturen -> Modifikation von Session/Login Daten (z.B. Modifikation von SAML assertions, umleitungen)


Massnahmen:

* IMMER Cookies benutzen, Session ID nie in der URL oder post übergeben, Secure Cookies nutzen
* User auf allen Tiers authentifizieren (Extern Session ID/intern mappen)
* keine eigenen Krypto Implementationen
* lange Ursername/PW etablieren, failed logins loggen
* Passwörter nicht Klartext speichern oder übermitteln
* PW Recovery Mechanismen sicher umsetzen


**5.1.5. XSS**

Cross-Site Scripting
	Ausführen von eingeschleustem Javascript Code auf einem andern Client
Arten
	Stored
		* Der Code wird serverseitig persistiert und mit der Seite ausgeliefert.
		* Bsp: Ein Angreifer schreibt ein Snippet in ein Gästebuch. Jeder, der die Einträge anschaut, führt das eingebettete Script aus
	Reflected
		* Ein Angreifer schreibt ein Snippet in ein Eingabefeld, das sofort andern Benutzern dargestellt wird
		* Bsp: Search History
Gegenmassnahmen
	* Escaping of output: Steuerzeichen für Scripts Escapen (<,>,',")
	* validate input (reject, delete or replace "dangerious" characters or tags)
	* CSP (Content Security policy)


6 Web Application Security 2
============================

6.1 Injection
-------------

**6.1.1. Port 80 & Firewalls**

Gegen Angriffe auf Application Level über Port 80 nützt eine Firewall nichts. Wenn sie Port 80 blockieren würde, würde aller Verkehr geblockt.


**6.1.2. Angriffe / Layer**

Die unteren Layer sind mittlerweile sehr sicher implementiert und Schwachstellen ausgemerzt. Auf Application Level hingegen werden es mit jeder Applikation, die am Netz hängt neue.


**6.1.3. SQL Injection**

Der Angreifer bricht mit einem Steuerzeichen aus dem Kontext (Value) aus und kann dann fast beliebig Kommandos hnzufügen.

.. code-block:: php

	// search for employee to list them
	$employeeName = $_POST["searchName"];
	$statement = "SELECT name, image FROM employees WHERE name LIKE '%"+$employeeName+"%'";
	
	
Ein Angreifer beendet durch einfügen eines ' das Statement, fügt ein beliebiges Kommando hinzu und kommentiert den Rest aus:

::

	Hans%' UNION SELECT username, password FROM employee WHERE '' == '
	

Dadurch entsteht das folgende Statement, das noch die Benutzernamen und Passwörter der Angestellten ausgibt:

.. code-block:: sql

	SELECT name, image FROM employees WHERE name LIKE '%Hans%' UNION SELECT username, password FROM employee WHERE '' == ''
	
	
**6.1.4. Technische Grundlage**

Siehe Beispiel Vorherige Frage.

Der Angreifer bricht mit ' oder -- aus dem Value-Kontext in den Steuerungskontext aus.


**6.1.5. EXEC**

* Der Angreifer kann alles ausführen, was der DB User auch kann. Kann er z.B. mit EXEC eine Remote Shell aufmachen, kann er beliebig Schadcode nachladen und asführen.
* Zudem kann er Verbindungen aufmachen intern, die nur lokale User können (z.B. Application Server angreifen)


**6.1.6. Blind / Time-Based SQL Injection**

Blind SQL Injection
	Um herauszufinden ob überhaupt Injection möglich ist: illegales Statement produzieren -> Wenn ein Fehler ausgegeben wird, hat die Injection funktioniert, auch wenn ansonsten über eine Injection kein Output ausgegeben werden kann.
Time Based
	An das Statement ein Command anhängen, das länger läuft (z.B. Benchmark). Funktioniert die Injection, verlängert sich die Antwortzeit des Servers -> Wenn keine Blind Injection möglich ist, weil keine Fehlermeldungen ausgegeben werden.
	

**6.1.7. User Defined Functions**

Kann ein Angreifer über Injection User Defined Functions erzeugen, kann er unter Umständen aus der DB ausbrechen und z.B. ein Tunnel nach aussen aufbauen, durch den er weiteren Code ausführen kann.


**6.1.8. Massnahmen gegen Injection**

* Escaping (Steuerzeichen wie ' oder -- escapen) -> keine 100%ige Sicherheit
* White/Blacklisting von Zeichen beim Input -> Nur mittelmässige Sicherheit
* Prepared Statements -> Sicher
* KEINE Dynamischen Prepared Statements!
* Rechte des DB Users beschränken -> darf nur das, was er wirklich muss
* Application Server Rechte einschränken -> darf nur das tun, was er wirklich muss
* Kein direkter Zugriff auf Application- und DB-Server
* Richtiges Error Message Handling


**6.1.9. Prepared Statement Vulnerability**

Kommt innerhalb eines Prepared Statement ein dynamischer Parameter vor, so ist dieser ebenfalls verwundbar.

.. code-block:: php

	$stmt = prepareStatement("UPDATE COFFEES SET SALES=? WHERE COF_NAME "+ "LIKE '" + name + "'"); // insecure usage


6.2 Authentication & Session Management
---------------------------------------

**6.2.1. Begriffe**

Authentication
	Wer Zugriff haben darf auf App
Authorization
	Welche Operationen ein User mit der App machen darf
Identification
	Verifizieren der Identität
	
	
