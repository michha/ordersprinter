# Speicherkarte vorbereiten
* https://www.raspberrypi.org/downloads/noobs/
* _Noobs Lite_ herunterladen, auf (formatierte) Speicherkarte entpacken

# Raspbian Installation
* starten
* Raspbian auswählen (nicht Full)

# Raspbian Konfiguration
## nach der Basis-Installation
- VNC Interface aktivieren (Settings => Raspberry-Pi-Configuration => Interfaces: VNC)

## Pakete aktualisieren
`sudo apt-get update && sudo apt-get upgrade`

`sudo apt-get update && sudo apt-get dist-upgrade`

## Statische IP konfigurieren
https://electrondust.com/2017/11/25/setting-raspberry-pi-wifi-static-ip-raspbian-stretch-lite/

# OrderSprinter
## Webserver
TODO

## Java Printserver
1. Java Installation: `sudo apt-get install -y galternatives openjdk-8-jdk`
1. Prüfen mit `java --version`
1. Bestehende config.json in neue Datei zB _config_speisen.json_ kopieren
1. Folgende Parameter bearbeiten:
  - _printersize_ (bei Epson TM-T20II) auf 48
  - _printcode_ ändern (muss dann im UI eingetragen werden)
  - _baseurl_ auf statische IP des Webservers
  - _smallformat_ auf 1
3. Drucker starten über `sudo java -jar javaprinter.jar config_speisen.json`
