# Ostromgép: Részletes Használati Útmutató

Üdvözöl az **Ostromgép**! Ez az alkalmazás azért jött létre, hogy segítsen az edzéseid precíz naplózásában, a fejlődésed követésében és a progresszív túlterhelés (Progressive Overload) tudatos alkalmazásában.

---

## 1. Dashboard (Kezdőlap)

A **Dashboard** a főképernyő, ahol gyors áttekintést kapsz a jelenlegi állapotodról és a következő tennivalódról. Minden itteni kártya egy átrendezhető widget.

- **Next Mission (Következő küldetés)**: Az app javasol egy következő edzést a mentett rutinjaid alapján. Kattints a **„Start Mission”** gombra az azonnali kezdéshez.
- **Weekly Battle Log (Heti harci napló)**: Hétfőtől vasárnapig. A kitöltött kör jelzi, melyik napon edzettél már a héten.
- **Ready to Siege (Ostromra kész – Izomregeneráció)**: Hőtérkép az egyes izomcsoportok fáradtsági szintjéről.
  - **Zöld**: Regenerálódott, készen áll a terhelésre.
  - **Sárga**: Enyhe fáradtság, érezhető igénybevétel.
  - **Piros**: Erős fáradtság – pihentesd az adott izomcsoportot.
- **Quick Metrics (Gyors mutatók)**: Kattints a beviteli mezőre a napi testsúlyod rögzítéséhez, majd mentsd el a pipa gombbal. Az alatta lévő grafikon az elmúlt 7 mérésed trendjét mutatja.
- **Today's Workout (Mai edzés)**: Egy koppintással az MI összeállít egy teljes edzést a közelmúltad alapján.
- **Campaign (Hadjárat)**: Szinted, XP-sávod, heti szériád, küldetéseid és liga-szinted egy pillantásra – koppints rá (vagy a jobb felső trófea ikonra) a teljes **Hadjárat** képernyő megnyitásához (lásd 6. pont).
- **Training Block (Edzésblokk státusza)**: Ha van aktív periodizációs blokkod, mutatja az aktuális hetet és a **DELOAD** jelzést a regenerációs heteken. Üres, ha még nem indítottál blokkot.
- **Stalled Lifts (Elakadás-figyelő)**: Gyakorlatok, amelyeknek a becsült maximuma egy ideje nem nőtt, mindegyikhez egy javaslattal (deload / technika ellenőrzése / variáció / több volumen). Üres, ha jelenleg semmi nem stagnál.
- **Fresh Conquests (Friss hódítások)**: Az elmúlt 30 nap egyéni csúcsai, feltüntetve, hogy milyen típusú rekordról van szó (legnagyobb súly vagy szakasz volumen), és mennyi ideje történt.
- **Siege Watch (Ostromfigyelő)**: Az e heti ostrom váradnak élő, kicsinyített képe – koppints rá, hogy a Hadjárat képernyőre ugorj.
- **Edit Layout (Elrendezés szerkesztése)**: A dashboard alján lévő gombbal megnyílik egy párbeszédablak, ahol **átrendezheted** a widgeteket vagy **elrejtheted** azokat, amiket nem használsz. A lista görgethető, ha nem fér ki a képernyőn.

---

## 2. Workout (Edzés) indítása és Rutinok kezelése

A **Workout** fülön (alsó navigáció) választhatsz, hogyan szeretnél mozogni:

