---
title: Az Azure PowerShell telepítése Windows rendszeren a PowerShellGet használatával
description: Az Azure PowerShell telepítése a PowerShellGet segítségével
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 970742c91b327a1310ef5097edef40287ebf9f9b
ms.sourcegitcommit: bc88e64c494337821274d6a66c1edad656c119c5
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/20/2018
ms.locfileid: "46304080"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a>Az Azure PowerShell telepítése Windows rendszeren a PowerShellGet használatával

Ez a cikk az Azure PowerShell-modulok PowerShellGet segítségével való telepítésének lépéseit ismerteti Windows-környezetben. A PowerShellGet használata és a modulok kezelése az Azure PowerShell előnyben részesített telepítési módja, de ha mégis inkább a Webplatform-telepítővel vagy az MSI-csomaggal szeretné telepíteni, tekintse meg az [egyéb telepítési módszerekkel kapcsolatos](other-install.md) szakaszt.

Az Azure PowerShell más platformokon való telepítéséhez tekintse meg [az Azure PowerShell macOS és Linux rendszeren való telepítését és konfigurálását](install-azurermps-maclinux.md) ismertető témakört.

Az Azure PowerShell e verziója nem támogatja a klasszikus Azure üzemi modellt. A klasszikus üzemi modell támogatásához kövesse az [Azure PowerShell Service Management moduljának telepítésével](/powershell/azure/servicemanagement/install-azure-ps) kapcsolatos szakaszban található utasításokat.

## <a name="requirements"></a>Követelmények

A 6.0-s verziótól kezdve az Azure PowerShellhez a PowerShell 5.0-s vagy újabb verziója szükséges. Annak ellenőrzéséhez, hogy a PowerShell melyik verziója fut a számítógépén, futtassa a következő parancsot:

```powershell
$PSVersionTable.PSVersion
```

Ha elavult verzióval rendelkezik, tekintse meg a [meglévő Windows PowerShell frissítését](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell) ismertető témakört.

> [!IMPORTANT]
> Az ebben a dokumentumban bemutatott AzureRM modul .NET-keretrendszert használ. Ennek következtében nem kompatibilis a PowerShell 6.0-s verziójával, amely a .NET Core-t használja. Ha 6.0-s PowerShell verziót használ, kövesse a [macOS és Linux rendszerekre vonatkozó telepítési utasításokat](install-azurermps-maclinux.md).

## <a name="install-the-azure-powershell-module"></a>Az Azure PowerShell-modul telepítése

Megemelt jogosultsági szint szükséges a modulok PowerShell-galériából való telepítéséhez. Az Azure PowerShell telepítéséhez futtassa a következő parancsot egy emelt szintű munkamenetben:

```powershell
Install-Module -Name AzureRM
```

> [!NOTE]
> Ha a NuGet 2.8.5.201-esnél régebbi verzióval rendelkezik, a rendszer a legújabb verzió letöltését és telepítését kéri.

Alapértelmezés szerint a PowerShell-galéria nincs konfigurálva a PowerShellGet megbízható adattáraként. A PSGallery első használatakor a következő üzenet jelenik meg:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

A telepítés folytatásához válassza a `Yes` vagy a `Yes to All` lehetőséget.

Az `AzureRM` modul az Azure PowerShell-parancsmagok összesített modulja. A modul telepítésével letölti az összes elérhető Azure Resource Manager-modult, és használatra elérhetővé teszi a parancsmagjaikat.

## <a name="sign-in"></a>Bejelentkezés

Az Azure PowerShell használatának megkezdéséhez be kell tölteni az `AzureRM` modult az aktuális PowerShell-munkamenetbe az [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) parancsmaggal, majd be kell jelentkezni az Azure-beli hitelesítő adatokkal.

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Ezeket a lépéseket minden új PowerShell-munkamenet esetében meg kell ismételni. Az `AzureRM` modul automatikus importálásához be kell állítani egy PowerShell-profilt, amelyről a [profilokat ismertető](/powershell/module/microsoft.powershell.core/about/about_profiles) részben tudhat meg többet.
Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a munkamenetek között, tekintse meg a [Felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között](context-persistence.md) című részt.

## <a name="update-the-azure-powershell-module"></a>Az Azure PowerShell-modul frissítése

Frissítheti az Azure PowerShell-környezetet az [Update-Module](/powershell/module/powershellget/update-module) futtatásával. Ez a parancs __nem__ távolítja el a korábbi verziókat.

```powershell
Update-Module -Name AzureRM
```

Ha szeretné a rendszerből eltávolítani az Azure PowerShell régebbi verzióit, tekintse meg az [Azure PowerShell-modul eltávolítását](uninstall-azurerm-ps.md) ismertető szakaszt.

## <a name="use-multiple-versions-of-azure-powershell"></a>Az Azure PowerShell több verziójának használata

Lehetőség van az Azure PowerShell több verziójának telepítésére. Előfordulhat, hogy több verzióra van szüksége, ha helyszíni Azure Stack-erőforrásokat használ, illetve ha a Windows egy régebbi verzióját vagy a klasszikus Azure üzemi modellt használja. Régebbi verzió telepítéséhez a telepítéskor adja meg a `-RequiredVersion` argumentumot.

```powershell
# Install version 1.2.9 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

Az Azure PowerShell-modul betöltésekor alapértelmezés szerint a legújabb verzió lesz betöltve. Másik verzió betöltéséhez adja meg a `-RequiredVersion` argumentumot.

```powershell
# Load version 1.2.9 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

## <a name="provide-feedback"></a>Visszajelzés küldése

Ha hibát észlel az Azure PowerShell használata közben, [jelentse be a problémát a GitHubon](https://github.com/Azure/azure-powershell/issues).
A parancssorból a [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) parancsmaggal küldhet visszajelzést.

## <a name="next-steps"></a>További lépések

Az Azure PowerShell használatának megkezdéséhez tekintse meg az [Azure PowerShell használatának első lépéseit](get-started-azureps.md) ismertető szakaszt, amelyből többet tudhat meg a modulról és annak funkcióiról.