# CC.md — Memex PAIM app (archív/mentés)
> Pi5 | `/home/admin/server/memex-paim/` | GitHub: memex-paim/memex-paim

## Mi ez?
Kész Android app — Google Play Áruházban megjelent. **Ne módosítsd.**
Az éles, mérvadó kód a GitHubon van — ez a mappa csak helyi mentés/klón.

**Státusz:** Kész. Végigment a Play Store folyamatokon. 12 tesztelő kellene 14 napig a nyilvános kiadáshoz — egyelőre várakozás.

## Technikai adatok
- **Offline PWA** — Android Chrome-on fut, telepíthető (Add to Home Screen)
- **AI:** Claude / Gemini API key bekötve (felhasználó saját kulcsával)
- **Adatbázis:** SQLite (Python backend) + IndexedDB (böngésző oldal)
- **FTS5** — Full Text Search 5, SQLite beépített offline kereső, AI nélkül is működik
- **Semmi reklám, semmi felhasználói adatgyűjtés** — teljesen magában fut
- **Python FastAPI backend** a Pi5-ön (fejlesztői környezethez)

## Live
- App: **memexpaim.com/app/**
- Repo: **github.com/memex-paim/memex-paim** (master branch = éles)

## Ha mégis kellene valamit
```bash
cd /home/admin/server/memex-paim
git pull origin master   # frissítés GitHubról
```
Részletes dokumentáció: `README.md`, `app/MIRE_VALO.md`
