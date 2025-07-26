# 🧮 Rentenlückenrechner

**Version:** 0.9.1-beta  
**Sprache:** Python  
**Lizenz:**  MIT

📃 Lizenz
Dieses Projekt steht unter der MIT-Lizenz – siehe LICENSE für Details.

👤 Autor
[Steffen Tschirner]
📧 [rlr@hilf-dir-selber.de]
🌐 GitHub: github.com/SteffenTschirner/rentenlueckenrechner


## 📌 Beschreibung

Der **Rentenlückenrechner** ist ein einfaches Programm zur Berechnung der voraussichtlichen Rentenlücke im Alter.
Basierend auf:
- aktuellen Ausgaben
- persönlichen Inflation
- voraussichtlicher Rente laut Renteninformation
  - jährliche prozentuale Erhöhung der Rente bis zum Renteneintritt
  - jährliche prozentuale Erhöhung der Rente während der Rentenbezugszeit 
- Renteneintrittsalter
- Wunschalter
- Eingabe bereits vorhandener Zusatzeinkommen z.B. Zusatzrenten, Versicherungen, Kapitalerträge
  werden die Summe der Einkünfte und Ausgaben während der Rentenbezugszeit ermittelt und daraus die Rentenlücke bzw. ein vorhandener Überschuss errechnet.
- Bei einer vorhandenen Rentenlücke werden drei Beispielsparpläne mit unterschiedlichen Renditen zum Füllen der Rentenlücke ausgegeben.

Die Ergenisse werden anschließend in eine PDF Datei geschrieben.


---

## 🚀 Funktionen

- Kommandozeilenbasiertes Interface
- Berechnung der Rentenlücke
- Export der Ergebnisse als **PDF-Bericht** (via `fpdf`)

---

## 🛠️ Installation

### Voraussetzungen

Für das Ausführen der EXE Datei unter Windows gelten diese Voraussetzungen nicht.
- Python 3.8 oder höher
- fpdf

---

## ▶️ Verwendung

### Windows
rentenlueckenrechner.exe 

### Linux
python rentenlueckenrechner.py

