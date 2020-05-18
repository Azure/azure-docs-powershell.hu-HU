---
title: Azure PowerShell-szkriptek áttelepítése az AzureRM modulból az Az modulba
description: Ismerje meg a szkriptek az AzureRM modulból az új Az modulba való áttelepítésére szolgáló lépéseket és eszközöket.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/10/2019
ms.openlocfilehash: 02b39653ebb4aa0f74d2340a7be7b35e08d5e44d
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/05/2020
ms.locfileid: "81740099"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a>Az Azure PowerShell migrálása az AzureRM modulból az Az modulba

Az Az modul a funkciók tekintetében paritásban van az AzureRM modullal, de rövidebb és egységesebb parancsmagneveket használ.
Az AzureRM-parancsmagokhoz írt szkriptek nem működnek automatikusan az új modullal. Az áttérés megkönnyítése érdekében az Az olyan eszközöket nyújt, amelyekkel futtathatja az AzureRM-et használó meglévő szkripteket. Az új parancskészletekre való áttérés soha nem egyszerű, ebben a cikkben azonban segítünk megismerkedni az új modulra való átállás alapjaival.

Az AzureRM és az Az közötti kompatibilitástörő változások teljes listáját [az AzureRM és az Az közötti változások teljes listájában](migrate-az-1.0.0.md) találja.

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a>Annak ellenőrzése, hogy a meglévő szkriptek működnek-e az AzureRM legújabb kiadásával

A migrálási lépések előtt ellenőrizze, hogy az AzureRM mely verziói vannak telepítve a rendszeren. Ezzel biztosíthatja, hogy a szkriptek már a legújabb kiadáson fussanak, és megtudhatja, hogy az AzureRM mely verzióit kell eltávolítania.

Az AzureRM telepített verziója/verziói megtekintéséhez futtassa a következő parancsot:

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

Az AzureRM __legújabb__ elérhető kiadása a __6.13.1-es__. Ha nincs telepítve ez a verzió, a meglévő szkripteknek további módosításra lehet szükségük ahhoz, hogy az itt és a [kompatibilitástörő változások listájában](migrate-az-1.0.0.md) leírtakon kívül használni lehessen őket az Az modullal.

Ha a szkriptek nem működnek az AzureRM 6.13.1-es verziójával, frissítse őket az [AzureRM 5.x és 6.x migrálási útmutatója](/powershell/azure/azurerm/migration-guide.6.0.0) szerint.
Ha az AzureRM modul korábbi verzióját használja, mindegyik fő verzióhoz elérhető migrálási útmutató.

## <a name="uninstall-azurerm"></a>Az AzureRM eltávolítása

Nem garantált, hogy az Az modul kompatibilis lesz a meglévő, telepített AzureRM-mel a Windows PowerShell 5.1-ben. Az Az modul telepítése előtt [távolítsa el az AzureRM-et](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module).

