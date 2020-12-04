---
title: Azure PowerShell-szkriptek áttelepítése az AzureRM modulból az Az modulba
description: Ismerje meg az Azure PowerShell-szkriptek az AzureRM-ből az új Az PowerShell-modulba való migrálására szolgáló lépéseket és eszközöket.
ms.devlang: powershell
ms.service: azure-powershell
ms.topic: conceptual
ms.date: 12/1/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: bc37d0b73db0e6df226788795730730c077fcefa
ms.sourcegitcommit: cd243c8f6dc02dbd6234e764b065643dfd31dd8b
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/02/2020
ms.locfileid: "96502589"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a>Az Azure PowerShell migrálása az AzureRM modulból az Az modulba

Az AzureRM PowerShell-modul minden verziója elavult. Mostantól az [Az PowerShell-modul](install-az-ps.md) használatát javasoljuk az Azure-ral folytatott interakciókhoz.

## <a name="why-a-new-module"></a>Miért van szükség új modulra?

A legnagyobb és legfontosabb változás, hogy a .NET Standard-kódtáron alapuló [PowerShell](/powershell/scripting/overview) bevezetése óta a PowerShell platformfüggetlen termékké vált.

Ahogy a PowerShell nyelv esetében, most is elkötelezettek vagyunk az Azure-támogatás valamennyi platformra történő kiterjesztésében. Ez azt jelenti, hogy az Azure PowerShell-modulokat frissíteni kell a .NET Standard használata és a PowerShell Core-kompatibilitás érdekében. Ahelyett, hogy a meglévő AzureRM modulon hajtottunk volna végre összetett módosításokat a támogatás hozzáadásához, létrehoztuk az Az modult.

Egy új modul létrehozása lehetővé tette a mérnökeink számára, hogy egységesítsék a parancsmagok és modulok kialakítását és elnevezését. Mostantól az összes modul neve `Az.` előtaggal kezdődik, a parancsmagok pedig mind a `Verb-AzNoun` formát alkalmazzák. Ezt megelőzően a parancsmagnevek hosszabbak és inkonzisztensek voltak.

A modulok száma is csökkent: Egyes modulokat, amelyek ugyanazokkal a szolgáltatásokkal működtek, összevontunk. Mostantól egyazon szolgáltatás felügyeleti és adatsíkra vonatkozó parancsmagjait egyetlen modul tartalmazza. Azok számára, akik manuálisan kezelik a függőségeket és az importálásokat, ez az összevonás egyszerűbbé teszi a feladatokat.

Az új fontos módosítások elkészítésével a csapat elkötelezte magát amellett, hogy az Azure PowerShell-parancsmagokkal való használatát minden korábbinál egyszerűbbé tegye, valamint még több platformra kiterjessze.

## <a name="upgrading-to-az-powershell"></a>Frissítés az Az PowerShellre