- **Start Empty Workout (Üres edzés indítása)**: Nincs fix terv – ott helyben állítod össze a gyakorlatokat.
- **My Routines (Saját rutinok)**: Az általad létrehozott sablonok. Kattints a kártya **„Start Routine”** gombjára az indításhoz.
- **QR kódos importálás/exportálás**: A rutinlista feletti **QR ikonnal** olvashatsz be mások által megosztott terveket. Saját rutinjaidat a kártya három pont (⋯) menüjében a **Share via QR** opcióval oszthatod meg. A szerializáció adat-agnosztikus, így a teljesen egyedi, saját gyakorlataid is gond nélkül átkerülnek.
- **Manage Rotations (Rotációk kezelése)**: A jobb felső **rotáció ikonnal** (körkörös nyilak) csoportosíthatod a körbejárt rutinjaidat.
  - **Create Rotation (Rotáció létrehozása)**: Adj neki nevet, és válaszd ki, mely rutinok tartozzanak bele.
  - **Active Rotation (Aktív rotáció)**: Ha kiválasztasz egy rotációt, a dashboard **Next Mission** widgetjében már csak az ahhoz tartozó rutinok forognak.
- **New Routine (Új rutin)**: Új, elmenthető edzésterv a **Routine Editor**-ban (gyakorlatok, alapértelmezett ismétlésszám, szuperszettek).
- **Explore Routines (Rutinok felfedezése)**: Kétfüles képernyő. Az egyik fülön gyárilag összeállított tervek (Push-Pull-Legs, Full Body, …), amiket az **„Add to my routines”** gombbal menthetsz – ezek csak ideiglenes kitöltők, nem tökéletes programok. A másik fül az **AI Workout Generator** (lásd 8. pont).
- **Training Block**: Megnyitja a periodizáció-tervezőt (lásd 9. pont).

---

## 3. Active Workout (Aktív edzés)

Amikor elindítasz egy edzést, az alábbi eszközök állnak rendelkezésre:

### Felső sáv
- **Simple view kapcsoló** (lista / teljes képernyő ikon): vált a teljes sorozattáblázat és egy zavartalan **Simple view** között, ami egyszerre egy szettet mutat, és lapozhatsz köztük.
- **Plate Calculator** (számológép ikon): adj meg egy cél- és rúdsúlyt, és megmondja, milyen tárcsákat rakj fel oldalanként.
- **AI Assistant** (robot ikon): menü, ahol **súlyjavaslatot** kérhetsz az aktuális gyakorlatokra, vagy generálhatsz egy **dinamikus bemelegítő** vagy **statikus levezető** protokollt – rövid, illusztrált nyújtáslistát erre az edzésre.

### Workout Stats Header (Edzésstatisztika fejléc)
Fent mindig látod: **Duration (Időtartam)**, **Volume (Volumen)**, **Sets (Szettek)**, plusz a pihenőidő visszaszámlálását.

### Exercise Block (Gyakorlat blokk) interakciók
- **Miniatűr kép**: kattints a gyakorlat melletti kis képre – ha van hozzá videó, elindul, egyébként a kép nagyítva jelenik meg.
- **Notes (Jegyzet)**: a gyakorlat neve alatt közvetlenül írhatsz.
- **Rest Timer (Pihenőidő)**: kattints a pihenősávban az időre a módosításhoz (±15 mp) vagy a kihagyáshoz.
- **⋯ menü**: **Move Up/Down** (Mozgatás), **Edit** (Szerkesztés), **Create / Remove Superset** (Szuperszett), **Replace exercise** (Csere) és **Delete** (Törlés).

### Sorozatok táblázata
- **Szett száma (1, 2, 3…)**: **kattints a számra**, hogy **Warmup set**-té (bemelegítő) alakítsd – a sor sárgára vált.
- **Previous (Előző)**: a legutóbbi adataid ehhez a gyakorlathoz.
- **KG / Reps (Súly / Ismétlés)**: kattints a mezőkbe az adatokhoz.
- **RPE**: kattints a kötőjelre az RPE oszlopban, és válassz a felugró listából.
- **Complete gomb**: kattints a sor végén a négyzetre a szett befejezéséhez – ez indítja az automatikus pihenőidőt is. Ha megdöntöd a korábbi csúcsodat, egy rekord-jelzés villan.
- **Sorozat törlése**: **húzd el a sort balra** a törléshez.

