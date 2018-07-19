---
title: Kísérleti Azure PowerShell-modulok használata
description: A kísérleti Azure PowerShell-modulok filozófiájának és használatának ismertetése.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/05/2017
ms.openlocfilehash: ac571363d79c83b268b5c25f65b14f16d4b86e71
ms.sourcegitcommit: 8b882d1c27d9e323447ff85f56d11bbf5e244d7f
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2018
ms.locfileid: "39110415"
---
# <a name="using-experimental-azure-powershell-modules"></a>Kísérleti Azure PowerShell-modulok használata

Mivel az Azure a fejlesztői eszközökre (különösen a parancssori felületekre) helyezi a hangsúlyt, az Azure PowerShell csapata az Azure PowerShell felhasználói felületének számos fejlesztésével kísérletezik.

## <a name="experimentation-methodology"></a>Kísérleti módszertan

A kísérletezés érdekében új Azure PowerShell-modulokat hozunk létre, amelyek az Azure SDK meglévő funkcióit új, könnyebben használható módon kezelik. A parancsmagok a legtöbb esetben pontosan megegyeznek a meglévő parancsmagokkal. A kísérleti parancsmagok azonban olyan egyszerűsített jelölésrendszert és intelligensebb alapértelmezett értékeket kínálnak, amelyekkel könnyebben hozhatók létre és kezelhetők az Azure-erőforrások.

Ezek a modulok a meglévő Azure PowerShell-modulok mellett telepíthetők. A parancsmagneveket lerövidítettük, hogy rövidebb neveket kelljen megadni, illetve hogy elkerüljük a névütközést a meglévő, nem kísérleti parancsmagokkal.

A kísérleti modulok az alábbi elnevezési szabályt követik: `AzureRM.*.Experiments`. Ez a elnevezési szabály az előzetes verziójú modulok elnevezéséhez hasonló: `AzureRM.*.Preview`. Az előzetes verziójú modulok nem azonosak a kísérleti modulokkal. Az előzetes modulok az Azure-szolgáltatások olyan új funkcióit valósítják meg, amelyek csak előzetes ajánlatként érhetők el. Az előzetes verziójú modulok a meglévő Azure PowerShell-modulokat váltják fel, és ugyanazokat a parancsmag- és paraméterneveket használják.

## <a name="how-to-install-an-experimental-module"></a>A kísérleti modulok telepítése

A kísérleti modulok a meglévő Azure PowerShell-modulokhoz hasonlóan a PowerShell-galériában vannak közzétéve. A kísérleti modulok listájának megtekintéséhez futtassa a következő parancsot:

```azurepowershell-interactive
Find-Module AzureRM.*.Experiments
```

```output
Version Name                         Repository Description
------- ----                         ---------- -----------
1.0.25  AzureRM.Compute.Experiments  PSGallery  Azure Compute experiments for VM creation
1.0.0   AzureRM.Websites.Experiments PSGallery  Create and deploy web applications using Azure App Services.
```

A kísérleti modulok telepítéséhez használja a következő parancsokat egy emelt szintű PowerShell-munkamenetből:

```azurepowershell-interactive
Install-Module AzureRM.Compute.Experiments
Install-Module AzureRM.Websites.Experiments
```

### <a name="documentation-and-support"></a>Dokumentáció és támogatás

A dokumentációt a telepítőcsomag tartalmazza, és a `Get-Help` parancsmaggal érhető el. A kísérleti modulokhoz nem jelenik meg hivatalos dokumentáció.

