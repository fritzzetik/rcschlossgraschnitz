# Barrierefreiheitscheck nach WCAG 2.2 AA

Prüfdatum: 9. November 2026. Gegenstand: die statische Vereinswebsite, Startseite und alle 13 verbleibenden internen Vereinsunterseiten. „Gewährleistung“ und „Widerruf“ wurden auf ausdrücklichen Wunsch des Auftraggebers entfernt.

## Ergebnis

Die gezielte Prüfung hat konkrete Barrieren gefunden und zu Korrekturen geführt. Die nachfolgend gemessenen HTML-Textkontraste, schmalen Layouts und geprüften Tastaturabläufe sind nach der Überarbeitung unauffällig. Daraus folgt keine vollständige WCAG-Konformitätserklärung: insbesondere echte Screenreader-Nutzung, nativer Browserzoom und alle visuellen Zustände sind noch nicht vollständig geprüft.

## Befunde und Korrekturen

| Bezug | Befund vor der Korrektur | Umsetzung und Nachprüfung |
| --- | --- | --- |
| 1.1.1 Nicht-Text-Inhalt, A | 217 Bildvorkommen hatten nur eine allgemeine Beschreibung mit „Vereinsaufnahme“. | Für alle 219 übernommenen Bilddateien wurden motivbezogene Alternativtexte hinterlegt; 222 Bildvorkommen einschließlich Wiederverwendungen aktualisiert. Keine dieser allgemeinen Beschreibungen mehr vorhanden. Zuordnung in `BILDTEXTE.csv`. Namen von Schulpferden nur aus der bestehenden Zuordnung übernommen; unbekannte Menschen nicht identifiziert. |
| 1.1.1 und 1.4.5 Bilder von Text, A/AA | Angebotsdetails, Preise und Termine standen teilweise ausschließlich in Grafiken. | Sechs Grafiken erhielten vollständige sichtbare HTML-Textfassungen. Historische Veranstaltungen von 2025 sind mit ihrem Datum beschrieben. Die übrigen Preise bleiben Angaben aus den bestehenden Grafiken und sind dadurch nicht neu bestätigt. |
| 1.4.3 Kontrast, AA | Vier Datumsangaben im Pressebereich: 4,428:1. Fußzeile: 4,427:1. Beide unter 4,5:1. | Textfarbe auf `#526174` geändert. Nachmessung: 5,592:1 auf `#f3f1e9` und 6,003:1 auf `#faf9f5`. Keine weiteren Unterschreitungen in den gemessenen normalen HTML-Textzuständen der Startseite und 13 Unterseiten. |
| 2.5.3 Beschriftung im Namen, A | Sichtbar „Ersten Reittermin vereinbaren“, hinterlegt „Ersten Reittermin telefonisch vereinbaren“. | Abweichendes `aria-label` entfernt. Der zugängliche Name stammt nun direkt aus dem sichtbaren Buttontext einschließlich Ansprechpartner und Telefonnummer. |
| 1.4.12 Textabstände, AA; 1.4.10 Umbruch, AA | Bei den W3C-Testabständen und 320 Pixel Breite liefen Navigation und lange Wörter über den Bildschirmrand. | Flexible Kopfzeile, Umbruch langer Wörter, flexible Inhaltsraster und FAQ-Zeilen. Kein horizontaler Überlauf auf Startseite und 13 Unterseiten in der Textabstands-Testkopie. |
| Tastaturbedienung von Bildern, 2.1.1, A | Einzelne noch nicht geladene Bilder hatten Bildbuttons mit 0 × 0 Pixeln. | Intrinsische Bildgrößen ergänzt und Bildbuttons in Einzelfiguren vor dem Laden dimensioniert. Am letzten Kinderangebotsbild erneut geprüft: bedienbare Fläche vor dem Laden, Öffnen mit Enter, Schließen mit Escape, Fokus kehrt zum Auslöser zurück. |

## Weitere Verbesserungen der Orientierung

- Das mobile Menü setzt den Fokus beim Öffnen auf den ersten Eintrag, schließt bei Verlassen der Navigation und lässt sich mit Escape schließen.
- Interne Unterseiten bekommen einen zum Inhalt passenden Dokumenttitel, etwa „Impressum · Reitclub Graschnitz“.
- Auf internen Unterseiten ist ein sichtbarer Hauptinhaltsbereich für assistive Navigation vorhanden; auf der Startseite bleibt es beim ursprünglichen Hauptbereich.
- Die Abschnittsüberschrift zum ersten Besuch steht in der Lesereihenfolge vor dem untergeordneten Pferdeporträt. Die Überschriften der Textfassungen in den Kinderangeboten folgen auf Ebene 2.

