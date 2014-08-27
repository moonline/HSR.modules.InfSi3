============================================
Top 10 mobile controls and design principles
============================================


.. contents:: Inhaltsverzeichnis


1. Identify and protect sensitive data on the mobile device
===========================================================

:Risiko: Mobilgeräte haben ein grösseres Risiko verloren zu gehen. Ungeschützte sensitive Daten stellen ein entsprechendes Problem dar.

1) **Klassifizierung** von Datastorages nach ihrer Sensitivität und Validierung der Sicherheit von API calls, die auf sensitiven Daten ausgeführt werden
2) Sensitive Daten **serverseitig statt clientseitig speichern**, da verschlüsselte Verbindungen und serverseitige sichere Storages heute weit verbreitet sind.
3) Für lokale Dateien die **File Encrypten API** benutzen. Wird der Verschlüsselungskey durch den Device-Unlock-Key gesichert, so hängt die komplette Sicherheit von diesem ab. Zusätzliche Sicherheit bietet die Möglichkeit zur Remote-entfernung des Verschlüsselungskey für den Diebstahlfall.
4) Sensitive Daten **nicht abspeichern, bevor sie verschlüsselt** wurden
5) Zugriff auf sensitive Daten über **Kontextregeln** absichern (z.B: Die Wallet app kann nur benutzt werden, wenn sich das Gerät im eigenen Land befindet).
6) **GPS/Tracking** Daten nicht länger zurück als für die Applikation erforderlich speichern.
7) **Shared Storages sind unsicher** (Cache, temporary memory, public shared storages such as address book, media gallery, audio files, ...) und sollten nicht für sensitive Daten benutzt werden (z.B: sollten Bilder mit Lokationsdaten nicht in der öffentlichen Gallery abgelegt werden)
8) Für sensitive persönliche Daten sollte ein **regelmässiger Löschvorgang** das Existieren von Daten über den Soll-Zeitraum hinaus verhindern (z.B: Cache)
9) Es gibt keine **Löschvorgänge für Flash Memory**, entsprechend sind sicheres Key management und Datenverschlüsselung besonders wichtig.
10) Die **Sicherheit von Daten** sollte über ihren gesammten **Lebenszyklus** berücksichtigt werden.
11) **Minimale Offenheit** bezgl. Daten: Nur Daten sammeln, die wirklich notwendig sind für die Applikation.
12) **Nicht-persistente Identifiers** verwenden innerhalb Apps oder für sessions/cookies, die nicht mit andern Apps geteilt werden (z.B: nicht die Device ID als identifier verwenden, wenn nicht unbedingt nötig).
13) Apps auf Managed Devices sollten die **remote Wipe- und Kill-Switch API** benutzen, um sensitive Daten bei Geerätverlust zu löschen.
14) Für applikationsspezifische Kill-Switch mechanismen muss eine **starke Authentisierung** umgesetzt werden, um Missbrauch zu verhindern.



2. Handle password credentials securely on the device
=====================================================

:Risiko: Spyware, Überwachung, Finanzmalware: Benutzer Credentials erlauben wenn gestohlen nicht nur Zugriff auf das Gerät selbst sondern kompromitieren möglicherweise auch noch andere Services und vom Benutzer benutzte Accounts.


1) **Tokens anstelle Passwörtern** verwenden (sicherh auf dem Gerät speichern und per TLS übertragen). Tokens sollten immer an einen Service gebunden sein und es sollte die neuste Version der Authoriserungsstandards benutzt werden.
2) **Verschlüsselung und Key Strage des OS**, wenn Passwörter unbedingt auf dem Device gespeichert werden müssen.
3) Wenn vorhanden **Secure Elements** (z.B: speziell verschlüsselte SD Karten module) als Storage nutzen.
4) Dem Benutzer ermöglichen, Passwörter zu wechseln auf dem Gerät.
5) Passwörter und Credentials dürfen nur verschlüsselt oder gehashed in gewöhliche **Backups** eingebunden werden.
6) Visuelle Passwörter ermöglichen höhere Entropie (einfacheres Erinnern für User), sollten aber nur verwendet werden, wenn die Entropie gewährleistet werden kann.
7) Swipe-based Passwörter sind für **Smudge-Attacken** (Fettspuren auf dem Display) verletzlich. Massnahmen wie das erlauben von Musterwiederholung sollten gegen Smudge-Attacken eingesetzt werden.
8) Die **Entropie** von allen Passwörtern überprüfen, auch visuellen
9) Keine Secrets in **App Binaries** speichern.


3. Ensure sensitive data is protected in transit
================================================

:Risiko: Netzwerkspoofing Attacken, Überwachung. Sensitiven Daten auf unsicheren Channels können abgefangen werden.


1) **Provider Netzwerke und Wi-Fi's** sind unsicher.
2) Apps sollten **End-zu-End Kanäle** wie TLS verwenden um sensitive Daten zu übertragen.
3) Starke und gut bekannte **Verschlüsselungsalgorithmen** wie AES verwenden.
4) **Zertifikate** von vertrauenswürdigen CA Anbietern verwenden. Vorsicht mit self-signed Zertifikaten. TLS Kette immer validieren und niemals deaktivieren.
5) Nur Verbindungen mit Remote Endpunkten aufbauen, deren **Identität verifiziert** wurde (z.B. mit Zertifikaten).
6) Der Benutze sollte im UI einfach erkennen, ob ein **Zertifikat valide** ist.
7) Über **SMS oder MMS** sollten keine sensitiven Daten versendet werden.