Az AzureRM-parancsmagokhoz írt szkriptek nem működnek automatikusan az Az modullal. A váltás megkönnyítése érdekében lett kifejlesztve az [AzureRM és Az közötti migrálási eszközkészlet](https://github.com/Azure/azure-powershell-migration). Az új parancskészletekre való áttérés soha nem egyszerű, ebben a cikkben azonban segítünk megismerkedni az Az PowerShell-modulra való átállás alapjaival. Ha érdekli, miért jött létre az Az PowerShell-modul, olvassa el [az Azure PowerShell új Az moduljának ismertetését](new-azureps-module-az.md).

Az új parancsmagnevek úgy lettek kidolgozva, hogy könnyen megjegyezhetők legyenek. A parancsmagnevekben az `AzureRm` és az `Azure` helyett az `Az` használható. Például a régi `New-AzureRMVm` parancs megfelelője a `New-AzVm` parancs lett.
A migrálás azonban többet jelent az új parancsmagok nevének megismerésénél. Vannak átnevezett modulok, paraméterek és más fontos változások is.

Az AzureRM és az Az közötti kompatibilitástörő változások teljes listáját [az AzureRM és az Az közötti változások teljes listájában](migrate-az-1.0.0.md) találja.

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a>Annak ellenőrzése, hogy a meglévő szkriptek működnek-e az AzureRM legújabb kiadásával

A migrálási lépések előtt ellenőrizze, hogy az AzureRM mely verziói vannak telepítve a rendszeren.
Ezzel biztosíthatja, hogy a szkriptek már a legújabb kiadáson fussanak, és megtudhatja, hogy az AzureRM mely verzióit kell eltávolítania.

Az AzureRM telepített verziója/verziói megtekintéséhez futtassa a következő példaparancsot:

```azurepowershell
Get-Module -Name AzureRM -ListAvailable -All
```

Az AzureRM **legújabb** elérhető kiadása a **6.13.1-es**. Ha nincs telepítve ez a verzió, a meglévő szkriptek további módosítást is igényelhetnek az ebben a cikkben és a [kompatibilitástörő változások listájában](migrate-az-1.0.0.md) leírtakon túlmenően, hogy használni lehessen őket az Az modullal.

Ha a szkriptek nem működnek az AzureRM 6.13.1-es verziójával, frissítse őket az [AzureRM 5.x és 6.x migrálási útmutatója](/powershell/azure/azurerm/migration-guide.6.0.0) szerint. Ha az AzureRM modul korábbi verzióját használja, mindegyik fő verzióhoz elérhető migrálási útmutató.

## <a name="option-1-recommended-automatically-migrate-your-powershell-scripts"></a>1\. lehetőség (ajánlott): PowerShell-szkriptek automatikus migrálása

Ez az ajánlott lehetőség minimálisra csökkentheti az AzureRM-szkriptek az Az-ba való migrálásához szükséges erőfeszítést.

### <a name="install-the-azurerm-to-az-migration-toolkit"></a>Az AzureRM és Az közötti migrálási eszközkészlet telepítése

```azurepowershell
Install-Module -Name Az.Tools.Migration
```

### <a name="convert-your-scripts-automatically"></a>Szkriptek automatikus konvertálása

Az AzureRM és Az közötti migrálási eszközkészlettel létrehozhat egy tervet, amely megállapítja, milyen módosításokat kell végrehajtani a szkripteken, mielőtt valóban módosítaná azokat és telepítené az Az PowerShell-modult.

A [PowerShell-szkriptek az AzureRM modulból az Az PowerShell-modulba történő automatikus migrálásának](quickstart-migrate-azurerm-to-az-automatically.md) gyorsútmutatója végigvezet a PowerShell-szkriptek AzureRM-ből az Az PowerShell-modulba való automatikus frissítésének teljes folyamatán.

## <a name="option-2-use-compatibility-mode-with-enable-azurermalias"></a>2\. lehetőség: Kompatibilitási üzemmód használata az Enable-AzureRmAlias parancsmaggal

Az Az modul kompatibilitási módjával továbbra is használhatja a meglévő szkripteket az új szintaxis frissítése közben. Az [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) parancsmag aliasok segítségével kompatibilitási módot biztosít. Ez az üzemmód lehetővé teszi a meglévő szkriptek minimális módosítással történő használatát, míg az Az-be történő teljes migráláson dolgozik. Alapértelmezés szerint az `Enable-AzureRmAlias` a kompatibilitási aliasokat csak az aktuális PowerShell-munkamenethez engedélyezi. Használja a `Scope` paraméterét a kompatibilitási aliasok PowerShell-munkamenetek közötti megtartásához. További információ az [Enable-AzureRmAlias referenciadokumentációjában](/powershell/module/az.accounts/enable-azurermalias) található.

> [!IMPORTANT]
> Annak ellenére, hogy a parancsmagok aliasnévvel rendelkeznek, az Az-parancsmagoknak lehetnek új (vagy átnevezett) paraméterei, illetve módosított visszaadott értékei. Az aliasok engedélyezése nem elegendő a migrálás elvégzéséhez. Tekintse meg a [kompatibilitástörő változások teljes listáját](migrate-az-1.0.0.md), amelyből megtudhatja, hol lehet szükség a szkriptek frissítésére.

## <a name="option-3-migrate-your-scripts-in-visual-studio-code-with-the-azure-powershell-extension"></a>3\. lehetőség: Migrálja a szkripteket a Visual Studio Code-ban az Azure PowerShell-bővítménnyel

### <a name="install-the-azure-powershell-extension-for-visual-studio-code"></a>Telepítse a Visual Studio Code-hoz készült Azure PowerShell-bővítményt

Telepítse a [VSCode-hoz készült Azure PowerShell-bővítményt](https://marketplace.visualstudio.com/items?itemName=azps-tools.azps-tools)

### <a name="convert-your-scripts-manually"></a>Konvertálja manuálisan a szkripteket

1. Töltse be az AzureRM-et a VSCode-ban
2. Indítsa el a migrálást a parancspaletta (`Ctrl+Shift+P`) megnyitásával, majd a `Migrate Azure PowerShell script` lehetőség kiválasztásával
3. Válassza ki az `AzureRM` forrásverziót
4. Kövesse az egyes aláhúzott parancsokhoz vagy paraméterekhez ajánlott műveleteket.

## <a name="next-steps"></a>További lépések

[Az AzureRM eltávolítása](uninstall-az-ps.md#uninstall-the-azurerm-module)
[Az Azure PowerShell telepítése](install-az-ps.md)