Diese Verbesserungen sind nicht sämtlich als eigenständiger WCAG-Verstoß gewertet; sie erleichtern insbesondere die Orientierung mit Tastatur und assistiven Werkzeugen.

## Prüfmethode

- HTML- und DOM-Prüfung, einschließlich Sprache `de`, Alternativtexten, Formularbeschriftung, Rollen, Verweiszielen und Dokumenttiteln.
- Berechnung der Textkontraste aus den tatsächlich berechneten CSS-Farben und Hintergrundflächen nach relativer sRGB-Luminanz; normale Texte 4,5:1, große Texte 3:1. Texte über Fotos und komplexe Hintergründe wurden nicht als automatisch bestanden gewertet.
- Browserprüfung bei 320 Pixel Breite sowie Laptopansicht. Die Breitenprüfung ist ein Reflow-Test und kein Nachweis echten Browserzooms.
- Separate lokale Testkopie mit 1,5-facher Zeilenhöhe, 2 em Absatzabstand, 0,12 em Zeichenabstand und 0,16 em Wortabstand. Diese Testregeln wurden nicht in die veröffentlichte Website übernommen.
- Tastatur-Stichproben: Sprunglink auf Start- und Unterseite, Menü, Abschnittswechsel und Bilddialog. Fokusmarkierung und Rückkehr des Fokus geprüft. Kein Telefonanruf ausgelöst.
- Lokale Bilddateien und interne Verweisziele geprüft; keine fehlenden Ziele, extern nachgeladenen Medien, Formulare oder eingebetteten Drittseiten. JavaScript auf Syntaxfehler geprüft.

Es wurde kein axe-, Lighthouse- oder vollständiger Screenreader-Prüflauf ausgeführt. Der Check verwendet eigene DOM-/Kontrastmessungen und manuelle Browserprüfung.

## Verbleibende Prüfung

1. Vollständiger Durchlauf mit NVDA/Firefox beziehungsweise VoiceOver/Safari, einschließlich Lesereihenfolge, aller FAQ-Zustände und dynamischer Kontaktzuordnung.
2. Nativer Browserzoom bis 200 % sowie 400 % unter realen Browser- und Geräteeinstellungen. 320 CSS-Pixel Breite allein decken diese Prüfungen nicht vollständig ab.
3. Kontraste aller Hover-, Fokus- und deaktivierten Zustände, nicht-textlicher Bedienelemente sowie der Originalgrafiken und Fotobeschriftungen. Die sichtbaren Textfassungen der Flyer sind eine zusätzliche zugängliche Darstellung; das Farblayout der Originalgrafiken wurde nicht neu gestaltet.
4. Systematische Prüfung aller relevanten A- und AA-Kriterien, einschließlich Zeigerbedienung, Zielgrößen samt Abstands-Ausnahmen und vollständiger Fokusreihenfolge.
5. Redaktionelle Kontrolle der Bildbeschreibungen durch den Verein, insbesondere bei kleinen Archivaufnahmen. Die Texte wurden anhand der vorhandenen Fotos erstellt; sie bestätigen keine Bildrechte, Personenidentitäten oder heutige Vereinszugehörigkeit.

## Maßgebliche Referenzen

- [WCAG 2.2 Schnellreferenz](https://www.w3.org/WAI/WCAG22/quickref/)
- [1.1.1 Nicht-Text-Inhalt](https://www.w3.org/WAI/WCAG22/Understanding/non-text-content.html)
- [1.4.3 Mindestkontrast](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html)
- [1.4.5 Bilder von Text](https://www.w3.org/WAI/WCAG22/Understanding/images-of-text.html)
- [1.4.12 Textabstände](https://www.w3.org/WAI/WCAG22/Understanding/text-spacing.html)
- [2.5.3 Beschriftung im Namen](https://www.w3.org/WAI/WCAG22/Understanding/label-in-name.html)
- [2.4.11 Nicht verdeckter Fokus](https://www.w3.org/WAI/WCAG22/Understanding/focus-not-obscured-minimum.html)
