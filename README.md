# Linux alapok gyakorlat tantárgy (72 óra)
#### 1 év, 36 hét, 2 óra hetente


        11.3. Témakörök
            11.3.1. Linux parancssor használata
A témakör célja a gyakorlati parancssor használat készségszintű elsajátíttatása. A tanulók legyenek képesek Linux parancsokat használni, az egyes utasítások szintaktikáját, a paraméterek használatát önállóan kideríteni. Az alábbi felsorolás tartalmazza a témakör tanítása során feldolgozandó tartalmakat:
1. –	Virtuális terminálok használata.
1. –	Linux parancssor megismerése néhány utasításon keresztül (pl. whoami, uname, pwd).
1. –	Parancselőzmények használata.
1. –	Környezeti változók, $PATH kiíratása képernyőre. A echo és which utasítások.
1. –	Helyettesítő karakterek használata.
1. –	Alias nevek megadása.
1. –	Manuálok használata. A whatis utasítás.
1. –	Az info oldalak használata.
1. –	Utasítások --help opciója.
1. –	Fájlok keresése, a locate utasítás.

            11.3.2. Fájl- és könyvtárkezelés, tömörítés
A témakör célja, hogy a tanulók legyenek képesek önállóan egyszerű fájl- és könyvtárkezelés műveleteket elvégezni, fájlokat és könyvtárakat archiválni és tömöríteni. Az alábbi felsorolás tartalmazza a témakör tanítása során feldolgozandó tartalmakat:
1. –	Navigáció a könyvtárszintek között, a cd és pwd parancsok.
1. –	Könyvtártartalom kilistázása.
1. –	Fájlok megtekintése, a cat, more és less utasítások használata.
1. –	Fájlok és könyvtárak másolása, áthelyezése és átnevezése.
1. –	Fájlok és könyvtárak létrehozása és törlése.
1. –	Fájlok véletlen felülírásának megakadályozása.
1. –	Szimbolikus és hard linkek létrehozása.
1. –	Fájlrendszerek csatolása: a mount utasítás.
1. –	Archív és tömörített állományok létrehozása, kicsomagolása: tar, gzip, és zip/unzip utasítások használata.

            11.3.3. Bevezetés a héjprogramozásba
A témakör célja a tanulók héjprogramozásba való bevezetése. Nem cél, hogy a tanulók képesek legyenek egy összetett szkript megírására, de ismerjék a paraméter átadást, és a vezérlőszerkezetek (elágazás, ciklus) használatának módját. A témakör feldolgozása során ismerjenek meg legalább egy szkriptek megírására alkalmas parancssori szövegszerkesztő programot. Az alábbi felsorolás tartalmazza a témakör tanítása során feldolgozandó tartalmakat:
1. –	I/O átirányítás.
1. –	Fájlok és fájltartalmak keresése.
1. –	Utasítások láncolása (pipeline).
1. –	Szöveges fájlok létrehozása, szerkesztése.
1. –	Egyszerű shell szkriptek létrehozása, paraméter átadás.
1. –	Vezérlőszerkezetek használata szkriptekben.

            11.3.4. Hálózati beállítások ellenőrzése, konfigurációja
A témakör célja, hogy a tanulók képesek legyenek a hálózati beállítások ellenőrzésére, azok konfigurálására. Az alábbi felsorolás tartalmazza a témakör tanítása során feldolgozandó tartalmakat:
1. –	Hálózati beállítások ellenőrzése, az ifconfig utasítás.
1. –	Irányítási információk megjelenítése, a route utasítás.
1. –	Az /etc/hosts fájl vizsgálata.
1. –	A localhost és egyéb hosztok elérhetőségének vizsgálata ping utasítással..
1. –	Névszerver ellenőrzése, az /etc/resolv.conf fájl vizsgálata.
1. –	A netstat program használata.
1. –	Hálózati interfész konfigurációja, alapértelmezett átjáró beállítása.
1. –	Az ssh utasítás.

            11.3.5. Csomag- és processzkezelés
A témakör célja, hogy a tanulók legyenek képesek a használt Linux rendszerben csomagokat telepíteni, frissíteni, törölni, valamint a telepített csomagok listáját megjeleníteni. Tudják továbbá megnézni a futó processzeket, azok futását szükség esetén megszakítani. Az alábbi felsorolás tartalmazza a témakör tanítása során feldolgozandó tartalmakat:
1. –	Csomagkezelés, csomagtípusok.
1. –	Debian csomagok telepítése, frissítése, törlése és kilistázása.
1. –	RPM csomagok telepítése, frissítése, törlése és kilistázása.
1. –	Processz hierarchia, a pstree utasítás.
1. –	Folyamatok listázása: ps és top utasítások használata.
1. –	Futó processz megszakítása.
1. –	Napló fájlok vizsgálata.

            11.3.6. Felhasználói fiókok kezelése
A témakör célja, hogy a tanulók képesek legyenek parancssori eszközökkel csoportokat és felhasználókat létrehozni, törölni, módosítani, az egyes felhasználókat csoportokhoz hozzárendelni. Az alábbi felsorolás tartalmazza a témakör tanítása során feldolgozandó tartalmakat:
1. –	Bejelentkezés rendszergazdaként: su és sudo utasítások használata.
1. –	A who és w utasítások.
1. –	Csoportok létrehozása, törlése, módosítása: groupadd, groupdel, groupmod utasítások.
1. –	Az /etc/group fájl vizsgálata.
1. –	Felhasználói fiókok létrehozása, törlése, módosítása: useradd, userdel és usermod utasítások.
1. –	Felhasználói fiókok csoporthoz rendelése.

            11.3.7. Jogosultságok beállítása
A témakör célja, hogy a tanulók legyenek képesek fájloknak és könyvtáraknak a tulajdonosának, csoportjának a meghatározására, azok megváltoztatására. Tudják az olvasási, írási és végrehajtási jogokat igény szerint beállítani. Az alábbi felsorolás tartalmazza a témakör tanítása során feldolgozandó tartalmakat:
1. –	Fájlok és könyvtárak tulajdonosának és csoportjának meghatározása.
1. –	Fájlok és könyvtárak tulajdonosának a megváltoztatása: a chown utasítás.
1. –	Fájl és könyvtárak jogosultságai, azok beállítása: a chmod utasítás.
