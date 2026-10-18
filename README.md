# BRTG modpack katalógus

Ez a nyilvános, a launcher forráskódjától különálló katalógus-repó. A BRTG Launcher az itt tárolt `catalog.json` fájlt olvassa, a letöltés után ellenőrzi a ZIP SHA-256 lenyomatát, majd az archívum importját átadja a Prism Launchernek. A repó fájljai bárki számára elérhetők.

## Csomag közzététele

1. Készítsd el és teszteld a modpackot Prism Launcherben.
2. Exportáld olyan ZIP-fájlba, amelyet a Prism Launcher importálni tud.
3. Feltöltés előtt távolítsd el a személyes vagy géphez kötött adatokat: szerverlistákat és címeket, világmentéseket, kliensállapotot, naplókat és hitelesítő adatokat.
4. Töltsd fel a ZIP-et ennek a repónak a GitHub Release-éhez. Minden packkiadáshoz használj egyedi verziót és letöltési fájlnevet.
5. Add hozzá a `catalog.json` `packs` listájához a pack adatait és a kiadás HTTPS-letöltési címét.
6. Számold ki a ZIP SHA-256 lenyomatát, és írd be a `sha256` mezőbe. A launcher telepítés előtt ellenőrzi ezt az értéket.

## Katalógusbejegyzés formátuma

```json
{
  "id": "brtg-survival",
  "name": "BRTG Survival",
  "description": "Rövid leírás a modpackról.",
  "minecraftVersion": "1.20.1",
  "loader": "Forge",
  "version": "1.0.0",
  "downloadUrl": "https://github.com/Hunday2001/BRTGLauncherModpacks/releases/download/brtg-survival-1.0.0/brtg-survival-1.0.0.zip",
  "sha256": "64 hexadecimális karakterből álló SHA-256 érték"
}
```

Az első katalógusbejegyzés a **Hunday 26.3 Fabric Client** csomag. Amikor új packot teszel a listába és a Release-hez feltöltöd a ZIP-et, az minden telepített BRTG Launcherben megjelenik a **Közösségi packok** oldalon a következő katalógusfrissítéskor.
