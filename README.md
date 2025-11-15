# Dynamic Research Slots Reborn
Dieses Repository enthaelt die ueberarbeitete und erweiterte Version der Mod **"Dynamic Research Slots Reborn"** fuer *Hearts of Iron IV*.

## Was die Mod macht (fuer Spieler)

- Die Anzahl deiner Forschungsslots ist nicht mehr statisch, sondern haengt von deiner **Industrie** ab.
- Zivile Fabriken, Militaerfabriken, Werften und **Experimentalfabriken** liefern sogenannte **Research Power (RP)**.
- Wenn deine RP bestimmte Schwellen ueberschreitet, erhaelst du zusaetzliche Forschungsslots.
- Ein Teil der Slots sind **Easy Research Slots**: Sie sind leichter zu halten (benoetigen weniger RP).

Im Spiel findest du:

- Eine **Entscheidung** in der Kategorie `dynamic_research_slots_decisions`, die dir eine Uebersicht deiner aktuellen RP und der naechsten Schwelle anzeigt.
- Eine **HELP-Entscheidung**, die ein Popup mit einer ausfuehrlichen Erklaerung aller Mechaniken oeffnet.
- Einen eigenen **Custom Game Rules-Tab** "Dynamic Research", in dem du globale Einstellungen fuer Easy Slots und RP-Faktoren anpassen kannst.

## Installation & Nutzung

- Die Mod wird wie ueblich ueber den HOI4 Launcher geladen (Steam Workshop / lokale Mod-Datei).
- Stelle sicher, dass die Mod nach anderen grossen Overhaul-Mods geladen wird, die eigene Research-Slot-Mechaniken haben koennten.
- Die Mod ueberschreibt keine Vanilla-Tech- oder Fokusbaeume, sondern arbeitet ueber **scripted_effects**, **on_actions**, **decisions** und **game_rules**.

## Unterstuetzte Version / Kompatibilitaet

- Zielversion: aktuelle HOI4-Version zum Zeitpunkt der letzten Aktualisierung dieses Repos.
- Die Mechanik ist bewusst generisch gehalten und sollte mit den meisten Content-Mods kompatibel sein, solange diese nicht ebenfalls massiv an Forschungsslots und den zugrundeliegenden Engine-Mechaniken drehen.

## Konfiguration im Spiel (Custom Game Rules)

Im Custom-Game-Rules-Menue findest du u.a.:

- **Easy Research Slots (Base)** - zusaetzliche Easy Slots fuer alle Laender.
- **Easy Slot RP Cost Factor** - wie viel RP ein Easy Slot im Vergleich zu einem normalen Slot kostet.
- **Factory Weights** - wie stark Zivil-/Militaerfabriken und Werften gewichtet werden.
- **War RP / Alliance RP** (falls aktiviert) - globale Modifikatoren fuer Forschung in Kriegszeiten bzw. in Allianzen.

Nicht-Standard-Optionen koennen in einigen Faellen **Achievements deaktivieren** (siehe Game-Rules-Beschreibung im Spiel).

## Fuer Modder / technische Dokumentation

Wenn du die Mod erweitern, balancieren oder in eine groessere Mod integrieren moechtest, lies bitte die technische Uebersicht:

- `DYNAMIC_RESEARCH_SLOTS.md` - detaillierte Beschreibung der internen Logik (Research Power, Schwellenwerte, Easy Slots, Game Rules, Debug-Tools usw.).

Wichtige Skriptdateien:

- `common/scripted_effects/00_dynamic_research_slots_scripted_effects.txt` - zentrale RP-Berechnung, Slot-Logik und Modifier.
- `common/on_actions/00_dynamic_research_slots_on_actions.txt` - Verankerung im Spielablauf (Start / taegliche Updates).
- `common/decisions/*.txt` und `events/dynamic_research_slot_events.txt` - UI, Hilfe-Popup, Debug-Overlay.
- `common/game_rules/00_dr_dynamic_research_rules.txt` - Konfiguration per Custom Game Rules.

## Weiterentwicklung

- Aenderungen sollten nach Moeglichkeit in den bestehenden Effekten und Variablen stattfinden, um die Debug-Tools und die bestehende Dokumentation nutzbar zu halten.
- Fuer neue RP-Quellen (Ideen, National Spirits, Technologien usw.) bitte sowohl die tatsaechliche Berechnung als auch die Anzeige-Variablen (z.B. `facility_research_power` oder neue Variablen) erweitern.

Weitere technische Hintergruende findest du in `DYNAMIC_RESEARCH_SLOTS.md` und in der begleitenden PDF "Technische Dokumentation - Modding in Hearts of Iron IV (HOI4)".
