=======================================
FS14 InfSi3 Repetitionsfragen Antworten
=======================================

Dieses Dokument wird vorzu erweitert. Ergänzungen und Antworten sind herzlich willkommen.
Repetitionsfragen: https://github.com/moonline/HSR.modules.InfSi3/blob/master/RepetitionQuestions.rst


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

