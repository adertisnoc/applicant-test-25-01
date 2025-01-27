# Konténerizált PHP alkalmazás és MariaDB backend beállítása frontend proxyn keresztül

## Feladat leírása

### Az alkalmazás 

Egy egyszerű, minta PHP alkalmazást használunk, elérhetősége: https://github.com/mariadb-developers/php-quickstart

### Feladat célja

Konténerizáld az alkalmazást.
Hozz létre egy MariaDB adatbázis-konténert, amelyet az alkalmazás használ.
Állíts be egy frontend proxyt, amelyen keresztül az alkalmazás elérhető lesz a böngészőben.
Készíts telepítési és üzemeltetési dokumentációt a projekthez.

### Elvégzendő lépések

#### Dockerfile létrehozása a PHP alkalmazás számára

Használd a PHP hivatalos Docker image-ét (php:8.2-apache vagy hasonló).
Másold be a forráskódot a konténerbe.
Telepítsd/engedélyezd a szükséges PHP-bővítményeket (pl. pdo_mysql).

#### docker-compose.yml fájl készítése

Indíts a PHP alkalmazást külön konténerben.
Indíts egy MariaDB adatbázis-konténert, az alkalmazáshoz tartozó séma inicializálásával ha szükséges.
Állíts be egy proxyt, amely biztosítja, hogy az alkalmazás elérhető legyen egy adott hostname (pl. php-app.local) alatt.

#### Hálózati kapcsolatok

Gondoskodjon arról, hogy a PHP alkalmazás megfelelően tudjon csatlakozni a MariaDB-hez, valamint arról hogy minden konténer csak a szükséges hálózathoz vagy másik konténerhez csatlakozhasson.

#### Dokumentáció

Készíts dokumentációt Markdown formátumban, amely tartalmazza a lépéseket a rendszer telepítéséhez és indításához.
Adj néhány troubleshooting tippet, monitorozási lehetőséget. Fejtsd ki, hogy a rendszert hogyan lehet a futtató gép indulásakor elindítani automatikusan.

### Végeredmény

Egy működő alkalmazás, amelyet böngészőben elérhetünk a proxy által biztosított útvonalon.
Dokumentáció, amely tartalmazza:

- az alkalmazás indításának lépéseit
- hogyan lehet hozzáférni az alkalmazáshoz
- a használt konfigurációk rövid magyarázatát

## Alternatív megoldási lehetőségek, tippek

A feladatot a Dockertől eltérhető környezetben is megvalósíthatod, pl. MicroK8s vagy Podman konténerek és Podman Compose használatával.

A feladat megvalósításához bármilyen segítséget igénybe vehetsz, de a feladat bemutatásakor a végeredmény működésének lényegét át kell tudnod adni, illetve értened kell a rendszer működését.

Kiegészítések, javítások megengedettek, a dokumentációba is kerülhet olyan témakör, amely nem volt a feladat meghatározott célja.