> [!IMPORTANT]
>
> Ha nem áll készen arra, hogy eltávolítsa az AzureRM modult a rendszerből, a [PowerShell Core](/powershell/scripting/install/installing-powershell-core-on-windows) 6.x vagy újabb verziójához is telepítheti az Az modult. A PowerShell Core és a Windows PowerShell 5.1 különböző modultárat használ, így nem lesznek ütközések. Ettől még [engedélyezheti az aliasokat](#enable-azurerm-compatibility-aliases) a PowerShell Core-ban.

## <a name="install-the-azure-powershell-az-module"></a>Az Azure PowerShell Az modul telepítése

Az első lépés az Az modul telepítése a platformra. Az Az telepítésekor ajánlott eltávolítani az AzureRM-et. A következő lépésekben bemutatjuk, hogyan futtathatja továbbra is meglévő szkriptjeit, és hogyan biztosíthatja a régi parancsmagnevek kompatibilitását.

Az Azure PowerShell Az moduljának telepítéséhez kövesse az [Az modul telepítése](install-az-ps.md) című szakaszban leírt utasításokat.

> [!NOTE]
> Ekkor érdemes lehet futtatni az Az modulban található [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) parancsmagot, hogy meggyőződjön arról, hogy az AzureRM összes verziója el lett távolítva, és nem fog ütközéseket okozni.

## <a name="enable-azurerm-compatibility-aliases"></a>Az AzureRM kompatibilitási aliasok engedélyezése

Miután az AzureRM-et eltávolította, és megbizonyosodott róla, hogy a szkriptek működnek az AzureRM legfrissebb verziójával, a következő lépés az Az modul kompatibilitási módjának engedélyezése. A kompatibilitás a következő paranccsal engedélyezhető:

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

Az aliasok segítségével továbbra is használhatja a régi parancsmagneveket, ha az Az modul telepítve van. Az aliasok a kiválasztott hatókör profiljába lesznek írva. Ha nincs profil, a rendszer létrehoz egyet.
A `CurrentUser` értéknél nagyobb `-Scope` használatakor megfelelő engedélyek szükségesek a megfelelő profilfájl létrehozásához vagy frissítéséhez.

> [!IMPORTANT]
> __Csak__ a parancsmagok neve rendelkezik aliassal, a modulok neve nem. Ha `#Requires` vagy `Import-Module` utasítást, `.psd1` függőségi listáit vagy teljes parancsmagneveket használ, mindenképpen ekkor migrálja őket. Ehhez kövesse a [kompatibilitástörő változások listájában](migrate-az-1.0.0.md) ismertetett, a modulnevekre vonatkozó folyamatokat.

> [!WARNING]
>
> Használhat más hatókört (`-Scope`) is a parancsban, ez azonban nem ajánlott. Ezek az aliasok a kiválasztott hatókör felhasználói profiljába lesznek írva, ezért érdemes őket minél korlátozottabb hatókörhöz engedélyezni. Az aliasok rendszerszintű engedélyezése emellett a többi felhasználónak is problémát okozhat, akiknél az AzureRM van telepítve a helyi hatókörükben.

Az alias mód engedélyezése után futtassa újra a szkripteket, és győződjön meg róla, hogy továbbra is a vártnak megfelelően működnek.
Néhány paraméter neve módosult, hozzá lett adva vagy szükségessé vált az Az modulhoz. Előfordulhat, hogy a parancsmagok kimeneti típusa is megváltozott. A változások részletes leírása a [kompatibilitástörő változások listájában](migrate-az-1.0.0.md) található.

## <a name="update-cmdlets-modules-and-parameters"></a>Parancsmagok, modulok és paraméterek frissítése

Ha frissítette a szkripteket, és aliasokkal futtatja őket, akkor szánjon időt arra, hogy frissítse őket az új parancsmagok használatához és a többi módosítás, például az új funkciók előnyeinek kihasználásához. A legtöbb szkript esetében csak a parancsmagneveket kell frissíteni, [az Az új parancsmag-elnevezési sémája szerint](migrate-az-1.0.0.md#cmdlet-noun-prefix-changes). Előfordulhat, hogy néhány további módosítást is el kell végeznie ahhoz, hogy a szkriptek működjenek, attól függően, hogy mire valók, és az Azure PowerShell mely funkcióit használják.

Például ha a [Blob Storage-parancsmagokat](migrate-az-1.0.0.md#azstorage-previously-azurestorage-and-azurermstorage) teljesen átdolgozták, hogy egy új, aszinkron modellt használjanak, az ezeket használó szkriptek frissítése több munkával fog járni, mint azoké a szkripteké, amelyeknél csak a parancsmagnevek terén történt lényeges változás.

Ha eddig csak kisebb, egyszerű módosításokat kellett végrehajtania a szkripteken, vagy ha azok az aliasok engedélyezésekor további módosítások nélkül is működnek, akkor is tekintse át az [Az 1.0.0 kompatibilitástörő változásainak teljes listáját](migrate-az-1.0.0.md), hogy meggyőződjön arról, hogy nem támaszkodik az aliasok „átlátható” viselkedésére, ami a parancsmagnevek módosítása és az aliasok letiltása után megszűnhet.

## <a name="disable-aliases"></a>Aliasok letiltása

Ha befejezte a migrálást, és már nem támaszkodik az aliasok viselkedésére, javasoljuk, hogy tiltsa le az aliasokat. Ezt a [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias) parancsmaggal teheti meg.

> [!IMPORTANT]
> A parancsmag futtatásakor __győződjön meg arról,__ hogy minden olyan `-Scope`-hoz meghívja, amelyhez a `Enable-AzureRmAlias` meg lett hívva, különben maradhatnak olyan szkriptek a rendszerben, amelyek az aliasok viselkedésére támaszkodnak.
