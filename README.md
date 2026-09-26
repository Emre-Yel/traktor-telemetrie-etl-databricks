# Traktor-Telemetrie-Pipeline (Databricks/PySpark)

Simuliertes Data-Engineering-Projekt zur Verarbeitung von Sensordaten landwirtschaftlicher 
Maschinen nach dem Medallion-Architektur-Prinzip (Bronze/Silver/Gold), umgesetzt in 
Databricks mit PySpark.

## Hintergrund
Das Projekt simuliert Telemetriedaten (Motortemperatur, Drehzahl, Kraftstoffverbrauch) 
von Traktoren, wie sie in der Praxis von Sensoren erfasst werden könnten. Die Daten sind 
künstlich generiert und enthalten bewusst eingebaute Fehler (fehlende Werte, unrealistische 
Ausreißer), um einen realistischen Bereinigungsprozess zu üben.

## Architektur
- **Bronze-Schicht:** Rohdaten mit simulierten Sensorfehlern
- **Silver-Schicht:** Bereinigte Daten (fehlerhafte Werte gefiltert, fehlende Werte entfernt), 
  ergänzt um eine Warnindikator-Spalte für kritische Motortemperaturen
- **Gold-Schicht:** Aggregierte Kennzahlen pro Maschinenmodell (Ø Temperatur, Verbrauch, 
  Anzahl kritischer Überhitzungen), verknüpft mit Maschinen-Stammdaten

## Tech Stack
PySpark, Databricks, Matplotlib, Pandas

## Hinweis
Dies ist ein Lernprojekt mit synthetisch generierten Daten, kein echter Datensatz.

## Screenshot
<img width="714" height="451" alt="image" src="https://github.com/user-attachments/assets/f93ff1ab-a0fc-45b6-8d54-f5006ac33aaf" />