### 📄 Beispielausgabe
```
Rentenlückenrechner


Autor: Steffen Tschirner (rlr@hilf-dir-selber.de)    Version:0.9.1-beta    letzte Änderung:26.07.2025


Das Programm errechnet nach Eingabe der notwendigen Informationen die aktuelle Rentenlücke.
Bitte lesen Sie zuvor die beiliegende Beschreibung die erklärt,
welche Informationen benötigt werden und wie das Programm funktioniert.


Einschränkungen in der aktuellen Version:
(aktuell sind keine Fehler bekannt).



Geben Sie Ihr Geburtsjahr (z.B. 1980) ein: 1969
Geben Sie Ihr Renteneintrittsalter (z.B. 67) ein: 67
Geben Sie Ihr Wunschalter (z.B. 90) ein: 90
-----------------------------------------------------------------------------------
Geburtsjahr: 1969
Renteneintrittsalter: 67
Wunschalter: 90
Aktuelles Jahr: 2025
Sie sind aktuell 56 Jahre alt.
Jahre bis zum Wunschalter: (90): 34
Renteneintritt: 2036
Jahre bis zum Renteneintritt: 11
Jahre mit Rentenbezug: 23
-----------------------------------------------------------------------------------
Geben Sie Ihre aktuellen monatlichen Ausgaben (ohne Investitionen) ein: 2800,01
Ausgaben und Inflation
Monatliche Ausgaben: 2800.01 Euro
Jährliche Ausgaben: 33600.12 Euro
Geben Sie Ihre persönliche Inflation in Prozent ein: 3,25
Persönliche Inflation: 3.25%
Die eingegebene Inflation wird auf die Hochrechnung der Ausgaben angewendet.
-----------------------------------------------------------------------------------
Geben Sie Ihre monatliche Rente (aktuell zu erwartende Rente laut Bescheid RV) ein: 2400,01
Einkommen
Monatliche Rente laut Bescheid RV: 2.400,01 Euro
Die monatliche Rente wird um die Kranken- und Pflegeversicherung (aktuell 14,6%) reduziert.
Ausgezahlte Rente: 2.049,61 Euro. (dieser Wert wird für die Berechnung der Rentenlücke verwendet)
------------------------------------
Geben Sie die jährliche prozentuale Erhöhung der Rente bis zum Renteneintritt ein: 1,01
Geben Sie die jährliche prozentuale Erhöhung der Rente während des Rentenbezugs ein: 1,02
Rentenanpassungen
Jährliche Rentenerhöhung bis zum Renteneintritt: 1.01%
Jährliche Rentenerhöhung während des Rentenbezugs: 1.02%
-----------------------------------------------------------------------------------
Zusätzliche Einkünfte
Sie können jetzt weitere Einkünfte, wie private Renten-, Lebensversicherungen oder andere Einkünfte, eingeben.
Geben Sie den Namen des Einkommens ein (oder 'stop' zum Beenden): DV
Geben Sie das Jahr(YYYY) ein ab dem sie das Einkommen DV erhalten: 2036
Geben Sie die Höhe des monatlichen Einkommens DV ein: 200,02
Geben Sie das jährliche Wachstum in Prozent (0 für kein Wachstum) für DV ein: 0,02
-----------------------------------------------------------------------------------
Geben Sie den Namen des Einkommens ein (oder 'stop' zum Beenden): Kapitalerträge
Geben Sie das Jahr(YYYY) ein ab dem sie das Einkommen Kapitalerträge erhalten: 2036
Geben Sie die Höhe des monatlichen Einkommens Kapitalerträge ein: 2000,01
Geben Sie das jährliche Wachstum in Prozent (0 für kein Wachstum) für Kapitalerträge ein: 3,2
-----------------------------------------------------------------------------------
Geben Sie den Namen des Einkommens ein (oder 'stop' zum Beenden): stop
-----------------------------------------------------------------------------------
Übersicht der monatlichen Einkünfte und Ausgaben zum Renteneintritt:
monatliche ausgezahlte Rente zum Renteneintritt (2036): 2.289,18 Euro
monatliche Ausgaben zum Renteneintritt (2036): 3.980,62 Euro
-----------------------------------------------------------------------------------
Berechnung der Rentenlücke
Während der Rentenbezugszeit von 23 Jahren haben Sie folgende Einkünfte und Ausgaben:
Summe der Renteneinkünfte: 715.253,53 Euro
Zusätzliche Einkünfte durch DV: 55.338,21 Euro
Zusätzliche Einkünfte durch Kapitalerträge: 823.258,17 Euro
Summe der Ausgaben : 1.649.186,21 Euro
-----------------------------------------------------------------------------------
Ergebnis
Die Rentenlücke beträgt: 55.336,30 Euro.
-----------------------------------------------------------------------------------
Beispielrechnung mit 3% Rendite um die Rentenlücke zu schließen
Bei 3% müsste man 11 Jahre lang monatlich 354,36 Euro investieren, um eine Rentenlücke von 55.336,30 Euro zu schließen.

Beispielrechnung mit 7% Rendite um die Rentenlücke zu schließen
Bei 7% müsste man 11 Jahre lang monatlich 279,49 Euro investieren, um eine Rentenlücke von 55.336,30 Euro zu schließen.

Beispielrechnung mit 9% Rendite um die Rentenlücke zu schließen
Bei 9% müsste man 11 Jahre lang monatlich 246,84 Euro investieren, um eine Rentenlücke von 55.336,30 Euro zu schließen.

-----------------------------------------------------------------------------------
Eine PDF Datei mit der Berechnung wurden im aktuellen Verzeichnis erstellt: Rentenluecken-Berechnung_26-07-2025_22-18-11.pdf
``
