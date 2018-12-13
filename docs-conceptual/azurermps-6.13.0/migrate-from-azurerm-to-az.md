---
title: Azure PowerShell-szkriptek áttelepítése az AzureRM modulból az Az modulba
description: Ismerje meg a szkriptek az AzureRM modulból az új Az modulba való áttelepítésére szolgáló lépéseket és eszközöket.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/07/2018
ms.openlocfilehash: 720387ec1b23f10ddf2b153cf0705b2b6d1b7b82
ms.sourcegitcommit: 087c588169786c005a3c177624fb3ac6c8870125
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/13/2018
ms.locfileid: "53216194"
---
# <a name="migrate-from-azurerm-to-azure-powershell-az"></a>Áttelepítés az AzureRM modulból az Azure PowerShell Az modulba

Az Az modul a funkciók tekintetében paritásban van az AzureRM modullal, de rövidebb és egységesebb parancsmagneveket használ.
Az AzureRM-parancsmagokhoz írt szkriptek nem működnek automatikusan az új modullal. Az áttérés megkönnyítése érdekében az Az olyan eszközöket nyújt, amelyekkel futtathatja az AzureRM-et használó meglévő szkripteket. Az új parancskészletekre való áttérés soha nem egyszerű, ebben a cikkben azonban segítünk megismerkedni az új modulra való átállás alapjaival.

## <a name="ensure-your-existing-scripts-work-with-the-latest-azurerm-release"></a>Gondoskodjon róla, hogy a meglévő szkriptek működjenek az AzureRM legfrissebb kiadásával.

Ez az a legfontosabb lépés! Futtassa a meglévő szkriptjeit, és ellenőrizze, hogy működnek-e az AzureRM _legfrissebb_ kiadásával (__6.13.0__). Ha a szkriptek nem működnek, tekintse át [az AzureRM áttelepítési útmutatóját](migration-guide.6.0.0.md).

## <a name="install-the-azure-powershell-az-module"></a>Az Azure PowerShell Az modul telepítése

Az első lépés az Az modul telepítése a platformra. Az Az telepítéséhez el kell távolítania az AzureRM-et.
A következő lépésekben bemutatjuk, hogyan futtathatja továbbra is meglévő szkriptjeit, és hogyan biztosíthatja a régi parancsmagnevek kompatibilitását.

Az Azure PowerShell Az modul telepítéséhez hajtsa végre az alábbi lépéseket:

* [Az AzureRM modul eltávolítása](uninstall-azurerm-ps.md). Győződjön meg róla, hogy az AzureRM _összes_ telepített verzióját eltávolítja, és nem csak a legutóbbi verziót.
* [Az Az modul telepítése](install-az-ps.md)

## <a name="a-namealiasesenable-azurerm-alias-mode"></a><a name="aliases"/>Az AzureRM alias módjának engedélyezése

Miután az AzureRM-et eltávolította, és megbizonyosodott róla, hogy a szkriptek működnek az AzureRM legfrissebb verziójával, ideje engedélyeznie az Az modul kompatibilitási módját. A kompatibilitás a következő paranccsal engedélyezhető:

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

Az aliasok segítségével továbbra is használhatja a régi parancsmagneveket, ha az `Az` modul van telepítve. Az aliasokat a kiválasztott hatókör felhasználói profiljába lesznek írva. Ha nincs felhasználói profil, a rendszer létrehoz egyet.

> [!WARNING]
>
> Használhat más hatókört (`-Scope`) is a parancsban, ez azonban nem ajánlott! Ezek az aliasok a kiválasztott hatókör felhasználói profiljába lesznek írva, ezért érdemes őket minél korlátozottabb hatókörhöz engedélyezni. Az aliasok rendszerszintű engedélyezése emellett a többi felhasználónak is problémát okozhat, akiknél az `AzureRM` van telepítve a helyi hatókörükben.

Az alias mód engedélyezése után futtassa újra a szkripteket, és győződjön meg róla, hogy továbbra is a vártnak megfelelően működnek. 

## <a name="change-module-imports-and-cmdlet-names"></a>A modulimportálások és parancsmagnevek módosítása

Általánosságban véve a modulnevek módosultak, így az `AzureRM` és az `Azure` is `Az` lett, és ugyanez igaz a parancsmagokra is.
Az `AzureRM.Compute` modul új neve például `Az.Compute`. A `New-AzureRmVM` `New-AzVM` lett, a `Get-AzureStorageBlob` pedig `Get-AzStorageBlob`.

Van néhány kivétel is ez alól a szabály alól, amelyeket érdemes figyelembe venni, mielőtt bármit átnevezne:

| AzureRM modul | Az modul |
|----------------|-----------|
| AzureRM.DataFactories | Az.DataFactory |
| AzureRM.DataFactoryV2 | Az.DataFactory |
| AzureRM.RecoveryServices.Backup | Az.RecoveryServices |
| AzureRM.RecoveryServices.SiteRecovery | Az.RecoveryServices |

## <a name="summary"></a>Összegzés

Ezeknek a lépéseknek a végrehajtásával frissítheti az összes meglévő szkriptet az új modul használatára. Amennyiben az áttelepítést során valamelyik lépéssel kapcsolatban kérdés vagy probléma merült fel, amely megnehezítette a dolgát, várjuk a megjegyzéseit a cikk alatt, hogy fejleszthessük az útmutatót.
