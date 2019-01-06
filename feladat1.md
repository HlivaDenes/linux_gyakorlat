# Feladatsor

1. Írassuk ki az aktuális könyvtár nevét:
```bash
$pwd
```
2. Írassuk ki az aktuális könyvtár tartalomjegyzékét teljes részletességgel:

$ls –la

3. Hozzunk létre egy temp és egy munka könyvtárat az aktuális könyvtáron belül:

$mkdir temp
$mkdir munka

4. Készítsünk egy szöveges állományt forras néven a saját könyvtárunkban bármilyen
tartalommal. A Ctrl+D billentyűkombináció hatására befejeződik a beírás, és lementődik a
szöveg.
$cat > forras
szöveg
Ctrl+D

5. Nézzük meg az állomány tartalmát:
$cat forras

6. Másoljuk be az állományt a temp és a munka könyvtárakba forr_temp és forr_munka
néven.
$cp ./forras ./temp/forr_temp
$cp forras munka/forr_munka

7. Tegyük a forr_temp–et írásvédetté:
$chmod –w ./temp/forr_temp

8. Készítsünk a munka könyvtárban hardlinket a forras állományra:
$ln ./forras ./munka/forras_link

9. Készítsünk a temp könyvtárban szimbolikus hivatkozást a forras állományra:
$ln –s /home/hallgato/forras ./temp/forras_szlink

10. Nézzük meg, hogy hány hardlink hivatkozás van a forras-ra:
$ls –la forras

11. Töröljük az egyik merev keresztkapcsolatot. Írassuk ki, hogy ezután hány hivatkozás van a
forras-ra.
$rm ./munka/forras_link

12. Töröljük a konzolablak tartalmát.
$clear

13. Csomagoljuk be a munka, és a temp könyvtárakat valamint a forras állományt.
$tar –cvf csomag.tar munka temp forras 

14. Ellenőrizzük le a csomag tartalmát:
$tar –tvf csomag.tar

15. Tömörítsük a csomagot:
$gzip csomag.tar

16. Mozgassuk át a csomagot a munka könyvtárba, és csomagoljuk ott ki:
$mv csomag.tar.gz ./munka
$gzip –dv ./munka/csomag.tar.gz.

17. Lépjünk be a munka könyvtárba majd csomagoljuk ott ki a csomag.tar állományt.
$cd munka
$tar –xvf csomag.tar

18. Lépjünk ki a munka könyvtárból, majd töröljük a munka és a temp könyvtárakat.
$cd ..
$rm –dvr munka
$rm –dvr temp

19. Töröljük a forrás állományt.
$rm forras

