# 🛡 Mögliche Aktionen und Kosten 🎲  

## 📌 Übersicht  
Während des Spiels können **Verteidiger** (Spieler) und der **Angreifer** (Spielleiter) verschiedene Aktionen ausführen.  
Jede Aktion hat eine **Kostenbewertung (Aktionseinheiten – AE)** und spezifische Auswirkungen auf das Spiel.  

---

## 🔹 **Verteidiger-Aktionen**  

| **Aktion** | **Kosten (AE)** | **Effekt für den Angreifer** | **Effekt für die Verteidiger** |  
|-----------|-------------|----------------|----------------|  
| **Scannen / Alarme prüfen** | 1 AE | Erfolgreich erkannte infizierte Systeme müssen aufgedeckt werden. | Scannt ein System auf Infektion (Ergebnis in der nächsten Runde). |  
| **Isolieren** | 2 AE | Das System ist isoliert und kann nicht mehr für Angriffe genutzt werden. Nach einer Runde ist eine neue Infektion möglich. | Das System ist isoliert, wird bereinigt und ist eine Runde nicht verfügbar. |  
| **Passwort zurücksetzen** | 1 AE | Account kann nicht mehr genutzt werden. | Das Passwort eines Accounts wird zurückgesetzt und kann nicht mehr für Angriffe verwendet werden. |  
| **Forensik** | 2 AE | Ein Infektionspfad (also alle infizierten Geräte) wird offengelegt. | Ein Infektionspfad wird offengelegt. Muss von einer bereits identifizierten Infektion ausgehen. |  
| **Patchen** | 2 AE | Infektions-Kosten für dieses System werden verdreifacht. | Behebt eine Schwachstelle und verhindert erneute Infektion. |  

---

## 🔹 **Angreifer-Aktionen**  

| **Aktion** | **Kosten (AE)** | **Effekt für die Verteidiger** | **Effekt für den Angreifer** |  
|-----------|-------------|----------------|----------------|  
| **Infizieren / Remote Code Execution / Lateral Movement** | 1 AE | Die Verteidiger müssen nun auf ihrem Verteidigerbrett nach diesem System/Benutzer suchen. | Das betroffene System wird infiziert und kann zur weiteren Verbreitung genutzt werden. Drei erfolgreiche Infektionen in einer Zone übernehmen die komplette Zone und erleichtern Escalation. |  
| **Verschlüsselung** | 1 AE | Aktionen, für die diese Systeme gebraucht werden, schlagen fehl. | Erfolgreich infizierte Systeme werden verschlüsselt und stehen nicht mehr für die Verteidigung bereit. |  
| **Denial of Service (DoS)** | 1 AE | Aktionen, für die das System gebraucht wird, schlagen für eine bestimmte Anzahl von Runden fehl. | Das Zielsystem ist für eine bestimmte Zahl von Runden nicht mehr brauchbar. |  
| **Obfuscation** | 2 AE | Forensik schlägt fehl. | Der Angreifer manipuliert Logs oder andere Systemdaten, um die Verteidiger in die Irre zu führen. |  
| **Escalation of Privilege** | 2 AE (1 AE, wenn eine benachbarte Zone komplett übernommen ist) | Die Verteidiger müssen nun auf ihrem Verteidigerbrett nach diesem System/Benutzer suchen. | Der Angreifer erhöht die Rechte des infizierten Systems/Benutzers und dringt so in die nächste Zone vor. |  


---

# 🛡 Infektionspfade für Aktion Infizieren und Escalation of Privilege 🎲  

## 📌 Übersicht  
Diese Tabelle beschreibt die möglichen **Infektionspfade**, die während des Spiels durch die Aktionen **Infizieren** oder **Escalation of Privilege** ausgelöst werden können.  
Einige Angriffe haben **zusätzliche Kosten (AE)**, wenn sie auf komplexere Ziele oder mit erweiterten Methoden durchgeführt werden.  

