---
title: Az Azure PowerShell telepítése Windows rendszeren a PowerShellGet használatával
description: Az Azure PowerShell telepítése a PowerShellGet segítségével
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: 2615d1efef05c892552d7ccbea6fcff37f871039
ms.sourcegitcommit: c19bf5a96a82a56e2b1fa9ab5e106690f850cedf
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/27/2020
ms.locfileid: "87177458"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a>Az Azure PowerShell telepítése Windows rendszeren a PowerShellGet használatával

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Ez a cikk a PowerShell 5.x verziójához készült Azure PowerShell-modulok telepítésének lépéseit ismerteti Windows-környezetben a PowerShellGet használatával. A PowerShellGet használata és a modulok kezelése az Azure PowerShell előnyben részesített telepítési módja, de ha mégis inkább a Webplatform-telepítővel vagy az MSI-csomaggal szeretné telepíteni, tekintse meg az [egyéb telepítési módszerekkel kapcsolatos](other-install.md) szakaszt.

Az Azure PowerShell e verziója nem támogatja a klasszikus Azure üzemi modellt. A klasszikus üzemi modell támogatásához kövesse az [Azure PowerShell Service Management moduljának telepítésével](/powershell/azure/servicemanagement/install-azure-ps) kapcsolatos szakaszban található utasításokat.

> [!IMPORTANT]
> Az AzureRM modul a macOS és a Linux esetében nem támogatott. Az Azure PowerShell-parancsmagok ezeken a platformokon való használatával kapcsolatban lásd: [Az Az modul telepítése](/powershell/azure/install-az-ps).

## <a name="requirements"></a>Követelmények

A 6.0-s verziótól kezdve az Azure PowerShellhez a PowerShell 5.0-s vagy újabb verziója szükséges. Annak ellenőrzéséhez, hogy a PowerShell melyik verziója fut a számítógépén, futtassa a következő parancsot:

```powershell-interactive
$PSVersionTable.PSVersion
```

Ha elavult verzióval rendelkezik, tekintse meg a [meglévő Windows PowerShell frissítését](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell) ismertető témakört.

> [!IMPORTANT]
> Az ebben a dokumentumban bemutatott AzureRM modul .NET-keretrendszert használ. Ennek következtében nem kompatibilis a PowerShell 6.0-s verziójával, amely a .NET Core-t használja. Ha 6.0-s PowerShell verziót használ, kövesse a [macOS és Linux rendszerekre vonatkozó telepítési utasításokat](/powershell/azure/install-az-ps).

## <a name="install-the-azure-powershell-module"></a>Az Azure PowerShell-modul telepítése

Megemelt jogosultsági szint szükséges a modulok PowerShell-galériából való telepítéséhez. Az Azure PowerShell telepítéséhez futtassa a következő parancsot egy emelt szintű munkamenetben:

```azurepowershell-interactive
Install-Module -Name AzureRM -AllowClobber
```

> [!NOTE]
> Ha a NuGet 2.8.5.201-esnél régebbi verzióval rendelkezik, a rendszer a legújabb verzió letöltését és telepítését kéri.

Alapértelmezés szerint a PowerShell-galéria nincs konfigurálva a PowerShellGet megbízható adattáraként. A PSGallery első használatakor a következő üzenet jelenik meg:

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

A telepítés folytatásához válassza a `Yes` vagy a `Yes to All` lehetőséget.

Az `AzureRM` modul az Azure PowerShell-parancsmagok összesített modulja. A modul telepítésével letölti az összes elérhető Azure Resource Manager-modult, és használatra elérhetővé teszi a parancsmagjaikat.

## <a name="sign-in"></a>Bejelentkezés

Az Azure PowerShell használatának megkezdéséhez jelentkezzen be Azure-beli hitelesítő adataival.

```azurepowershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
> Ha letiltotta az automatikus modulbetöltést, manuálisan kell importálnia a modult a(z) `Import-Module AzureRM` segítségével. A modul felépítéséből adódóan ez eltarthat néhány másodpercig.

Ezeket a lépéseket minden új PowerShell-munkamenet esetében meg kell ismételni. Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a PowerShell-munkamenetek között, tekintse meg a [Felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között](context-persistence.md) című cikket.

## <a name="update-the-azure-powershell-module"></a>Az Azure PowerShell-modul frissítése

Frissítheti az Azure PowerShell-környezetet az [Update-Module](/powershell/module/powershellget/update-module) futtatásával. Ez a parancs **nem** távolítja el a korábbi verziókat.

```powershell-interactive
Update-Module -Name AzureRM
```

Ha szeretné a rendszerből eltávolítani az Azure PowerShell régebbi verzióit, tekintse meg az [Azure PowerShell-modul eltávolítását](uninstall-azurerm-ps.md) ismertető szakaszt.

## <a name="use-multiple-versions-of-azure-powershell"></a>Az Azure PowerShell több verziójának használata

Lehetőség van az Azure PowerShell több verziójának telepítésére. Ha szeretné ellenőrizni, hogy több Azure PowerShell-verzió is telepítve van-e, használja a következő parancsot:

```azurepowershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions | select Name,Version
```

Ha el szeretné távolítani az Azure PowerShell egyik verzióját, tekintse meg az [Azure PowerShell-modul eltávolítását](uninstall-azurerm-ps.md) ismertető szakaszt.

Előfordulhat, hogy több verzióra van szüksége, ha helyszíni Azure Stack-erőforrásokat használ, illetve ha a Windows egy régebbi verzióját vagy a klasszikus Azure üzemi modellt használja. Régebbi verzió telepítéséhez a telepítéskor adja meg a `-RequiredVersion` argumentumot.

```azurepowershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

Az Azure PowerShell-modul betöltésekor alapértelmezés szerint a legújabb verzió lesz betöltve. Másik verzió betöltéséhez adja meg a `-RequiredVersion` argumentumot.

```azurepowershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a>Visszajelzés küldése

Ha hibát észlel az Azure PowerShell használata közben, [jelentse be a problémát a GitHubon](https://github.com/Azure/azure-powershell/issues). A parancssorból a [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) parancsmaggal küldhet visszajelzést.

## <a name="next-steps"></a>Következő lépések

Az Azure PowerShell használatának megkezdéséhez tekintse meg az [Azure PowerShell használatának első lépéseit](get-started-azureps.md) ismertető szakaszt, amelyből többet tudhat meg a modulról és annak funkcióiról.
