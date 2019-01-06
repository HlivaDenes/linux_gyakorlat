Írassuk ki az aktuális könyvtár nevét:
$pwd

Írassuk ki az aktuális könyvtár tartalomjegyzékét teljes részletességgel:
$ls –la

Hozzunk létre egy temp és egy munka könyvtárat az aktuális könyvtáron belül:
$mkdir temp
$mkdir munka

Készítsünk egy szöveges állományt forras néven a saját könyvtárunkban bármilyen
tartalommal. A Ctrl+D billentyűkombináció hatására befejeződik a beírás, és lementődik a
szöveg.
$cat > forras
szöveg
Ctrl+D

Nézzük meg az állomány tartalmát:
$cat forras

Másoljuk be az állományt a temp és a munka könyvtárakba forr_temp és forr_munka
néven.
$cp ./forras ./temp/forr_temp
$cp forras munka/forr_munka

Tegyük a forr_temp–et írásvédetté:
$chmod –w ./temp/forr_temp

Készítsünk a munka könyvtárban hardlinket a forras állományra:
$ln ./forras ./munka/forras_link

Készítsünk a temp könyvtárban szimbolikus hivatkozást a forras állományra:
$ln –s /home/hallgato/forras ./temp/forras_szlink

Nézzük meg, hogy hány hardlink hivatkozás van a forras-ra:
$ls –la forras

Töröljük az egyik merev keresztkapcsolatot. Írassuk ki, hogy ezután hány hivatkozás van a
forras-ra.
$rm ./munka/forras_link

Töröljük a konzolablak tartalmát.
$clear

Csomagoljuk be a munka, és a temp könyvtárakat valamint a forras állományt.
$tar –cvf csomag.tar munka temp forras 

Ellenőrizzük le a csomag tartalmát:
$tar –tvf csomag.tar

Tömörítsük a csomagot:
$gzip csomag.tar

Mozgassuk át a csomagot a munka könyvtárba, és csomagoljuk ott ki:
$mv csomag.tar.gz ./munka
$gzip –dv ./munka/csomag.tar.gz.

Lépjünk be a munka könyvtárba majd csomagoljuk ott ki a csomag.tar állományt.
$cd munka
$tar –xvf csomag.tar

Telepítsük fel a tree programot.
$sudo apt-get install tree

Vizsgáljuk meg a munka alatti könyvtárak tartalmát a tree parancs segítségével.
$tree

Lépjünk ki a munka könyvtárból, majd töröljük a munka és a temp könyvtárakat.
$cd ..
$rm –dvr munka
$rm –dvr temp

Töröljük a forrás állományt.
$rm forras

Hozzunk létre egy felhasználót interaktív módon parancssorból az adduser program segítségével.
$ sudo adduser gyakorlo
"gyakorlo" felhasználó létrehozása...
"gyakorlo" (1002) új csoport létrehozása...
"gyakorlo" (1002) felhasználó létrehozása "gyakorlo"
csoporttal...
A(z)'/home/gyakorlo' saját könyvtár létrehozása...
Fájlok másolása innen: '/etc/skel'
Adja meg az új UNIX jelszót:
Írja be újra a UNIX jelszót:
passwd: a jelszó sikeresen frissült
gyakorlo felhasználói információinak cseréje
Add meg az új értéket vagy üss ENTER-t az alapértelmezetthez
TELJES Név []: Gyakorló Hallgató
Szobaszám []: 13
Munkahelyi telefon []: 1313
Otthoni telefon []: +36-99-999999
Egyéb []:
Is the information correct? [Y/n] Y

Ellenőrizzük le az eredményt:
$ cat /etc/passwd | grep gyakorlo
gyakorlo:x:1002:1002:Gyakorló Hallgató,13,1313,+36-99-
999999:/home/gyakorlo:/bin/bash

Jelentkezzünk be gyakorlo felhasználóként, majd jelentkezzünk ki.

Hozzunk létre egy felhasználót parancssorból mindent előre megadva a useradd program segítségével.
$ sudo useradd dolgozo -c "Dolgozó Jenőke,13,1313,+36-99-
999999" -g users -m -d /home/dolgozo -s /bin/bash
$ sudo passwd dolgozo
Adja meg az új UNIX jelszót:
Írja be újra a UNIX jelszót:
passwd: a jelszó sikeresen frissült

Ellenőrizzük le az eredményt:
$ cat /etc/passwd | grep dolgozo
dolgozo:x:1003:100:Dolgozó Jenőke,99,9999,+36-99-
999999:/home/dolgozo:/bin/bash

Jelentkezzünk be proba felhasználóként, majd jelentkezzünk ki.

Készítsünk egy szkriptet, ami ciklus segítségével létrehoz 9 felhasználói fiókot.
Egy lehetséges megoldást az alábbiakban láthatunk:
#!/bin/bash
# Felhasználói fiókok létrehozása
N=9
for ((a=1; a <= N ; a++))
do
 sudo useradd hallgato$a -c "Hallgató $a" -g users -m -d
/home/hallgato$a -s /bin/bash
done

A fenti mintát követve készítsünk egy szkriptet, ami törli a felhasználókat és könyvtáraikat.


