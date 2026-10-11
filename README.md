# Mein Haushaltsbuch 2.1

[Android-App direkt herunterladen](./Mein-Haushaltsbuch-2.1.apk?raw=true)

Komplett offline ab Android 8. Modernisierte Oberfläche mit großen Bedienelementen und Navigation für Haushalt, Konten und Export. Die App benötigt keine Internetberechtigung.

## Korrektur in Version 2.1

Eine mehrdeutige SQL-Sortierung verhinderte das Öffnen eingerichteter Konten und damit den Zugriff auf die Bearbeitung. Die Kassenbuch-Abfrage verwendet jetzt eindeutige Spaltennamen. Öffnen aller 14 Kassenbücher und nachträgliche Änderungen an Konten mit und ohne Buchungen im Datenbanktest geprüft. Das Datenbankschema ist unverändert.

## Als Update installieren

APK herunterladen, unter Dateien > Downloads öffnen und über die bestehende App installieren. Nicht deinstallieren und keine App-Daten löschen. Paketname und Signierschlüssel sind gleich geblieben. Vorhandene Buchungen bleiben erhalten.

## Einmal die Konten einrichten

Unter Konten den aktuellen Stand jedes Kontos eintragen. Vorbereitet sind:

- Girokonten: Trade Konto, PAF Konto, Keh Konto, Db Konto
- Bargeld
- Sparkonten: PAF Cash, Keh Cash
- Depot: Trade Depot
- Kredite: Skb Kredit, Db Kredit, Db Kreditkarte, SPK Kredit, Plan Kredit, Easybank Kredit

Für Kredite die offene Restschuld positiv eingeben; intern wird sie als negativer Bestand geführt. Der Stichtag des Startsaldos liegt vor oder am Tag der ersten erfassten Kontobuchung. Weitere Konten und Kategorien können jederzeit angelegt werden.

Vorhandene Buchungen aus Version 1 enthalten kein Zahlungskonto. Sie bleiben im Haushaltsbuch mit dem Hinweis Ohne Konto und verändern die neu eingerichteten Kontostände nicht.

## Buchungen und Umbuchungen

Bei einer Ausgabe Betrag, Zahlungskonto und Kategorie wählen. Beispiel: 20 Euro Lebensmittel, bezahlt von Trade Konto. Diese Ausgabe erscheint genau einmal im Haushaltsbuch und reduziert den Kontostand um 20 Euro.

Das Kassenbuch pro Konto zeigt alle Bewegungen mit dem jeweils berechneten Kontostand. Umbuchungen reduzieren das Quellkonto und erhöhen das Zielkonto; sie tauchen nicht als Einnahme oder Ausgabe im Haushaltsbuch auf. Kredit-Tilgungen als Umbuchung reduzieren die offene Restschuld; Zinsen und Gebühren separat als Ausgabe buchen.

Budgetmonat 15.–14. Bei frühem Gehalt kann der Monatsstart nach Bestätigung vorgezogen werden.

## Monatlicher Export

Unter Mehr den Export teilen oder als Datei speichern und monatlich in den gewünschten Analyse-Chat hochladen. Die vollständige SQLite-Datenbank enthält alle Budgetmonate, Kategorien, Konten, Startsalden, Buchungen und Umbuchungen. Die App führt keine Analysen aus und überträgt keine Daten automatisch. Sicherungen aus der alten Version können weiterhin wiederhergestellt werden.

## Prüfstand

APK-Build und Signatur geprüft. Datenbank-Migration, 20-Euro-Ausgabe, Ausschluss von Umbuchungen aus dem Haushaltsbuch, Kredit-Tilgung, Rückgängigmachen und vollständiger Export geprüft. Browser-Tests der lokalen Oberfläche mit Beispieldaten inklusive 320-Pixel-Layout bestanden. Noch kein Test auf einem echten Android-Smartphone.

Das Repository enthält keine Finanzdaten und keine privaten Signierschlüssel.
