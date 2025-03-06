Ein tabellarisches **Spielfeld-Protokoll** könnte als eine Art **Incident-Tracking-Sheet** aufgebaut sein, das sowohl die **aktuellen Zustände der Systeme** als auch die **durchgeführten Aktionen pro Runde** dokumentiert.  

Zwei Vorschläge:  

1️⃣ **Token-System auf einem echten Spielfeld** (Physische Lösung)  
2️⃣ **Tabellarisches Protokoll** (Digitale Lösung)  

---

## **1️⃣ Token-System für ein physisches Spielfeld** 🏴‍☠️  
- Jedes System wird auf einem **gedruckten Spielfeld** als Kärtchen oder Feld dargestellt. Beispiele:
- **Tokens oder Marker** zeigen den aktuellen Status:  
  - 🔴 **Infiziert (1x)**  
  - 🔥 **Kritisch (2x infiziert)**  
  - ⚠️ **Zone übernommen (3x infiziert → gesamte Zone fällt)**  
  - 🛑 **Isoliert**  
  - 🛡 **Gepatcht**  
- Aktionen (z. B. Scannen, Isolieren) können durch kleine farbige Chips oder Karten dargestellt werden.  

**Vorteile:**  
✅ **Visuell greifbar** → Spieler sehen sofort, welche Systeme betroffen sind.  
✅ **Schnelle Anpassung** → Tokens können leicht verschoben oder geändert werden.  
✅ **Mehr Dynamik** → Spieler können gemeinsam diskutieren und das Spielfeld verändern.  

---

## **2️⃣ Tabellarisches Protokoll für den digitalen Ablauf** 📝  
Falls das Spiel **rein tabellarisch geführt wird**, könnte die Tabelle so aufgebaut sein:  

### **🔹 Beispiel für eine Incident-Protokoll-Tabelle**  

| Runde | System / Zone          | Status vorher  | Aktion Verteidiger | Aktion Angreifer | Status nachher |
|-------|------------------------|---------------|--------------------|-----------------|----------------|
| 1️⃣   | Webserver (DMZ)        | 🟢 Gesund     | 🔍 Scan           | 🎭 Infizieren   | 🔴 Infiziert (1x) |
| 1️⃣   | AD-Server (Zone 1)      | 🟢 Gesund     | -                 | 🚀 Phishing     | 🟢 Gesund |
| 2️⃣   | Webserver (DMZ)        | 🔴 Infiziert  | 🛡 Patch          | 🎭 Infizieren   | 🔴 Infiziert (bleibt) |
| 2️⃣   | AD-Server (Zone 1)      | 🟢 Gesund     | -                 | 🔥 Escalation  | 🔴 Infiziert (1x) |
| 3️⃣   | Webserver (DMZ)        | 🔴 Infiziert  | 🛑 Isolieren      | -               | 🟡 Isoliert |
| 3️⃣   | AD-Server (Zone 1)      | 🔴 Infiziert  | -                 | 🎭 Infizieren   | 🔥 Kritisch (2x) |
| 4️⃣   | AD-Server (Zone 1)      | 🔥 Kritisch   | 🔍 Forensik       | 🎭 Infizieren   | 💀 Zone übernommen |

---

### **🔹 Erklärung der Spalten**  
- **Runde:** Zählt die Spielrunden.  
- **System / Zone:** Welche Infrastruktur betroffen ist.  
- **Status vorher:** Zeigt den Zustand vor dieser Runde.  
- **Aktion Verteidiger:** Zeigt durchgeführte Verteidigungsmaßnahmen.  
- **Aktion Angreifer:** Welche Angriffe ausgeführt wurden.  
- **Status nachher:** Endstatus nach Verarbeitung der Aktionen.  

**Legende für Status-Symbole:**  
🟢 Gesund → Das System funktioniert normal.  
🔴 Infiziert (1x) → Das System wurde angegriffen und infiziert.  
🔥 Kritisch (2x) → System ist stark kompromittiert.  
💀 **Zone übernommen** → Die gesamte Sicherheitszone ist unter feindlicher Kontrolle.  
🟡 Isoliert → Das System wurde vom Netzwerk getrennt.  
🛡 Gepatcht → Die Schwachstelle wurde behoben.  

---

### **🔹 Vorteile der Tabellarischen Lösung:**  
✅ **Digitale Nachverfolgbarkeit** → Einfache Dokumentation für spätere Analysen.  
✅ **Gute Übersicht über Infektionsketten** → Man sieht genau, wann sich etwas ausbreitet.  
✅ **Automatisierbar (Google Sheets, Excel)** → Status kann leicht aktualisiert werden.  

---

## **🔹 Welche Lösung passt besser?**  
📌 **Token-Spielfeld** → Wenn das Spiel **physisch mit echten Karten und Markern gespielt wird**.  
📌 **Tabellarisches Protokoll** → Wenn das Spiel **in einem digitalen Format (Excel/Sheets)** gespielt wird.  
