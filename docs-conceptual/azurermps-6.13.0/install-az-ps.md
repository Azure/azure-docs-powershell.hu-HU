---
title: Az Azure PowerShell Az telepítése a PowerShellGet segítségével
description: Az Azure PowerShell telepítése a PowerShellGet segítségével Windows, macOS és Linux rendszeren.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: 32e96c6459c9db0c4b9eda0cc170c85ba99a22ca
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/22/2018
ms.locfileid: "52259794"
---
# <a name="install-the-azure-powershell-az-module"></a>Az Azure PowerShell Az modul telepítése

Ez a cikk az Azure PowerShell-modulok a PowerShellGet használatával való telepítését mutatja be. Az útmutatás Windows, macOS és Linux platformon használható. Az Az előzetes kiadásában más telepítési módszerek támogatottak. 

## <a name="requirements"></a>Követelmények

Az Azure PowerShell a Windows alatt a PowerShell 5.x, más platformon a PowerShell 6.x verziójával működik. Annak ellenőrzéséhez, hogy a PowerShell melyik verziója fut a számítógépén, futtassa a következő parancsot:

```powershell-interactive
$PSVersionTable.PSVersion
```

Ha elavult verzióval rendelkezik, vagy nincs telepítve a PowerShell, tekintse át [a PowerShell különféle verzióinak telepítését](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6) ismertető témakört. A platformokra vonatkozó telepítési információk azon az oldalon keresztül érhetők el.

## <a name="install-the-azure-powershell-module"></a>Az Azure PowerShell-modul telepítése

> [!IMPORTANT]
>
> Az `AzureRM` és az `Az` modul nem lehet egyszerre telepítve ugyanazon a rendszeren. Az `Az` modul telepítéséhez az `AzureRM` modult el kell távolítani. Az erre vonatkozó utasításokért lásd: [Az Azure PowerShell-modul (AzureRM) eltávolítása](uninstall-azurerm-ps.md).

A modulok globális hatókörben való telepítéséhez megemelt jogosultsági szint szükséges a PowerShell-galériából való telepítés esetén. Az Azure PowerShell telepítéséhez futtassa a következő parancsot egy emelt szintű munkamenetben („Futtatás rendszergazdaként” a Windows, vagy felügyelői jogosultságok a macOS vagy a Linux alatt):

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

Ha nem rendelkezik rendszergazdai jogosultsággal, a `-Scope` argumentum hozzáadásával végezhet telepítést az aktuális felhasználó számára.

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

Alapértelmezés szerint a PowerShell-galéria nincs konfigurálva a PowerShellGet megbízható adattáraként. A PSGallery első használatakor a következő üzenet jelenik meg:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

A telepítés folytatásához válassza a `Yes` vagy a `Yes to All` lehetőséget.

Az `Az` modul az Azure PowerShell-parancsmagok összesített modulja. A modul telepítésével letölti az összes elérhető Azure Resource Manager-modult, és használatra elérhetővé teszi a parancsmagjaikat.

## <a name="sign-in"></a>Bejelentkezés

Az Azure PowerShell használatának megkezdéséhez jelentkezzen be Azure-beli hitelesítő adataival.

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> Ha letiltotta az automatikus modulbetöltést, manuálisan kell importálnia a modult a(z) `Import-Module Az` segítségével. A modul felépítéséből adódóan ez eltarthat néhány másodpercig.

Ezeket a lépéseket minden új PowerShell-munkamenet esetében meg kell ismételni. Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a PowerShell-munkamenetek között, tekintse meg a [Felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között](context-persistence.md) című cikket.

## <a name="update-the-azure-powershell-module"></a>Az Azure PowerShell-modul frissítése

Frissítheti az Azure PowerShell-környezetet az [Update-Module](/powershell/module/powershellget/update-module) futtatásával. Ez a parancs __nem__ távolítja el a korábbi verziókat.

```powershell-interactive
Update-Module -Name Az
```

Ha szeretné a rendszerből eltávolítani az Azure PowerShell régebbi verzióit, tekintse meg az [Azure PowerShell-modul eltávolítását](uninstall-azurerm-ps.md) ismertető szakaszt.

## <a name="use-multiple-versions-of-azure-powershell"></a>Az Azure PowerShell több verziójának használata

Lehetőség van az Azure PowerShell több verziójának telepítésére. Ha szeretné ellenőrizni, hogy több Azure PowerShell-verzió is telepítve van-e, használja a következő parancsot:

```powershell-interactive
Get-Module -Name Az -List | select Name,Version
```

Ha el szeretné távolítani az Azure PowerShell egyik verzióját, tekintse meg az [Azure PowerShell-modul eltávolítását](uninstall-azurerm-ps.md) ismertető szakaszt.

Az `Az` modul adott verziójának betöltéséhez használja a `-RequiredVersion` argumentumot az `Install-Module` vagy az `Import-Module` parancsban:

```powershell-interactive
Install-Module -Name Az -RequiredVersion 0.4.0
Import-Module -Name Az -RequiredVersion 0.4.0
```

Ha a modul több verziója is telepítve van, alapértelmezés szerint a legújabb verzió töltődik be.

## <a name="provide-feedback"></a>Visszajelzés küldése

Ha hibát észlel az Azure PowerShell használata közben, [jelentse be a problémát a GitHubon](https://github.com/Azure/azure-powershell/issues).
A parancssorból a [Send-Feedback](/powershell/module/az.profile/send-feedback) parancsmaggal küldhet visszajelzést.

## <a name="next-steps"></a>További lépések

Az Azure PowerShell használatának megkezdéséhez tekintse meg az [Azure PowerShell használatának első lépéseit](get-started-azureps.md) ismertető szakaszt, amelyből többet tudhat meg a modulról és annak funkcióiról.
