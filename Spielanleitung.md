# 🛡 Spielanleitung für die Incident-Response-Tabletop-Übung 🎲  

## 📌 Ziel des Spiels  
Ein Incident-Response-Team muss eine **Cyberattacke** untersuchen, eindämmen und beseitigen, während sich die Infektion weiter ausbreitet.  

- **Der Spielleiter** kontrolliert das "Angreiferbrett" und kann pro Runde neue Infektionen setzen.  
- **Die Spieler** agieren als SOC-Analysten und arbeiten auf ihrem "Verteidigerbrett", um Infektionen zu erkennen, Systeme zu isolieren und das Netzwerk zu sichern.  

---

## 🔹 Vorbereitung  

1️⃣ **Der Spielleiter bereitet das Angreiferbrett vor:**  
- Zeichnet die Infrastruktur ein.  
- Markiert die **initial infizierten Systeme und Angriffsvektoren**.  
- Optional: Legt eine **Infektionsroute** fest (z. B. „Malware springt nach 3 Runden auf den Fileserver“).  

2️⃣ **Die Spieler erhalten ihr Verteidigerbrett:**  
- Es funktioniert ähnlich wie beim Spiel „Schiffe versenken“.  
- Die Spieler haben keine Kenntnis der Infektionen und müssen sie entdecken.  

3️⃣ **Der Spielleiter und die Spieler führen pro Runde Aktionen durch.**  

---

## 🔹 Spielablauf  

### **🔸 Runde 1: Der Vorfall tritt ein**  
- **Optional:** Der Spielleiter gibt den Spielern ein **Start-Event** (z. B. „Ein Benutzer meldet eine Ransomware-Nachricht“).  
- Die Spieler beginnen mit der **Erkennungsphase:**  
  - Sie können Logs untersuchen, betroffene Systeme befragen und analysieren.  
  - Jede bestätigte Infektion wird mit einem **roten Marker** auf dem Verteidigerbrett markiert.  
  - **Der Spielleiter trägt Infektionen nur dann auf dem Verteidigerbrett nach, wenn die Spieler sie durch Analysen aufgedeckt haben!**  

---

### **🔸 Runde 2–X: Untersuchung, Eindämmung & Eskalation**  
- Die Spieler wählen pro Runde eine **begrenzte Anzahl an Aktionen** (siehe „Begrenzung der Aktionen“).  
- Jede Aktion zeigt **erst in der nächsten Runde Wirkung** (z. B. ein Scan aus Runde 2 liefert erst in Runde 3 ein Ergebnis).  
- Der Spielleiter **spielt pro Runde eine neue Infektion aus** (optional nach Schwierigkeitsgrad).  

Beispielablauf für eine Runde:  

1️⃣ **Spieler entscheiden sich für Aktionen** (z. B. Scan, Isolierung).  
2️⃣ **Spielleiter verarbeitet die Aktionen & gibt Ergebnisse der vorherigen Runde bekannt.**  
3️⃣ **Spielleiter trägt eine neue Infektion (wenn nötig) ins Angreiferbrett ein.**  
4️⃣ **Die nächste Runde beginnt.**  

🔻 **Das Spiel endet, wenn:**  
✅ Die Infektion erfolgreich gestoppt wurde.  
❌ Die gesamte Infrastruktur kompromittiert ist (Game Over).  
⏳ Ein gesetzter Zeitrahmen abgelaufen ist.  

---

## 🔹 Begrenzung der Aktionen pro Runde (Ressourcen-Mechanik)  
Jede Runde hat das Team nur eine **begrenzte Anzahl von Aktionen**. Die Ressourcen hängen von der **Teamgröße** und dem **Schwierigkeitsgrad** ab:  

| **Schwierigkeitsgrad** | **Max. Aktionen pro Runde** | **Erklärung** |  
|------------------|----------------------|------------------------|  
| **Leicht**      | 5 Aktionen           | Viele Ressourcen verfügbar, einfaches Handling. |  
| **Mittel**      | 3 Aktionen           | Realistische Ressourcenverteilung. |  
| **Schwer**      | 2 Aktionen           | SOC unterbesetzt, hohe Herausforderung. |  

Beispiel-Aktioen und Beispiel-Kosten eine **Aktionseinheit (AE)**, die das Team verwalten muss.  

