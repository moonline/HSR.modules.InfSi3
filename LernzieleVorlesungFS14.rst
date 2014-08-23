====================================
Lernziele & Chats (Vorlesungsfolien)
====================================

Lernziele, Chats & Fallstudien der Vorlesungsfolien (wo vorhanden).



1 Information Security Management
=================================



2 Location Based Services & Datenschutz
=======================================

* Sie können verschiedene Location Based Servicesund deren Potenzial beschreiben.
* Sie kennen die wichtigsten Punkte des SchweizerDatenschutzgesetzes.
* Sie können die Funktionsweise und Genauigkeitverschiedener Lokalisierungstechnologien erklären.
* Sie haben Ihr Bewusstsein in Bezug auf die Erfassung, Weitergabe und den Schutz (die Sicherheit) von Personendaten «geschärft».


:chat: Zählen Sie Dienste auf, bei welchen Sie Angaben zu Ihrer Position (Standort) an Dritte weiter geben (Web und Mobile).
:Fallbeispiel: Sie beraten eine Anwaltskanzlei in Bezug auf Datenschutzfragen. Die Kanzlei bietet auf ihren Webseiten UsageTracking (z.B. Google-Analytics) und UserFeedback (z.B. Facebook “gefällt mir”) an.

	a) Was weiss wer über die Webseiten-Besucher der Anwaltskanzei?
	b) Was gilt es in diesem Zusammenhang zu beachten?
	
	
:Chat: Handelt es sich bei Lokationsdaten um Personendaten?
:Fallstudie: Die Firma Logistep identifiziert IP-Adressen von Musikdownload Anbietern und gibt deren IP-Adressen an ihre in- und ausländischen Auftraggeber, welche die identifizierten Download-Anbieter mit Strafanzeigen und Schadenersatz-forderungen konfrontieren. Klären Sie ab, ob eine IP-Adresse in der Schweiz in diesem Zusammenhang als Personendatum gilt oder nicht. (BR-Entscheid zum Fall Logistep) 
	
	a) Wie sieht das in Deutschland aus?
	b) Im Google Streetview Entscheid wurde dieses Thema auch behandelt.
	c) Zu welchem Schluss kam man dort?
	
	
:Übung: Ihre Firma hat für die Aussendienstmitarbeiter GPS-Systeme beschafft und will diese auch für Flottenmanagement-Aufgaben und Arbeitszeitüberwachung einsetzen. Wie beurteilen Sie als BDSB diesen Ansatz?
:Chat:  Lokationsdaten auf Smartphone

	a) Wie viele Ihrer Mobile Apps erfassen Lokationsdaten?
	b) Wohin werden diese Daten geschickt?
	c) Wie können Sie überprüfen, ob Lokationsdaten erfasst und
	d) wohin sie geschickt werden?


	
3 Software Security
===================

:Selbststudium: MS Simple SDL



4 Web Application Security
==========================

:Chat: Note sensitive information handeled by web applications (view of application operator and user, give type of sensitivity i.e. C, I, A)

:Chat: Two elements have the same origin, if the protocol, port, and host are the same for both pages. Which of the following elements is considered as same origin as **http://www.company.com/dir/page.html**

	a) http://www.company.com/dir2/other.html
	b) https://www.company.com/secure.html
	c) http://www.company.com/dir/inner/another.html
	d) http://www.company.com:81/dir/etc.html
	e) http://news.company.com/dir/other.html
	
:Solution: SO, not SO (different protocol), SO, not SO (different port), not SO (different host)
	
:Selbststudium: OWASP-Top10MobileSecurityControls.docx

:SelbstStudium: OWASP-MobileThreatModeling.docx

:Chat: Explain what happens when injecting the following inputs

	a) shows?:
	
	   .. code-block:: php
	
		$uname=joe’ -- and $pwd=‘xyz’ SELECT uname FROM accounts 
		WHERE ...
			 
	
	b) shows?:
	
	   .. code-block:: php
	
		$uname=joe and $pwd=‘OR uname = ’joe SELECT uname 
		FROM accounts WHERE ...
			
			
:Solutions:

	a)  $uname=joe’ -- and $pwd=‘xyz’ SELECT uname FROM accounts WHERE uname = ‘joe’ -- ’ AND pwd=‘xyz’ > everything after - - is considered as comment 
	b) $uname=joe and $pwd=‘OR uname = ’joe SELECT uname FROM accounts WHERE uname = ‘joe’ AND pwd=‘‘OR uname = ’joe’ > additional OR statement allows for any check (for known uname or anything true e.g. 1=1)


:Chat: OWASP Application Security Architecture Cheat Sheet https://www.owasp.org/index.php/Cheat_Sheets 

	a) Studieren Sie das OWASP Application Security Architecture Cheat Sheet
	b) Notieren Sie anhand dieser «Checkliste», was in Ihrer SA/BA oder Arbeitsumgebung in Bezug auf die Sicherheit zu beachten wäre:


:Chat: Complete the missing information which is needed to „route“ a client‘s request through the „man-in-the-middle“ Proxy

	.. image:: img/chat1.jpg
	