A szuperszettbe kötött gyakorlatok színes bal szegéllyel és „SUPERSET” felirattal vannak csoportosítva.

---

## 4. Exercises (Gyakorlatok) kezelése

A **Profile** fülön nyisd meg az **Exercises** könyvtárat:

- **Create Exercise (Gyakorlat létrehozása)**: a jobb felső **„Create”** gombbal. Add meg a nevét, az alapértelmezett ismétlési tartományát (**Rep Range**), tölts fel képet, és válaszd ki az érintett izomcsoportokat (**Muscle Groups**) és a szükséges eszközt (**Equipment**).
- **Edit Exercise (Szerkesztés)**: kattints bármelyik gyakorlatra a listában vagy az edzés közbeni menüben.
  - Saját gyakorlatok: minden adat szerkeszthető (név, kép, izmok, eszköz).
  - Alapértelmezett gyakorlatok: biztonsági okból csak az ismétlési tartomány módosítható, a kép fix.

---

## 5. Statistics (Statisztika)

A **Statistics** képernyő (Profile fül) egy teljes elemző nézet:

- **Summary (Összegzés)**: Workouts, Volume, Time, Avg. Workout, Longest Streak, This Month.
- **Last 7 Days**: hőtérkép arról, mely napokon edzettél.
- **Muscle Group Distribution**: donut-diagram és elöl/hátul testtérkép a mostanában megdolgoztatott izmokról.
- **Set Distribution**: sorozatszám izomcsoportonként.
- **Top Exercises**: a legtöbbször végzett gyakorlataid.
- **Personal Records**: a legnehezebb szett és a legnagyobb volumen gyakorlatonként.
- **1RM Progression**: válassz egy gyakorlatot, és látod a becsült egyismétléses maximumod (one-rep max) trendjét az időben (Epley / Brzycki becslés). Ehhez néhány naplózott edzés kell az adott gyakorlatból.
- **Stalled Lifts (Elakadás-figyelő)**: gyakorlatok, amelyeknek a becsült maximuma pár hete nem javult, mindegyikhez egy javaslattal (deload, technika ellenőrzése, variáció beiktatása, vagy több volumen). Koppints rá az adott gyakorlat részleteihez.
- **Monthly Summary**: havi edzés- és volumen-összegek.

---

## 6. A Hadjárat (Campaign)

Koppints a jobb felső trófea ikonra a Dashboardon (vagy a Hadjárat widgetre) a **Hadjárat** képernyő megnyitásához – egy várostrom-témájú, teljes egészében az edzésnaplódból számolt játékosított réteg. A tetején lévő **(i)** infó ikonra koppintva megnyílik a teljes, pontos képleteket tartalmazó útmutató; itt a rövid összefoglaló.

- **XP és szintek**: minden befejezett edzés XP-t ad (alap mennyiség, volumen-bónusz, bónusz minden megdöntött személyes rekordért, mindezt a heti szériád szorozza fel). A felgyűlt XP-ből szintet lépsz.
- **E heti ostrom**: minden hét egy roham egy vár ellen. A vár HP-ja a saját, közelmúltbeli heti volumencélod, így a vár **mérete** is ehhez igazodik – kisebb célnál egy szerény őrposzt vagy erőd, nagy célnál egy teljes, tornyos Citadella. Edzés közbeni volumennel sebzed: 50%-nál áttöröd a kaput, 100%-nál beveszed a várat, 150%-nál elsöprő győzelmet aratsz (a vár fehér zászlót tűz ki). A falak és tornyok láthatóan omlanak a haladásoddal, sosem ugyanúgy kétszer.
- **Heti küldetések**: minden héten 3 forgó kihívás (edzz N-szer, dönts meg egy rekordot, teljesíts egy volumen- vagy szettcélt, eddz több izomcsoportot, egy hosszú edzés, korai heti edzés). Mindhárom teljesítése bónusz XP-t ad.
- **Liga és szezon**: egy szezon egy naptári hónap. A liga-pontszámod a konzisztenciából jön – edzések, aktív hetek és szériád, nem a nyers erő –, így kezdőknek is fair marad. Emelkedj Réztől Bronzon, Ezüstön, Aranyon, Platinán át egészen Gyémántig. Koppints a Liga kártyára a teljes ranglétráért, ami megmutatja, mennyire vagy az egyes szintektől.
- **Jelvények**: 34 kitüntetés, nehézség szerint Bronztól Platináig rendezve, éremszínezéssel, 3 oszlopos rácsban. Koppints bármelyikre, hogy pontosan lásd, mi kell a megszerzéséhez.
- **Értesítések**: push értesítés érkezik ligalépéskor, minden heti küldetés teljesítésekor és új jelvénynél. Kikapcsolható: **Beállítások → Emlékeztetők → Hadjárat értesítések**.