---

## 🔹 **Infektionspfade für Angriffe**  

| **Startpunkt** | **Vektor** | **Zielzone** | **Beschreibung** | **Aktion(en)** | **Besondere Kosten** |  
|--------------|-----------|-------------|-----------------|------------|-----------------|  
| **Interne Applikationsserver** | Exploit (Zero-Day) | Zentrale Datenbanken | Schwachstelle in einer geschäftskritischen Applikation erlaubt direkten Datenbankzugriff. | Infizieren | +1 AE |  
| **Extern** | Exploit (öffentliche Schwachstelle) | Webserver / DMZ | Angriff auf ungepatchten Apache/Nginx-Server. | Infizieren | — |  
| **AD-Server** | Golden Ticket Attack | Vollständige Infrastruktur | Kerberos-Ticket-Fälschung für unbegrenzten Zugriff. | Escalation of Privilege | — |  
| **Datenbankserver** | SQL Injection | Vertrauliche Daten (z. B. Kundendatenbank) | Daten werden ausgelesen und exfiltriert. | Infizieren | — |  
| **DMZ (Mailserver)** | Phishing (Intern) | Standard Client | Ein kompromittierter Mailserver versendet Phishing-Mails mit Malware-Anhängen an interne Mitarbeiter. | Infizieren | — |  
| **Extern** | Drive-By-Download | Standard Client | Nutzer besucht eine infizierte Website und lädt unbewusst Malware herunter. | Infizieren | — |  
| **Standard Benutzer & Berechtigungen** | Schwachstelle | Standard Client | Ungepatchtes Endgerät wird über eine interne Exploit-Kette kompromittiert. | Infizieren | — |  
| **DMZ (VPN-Gateway)** | Gestohlene Zugangsdaten | Standard Benutzer & Berechtigungen | Angreifer nutzt kompromittierte VPN-Zugangsdaten, um sich ins Firmennetzwerk einzuloggen. | Infizieren | — |  
| **Extern** | Phishing (Extern) | Standard Benutzer & Berechtigungen | Nutzer gibt Anmeldeinformationen preis oder öffnet eine schädliche Datei. | Infizieren | — |  
| **Extern** | Supply-Chain (Manipulierte Software) | Serverinfrastruktur | Ein Update von einem Drittanbieter enthält eine Backdoor. | Infizieren | — |  
| **Remote-Zugriffssysteme** | Exploit auf VPN-/Jump-Host | Netzwerkkomponenten | Kompromittierter VPN-Zugang ermöglicht direkte Angriffe auf Firewalls und Router. | Escalation of Privilege | +1 AE |  
| **AD-Server** | Credential Dumping | Netzwerkgeräte (Firewalls, Router, Switches) | Hashes oder Klartext-Passwörter werden ausgelesen, um Netzwerkgeräte zu übernehmen. | Escalation of Privilege | — |  
| **Extern** | Spearphishing (Extern) | Kritische Benutzer / IT-Admins | Besonders gut gestaltete Phishing Mails. | Infizieren | +1 AE |  
| **Datenbankserver** | SQL Injection | Kerninfrastruktur-Datenbanken | Daten werden aus der zentralen Datenbank exfiltriert oder manipuliert. | Infizieren | +1 AE |  
| **Standard Benutzer & Berechtigungen** | Credential Theft | IT-Admin-Konto | Angreifer nutzt Mimikatz oder Keylogger, um sich Admin-Rechte zu verschaffen. | Escalation of Privilege | +1 AE |  
| **Standard Client** | Pass-the-Hash | IT-Admin-Konto | Angreifer extrahiert Hashes und authentifiziert sich als Admin. | Infizieren | — |  
| **Webserver** | Log4Shell / RCE | Interne Infrastruktur | Angreifer nutzt eine Remote-Code-Execution-Schwachstelle, um internen Code auszuführen. | Infizieren | — |  
| **DMZ (Reverse Proxy)** | Fehlkonfigurierte ACLs | Interne Applikationsserver | Ein falsch gesetzter Zugriffsschutz ermöglicht direkten Zugriff auf interne Ressourcen. | Infizieren | — |  
| **DMZ (Webserver)** | Exploit (ungepatchte Software) | Interne Applikationsserver | Angreifer nutzt bekannte Schwachstellen in Apache, Nginx oder Tomcat aus. | Infizieren | — |  
| **AD-Server** | Privilege Escalation (Golden Ticket Attack) | Hypervisor & Netzwerkkomponenten | Angreifer nutzt Kerberos-Ticket-Fälschung, um sich Domänen-Admin-Zugriff zu verschaffen. | Escalation of Privilege | — |  
| **IT-Admin-PC** | Pass-the-Hash | Hypervisor | Angreifer bewegt sich seitlich über SMB und übernimmt Hypervisor-Steuerung. | Infizieren | — |  
| **Netzwerkgeräte (Router, Firewall, Switches)** | Firmware Backdoor | Gesamte Infrastruktur | Manipulierte Firmware auf einem Netzwerkgerät erlaubt Spionage oder Persistenz. | Infizieren | — |  
| **DMZ (Webserver)** | Web Shell | File Server & Datenbankserver | Ein Angreifer lädt eine Web Shell hoch und erhält Remote-Zugriff auf interne Systeme. | Infizieren | — |  
| **Standard Benutzer & Berechtigungen** | Ransomware | File Server | Infektion über SMB breitet sich aus. | Infizieren | — |  
| **IT-Admin-Konto** | Privilege Escalation | Domain Controller | Admin-Konto wird genutzt, um volle Domänenkontrolle zu übernehmen. | Escalation of Privilege | — |  
| **IT-Admin-Client** | Pass-the-Hash | Domain Admin Rechte | Passwörter werden ausgelesen. | Escalation of Privilege | — |  
| **Extern** | DoS | DMZ (Webserver, VPN-Gateway) | Angriff überlastet externe Dienste mit Anfragen. | Infizieren | — |  
| **DMZ (Webserver)** | SQL Injection | Datenbankserver | Angreifer führt SQL-Befehle aus, um sich Zugang zu sensiblen Daten zu verschaffen. | Infizieren | — |  
| **Standard Benutzer & Berechtigungen** | Schatten-IT | Datenbankserver | Unsicherer Cloud-Speicher (Dropbox, Google Drive) wird missbraucht. | Infizieren | — |  
| **Webserver** | SSRF (Server-Side Request Forgery) | Cloud-Umgebung | Über SSRF können interne Cloud-API-Dienste angegriffen werden. | Infizieren | — |  
| **IT-Admin-Konto** | Skript-Manipulation | Clients | Schadcode wird als „offizielles Update“ verteilt. | Infizieren | — |  
| **Mailserver** | Malware-Weiterleitung | Clients | Ein infizierter Mailserver speichert und verteilt schädliche Anhänge im Unternehmensnetz. | Infizieren | — |  
| **File Server** | Ransomware | Backup-Server | Ransomware verschlüsselt zuerst Produktionsdaten und löscht danach die Backups. | Infizieren | — |  
| **IT-Admin-Konto** | Manuelle Manipulation | Backup-Server | Böswilliger Insider löscht oder manipuliert Backups, um Ransomware-Erpressung zu erleichtern. | Infizieren | — |  

---

## 🎯 **Strategische Überlegungen**  
- **Verteidiger müssen sich auf kritische Zonen konzentrieren, um Eskalationen zu verhindern.**  
- **Angreifer können über mehrere Runden hinweg schrittweise in höhere Sicherheitszonen eindringen.**  
- **Je nach Spielregeln können zusätzliche Infektionskosten für besonders komplexe Angriffe erhoben werden.**  

