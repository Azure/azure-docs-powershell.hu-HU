---
title: Az Azure PowerShell telepítése a PowerShellGet segítségével
description: Az Azure PowerShell telepítése a PowerShellGet segítségével
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 269119333b2197a15ed7bb50e3e5d90588456174
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/23/2019
ms.locfileid: "63068880"
---
# <a name="install-the-azure-powershell-module"></a>Az Azure PowerShell-modul telepítése

Ez a cikk az Azure PowerShell-modulok a PowerShellGet használatával való telepítését mutatja be. Az útmutatás Windows, macOS és Linux platformon használható. Az Az modulhoz jelenleg nem támogatottak más telepítési módszerek.

## <a name="requirements"></a>Követelmények

Az Azure PowerShell Windows rendszeren a PowerShell 5.1 vagy újabb, más platformon a PowerShell 6-os verziójával működik.
A PowerShell verziójának megtekintéséhez futtassa az alábbi parancsot:

```powershell-interactive
$PSVersionTable.PSVersion
```

Ha elavult verzióval rendelkezik, vagy nincs telepítve a PowerShell, tekintse át [a PowerShell különféle verzióinak telepítését](/powershell/scripting/setup/installing-powershell) ismertető témakört. A platformokra vonatkozó telepítési információk azon az oldalon keresztül érhetők el.

Ha Windows rendszeren futtatja a PowerShell 5-ös verzióját, akkor a .NET-keretrendszer 4.7.2-es verziójának is telepítve kell lennie. A .NET-keretrendszer új verziójának frissítésével vagy telepítésével kapcsolatos utasításokat a [.NET-keretrendszer telepítési útmutatójában](/dotnet/framework/install) találja.

## <a name="install-the-azure-powershell-module"></a>Az Azure PowerShell-modul telepítése

> [!IMPORTANT]
>
> Az AzureRM és az Az modul egyszerre is telepítve lehet ugyanazon a rendszeren. Ha mindkettő telepítve van, __ne engedélyezze az aliasokat__.
> Az aliasok engedélyezése ütközéseket okozhat az AzureRM parancsmagok és az Az-parancsaliasok között, ami nem várt működéshez vezethet.
> Az Az modul telepítése előtt ajánlott eltávolítani az AzureRM-et. Az AzureRM-et bármikor eltávolíthatja, illetve bármikor engedélyezheti az aliasokat. Az AzureRM-parancsaliasokról [az AzureRM modulból az Az modulba való áttelepítést](migrate-from-azurerm-to-az.md) ismertető szakaszban olvashat.
> Az eltávolításra vonatkozó útmutatásért lásd a következő cikket: [Az AzureRM modul eltávolítása](uninstall-az-ps.md#uninstall-the-azurerm-module). 

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

Az Az modul az Azure PowerShell-parancsmagok összesített modulja. A modul telepítésével letölti az összes elérhető Azure Resource Manager-modult, és használatra elérhetővé teszi a parancsmagjaikat.

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

Frissítheti az Azure PowerShell-környezetet az [Update-Module](/powershell/module/powershellget/update-module) futtatásával. Ez a parancs __nem__ távolítja el a régebbi verziókat.

```powershell-interactive
Update-Module -Name Az
```

Az Azure PowerShell régebbi verzióinak eltávolításáról [Az Azure PowerShell-modul eltávolítása](uninstall-az-ps.md) című szakaszban olvashat.

## <a name="use-multiple-versions-of-azure-powershell"></a>Az Azure PowerShell több verziójának használata

Lehetőség van az Azure PowerShell több verziójának telepítésére. Ha szeretné ellenőrizni, hogy több Azure PowerShell-verzió is telepítve van-e, használja a következő parancsot:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

Ha el szeretné távolítani az Azure PowerShell egyik verzióját, tekintse meg az [Azure PowerShell-modul eltávolítását](uninstall-az-ps.md) ismertető szakaszt.

Az `Az` modul adott verziójának telepítéséhez vagy betöltéséhez használja a `-RequiredVersion` argumentumot:

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

Ha a modul több verziója is telepítve van, alapértelmezés szerint a modul automatikus betöltésével és az `Import-Module` használatával töltse be a legújabb verziót.

## <a name="provide-feedback"></a>Visszajelzés küldése

Ha hibát észlel az Azure PowerShellben, [jelentse be a problémát a GitHubon](https://github.com/Azure/azure-powershell/issues).
A parancssorból a [Send-Feedback](/powershell/module/az.accounts/send-feedback) parancsmaggal küldhet visszajelzést.

## <a name="next-steps"></a>További lépések

Az Azure PowerShell-modulokról és azok funkcióiról az [Azure PowerShell használatának első lépéseit](get-started-azureps.md) ismertető szakaszban talál további információt.
Ha ismeri az Azure PowerShellt, és az AzureRM-ből végez migrálást, tekintse meg [az AzureRM modulból az Az modulba való áttelepítést](migrate-from-azurerm-to-az.md) ismertető szakaszt.