:Solution:

	* Client -> Proxy: http://www.abc.ch
	* Client Config: HTTP-Proxy = proxy.hsr.ch:8080 for all traffic
	* Proxy -> Server: http:// www.abc.ch



5 HackingLab 1: Injection
=========================



6  Identity & Access Management (Authentication)
================================================

:Chat: Wo müssen Identifikationen und Authentifikation geliefert werden?

:Chat: Give an estimate for your helpdesk cost due to password problems

	.. image:: img/chat2.jpg


7 HackingLab 2: Broken I&A, Session Management
==============================================



8 Mobile Security
=================

* Sie können Sicherheitsprobleme im Smartphone Umfeld beschreiben und mit denjenigen der PC-Welt vergleichen.
* Sie können die Threat Modeling Systematik im Bereich Smartphones anwenden.
* Sie kennen Mobile Security Top 10 Listen und können einzelne Punkte anhand von Beispielen erklären.


:Chat: Moves Application Overview, Use Cases and Users

	a) Was kann/macht die Anwendung
	b) Business Case
	c) Use Case
	d) User
	e) Vertrauensgrenzen
	
:Chat: Data
	
	a) Datentypen
	b) Datennutzer
	c) Datenspeicherung
	d) Anforderungen
	
:Chat: Klassieren Sie die im folgenden aufgeführten Vulnerability Beispiele in die von OWASP Attack Scenarios

	1. Local Memory / Storage based methods
	2. OS and Application Level Methods
	3. Endpoints Based Methods
	4. Communication Channel Based Methods (Wireless interfaces based methods)
	5. Miscellaneous Methods (microphone, camera

:Chat: Inwiefern unterscheiden sich im Privaten Bereich eingesetzte PC – Notebook – Tablet – Smartphones in Bezug auf Sicherheitsaspekte?

	1. Anwendungen (Understand and Describe Application Architecture)
	2. Daten (Identify Security Objectives)
	3. Bedrohungen (Identify Threat Agents)
	4. Angriffsformen, Verletzlichkeiten (Identify Methods of Attack)
	5. Massnahmen (Define Controls)
:Chat: Welche der „Regeln für die Sicherheit Ihres Computers“ beachten Sie auf dem Smartphone?

	1. Firewall muss immer aktiv und aktuell sein
	2. Echtzeit Anti Virus und Anti Spionage Software installieren und aktualisiert halten
	3. Daten sichern und Backup Prozess testen
	4. Starke Passwörter verwenden
	5. Automatische Updates installieren (mindestens vom Betriebssystem, aber auch für Programme)
	6. Nutzungsrichtlinien schulen (z.B. Umgang mit E-Mail, Spam 	und Downloads)
	7. Wichtiges beim Surfen schulen (z.B. Browser Einstellungen, Suchmaschinen, was ist gefährlich und vieles mehr)
	8. Sensitive Daten verschlüsselt abspeichern
	

9 Smartphone Platform & Process Security
========================================

:SelbstStudium: ENISA_Smartphone_Security_Appstores_v28_2013.pdf



10 Sicherheitsüberprüfung
=========================

* Ablauf und wichtige Aspekte bei Sicherheitsprüfungen kennen:
	* Begründung von Sicherheitsprüfungen
	* Prüferhandwerk
		* Ansätze
		* Vorgehen
		* Umfang
		* Prüftiefe
* Erfahrungen aus der Praxis
* “Tipps” für zukünftige Prüfer und Geprüfte
* Übungen: Planung und Durchführung einer Sicherheitsprüfung


:Chat: Scoping: Im Rahmen eines Prüfauftrages soll festgestellt werden, ob die eingesetzten Firewalls einen «angemessenen» Schutz bieten. Geben Sie Beispiele an, was auf den folgenden Ebenen geprüft werden sollte?

	* Prozessebene:
	* Applikationsebene:
	* Infrastrukturebene:

:Solution: Scoping

	* Prozessebene: Ist der Betrieb angemessen organisiert? (Change Management, Incident Management, ...), Einhaltung von Richtlinien, Standards? 
	* Applikationsebene: Sind die Firewall-Regeln sinnvoll und richtig? Sind die Zonen sinnvoll festgelegt (Netzwerk-Architektur)?
	* Infrastrukturebene: Ist die Plattform richtig aufgesetzt (HW, OS, Patches, Updates, System Hardening)

:Chat: Geben Sie Vor- und Nachteile von automatisierten Scans (Scanner) an:

	* Vorteile: 
	* Nachteile: 


:Solution: Scanner

	* Vorteile
		* Sicherstellung der Vollständigkeit
		* Schnelle und günstige Aussage zu Systemzustand (tendenz)
		* Kann Anhaltspunkte für vertiefte Prüfungen geben
		
	* Nachteile
		* Grosse Anzahl von false positives
		* Grosser Aufwand für die Bereinigung der Meldungen. Die Beurteilung von Schwachstellen der Scanner (CVE) kann nicht immer eins zu eins übernommen werden.
		* Aufwändige Arbeit, Risiko-Einschätzung kann nur Ansatzweise durch den Scanner übernommen werden.


11 SSO-Portal
=============


		
12 Online-Banking
=================



13 Forensik
===========


