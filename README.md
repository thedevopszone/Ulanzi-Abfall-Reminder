# Ulanzi-Abfall-Reminder
einfache Überwachung und Anzeige Abfalltermine auf "Ulanzi Pixel Clock mit Awtrix Light"


https://github.com/Deepintheeast/Ulanzi-Abfall-Reminder/assets/136626582/b3f03a60-cecd-4f2b-96ce-ce9eb8b0d0ae


das Script wird bei mir einmal täglich per Cron über ein Shellscript aufgerufen

``01 17  *  *  *    /home/pi/scripts/Ulanzi-Abfall-Reminder/start.sh    >/dev/null``

und checkt ob für den "morgigen" Tag Abholtermine anstehen.

Ist das der Fall erhalte ich eine entsprechende "Notifikation" auf dem Ulanzi die erst wieder weg geht wenn
man diese durch Druck der mittleren Taste am Ulanzi bestätigt!



Die Entsorgungstermine im "CSV Format" bekomme ich von der Website meines Entsorgers.

Sie müssen für jede "Tonne" als seperate Datei, im selben Verzeichnis wie das Script, vorhanden sein <br> (gelb.csv , blau.csv , rest.csv , bio.csv) <br>und folgendes Format haben:

```
Blaue Tonne 
02.01.2023 
30.01.2023 
27.02.2023 
27.03.2023 
24.04.2023
22.05.2023
19.06.2023
17.07.2023
14.08.2023
11.09.2023
09.10.2023
06.11.2023
04.12.2023
```

Der Eintrag in der ersten Zeile stört nicht und kann so bleiben!
