# UX Optimierungen und neues Startbild

Stand: 9. November 2026. Umsetzung nach Freigabe des Auftraggebers. Ziel sind bessere Lesbarkeit, eine einfachere Bedienung und ein ruhiger, professioneller Vereinsauftritt für junge Pferdefans und Eltern.

## Gestalterische Grundlage

Der Magazinstil bleibt die Grundlage: großzügige Fotos, elegante Überschriften und klare Inhaltsbereiche. Die Vereinsfarben Navy, Gold und Creme sowie DM Serif Display und DM Sans bleiben erhalten. Aus den Referenzen werden passende Prinzipien übernommen, keine vollständige Vorlage und keine zusätzlichen Funktionen wie Mitgliederportal, Buchungssystem oder CMS.

- **Editorial Grid / Magazine:** Bildgeschichten mit klarer redaktioneller Hierarchie.
- **Minimalism & Swiss Style:** nachvollziehbare Struktur, konsistente Abstände und Beschriftungen.
- **Organic Biophilic:** natürliche Fotografie und warme Flächen, ohne die Vereinsfarben durch eine neue grüne Farbwelt zu ersetzen.
- **Vibrant & Block-based:** zurückhaltende goldene und blaue Akzente bei den Angebotskarten.

Die Zuordnung ist eine gestalterische Bewertung. Die Skill-Empfehlungen zu gemeinnützigen Organisationen und Gemeinschaft passen zum Auftrag besser als die auf Fans, Tickets und Merchandise ausgerichtete Sportclub-Vorlage.

## Umgesetzte Änderungen

| Bereich | Umsetzung und Zweck |
| --- | --- |
| Lesbarkeit | Wichtige Beschreibungstexte auf 16 Pixel, Einstiegsabsatz am großen Bildschirm auf 18 Pixel; Navigation und viele ergänzende Links auf 14 Pixel. Kleine Markenbeschriftungen bleiben gestalterisch untergeordnet. |
| Handy-Einstieg | Überschrift auf 44 Pixel, kompaktere Abstände und kürzerer Einleitungstext. Das Foto erscheint früher; der Kontaktbutton bleibt davor sichtbar. |
| Kontaktweg | Die Einstiegsbuttons heißen einheitlich „Ersten Reittermin vereinbaren“ und führen zum erklärten Ablauf. Der dortige Telefonlink nennt Christoph und die Rufnummer. Training und Einstellbetrieb behalten ihre passenden Wege. |
| Vereinsberichte | Sonderprüfung und Schulpferde-Trophy erscheinen jeweils einmal als Bildkarte mit Datum, Bericht und ursprünglichem Facebook-Link. Der Halloween-Ritt bleibt eine historische Bildergeschichte. Der bisherige Anker `#vereinsberichte` bleibt nutzbar. |
| Bedienflächen | Menü und Dialog-Schließen jeweils 48 × 48 Pixel. Navigation, wichtige Links und Buttons haben großzügigere Bedienhöhen. Diese Werte sind Komfortziele, keine behauptete Zertifizierung. |
| Tastatur | Sichtbare Fokusmarkierungen, Sprunglink zum Inhalt, Fokus auf Zielüberschrift bei interner Navigation und Schließen des mobilen Menüs mit Escape. Alle 219 übernommenen Bildvorkommen erhalten echte Schaltflächen für die Vergrößerung. Escape schließt den Bilddialog; der Fokus kehrt zum Auslöser zurück. |
| Einheitlichkeit | Gemeinsame Größen für Fließtext, Nebeninformationen, Kartenabstände und Abschnittsabstände sowie dezente Rundungen. Angebotskarten mit klaren Farbakzenten und einheitlichen Bildkarten. |

## Entscheidung zum Startbild

Der Auftraggeber hat ausdrücklich **„Pferde am Zaun“** ausgewählt.

- Datei: `webseite/images/optimized/i21314ff4fda655ef.webp`
- Motiv: Pferde am Holzzaun mit Bäumen und Berglandschaft.
- Herkunft: bereits lokal übernommener Bildbestand der bisherigen Vereinswebsite.
- Bildunterschrift: „Stallleben in Graschnitz“.
- Das Foto wird im Original verwendet; nur der sichtbare Ausschnitt passt sich dem Bildschirm an.
- Das kleine überlagerte Halloween-Bild entfällt im Einstieg. So bekommt das neue Motiv mehr Ruhe und Platz.
- Die Aufnahme wird keinem aktuellen Termin und keiner identifizierten Person zugeordnet. Bestehende Bildfreigaben und fachliche Prüfpunkte aus `OFFENE-PUNKTE.md` bleiben relevant.

Das ebenfalls betrachtete Foto „Mensch und Pferd am Stall“ (`i35446c0a3812e676.webp`) wurde nicht ausgewählt. Die Startbildentscheidung ersetzt die entsprechende Beschreibung in der ursprünglichen Jugend-Weiterentwicklung.

## Prüfung und technische Grenzen

- Darstellung bei 320, 390, 768 und 1280 Pixel Bildschirmbreite auf seitlichen Überlauf geprüft; zusätzlich große Laptopansicht angesehen.
- Mobiles Menü, Sprung zum Erstbesuch, Eltern-FAQ, Bilddialog per Enter und Escape sowie Rückkehr des Fokus geprüft.
- Telefonzuordnung des Einstellbetriebs und des Schulbetriebs geprüft, ohne einen Anruf auszulösen.
- Texte aller 15 internen Vereinsunterseiten einschließlich Rechtstexten mit dem vorherigen Stand verglichen: unverändert.
- Interne Verweisziele und lokale Bilddateien geprüft; keine externen Bild-, Schrift-, Skript- oder CSS-Ladeadressen, keine eingebetteten Drittseiten und keine Formulare.
- JavaScript auf Syntaxfehler geprüft. Dies ist eine gezielte Funktions- und Darstellungsprüfung, kein vollständiges Barrierefreiheits- oder Rechtsaudit.

Die Website bleibt eine statische HTML-Datei mit lokalen Bildern und eingebetteten Schriften. Die vorhandene Dokumentation offener fachlicher Angaben bleibt maßgeblich.

## Referenzen

- [UI UX Pro Max Stilkatalog](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill/blob/main/src/ui-ux-pro-max/data/styles.csv)
- [Empfehlungen für Website-Typen](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill/blob/main/src/ui-ux-pro-max/data/products.csv)
- [UX-Kurzreferenz](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill/blob/main/.claude/skills/ui-ux-pro-max/references/quick-reference.md)

Die Referenzen wurden als Gestaltungs- und Prüfhilfe gelesen; es wurde kein fremdes Skill-Skript installiert oder ausgeführt.
