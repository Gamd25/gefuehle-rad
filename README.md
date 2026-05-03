# Gefühlskarten-Rad mit Firebase-Synchronisation

Diese Version entfernt gezogene Karten für alle Nutzer synchron.

## Enthalten

- index.html
- assets/Gefühl_01.jpg bis Gefühl_39.jpg
- assets/holz_ratsche.wav
- assets/ding.wav
- .nojekyll

## Firestore-Regeln

Firebase Console → Firestore Database → Rules:

rules_version = '2';

service cloud.firestore {
  match /databases/{database}/documents {
    match /wheelState/{document} {
      allow read, write: if true;
    }
  }
}

Danach auf Publish / Veröffentlichen klicken.

## GitHub Pages

1. ZIP entpacken.
2. Alle Dateien in dein Repository hochladen.
3. Settings → Pages.
4. Source: Deploy from branch.
5. Branch: main, Folder: /root.
6. Link in Moodle Iframe Embedder bei Quelle eintragen.

## Moodle Iframe Embedder

- Breite: 100%
- Minimale Breite: 300px
- Höhe: 750px
- Quelle: dein GitHub-Pages-Link


## Neue Funktion

Diese Version zeigt rechts eine synchronisierte Liste „Bereits gezogen“. Dort werden alle verwendeten Karten mit kleinem Vorschaubild angezeigt.
