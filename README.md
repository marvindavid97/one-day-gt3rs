# ONE DAY — GT3 RS

Eine mobile Geschenkseite für einen NFC-Tag: Beim Antippen läuft eine kurze
Startsequenz ("Key detected"), danach folgen ein animierter Drehzahlmesser und
ein persönlicher Geburtstagsgruß.

## Aufbau

| Datei | Zweck |
| --- | --- |
| `index.html` | Startsequenz, Drehzahlmesser, Einstiegstext |
| `birthday.html` | Die eigentliche Geburtstagskarte |
| `assets/` | Schlüsselbild (freigestellt), Wappen, Favicon, Teilen-Vorschau |

Kein Build-Schritt, keine Abhängigkeiten, keine Serverlogik — zwei HTML-Dateien
mit eingebettetem CSS und etwas JavaScript.

## GitHub Pages

Unter **Settings → Pages** als Quelle **Deploy from a branch**, Branch `main`,
Ordner `/ (root)`. Die veröffentlichte URL auf den NFC-Tag schreiben:

```
https://marvindavid97.github.io/one-day-gt3rs/
```

Die `.nojekyll`-Datei sorgt dafür, dass Pages die Dateien unverändert ausliefert.

## Hinweise

- Beide Seiten sind auf `noindex` gesetzt. Der Link funktioniert normal, die
  Seite taucht aber nicht in Suchergebnissen auf — der Text ist persönlich.
- Die Assets zeigen einen Porsche-Schlüssel und das Wappen. Das ist für ein
  privates Geschenk unkritisch, wäre für eine beworbene oder kommerzielle
  Seite aber markenrechtlich heikel.
- Nach dem Austauschen eines Bildes den Cache-Buster in `index.html`
  hochzählen (`?v=3` → `?v=4`), sonst zeigen Handys die alte Version.

## Lokal ansehen

```
python3 -m http.server 4173
```

Dann `http://localhost:4173/` im Browser öffnen.
