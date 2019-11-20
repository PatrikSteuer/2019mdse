## Praktische Aufgabe: Docker-Image
Ihre Aufgabe ist es ein Docker-Image zu erzeugen, das einen Webserver enthält, der Markdown-Dateien als HTML gerendert darstellen kann.

### Anforderungen
* Der Webserver soll auf Port 8080 innerhalb des Containers laufen.
* Das Image soll die anzuzeigenden Markdown-Dateien über einen Volume-Mount akzeptieren. 
* Das Image soll auf Basis des Parent „alpine:latest“ erstellt werden (Befehl: „FROM alpine:latest“).
* Das Image soll durch folgenden Befehl zu starten sein: `docker run -v <lokaler/pfad/mit/markdown-dateien>:/markdown -p 8080:8080 <ihr_image>`.
* Danach soll mit dem Browser unter `http://localhost:8080` eine Übersicht der verfügbaren Markdown-Dateien angezeigt werden.

**Anmerkung:** Die Verwendung von open-source Komponenten um diese Aufgabe zu bewerkstelligen ist ausdrücklich erwünscht. Beispielweise können Sie folgenden Markdown-Server innerhalb ihres Docker-Images verwenden: `https://github.com/ohbarye/markdown-server`.

### Bewertung
Es sind ingesamt 4 Punkte zu erreichen, die sich auf folgende Teilaufgaben verteilen:
* Ein Dockerfile das erfolgreich mit "docker build" gebaut werden kann
* Ein Webserver der auf Port 8080 innerhalb des Containers läuft
* Der Webserver kann eine Markdown-Datei interpretieren und als HTML darstellen
* Das mounten eines Ordners mit Markdown-Dateien z.B. mit dem Befehl „docker run -v <lokaler/pfad/mit/markdown-dateien>:/markdown“ ist möglich. Der Webserver interpretiert die enthaltenen Markdown-Dateien korrekt.

### Abgabe 
Alle für den build des Image benötigten Dateien als ein .zip File per E-Mail.