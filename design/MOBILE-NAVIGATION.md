# Mobile Menünavigation: Touch- und Fokuskorrektur

Stand: 21. November 2026. Änderung an `webseite/index.html`.

## Fehlerbild und Ursache

Bei offenem Menü wurde jeder Fokusverlust außerhalb der Navigation als Schließsignal behandelt, auch `relatedTarget === null`. Ein fehlendes Folgeziel kann bei Touch-Bedienung auftreten. Dann verschwand die Navigation vor dem nachfolgenden Klick: Ein Menülink konnte nicht mehr getroffen werden oder ein Klick auf den Hamburger öffnete das gerade geschlossene Menü wieder.

Die vom Auftraggeber beschriebene Ereignisfolge wurde in einer separaten lokalen Browser-Testseite reproduziert. Das ist kein Nachweis einer bestimmten iOS-/Safari-Version und kein Test auf einem realen iPhone.

## Korrektur

- Gemeinsames `closeNav()` hält Sichtbarkeit, `aria-expanded` und Beschriftung des Hamburger-Buttons synchron.
- `focusout` schließt nur bei einem bekannten Folgeziel außerhalb von Navigation und Hamburger. Ein fehlendes Folgeziel allein löst keine Schließung aus.
- Ein Klick außerhalb schließt das Menü. Klicks auf Navigation oder Hamburger einschließlich deren SVG-Kindelementen werden davon ausgenommen.
- Menülinks schließen beim eigentlichen Klick. Escape schließt weiterhin und setzt den Fokus auf den Hamburger zurück.
- Dieselbe Fokusregel gilt zusätzlich für den Hamburger. Beim Tastaturtest zeigte sich, dass ein Tab-Wechsel vom letzten Menülink über den Hamburger nach außen sonst das Menü offen ließ.
- Keine Touch-Erkennung, keine Verzögerung und kein `preventDefault`; native Linkaktivierung bleibt erhalten. HTML, Gestaltung, Bilder und Vereinsinhalte wurden nicht geändert.

## Prüfung

In der Browser-Testseite lief die tatsächliche HTML-Datei in einem 390 Pixel breiten iframe. Fokus- und Klickereignisse wurden gezielt ausgelöst. Beim kritischen Linktest wurde nach `focusout` mit fehlendem Folgeziel das Element an der tatsächlichen Bildschirmposition des Links ermittelt und angeklickt. Dadurch erkennt der Test das vorzeitige Ausblenden, statt einen bereits unsichtbaren Link direkt zu aktivieren.

Ergebnis: **vorher 10/15, nachher 15/15 Prüfungen bestanden**. Die fünf zuvor nicht erfüllten Prüfungen waren fehlendes Fokus-Folgeziel, anschließender Linktreffer, anschließender Hamburger-Klick, Außenklick sowie Fokuswechsel vom Hamburger nach außen. Ergebnisprotokoll: `MOBILE-NAVIGATION-TEST.json`.

Zusätzlich mit echten Tastendrücken im Browser geprüft: Tab vom letzten Menülink zum Hamburger und weiter zum Seiteninhalt schließt das Menü; Escape schließt und gibt den Fokus an den Hamburger zurück. Die neue JavaScript-Fassung besteht die Syntaxprüfung. Der statische Website-Check meldet keine defekten internen Verweise und keine extern nachgeladenen Medien.

## Grenzen und Abnahme auf dem Gerät

Kein echtes iPhone und kein Safari-/WebKit-Test verfügbar. Die gezielte Regression bestätigt die Korrektur der nachgestellten Ereignisfolge. Nach Neuladen der aktualisierten Seite auf dem iPhone noch prüfen: wiederholt öffnen und schließen, jeden Menüpunkt antippen, außerhalb tippen und erneut öffnen. Die allgemeine Screenreader- und Browserzoom-Abnahme aus `WCAG-CHECK.md` bleibt davon unberührt.

## Referenzen

- [MDN: FocusEvent.relatedTarget](https://developer.mozilla.org/en-US/docs/Web/API/FocusEvent/relatedTarget): ein fehlendes Folgeziel kann auch beim Wechsel aus der Webseite auftreten und ist kein eindeutiges Außenklicksignal.
- [MDN: button – Clicking and focus](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/button#clicking_and_focus): Safari fokussiert Buttons beim Anklicken nicht wie die meisten anderen Browser.
