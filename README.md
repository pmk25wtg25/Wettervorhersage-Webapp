# Nordwetter

Nordwetter ist eine schlanke Wetterübersicht für den Browser. Die App zeigt die aktuellen Bedingungen, den Sonnenverlauf und eine Vorhersage für die kommenden drei Tage.

Die Oberfläche, Gestaltung und Logik befinden sich vollständig in einer einzigen HTML-Datei.

## Start

Die Anwendung kann direkt über `index.html` geöffnet werden. Für das Laden der Wetterdaten ist eine Internetverbindung erforderlich.

Wenn der Browser den direkten Zugriff über `file://` einschränkt, die App aus dem Projektordner über einen lokalen Server starten:

```bash
python3 -m http.server 8000
```

Danach im Browser `http://localhost:8000` aufrufen.

## Bedienung

    1. Einen Ort in das Suchfeld eintragen und die Abfrage starten.
    2. Einen der voreingestellten Orte Berlin, Hamburg oder München auswählen.
    3. Die gewünschte Temperatureinheit festlegen.
    4. Bei Bedarf zwischen hellem und dunklem Erscheinungsbild wechseln.

Die Wetterkarte zeigt neben der aktuellen Temperatur auch Wind, Luftfeuchtigkeit, Sichtweite, Luftdruck, Niederschlag, UV-Index und Sonnenzeiten.

## Dateien

    index.html    komplette Anwendung mit HTML, CSS und JavaScript
    README.md     Projektdokumentation

Es gibt keine weiteren lokalen Abhängigkeiten und keine erforderliche Installation.

## Verbindung und Datenschutz

Die Wetterdaten werden direkt von `https://wttr.in` geladen. Für eine Suche wird der eingegebene Ort an diesen Dienst übermittelt. Konten, API-Schlüssel und eigenes Tracking verwendet die App nicht.

Gespeichert wird lediglich die zuletzt gewählte Darstellung für den Hell- oder Dunkelmodus im lokalen Browser. Wetterdaten oder persönliche Profile werden nicht angelegt.

## Datenquelle und Technik

Die Abfrage verwendet den JSON-Endpunkt `https://wttr.in/<ORT>?format=j1`.

Die Anwendung basiert auf HTML, CSS und Vanilla JavaScript.