---

## 7. Profile (Profil), Előzmények és Beállítások

A **Profile** fülön:

- **Recent Workouts Volume Chart**: oszlopdiagram az elmúlt edzések összesített volumenéről, hogy lásd, nő-e a terhelésed.
- **Workouts**: megnyitja a teljes **Workout Log**-ot. Kattints egy korábbi edzésre a részletekért, majd az **AI Evaluation** gombbal kérj utólagos részletes elemzést arról az edzésről (az app nyelvén).
- **Calendar**: naptár nézetben böngészheted a múltat; a ponttal jelölt napokon volt edzésed, a mai nap körvonalazva van.
- **Recent Workouts lista**: az utolsó edzéseid kártyái – kattints a részletekért, vagy használd a **Copy workout** / **Save as routine** funkciókat az újrahasznosításhoz.
- **Settings (Beállítások)** (fogaskerék ikon): kártyákra bontott képernyő:
  - **Appearance**: név, profilkép, app nyelve, **megjelenés (Rendszer, Világos vagy Sötét)**, és a téma színe (**Piros, Sárga, Zöld, Kék, Lila**).
  - **Timer**: a pihenőidő rezgése, hangereje és hangja.
  - **Focus Mode (App Blocker)**: felület, ami visszaterel az edzéshez, ha más appot nyitnál meg közben.
  - **Data & Cloud Sync**: Google fiókkal (Firebase) belépve mentheted és visszaállíthatod az előzményeket, sablonokat és a könyvtárat. **Teljes adat export/import JSON-ként**, vagy **Import CSV** egy **Hevy** edzés-export beolvasásához.
  - **AI (Gemini API Key)**: illeszd be a kulcsod (titkosítva, az eszközön tárolva).
  - **Cable Presets**: mentsd el a csigás gépekhez használt gyakori súlybeállításokat a gyorsabb naplózáshoz.

---

## 8. AI Workout Generator (Gemini 3 Flash)

Az **Explore Routines** képernyő **AI Workout Generator** fülén készíthetsz egyedi, személyre szabott terveket.

