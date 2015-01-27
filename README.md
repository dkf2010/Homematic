# Homematic
Homematic Scripts etc.

## Alle Lichter aus v2.hms
Schaltet alle Lichter (o.ä.) aus. Basierend auf den IDs des Schalter-States.

Das übliche "Lichter-Aus"-Script verwende ich nicht. Dies liest per item.state() des aktuellen Wert des Schalters aus. Da ich ein Master-Slav-Script laufen habe, was auf "2 Mal AUS tasten" reagiert, würden bei mir einige Lampen wieder an gehen, wenn das Script alle Schalter aus schaltet, obwohl sie schon aus sind.

Die IDs habe ich mit folgender Erweiterung herausbekommen:
http://www.christian-luetgens.de/homematic/db-access/anwendung/Anwendung.htm

Leider habe ich noch keine Automatik gefunden, die mir die benötigten IDs liefert.

## X als Slave von Y
Schaltet eine Lampe (Slave) ein bzw. aus, wenn die erste Lampe (Master) ausgeschaltet wird, obwohl sie schon aus ist.

Master-Schalter | Master-Lampe | Slave-Lampe
:--|:--|:--
ein|ein|keine Änderung
aus|aus|keine Änderung
aus|aus|ein
aus|aus|aus

Achtung: Das beliebte Script "[Alle Lichter aus](http://www.homematic-inside.de/tecbase/homematic/scriptlibrary/item/alle-lichter-aus)" funktioniert nicht mehr, da dies auch Schalter aus schaltet, obwohl sie schon aus sind.