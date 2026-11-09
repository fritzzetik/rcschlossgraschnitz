# Grundlagen und Entscheidungen

Dokumentiert am 9. November 2026. Diese Datei hält die Entstehungsentscheidungen fest; sie ist kein vom Verein beschlossenes Markenhandbuch.

## Ausdrückliche Vorgaben

- Eine vollständige, professionell gestaltete Website für den Reitclub Schloss Graschnitz erstellen.
- Junge Menschen sowie Eltern mit pferdebegeisterten Kindern ansprechen.
- Die Website am Laptop unmittelbar vorzeigen können, auch offline.
- Vereinslogo, echte Vereinsbilder und Informationen der bisherigen Website und der Facebook-Seite verwenden.
- Farben und Gestaltung an der Vereinsidentität orientieren.
- Vereinsinformationen und Rechtstexte innerhalb der neuen Website zugänglich machen.
- Ausschließlich statische Auslieferung: kein CMS und keine automatische Facebook-Anbindung.
- Facebook als normalen externen Link anbieten.
- Regionale Medienbeiträge recherchieren, kurz zusammenfassen und auf die Originale verlinken.
- Übernahmevermerke, „Gestaltungsentwurf“ und sonstige sichtbare Entwurfs- und Bearbeitungshinweise entfernen, damit die Seite als fertiger Vorschlag gezeigt werden kann.
- Fertige Dateien in `C:\privat\rcschlossgraschnitz\webseite` und im Repository `fritzzetik/rcschlossgraschnitz` ablegen; Grundlagen im Ordner `design` erhalten.

## Gestalterische Annahmen

Die folgenden Entscheidungen wurden bei der Umsetzung getroffen. Sie sind keine zusätzlich bestätigten Vorgaben des Vereins.

- **Ansprache:** freundlich, direkt und überwiegend mit „du“ bzw. „ihr“. Eltern sollen praktische Orientierung finden, junge Pferdefans einen einladenden Zugang.
- **Inhaltlicher Schwerpunkt:** Einstieg ins Reiten, Gemeinschaft, Freude am Umgang mit Pferden und ein persönlicher Kontakt zum Schulbetrieb. Turniersport und Einstellbetrieb bleiben sichtbar.
- **Bildsprache:** echte Aufnahmen aus dem Vereinsleben statt generischer Stockfotos oder künstlich erzeugter Pferdebilder. Nachwuchs, gemeinsame Erfolge und die Anlage stehen im Vordergrund.
- **Farben:** dunkles Marineblau, warme Gold-/Gelbtöne und ein heller, leicht gebrochener Hintergrund. Die Werte sind gestalterische Ableitungen, keine belegten offiziellen Vereinsfarbwerte.
  - Text und primäre Flächen: `#1e3353`
  - Goldgelbe Akzente: `#e0c35a`
  - Hintergrund: `#faf9f5`
  - Sekundärer Text: `#626d7c`
  - Blaue Hervorhebungen: `#385984`
- **Schrift:** DM Serif Display für Überschriften und DM Sans für Fließtext. Die Schriftdaten sind eingebettet; Besucher laden sie nicht von Google nach.
- **Aufbau:** großzügige Bildbereiche, klare Hierarchie, gut lesbare Texte und reduzierte Navigation. Die Darstellung passt sich an kleinere Bildschirme an.

## Informationsarchitektur

Die Startseite führt durch Reitenlernen, Elternfragen, Anlage, Vereinsleben, Neuigkeiten, Presse, Vereinsbereiche und Kontakt. Ergänzend stehen 15 übernommene Inhaltsbereiche bereit, darunter Reitschule, Schulpferde, Kinderangebote, Einstellbetrieb, Training, Geschichte, Vorstand, Veranstaltungen, Bilder und Rechtstexte.

Die Inhaltsbereiche werden innerhalb derselben HTML-Datei über Anker wie `#seite-einstellbetrieb` geöffnet. Die Navigation wechselt dafür nicht zur alten Jimdo-Seite.

## Technische Entscheidungen

- Die ausgelieferte Website besteht aus HTML, eingebettetem CSS, einem kleinen JavaScript-Skript und lokalen Bildern.
- Kein CMS, keine Datenbank, keine Benutzerkonten, kein Buchungs- oder Zahlungsprozess.
- Keine Analysewerkzeuge, Social-Media-Einbettungen, reCAPTCHA oder extern geladenen Schriften im Website-Code.
- Kontakt über Telefon- und E-Mail-Links. Die Website selbst sendet keine Nachrichten.
- Externe Links führen ausschließlich zu den bewusst verlinkten Facebook- und Medienseiten. Sie werden erst beim Anklicken aufgerufen.
- Menünavigation, Kontakt-Auswahl, aufklappbare Fragen und Bildvergrößerung funktionieren lokal.
- 219 Bilder der bisherigen Website wurden für die Auslieferung auf maximal 1.400 Pixel je Kante verkleinert und als WebP komprimiert; zusätzliche Vereinsbilder und das Logo liegen ebenfalls lokal vor. Die ausgelieferte Website verwendet insgesamt 224 unterschiedliche Bilddateien.
- Die Entwicklung nutzte zunächst eine React/Vinext-Arbeitsfassung. Dieses Repository enthält bewusst die fertige statische Auslieferung; für Betrieb und Änderungen ist diese Entwicklungsumgebung nicht erforderlich.

## Redaktionelle Entscheidungen

- Vereinsangaben wurden aus den vorhandenen Quellen übernommen, nicht durch Rücksprache mit dem Verein neu bestätigt.
- Unbekannte aktuelle Preise, freie Plätze, Einstiegsalter und Ausrüstungsfragen werden auf der Startseite nicht erfunden. Für solche Fragen wird auf persönliche Kontaktaufnahme verwiesen.
- Die vorhandenen Detailseiten können ältere Angaben enthalten. Deren Aktualität ist gesondert zu prüfen.
- Veranstaltungen mit vergangenen Daten sind Rückblicke; sie werden nicht als kommende Termine beworben.
- Die MeinBezirk-Fundstellen sind als Community-Beiträge bzw. Veranstaltungshinweise gekennzeichnet. Der EQWO-Rückblick nennt eine Pressemeldung als Grundlage. Es wird keine unabhängige redaktionelle Berichterstattung behauptet.
- Presseartikel werden nur kurz in eigenen Worten zusammengefasst und verlinkt. Medienbilder wurden dafür nicht übernommen.
- Entfernte Entwurfsvermerke bedeuten keine rechtliche oder fachliche Freigabe. Offene Punkte bleiben in `OFFENE-PUNKTE.md` dokumentiert.