| **Aktion** | **Kosten (AE)** | **Beschreibung** |  
|-----------|-------------|----------------|  
| **Erkennen** | 1 AE | Scannt ein System auf Infektion (Ergebnis in der nächsten Runde). |  
| **Isolieren** | 2 AE | Trennt ein Gerät vom Netzwerk. |  
| **Passwort zurücksetzen** | 1 AE | Für kompromittierte Konten. |  
| **Forensik** | 2 AE | Tiefenanalyse eines Systems zur Ursachensuche. |  
| **Patchen** | 2 AE | Behebt eine Schwachstelle, damit sich Malware nicht weiterverbreitet. |  

**👉 Das Team muss diskutieren, welche Aktionen pro Runde am sinnvollsten sind.**  

---

## 🔹 Szenarien & Start-Events  

### **📌 Szenario 1: Ransomware-Attacke**  
🔹 **Beschreibung:**  
Ein Mitarbeiter öffnet eine E-Mail mit einem Anhang, der eine Schadsoftware enthält. Kurz darauf werden Dateien auf mehreren Systemen verschlüsselt, und eine Lösegeldforderung erscheint auf den Bildschirmen der betroffenen Geräte.  
Das SOC-Team muss herausfinden, wie sich die Ransomware ausgebreitet hat, welche Systeme betroffen sind und welche Maßnahmen zur Eindämmung und Wiederherstellung erforderlich sind.  

🎬 **Start-Event:**  
*"Ein Mitarbeiter aus der Buchhaltung meldet sich beim Helpdesk:  
'Mein Rechner ist extrem langsam, und plötzlich sehe ich eine Nachricht auf meinem Bildschirm, dass meine Dateien verschlüsselt wurden. Was soll ich tun?'*  

---

### **📌 Szenario 2: Supply-Chain-Angriff**  
🔹 **Beschreibung:**  
Ein Software-Update eines vertrauenswürdigen Drittanbieters wird ausgerollt, doch kurz darauf treten ungewöhnliche Aktivitäten in der IT-Infrastruktur auf.  
Sicherheitsanalysen zeigen, dass die aktualisierte Software eine **Backdoor** enthält, die Angreifern Zugriff auf interne Systeme ermöglicht.  
Das SOC-Team muss herausfinden, wie weit die Kompromittierung reicht, welche Systeme betroffen sind und welche Maßnahmen zur Eindämmung und Behebung ergriffen werden müssen.  

🎬 **Start-Event:**  
*"Nach einem routinemäßigen Software-Update einer Netzwerkmanagement-Software melden mehrere Systeme ungewöhnliche Netzwerkaktivitäten.  
Ein SIEM-Alarm weist auf verdächtige Verbindungen zu einer bekannten Command-and-Control-Domain hin."*  

---

### **📌 Szenario 3: Insider-Bedrohung**  
🔹 **Beschreibung:**  
Ein Mitarbeiter mit erweiterten Zugriffsrechten kündigt überraschend.  
Kurz darauf bemerkt das Security-Team ungewöhnliche **Datenbewegungen auf einen externen Cloud-Speicher**.  
Die Aufgabe des Teams ist es, festzustellen, ob es sich um einen böswilligen Insider handelt, welche Daten entwendet wurden und welche Maßnahmen zur Schadensbegrenzung und Beweissicherung notwendig sind.  

🎬 **Start-Event:**  
*"Ein Systemadministrator kündigt kurzfristig und gibt an, ab sofort freigestellt zu sein.  
Zwei Tage später zeigt ein interner Sicherheitsbericht, dass große Datenmengen aus der Forschungsabteilung auf einen Cloud-Speicherdienst hochgeladen wurden – kurz vor der Abmeldung des Mitarbeiters."*  

---

### **📌 Szenario 4: DDoS-Angriff**  
🔹 **Beschreibung:**  
Die Hauptwebsite und kritische interne Systeme sind plötzlich nicht mehr erreichbar.  
Erste Analysen zeigen eine **massive Überlastung durch ungewöhnlich hohen Datenverkehr aus verschiedenen Ländern**.  
Das Security-Team muss ermitteln, ob es sich um eine gezielte **DDoS-Attacke** handelt, welche Dienste betroffen sind und wie die Verfügbarkeit der Systeme wiederhergestellt werden kann.  

🎬 **Start-Event:**  
*"Die Website des Unternehmens ist plötzlich nicht mehr erreichbar.  
Die Netzwerküberwachung zeigt eine ungewöhnliche Menge an Anfragen von IP-Adressen aus verschiedenen Ländern."*  

---

## 📜 Lizenz  
Dieses Spiel ist inspiriert von **[Defensomania](https://github.com/Karneades/Defensomania)** und steht unter der **MIT-Lizenz**.  

---

Falls du noch Änderungen möchtest (z. B. Formatierung, weitere Szenarien), sag einfach Bescheid! 😊
