# app/ mappa – Offline PWA (Play Store verzió)

Ez a mappa tartalmazza majd a standalone offline PWA appot.
Fejlesztés még nem kezdődött el – a jelenlegi Pi-alapú rendszer tesztelése folyamatban.

## Mi lesz itt

```
app/
├── index.html       ← UI (az ui/index.html alapján, átírva offline-ra)
├── sw.js            ← Service Worker (cache + offline logika)
├── manifest.json    ← PWA manifest (Play Store / telepítés)
├── memex.js         ← SQLite WASM adatréteg (Pi helyett böngészőben fut)
├── icon-192.png
├── icon-512.png
└── sql-wasm.js      ← SQLite WASM library (~1MB, Google fejleszti)
```

## Mi változik a jelenlegi rendszerhez képest

| Jelenlegi (ui/) | App (app/) |
|-----------------|------------|
| FastAPI Pi szerver | nincs szerver |
| memex.db a Pi-n | SQLite WASM + OPFS a böngészőben |
| HTTP API hívások | közvetlen JS függvényhívások |
| Python backend | JavaScript adatréteg |

## Tesztelés

- **PC Chrome** – elegendő a fejlesztéshez, DevTools-szal debuggolható
- **Android Chrome** – végleges teszt telepítés előtt
- **Play Store** – TWA (Trusted Web Activity) wrapper, 0 sor Kotlin

## Mikor kezdjük

Amikor a jelenlegi Pi-alapú rendszer (ui/) stabil és tesztelve van.
