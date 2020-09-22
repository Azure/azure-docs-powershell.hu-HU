---
title: Az Azure PowerShell Az modul bemutatása
description: Bemutatkozik az új Azure PowerShell-modul, az Az, amely az AzureRM modult váltja le.
ms.date: 05/20/2020
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 0771bc474f43d8bbf392f2eba10da2e320d30556
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/01/2020
ms.locfileid: "89242647"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a>Az új Azure PowerShell Az modul bemutatása

2018 decemberétől az Azure PowerShell Az modul általánosan elérhetővé vált, és mostantól ez az Azure-ral való kommunikációhoz használható PowerShell-modul. Az Az rövidebb parancsokat és nagyobb stabilitást kínál, valamint több platformot is támogat. Az Az emellett funkcióparitást kínál az AzureRM-mel, így egyszerű migrálási útvonalat biztosít.

> [!NOTE]
> A PowerShell az Azure PowerShell-lel történő használatához az összes platformon a PowerShell 7.x vagy újabb verziója javasolt.

A legújabb Az modul révén az Azure PowerShell kompatibilis a PowerShell 6.2.4-es vagy újabb verziójával az összes platformon, beleértve a Windows, macOS és Linux rendszereket is. Windows rendszeren a PowerShell 5.1-es verziójával is kompatibilis.

Az Az egy új modul, ezért a verziószámozás vissza lett állítva 1.0.0-ra.

## <a name="why-a-new-module"></a>Miért van szükség új modulra?

A nagyobb frissítések kényelmetlenek lehetnek, ezért fontosnak tartjuk, hogy megosszuk a döntés okát, miért vezettünk be új modulokat, új parancsmagokkal az Azure PowerShellből történő eléréséhez.

A legnagyobb és legfontosabb változás, hogy a .NET Standard-kódtáron alapuló [PowerShell](/powershell/scripting/overview) bevezetése óta a PowerShell platformfüggetlen termékké vált.
Elkötelezettek vagyunk az Azure-támogatás valamennyi platformra történő kiterjesztésében, ami azt jelenti, hogy az Azure PowerShell-modulokat frissíteni kell a .NET standard használata és a PowerShell Core-kompatibilitás érdekében. Ahelyett, hogy a meglévő AzureRM modulon hajtottunk volna végre összetett módosításokat a támogatás hozzáadásához, létrehoztuk az Az modult.

Egy új modul létrehozása lehetővé tette a mérnökeink számára, hogy a parancsmagok és modulok kialakítását és elnevezését egységesítsék. Mostantól az összes modul neve `Az.` előtaggal kezdődik, a parancsmagok pedig mind a _Művelet_-`Az`_Főnév_ formát alkalmazzák. Ezt megelőzően a parancsmagnevek nemcsak hosszabbak voltak, de következetlenségek is voltak bennük.

A modulok száma is csökkent: Egyes modulokat, amelyek ugyanazokkal a szolgáltatásokkal működtek, összevontunk. Mostantól a felügyeleti és az adatsík parancsmagjait a szolgáltatásukhoz tartozó egyetlen modul tartalmazza. Azok számára, akik manuálisan kezelik a függőségeket és az importálásokat, ez egyszerűbbé teszi a feladatokat.

Ezekkel a fontos változtatásokkal, amelyekre az új Azure PowerShell-modul létrehozásához volt szükség, a csapat elkötelezte magát amellett, hogy az Azure PowerShell-parancsmagokkal történő használata minden eddiginél egyszerűbb legyen, és a korábbinál is több platformon legyen használható.

## <a name="upgrade-to-az"></a>Frissítés az Az modulra

Az Azure PowerShell-beli legfrissebb funkcióinak használatához érdemes minél hamarabb áttérnie az Az modul használatára. Ha nem áll készen az Az modul telepítésére az AzureRM helyett, több lehetősége is van, hogy kipróbálja az Az modult:

- Használjon egy `PowerShell` környezetet az [Azure Cloud Shell-lel](https://docs.microsoft.com/azure/cloud-shell/overview). Az Azure Cloud Shell egy böngészőalapú környezet, amely telepített Az modullal és engedélyezett `Enable-AzureRM` kompatibilitási aliasokkal rendelkezik.
- Tartsa meg a Windowshoz készült 5.1-es PowerShell-lel telepített AzureRM modult, de telepítse az Az modult a PowerShell 6.2.4-es vagy újabb verziójához. A Windows rendszerhez készült PowerShell 5.1 és a PowerShell 6.2.4-es és újabb verziói különböző modulgyűjteményeket használnak. Kövesse az utasításokat a [PowerShell legújabb verziójának](/powershell/scripting/install/installing-powershell) telepítéséhez, majd [telepítse az Az modult](install-az-ps.md) a PowerShell 6.2.4-es vagy újabb verziójából.

Frissítés meglévő AzureRM-telepítésből:

1. [Távolítsa el az Azure PowerShell AzureRM modult.](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)
2. [Telepítse az Azure PowerShell Az modult.](install-az-ps.md)
3. **NEM KÖTELEZŐ**: Engedélyezze a kompatibilitási módot, hogy aliasokat adjon az AzureRM-parancsmagokhoz az [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias) paranccsal, amíg meg nem ismeri az új parancskészletet. További részleteket a következő szakaszban vagy az [az AzureRM modulból az Az modulba való áttelepítést](migrate-from-azurerm-to-az.md) ismertető cikkben talál.

## <a name="migrate-existing-scripts-to-az"></a>Meglévő szkriptek áttelepítése az Az modulba

Az új parancsmagnevek úgy lettek kidolgozva, hogy könnyen megjegyezhetők legyenek. A parancsmagnevekben az `AzureRm` és az `Azure` helyett az `Az` használható. Például a régi `New-AzureRMVm` parancs megfelelője a `New-AzVm` parancs lett.
A migrálás azonban többet jelent az új parancsmagok nevének megismerésénél. Vannak átnevezett modulok, paraméterek és más fontos változások is.

Az AzureRM-ből az Az modulba történő migrálás megkönnyítéséhez számos erőforrás áll rendelkezésre:

- [Az AzureRM-ből az Az modulba történő migrálás első lépései](migrate-from-azurerm-to-az.md)
- [Az AzureRM és az Az 1.0.0 közötti kompatibilitástörő változások teljes listája](migrate-az-1.0.0.md)
- Az [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) parancsmag

Az Az modul kompatibilitási módjával továbbra is használhatja a meglévő szkripteket az új szintaxis frissítése közben. Az [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) parancsmag aliasok segítségével kompatibilitási módot biztosít, lehetővé téve a meglévő szkriptek minimális módosítással történő használatát, míg az Az-be történő teljes migráláson dolgozik. Alapértelmezés szerint az `Enable-AzureRmAlias` a kompatibilitási aliasokat csak az aktuális PowerShell-munkamenethez engedélyezi. Használja a `Scope` paraméterét a kompatibilitási aliasok PowerShell-munkamenetek közötti megtartásához. További információ az [Enable-AzureRmAlias referenciadokumentációjában](/powershell/module/az.accounts/enable-azurermalias) található.

> [!IMPORTANT]
> Annak ellenére, hogy a parancsmagok aliasnévvel rendelkeznek, az Az-parancsmagoknak lehetnek új (vagy átnevezett) paraméterei, illetve módosított visszaadott értékei. Az aliasok engedélyezése nem elegendő a migrálás elvégzéséhez. Tekintse meg a [kompatibilitástörő változások teljes listáját](migrate-az-1.0.0.md), amelyből megtudhatja, hol lehet szükség a szkriptek frissítésére.

## <a name="continued-support-for-azurerm"></a>Az AzureRM további támogatása

Az AzureRM modul nem bővül újabb parancsmagokkal vagy funkciókkal. Az AzureRM modul hivatalos karbantartása és hibajavítása azonban 2020 decemberéig nem szűnik meg.