Javasoljuk, hogy tesztelje ezeket a modulokat. A visszajelzések segítenek nekünk a modulok használhatóságának fejlesztésében és a felhasználói igények kielégítésében. Mivel azonban ezek kísérleti modulok, csak korlátozott támogatás érhető el hozzájuk. Kérdéseit és a hibajelentéseket egy [hibajegy](https://github.com/Azure/azure-powershell/issues) létrehozásával küldheti be a GitHub-adattárban.

## <a name="experiments-and-areas-of-improvement"></a>Kísérletek és fejlesztési területek

Ezeket a fejlesztéseket a versenytársaink termékeinek főbb előnyei alapján választottuk ki. Például az Azure CLI 2.0 egyik fontos eleme, hogy a parancsok _forgatókönyveken_, és nem _API felületeken_ alapulnak.
Az Azure CLI 2.0 számos intelligens alapértelmezett értéket alkalmaz, amelyekkel az „első lépések” forgatókönyvek könnyebben használhatók a végfelhasználók számára.

### <a name="core-improvements"></a>Központi fejlesztések

A központi fejlesztések a „józan megfontoláson” alapulnak, és az ilyen frissítések bevezetéséhez nem sok kísérletezés szükséges.

- Forgatókönyv-alapú parancsmagok – **Minden* parancsmagot forgatókönyvek, és nem az Azure REST-szolgáltatás köré kell építeni.

- Rövidebb nevek – Ez a parancsmagok (például: `New-AzureRmVM` => `New-AzVm`) és a paraméterek (például: `-ResourceGroupName` => `-Rg`) nevére is vonatkozik. A „régi” parancsmagokkal való kompatibilitás érdekében aliasok használhatók. Biztosítson _visszafelé kompatibilis_ paraméterkészleteket.

- Intelligens alapértékek – Adja meg a „szükséges” információkat intelligens alapértelmezett értékekkel. Például:
  - Erőforráscsoport
  - Hely
  - Függő erőforrások

### <a name="experimental-improvements"></a>Kísérleti fejlesztések

A kísérleti fejlesztések segítségével a csoport kísérletezéssel tesztelheti a jelentős változásokat.

- Egyszerű típusok – A létrehozási forgatókönyveknek távol kell esniük az összetett típusoktól és a konfigurációs objektumoktól. Egyszerűsítse a konfigurációt egy vagy két paraméterre.

- „Intelligens létrehozás” – Az „intelligens létrehozást” megvalósító egyik létrehozási forgatókönyvhöz _sincs_ kötelező paraméter: az összes szükséges információt az Azure PowerShell választja ki a saját belátása szerint.

- Szürke paraméterek – Sok esetben néhány paraméter „szürke” vagy félig választható. Ha a paraméter nincs megadva, a rendszer megkérdezi a felhasználót, hogy létrejöjjön-e a paraméter. Szintén célszerű, ha a szürke paraméterek a környezet alapján következtetnek ki egy értéket a felhasználó beleegyezésével.
  Hasznos lehet például, ha a szürke paraméter a legutóbb használt értéket javasolja.

- `-Auto` kapcsoló – Az `-Auto` kapcsoló „felhasználó által aktiválható” módon biztosítja a felhasználóknak _az összes beállítás alapértelmezett értékre való állítását_, ugyanakkor fenntartja a kötelező paraméterek integritását a fő útvonalon.

### <a name="feature-specific-switches"></a>Szolgáltatásspecifikus kapcsolók

A „Webalkalmazás létrehozása” forgatókönyv például egy `-Git` vagy `-AddRemote` kapcsolóval rendelkezhet, amely automatikusan egy távoli „azure” mappát ad hozzá egy meglévő Git-adattárhoz.

- Beállítható alapértelmezett értékek – A felhasználóknak képesnek kell lenniük arra, hogy alaphelyzetbe állítsanak bizonyos mindenütt jelenlevő paramétert (például `-ResourceGroupName` és `-Location`).

- Alapértelmezett méretek – Az erőforrások „méretei” megtéveszthetik a felhasználókat, mert sok erőforrás-szolgáltató különböző neveket használ (például „\_DS1\_v2 szabvány” vagy „S1”). A legtöbb felhasználót azonban jobban érdeklik a költségek. Ezért logikus „univerzális” méreteket meghatározni egy díjszabási ütemezés alapján. A felhasználók adott méretet választhatnak vagy hagyhatják, hogy az Azure PowerShell kiválassza a _legjobb lehetőséget_ az erőforrás és a költségvetés alapján.

- Kimeneti formátum – Az Azure PowerShell jelenleg `PSObject` elemeket ad vissza, és kevés konzolkimenet van. Lehetséges, hogy az Azure PowerShellnek információt kell megjelenítenie a felhasználónak a használt „intelligens alapértékekről”.
