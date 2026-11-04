# Kleiderspende – Website mit Registrierungsformular

Mehrseitige, responsive Website für einen fiktiven gemeinnützigen Verein, der Kleidung an
Krisengebiete spendet. Kernstück ist ein Formular, mit dem Spenderinnen und Spender ihre
Kleiderspende registrieren.

Reines **HTML5, Bootstrap 5.3 und JavaScript** – ohne Build-Schritt und ohne Backend.

## Seiten

| Seite | Inhalt |
|---|---|
| `index.html` | Vorstellung, Registrierungsformular |
| `abschluss.html` | Bestätigung mit den eingegebenen Angaben (aus der URL gelesen) |
| `geschichte.html` | Vereinsgeschichte |
| `mitglieder.html` | Mitglieder |
| `rechtliches.html` | Rechtliche Hinweise (im Footer verlinkt) |

## Formular-Logik

- Krisengebiet (Dropdown), Kleidungsart (Mehrfachauswahl), Übergabeart (Abholung oder Abgabe)
- Bei **Abholung** werden die Adressfelder eingeblendet und per JavaScript zu Pflichtfeldern;
  bei Abgabe an der Geschäftsstelle werden sie wieder ausgeblendet
- Abholungen gibt es nur in der Nähe der Geschäftsstelle: Die PLZ muss mit „10“ beginnen. Die
  Meldung erscheint direkt am Feld (Browser-Validierung), nicht als blockierendes Pop-up
- Die Bestätigungsseite liest die übermittelten Werte aus der Query-String-URL und zeigt sie an

## Responsives Layout und Barrierefreiheit

- Bootstrap-Grid, Navigation klappt auf kleinen Bildschirmen zum Burger-Menü zusammen
- Formularfelder sind mit Labels bzw. `aria-label` verknüpft, Bilder haben Alternativtexte,
  Seiten haben `lang="de"` und eine Meta-Beschreibung

## Lokal ansehen

Datei `index.html` im Browser öffnen. Bootstrap wird per CDN geladen (Internet nötig).
Alternativ mit einem kleinen Server: `python -m http.server` und <http://localhost:8000>.
