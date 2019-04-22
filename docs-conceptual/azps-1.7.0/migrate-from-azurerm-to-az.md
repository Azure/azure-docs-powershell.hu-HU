---
title: Azure PowerShell-szkriptek áttelepítése az AzureRM modulból az Az modulba
description: Ismerje meg a szkriptek az AzureRM modulból az új Az modulba való áttelepítésére szolgáló lépéseket és eszközöket.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 28122ca953d62b405f19effbbc680f2dc6202cca
ms.sourcegitcommit: ae4540a90508db73335a54408dfd6cdf3712a1e9
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/17/2019
ms.locfileid: "59364186"
---
# <a name="migrate-from-azurerm-to-azure-powershell-az"></a>Áttelepítés az AzureRM modulból az Azure PowerShell Az modulba

Az Az modul a funkciók tekintetében paritásban van az AzureRM modullal, de rövidebb és egységesebb parancsmagneveket használ.
Az AzureRM-parancsmagokhoz írt szkriptek nem működnek automatikusan az új modullal. Az áttérés megkönnyítése érdekében az Az olyan eszközöket nyújt, amelyekkel futtathatja az AzureRM-et használó meglévő szkripteket. Az új parancskészletekre való áttérés soha nem egyszerű, ebben a cikkben azonban segítünk megismerkedni az új modulra való átállás alapjaival.

Az AzureRM és az Az közötti kompatibilitástörő változások teljes listáját [az Az 1.0.0 migrálási útmutatójában](migrate-az-1.0.0.md) találja.

## <a name="check-for-installed-versions-of-azurerm"></a>Az AzureRM telepített verzióinak megtekintése

Az Az modul telepíthető az AzureRM modul mellett, de ez nem ajánlott. A migrálási lépések előtt ellenőrizze, hogy az AzureRM mely verziói vannak telepítve a rendszeren. Ha így tesz, biztosíthatja, hogy a szkriptek már a legújabb kiadáson fussanak, és megtudhatja, hogy engedélyezheti-e a parancsaliasokat az AzureRM eltávolítása nélkül.

Az AzureRM telepített verziója/verziói megtekintéséhez futtassa a következő parancsot:

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

## <a name="ensure-your-existing-scripts-work-with-the-latest-azurerm-release"></a>Gondoskodjon róla, hogy a meglévő szkriptek működjenek az AzureRM legfrissebb kiadásával.

Ez az a legfontosabb lépés! Futtassa a meglévő szkriptjeit, és ellenőrizze, hogy működnek-e az AzureRM _legfrissebb_ kiadásával (__6.13.1__). Ha a szkriptek nem működnek, tekintse át [az AzureRM áttelepítési útmutatóját](/powershell/azure/azurerm/migration-guide.6.0.0).

## <a name="install-the-azure-powershell-az-module"></a>Az Azure PowerShell Az modul telepítése

Az első lépés az Az modul telepítése a platformra. Az Az telepítésekor ajánlott eltávolítani az AzureRM-et. A következő lépésekben bemutatjuk, hogyan futtathatja továbbra is meglévő szkriptjeit, és hogyan biztosíthatja a régi parancsmagnevek kompatibilitását.

Az Azure PowerShell Az modul telepítéséhez hajtsa végre az alábbi lépéseket:

* __AJÁNLOTT__: [Az AzureRM modul eltávolítása](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module).
  Győződjön meg róla, hogy az AzureRM _összes_ telepített verzióját eltávolítja, és nem csak a legutóbbi verziót.
* [Az Az modul telepítése](install-az-ps.md)

## <a name="a-namealiasesenable-azurerm-compatibility-aliases"></a><a name="aliases"/>Az AzureRM kompatibilitási aliasok engedélyezése 

> [!IMPORTANT]
>
> Csak akkor engedélyezze a kompatibilitási módot, ha az AzureRM _összes_ verzióját eltávolította. A kompatibilitási mód a továbbra is elérhető AzureRM parancsmagokkal való engedélyezése váratlan működést okozhat. Hagyja ki ezt a lépést, ha úgy dönt, nem távolítja el az AzureRM-et, de vegye figyelembe, hogy az AzureRM-parancsmagok a régebbi modulokat használják, és nem hívnak meg Az-parancsmagokat.

Miután az AzureRM-et eltávolította, és megbizonyosodott róla, hogy a szkriptek működnek az AzureRM legfrissebb verziójával, a következő lépés az Az modul kompatibilitási módjának engedélyezése. A kompatibilitás a következő paranccsal engedélyezhető:

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

Az aliasok segítségével továbbra is használhatja a régi parancsmagneveket, ha az Az modul telepítve van. Az aliasokat a kiválasztott hatókör felhasználói profiljába lesznek írva. Ha nincs felhasználói profil, a rendszer létrehoz egyet.

> [!WARNING]
>
> Használhat más hatókört (`-Scope`) is a parancsban, ez azonban nem ajánlott. Ezek az aliasok a kiválasztott hatókör felhasználói profiljába lesznek írva, ezért érdemes őket minél korlátozottabb hatókörhöz engedélyezni. Az aliasok rendszerszintű engedélyezése emellett a többi felhasználónak is problémát okozhat, akiknél az AzureRM van telepítve a helyi hatókörükben.

Az alias mód engedélyezése után futtassa újra a szkripteket, és győződjön meg róla, hogy továbbra is a vártnak megfelelően működnek. 

## <a name="change-module-imports-and-cmdlet-names"></a>A modulimportálások és parancsmagnevek módosítása

Általánosságban véve a modulnevek módosultak, így az `AzureRM` és az `Azure` is `Az` lett, és ugyanez igaz a parancsmagokra is.
Az `AzureRM.Compute` modul új neve például `Az.Compute`. A `New-AzureRMVM` `New-AzVM` lett, a `Get-AzureStorageBlob` pedig `Get-AzStorageBlob`.

Van néhány kivétel is ez alól a szabály alól, amelyeket érdemes figyelembe venni. Egyes modulok a parancsmagok utótagjainak módosítása nélkül lettek átnevezve vagy meglévő modulokba egyesítve, csak az `AzureRM` vagy az `Azure` helyett szerepel `Az`. Egyéb esetben a parancsmag teljes utótagja módosult az új modulnévnek megfelelően.

| AzureRM modul | Az modul | Módosult a parancsmag utótagja? |
|----------------|-----------|------------------------|
| AzureRM.Profile | Az.Accounts | Igen |
| AzureRM.Insights | Az.Monitor | Igen |
| AzureRM.DataFactories | Az.DataFactory | Igen |
| AzureRM.DataFactoryV2 | Az.DataFactory | Igen |
| AzureRM.RecoveryServices.Backup | Az.RecoveryServices | Nem |
| AzureRM.RecoveryServices.SiteRecovery | Az.RecoveryServices | Nem |
| AzureRM.Tags | Az.Resources | Nem |
| AzureRM.MachineLearningCompute | Az.MachineLearning | Nem |
| AzureRM.UsageAggregates | Az.Billing | Nem |
| AzureRM.Consumption | Az.Billing | Nem |

## <a name="summary"></a>Összegzés

Ezeknek a lépéseknek a végrehajtásával frissítheti az összes meglévő szkriptet az új modul használatára. Amennyiben az áttelepítést során valamelyik lépéssel kapcsolatban kérdés vagy probléma merült fel, amely megnehezítette a dolgát, várjuk a megjegyzéseit a cikk alatt, hogy fejleszthessük az útmutatót.