4. Implement user authentication, authorization and session management correctly
================================================================================

:Risiko: Unauthorisierte Individuen können Zugriff auf sensitive Daten erhalten


1) **Starke Authentisierung** verlangen. Dem Benutzer Feedback für z.B. Passwortsicherheit geben. Die stärke der Authentisierung sollte von der sensitivität der Daten abhängen.
2) Garantieren, das das **Session management** richtig funktioniert.
3) **Nicht erratbare Session Identifiers** mit hoher Entropie verwenden. Sicher Seeds für Zufallszahlengeneratoren benutzen (nicht Datum+Uhrzeit, sondern z.B. Datum und Uhrzeit vermischt mit anderen Sensorwerten).
4) **Kontext** wie z.B. IP Location benutzen um die Sicherheit von Authentication zu erhöhen
5) **Mehr-Faktor Authentisierung** verwenden wo möglich
6) Authentication sollte auf der **User Identität** und nicht auf der Device Identität basieren


5. Keep the backend APIs (services) and the platform (server) secure
====================================================================

:Risiko: Angriffe auf Backend Systeme und Datenverlust wie Cloud-Systeme.


1) Checks einsetzen, ob **sensitive Daten an einen Service übermittelt** werden (z.B. Lokationsdaten in Bildern)
2) Alle Backend Services sollten **periodisch auf Verletzlichkeiten geprüft** werden, z.B. mit statischen Code Analysen und Fuzzy Testing
3) Gewährleisten, das der Backend Service mit einer **zuverlässigen/etablierten Konfiguration** und den neusten **Sicherheitspatches** läuft.
4) Gewährleisten, das Backend Server Angriffe loggen
5) Rate limiting und throttling per user/IP umsetzen um DDoS Angriffe zu minimieren
6) Auf DoS Verletzlichkeiten testen
7) Web Services, REST and API's auf abuse cases und Vulnerabilities testen


6. Secure data integration with third party services and applications
=====================================================================

:Risiko: Daten Leakage.


1) Die Sicherheit / **Vertrauenswürdigkeit** jeder 3rdParty Library/Code in der eigenen App überprüfen.
2) 3rdParty Library/Codes auf **Sicherheitpatches** überwachen und einspielen
3) **Daten validieren**, die von 3rdParty Apps geliefert werden, bevor die Applikaton sie verarbeitet.


7. Pay specific attention to the collection and storage of consent for the collection and use of the user’s data
=================================================================================================================

:Risiko: Ungewolltes preisgeben von persönlichen oder privaten Informationen, illegale Datenverarbeitung


1) **Privacy policy** einführen, dem User verfügbar machen, wenn er sein Einverständnis für einen Zugriff geben muss
2) **Einverständnisse** können auf verschiedene Arten zusammengafasst werden:
	* Zum Installationszeitpunkt
	* Zur Laufzeit wenn Daten übermittelt werden
	* Voreinstellungen, die der User nach Bedarf umstellen kann
	
3) Überprüfen, ob Apps **Einwilligungen sammeln**
4) **Kommunikation überprüfen**, um unbewusst freigegebene Daten aufzudecken
5) Einwilligung zur Übertragung von Daten speichern und dem Benutzer bei jeder **Übertragung wieder anzeigen**
6) Überprüfen, ob sich einzelne **Einwilligungen überlappen oder im Konflikt stehen**


8. Implement controls to prevent unauthorized access to paid-for resources (wallet, SMS, phone calls etc.)
=================================================================================================================

:Risiko: Apps geben automatischen Zugriff auf Premium Dienste (kostet)


1) **Logs** von Zugriff auf zahlungspflichtige Ressourcen in einem nicht manipulierbaren Format speichern und dem user für Monitoring zur Verfügung stellen
2) Benutzung von zahlungspflichtige Ressourcen auf **ungewöhnliche Benutzungsmuster** scannen und Reauthentication detektieren
3) **White-listing** verwenden für zahlungspflichtige Ressourcen, z.B. Anrufe, SMS
4) **API Calls** für zahlungspflichtige Ressourcen **authentisieren**
5) Sicherstellen, das Wallet API calls **keine Klartextinformationen** übermitteln
6) Den Benutzer **warnen und Einwilligung** verlangen für kostenpflichtiges App Verhalten
7) **Best Practises** wie "Fast dormancy", "caching" etc. implementieren um die Signallast für die Basisstation minimal zu halten


9. Ensure secure distribution/provisioning of mobile applications
=================================================================

:Risiko: Alle in diesem Dokument aufgeführten Risiken denkbar


1) Apps müssen so designed werden, dass sie **update für sicherheitspatches** erlauben
2) Apps über **offizielle AppStores** ausliefern (bieten Malware Scan)
3) **Feedback Channels** für User anbieten für Sicherheitsprobleme


10. Carefully check any runtime interpretation of code for errors
=================================================================

:Risiko: Zur Laufzeit interpretierter Code ermöglicht das einschleusen und ausführen von ungeprüftem Schadcode.


1) **Runtime code interpretation minimieren**, Interpreter mit minimalen Rechten laufen lassen
2) Umfassende **Escape-Syntax** angemessen definieren
3) Interpreter **Fuzzy-testen**
4) Interpreter **sandboxen**


Anhang & Referenzen
===================

Siehe Originaldokument