- **API Key**: szükséged lesz egy saját **Gemini API kulcsra**.
  1. **Kulcs igénylése**: nyisd meg a [Google AI Studio](https://aistudio.google.com/api-keys) oldalt, jelentkezz be, és hozz létre egy kulcsot.
  2. **Beállítás az appban**: Profile → **Settings** (fogaskerék) → **AI (Gemini API Key)** – illeszd be és mentsd. Biztonságosan, titkosítva (**EncryptedSharedPreferences**) tárolódik az eszközödön.
- **Training days per week (Heti edzésnapok)**: csúszka (1–7). Az MI a napok számához illő felosztást választ (PPL, Upper/Lower, Full Body, Arnold Split, …).
- **Additional preferences (Egyéni preferenciák)** (opcionális): szabad szöveg, pl. *„Vállsérülésem van, fókuszáljunk inkább a lábra és a hátra”* vagy *„Több izolációs gyakorlatot a karokra”*.
- **Generate Workout Plan**: az MI a gyári gyakorlattárból (**default_exercises.json**) állítja össze a tervet, és minden napra külön rutint ment a **My Routines** listádba. A jegyzeteket az app beállított nyelvén írja.
-  **API Key**: A generátor használatához szükséged lesz egy saját **Gemini API kulcsra**.
    1. **Kulcs igénylése**: Lépj a [Google AI Studio]([https://aistudio.google.com/](https://aistudio.google.com/api-keys)) oldalára, jelentkezz be a Google fiókoddal, majd kattints a **'Get API key'** gombra egy új kulcs létrehozásához.
    2. **Beállítás az appban**: Lépj a **Profile** fülre, kattints a jobb felső sarokban a **Settings** (fogaskerék) ikonra, majd görgess le az **AI (Gemini API Key)** részhez. Illeszd be a kulcsot és mentsd el. Az alkalmazás biztonságosan, titkosítva (**EncryptedSharedPreferences**) tárolja ezt az eszközödön.
-  **Training days per week (Heti edzésnapok)**: A csúszka segítségével állítsd be, hány napot tervezel edzeni egy héten (1-7 nap). Az MI automatikusan javasol egy optimális felosztást (pl. PPL, Upper/Lower, Full Body, Arnold Split) a napiszáma alapján.
-  **Additional preferences (Egyéni preferenciák)**: Ez egy opcionális mező, ahol speciális kéréseket adhatsz meg az MI-nek. Például: *„Vállsérülésem van, fókuszáljunk inkább a lábra és a hátra”*, vagy *„Szeretnék több izolációs gyakorlatot a karokra”*.
-  **Generate Workout Plan (Edzésterv generálása)**: A gomb megnyomása után az MI összeállítja a tervedet a gyári gyakorlattár (**default_exercises.json**) elemeiből, és minden napra külön-külön automatikusan elmenti a rutinokat a **My Routines** (Saját rutinok) listádba. Az AI generálás most már kétnyelvű, így a jegyzeteket az alkalmazás beállított nyelvének megfelelően írja.

---

## 9. Training Block (Periodizáció)

A **Training Block** képernyő egy rutinból strukturált, több hetes mezociklust csinál.

**Egy blokk tervezése:**
- **Forrás**: *Use existing routines* (válassz egy rutin-rotációt – a rutinjai lesznek az edzésnapok) vagy *Generate with AI* (írd le, mit szeretnél, és az MI elkészíti a felosztást).
- **Block length**: 4–8 hét.
- **Deload every N weeks**: milyen gyakran ékelődik be egy könnyebb regenerációs hét (az utolsó hét mindig deload).
- **Extra sets per week**: mennyire agresszíven növekszik a munkaszettek volumene minden nem-deload cikluson belül.

**Hogyan fut:** az app hétről hétre felépíti a tervet. A munka- (nem bemelegítő) szettek száma hétről hétre nő egy cikluson belül, és minden deload után nullázódik; a deload hetek nagyjából felére vágják a munkaszett-volument, és **DELOAD** jelzést kapnak. A blokk-képernyőn látod a **Week X / Y** állást, és onnan indíthatod az aktuális hét edzését. A bemelegítő szetteket sosem skálázza.

A blokkot bármikor törölheted, hogy visszatérj a normál rutin-edzéshez.

---

## 10. Automatikus Frissítés és Karbantartás

Az app indításkor ellenőrzi a hivatalos GitHub oldalát (**ateszk0/Ostromgep-workout-app**):

- Egy felugró ablak értesít az új verzióról.
- Az **Update** gomb a böngésződben megnyitja a release oldalt az új `.apk` letöltéséhez. Előtte exportáld az adataidat.
- Sose akasztja meg az edzést: internet nélkül némán fut a háttérben.

---

*Jó edzést és sikeres fejlődést az Ostromgéppel!*
