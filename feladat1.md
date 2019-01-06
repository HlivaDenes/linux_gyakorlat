# Feladatsor

1. Írassuk ki az aktuális könyvtár nevét:
```bash
$pwd
```

2. Írassuk ki az aktuális könyvtár tartalomjegyzékét teljes részletességgel:
```bash
$ls –la
```

3. Hozzunk létre egy temp és egy munka könyvtárat az aktuális könyvtáron belül:
```bash
$mkdir temp
$mkdir munka
```

4. Készítsünk egy szöveges állományt forras néven a saját könyvtárunkban bármilyen
tartalommal. A Ctrl+D billentyűkombináció hatására befejeződik a beírás, és lementődik a
szöveg.
```bash
$cat > forras
szöveg
Ctrl+D
```

5. Nézzük meg az állomány tartalmát:
```bash
$cat forras
```
6. Másoljuk be az állományt a temp és a munka könyvtárakba forr_temp és forr_munka
néven.
```bash
$cp ./forras ./temp/forr_temp
$cp forras munka/forr_munka
```

7. Tegyük a forr_temp–et írásvédetté:
```bash
$chmod –w ./temp/forr_temp
```

8. Készítsünk a munka könyvtárban hardlinket a forras állományra:
```bash
$ln ./forras ./munka/forras_link
```

9. Készítsünk a temp könyvtárban szimbolikus hivatkozást a forras állományra:
```bash
$ln –s /home/hallgato/forras ./temp/forras_szlink
```

10. Nézzük meg, hogy hány hardlink hivatkozás van a forras-ra:
```bash
$ls –la forras
```

11. Töröljük az egyik merev keresztkapcsolatot. Írassuk ki, hogy ezután hány hivatkozás van a
forras-ra.
```bash
$rm ./munka/forras_link
```

12. Töröljük a konzolablak tartalmát.
```bash
$clear
```

13. Csomagoljuk be a munka, és a temp könyvtárakat valamint a forras állományt.
```bash
$tar –cvf csomag.tar munka temp forras 
```

14. Ellenőrizzük le a csomag tartalmát:
```bash
$tar –tvf csomag.tar
```

15. Tömörítsük a csomagot:
```bash
$gzip csomag.tar
```

16. Mozgassuk át a csomagot a munka könyvtárba, és csomagoljuk ott ki:
```bash
$mv csomag.tar.gz ./munka
$gzip –dv ./munka/csomag.tar.gz.
```

17. Lépjünk be a munka könyvtárba majd csomagoljuk ott ki a csomag.tar állományt.
```bash
$cd munka
$tar –xvf csomag.tar
```

18. Lépjünk ki a munka könyvtárból, majd töröljük a munka és a temp könyvtárakat.
```bash
$cd ..
$rm –dvr munka
$rm –dvr temp
```

19. Töröljük a forrás állományt.
```bash
$rm forras
```
