# Dátum módosító VBA program – szabályalapú napeltolás

## 1. Mit csinál a program?

A program egy munkalap **kiválasztott dátumoszlopában** szereplő dátumokból új dátumokat számít az általad megadott **hét napja + napeltolás** szabályok alapján.

**Működés:**
- Meghatározott napokra (pl. szerda) napeltolást alkalmaz (pl. +5 nap)
- Ha egy dátum megfelel egy szabálynak, a VBA program napokat **hozzáad vagy kivon**
- Ha egy dátumhoz nincs megadott szabály, az **eredeti dátum** kerül át az új oszlopba
- A feldolgozás végén a program **összesíti**, hány dátum módosult

**Példa:**  
A szerdai napokra +5 nap eltolás kerül alkalmazásra.

---

## 2. Hogyan kell használni?

A program futtatásakor egymás után a következő adatokat kéri be:

### Oszlopok megadása
- Melyik oszlopban vannak az **eredeti dátumok**  
  (pl. `2` = B oszlop)
- Melyik oszlopba kerüljön az **új dátum**  
  (pl. `3` = C oszlop)

Az új oszlop tetejére automatikusan bekerül a fejléc:  
**„Módosított dátum”**

---

### Színezés beállítása
A program rákérdez, szeretnéd-e a módosított dátumok kiemelését:

- **Igen** → a módosult cellák halványsárga háttérszínt kapnak  
- **Nem** → nincs színezés, csak az új dátum kerül beírásra

---

### Szabályok megadása

Ezután egyesével megadhatod a dátummódosítási szabályokat.

#### Hét napja (számmal):
- `1` = Hétfő  
- `2` = Kedd  
- `3` = Szerda  
- `4` = Csütörtök  
- `5` = Péntek  
- `6` = Szombat  
- `7` = Vasárnap  

#### Napeltolás:
- Pozitív szám → előre tolás  
- Negatív szám → vissza tolás  

**Példák:**
- `+3` → három nappal később  
- `-2` → két nappal korábban  

Több szabály is megadható egymás után.

**Példa szabálylista:**
- Hétfő (+3)
- Szerda (-1)
- Péntek (+2)

Ha végeztél a szabályok megadásával, kattints a **Mégse (Cancel)** gombra a hét napjának megadásakor.

---

### Feldolgozás
A program:
- végigmegy az összes dátumon,
- alkalmazza a megadott szabályokat,
- az eredményt az új oszlopba írja.

---

## 3. A futás végén

A feldolgozás után:

- Megjelenik egy üzenet, amely mutatja, **hány dátum módosult**
- Az új oszlopban megtalálhatók a **kiszámított dátumok**
- Ha engedélyezted, a módosított sorok **sárga háttérrel kiemelve** jelennek meg

---

## 4. Videó bemutató

🎥 **Nézd meg a fájlok között található videót a program működéséről:**  
*(ide illeszd be a videó linkjét)*

