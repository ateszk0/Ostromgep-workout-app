---
permalink: /privacy/hu/
title: Ostromgep - Adatvédelmi tájékoztató
---

# Ostromgep - Adatvédelmi tájékoztató

_Utolsó módosítás: 2026-09-06 • Tervezet - közzététel előtt jogásszal átnézendő._

**Adatkezelő:** Attila Nagy, ostromgep@atisn.com.
Ez egy személyes, felnőtteknek szánt edzésnapló-alkalmazás. 16 év alatti gyerekeknek nem ajánlott.

## Röviden

- Amit rögzítesz, alapból **az eszközödön marad**.
- **Nincs analitika, nincs reklám, nincs harmadik feles követő.**
- Két dolog opcionális és alapból ki van kapcsolva: a **felhőmentés** (Firebase) és az **AI-funkciók** (Google Gemini).
- Az adataidat **JSON-ba exportálhatod**, és a fiókodat + minden adatot **az appon belül törölhetsz**.

## Amit az app az eszközödön tárol

Helyben, egy eszközön lévő adatbázisban és a beállításokban:

- Edzésnapló (gyakorlatok, sorozatok, ismétlések, súlyok, RPE/RIR, jegyzetek, időbélyegek)
- Rutinok, edzésblokkok, egyéni gyakorlatok, mappák
- Testsúlynapló (ha használod)
- A megjelenített neved és (opcionálisan) a profilképed
- Beállítások (téma, nyelv, emlékeztetők, időzítő, app-blokkoló lista, és hogy a
  regenerációs hőtérkép férfi vagy női testalakot rajzol-e)
- A saját Gemini API kulcsod, ha megadsz egyet (az Android Keystore-ral titkosítva tárolva)

Ez az adat nem kerül sehova, hacsak be nem kapcsolod a felhő-szinkront vagy az AI-funkciókat.

## Opcionális: Felhőmentés (Firebase)

Ha létrehozol egy fiókot és használod a „Feltöltés a felhőbe” gombot, az app a
fenti helyi adatok másolatát a **Google Firebase**-ben (Firestore +
Authentication) tárolja, a fiókodhoz kötött dokumentumban.

- Belépés: e-mail + jelszó, vagy Google-belépés (utóbbi megosztja az e-mail-címed és a neved).
- Cél: hogy másik eszközön visszaállíthasd az adataidat.
- Megőrzés: amíg nem törlöd. A **Beállítások → Adatok és szinkron → „Fiók és adatok
  törlése”** eltávolítja a felhő-dokumentumot és a belépési fiókodat.
- Adatfeldolgozó: Google (Firebase). Lásd a Google adatvédelmi tájékoztatóját.

## Opcionális: AI-funkciók (Google Gemini)

A rutingenerátor, a súlyjavaslatok, a bemelegítés/levezetés protokollok és az
edzés utáni elemzés szöveget küldenek a **Google Gemini API**-jának.

- **Alapból** ez a fejlesztő által üzemeltetett proxy-szerveren (Cloudflare
  Workers) keresztül megy, amely továbbítja a Gemininek. A proxy tárolja az
  API-kulcsot; a visszaélések korlátozásához rövid ideig (kb. 24 óra) az
  IP-címedet is eltárolja.
- **Mi kerül elküldésre:** a kéréshez tartozó gyakorlat-/edzésadat, az opcionális
  „egyéni kérés” mezőbe írt szöveg, és - csak ha bepipálod - a legutóbbi
  testsúlyod. Kort és magasságot az app nem gyűjt.
- **Ingyenes szint:** az alapértelmezett út a Gemini ingyenes szintjét
  használja. A Google az ingyenes szinten beküldött tartalmat felhasználhatja a
  modelljei fejlesztésére, és emberek is átnézhetik. Ha ezt nem szeretnéd, add
  meg a saját Gemini API-kulcsodat a **Beállítások → AI** menüben - ekkor az app
  közvetlenül hívja a Geminit, és a kulcsodra a Google fizetős szintű feltételei
  vonatkoznak (nincs tréningfelhasználás).
- Az AI kimenete generált szöveg, tévedhet. Nem orvosi vagy táplálkozási tanács.
- Adatfeldolgozók: Google (Gemini), Cloudflare (proxy).

## Egyéb hálózati tevékenység

- **Frissítés-ellenőrzés:** indításkor az app megkérdezi a GitHubtól, van-e
  újabb kiadás. A GitHub látja az IP-címed. Személyes adat nem megy. Ha a
  frissítés mellett döntesz, az app le tudja tölteni az új APK-t a GitHubról és
  átadja az Android csomagtelepítőjének, amit te magad hagysz jóvá; helyette a
  kiadási oldalt is megnyithatod böngészőben.
- **Android rendszer-backup:** az app kikapcsolja az automatikus Google
  felhő-mentést (`allowBackup=false`), így a helyi adataid nem kerülnek a
  Google-fiók mentésébe. Új eszközre a JSON exporttal vagy a felhő-synckel
  viheted át őket. (Készülékek közti közvetlen átvitel a telefonbeállításnál
  még lehetséges.)

## A jogaid

Attól függően, hol élsz (pl. GDPR/EGT, Egyesült Királyság, Kalifornia), jogod
lehet hozzáférni az adataidhoz, helyesbíteni, töröltetni, hordozni azokat, és
tiltakozni a kezelés ellen. Ebben az appban:

- **Hozzáférés / hordozhatóság:** Beállítások → Adatok és szinkron → „Teljes adat exportálása (JSON)”.
- **Törlés:** Beállítások → Adatok és szinkron → „Fiók és adatok törlése” (felhő +
  fiók). Az app eltávolítása törli az eszközön lévő adatot.
- Bármi máshoz írj ide: ostromgep@atisn.com.

## Változások

A tájékoztató lényeges változásait itt jelezzük, új „utolsó módosítás” dátummal.

- 2026-09-06: rögzítettük, hogy a regenerációs hőtérkép férfi/női testalak-
  választása a beállítások része (így felhőmentés esetén abba is bekerül), és
  hogy a frissítés-ellenőrzés mostantól az appon belül le tudja tölteni és
  telepíteni az új APK-t.
