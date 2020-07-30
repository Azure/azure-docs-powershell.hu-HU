---
title: Az Azure PowerShell telepítése Windows rendszeren a PowerShellGet használatával
description: Az Azure PowerShell telepítése a PowerShellGet segítségével
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/15/2018
ms.openlocfilehash: bd9cbdd66c1a9a623461ca8b0291ac1cb61f1e54
ms.sourcegitcommit: c19bf5a96a82a56e2b1fa9ab5e106690f850cedf
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/27/2020
ms.locfileid: "87177475"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a>Az Azure PowerShell telepítése Windows rendszeren a PowerShellGet használatával

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Ez a cikk a PowerShell 5.x verziójához készült Azure PowerShell-modulok telepítésének lépéseit ismerteti Windows-környezetben a PowerShellGet használatával. A PowerShellGet használata és a modulok kezelése az Azure PowerShell előnyben részesített telepítési módja, de ha mégis inkább a Webplatform-telepítővel vagy az MSI-csomaggal szeretné telepíteni, tekintse meg az [egyéb telepítési módszerekkel kapcsolatos](other-install.md) szakaszt.

Az Azure PowerShell e verziója nem támogatja a klasszikus Azure üzemi modellt. A klasszikus üzemi modell támogatásához kövesse az [Azure PowerShell Service Management moduljának telepítésével](/powershell/azure/servicemanagement/install-azure-ps) kapcsolatos szakaszban található utasításokat.

> [!IMPORTANT]
> Az AzureRM modul a macOS és a Linux esetében nem támogatott. Az Azure PowerShell-parancsmagok ezeken a platformokon való használatával kapcsolatban lásd: [Az Az modul telepítése](/powershell/azure/install-az-ps).

## <a name="requirements"></a>Követelmények

Az Azure PowerShell telepítéséhez a PowerShellGet 1.1.2.0-s vagy újabb verziója szükséges. Annak ellenőrzéséhez, hogy ez elérhető-e a rendszerén, futtassa a következő parancsot:

```powershell-interactive
Get-InstalledModule -Name PowerShellGet -AllVersions | Select-Object -Property Name,Version,Path
```

Az alábbihoz hasonló kimenetnek kell megjelennie:

```output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

Ha frissítenie kell a PowerShellGet-telepítést, futtassa a következő parancsot:

```powershell-interactive
Install-Module PowerShellGet -Force
```

Ha nincs telepítve a PowerShellGet, kövesse alább, az operációs rendszerének megfelelő táblázatban található utasításokat.

|Forgatókönyv|Telepítési utasítások|
|---|---|
|Windows 10<br/>Windows Server 2016|Az operációs rendszer részét képező Windows Management Framework (WMF) 5.0 beépített eleme|
|Frissítés a PowerShell 5-ös verziójára| <ol><li>[A WMF legújabb verziójának telepítése](https://www.microsoft.com/download/details.aspx?id=54616)</li><li>Futtassa az alábbi parancsot:<br/>```Install-Module PowerShellGet -Force```</li></ol>|
|A PowerShell 3-as vagy 4-es verziójával rendelkező Windows|<ol><il>[A PackageManagement-modulok beszerzése](https://go.microsoft.com/fwlink/?LinkID=746217)</il><li>Futtassa az alábbi parancsot:<br/>```Install-Module PowerShellGet -Force```</li></ol>|

> [!NOTE]
> A PowerShellGet használatához olyan végrehajtási szabályzatra van szükség, amely lehetővé teszi a szkriptek futtatását. A PowerShell végrehajtási házirendjével kapcsolatos további információk: [A végrehajtási házirendek áttekintése](/powershell/module/microsoft.powershell.core/about/about_execution_policies).
>
> [!IMPORTANT]
> Az ebben a dokumentumban bemutatott AzureRM modul .NET-keretrendszert használ. Ennek következtében nem kompatibilis a PowerShell 6.0-s verziójával, amely a .NET Core-t használja. Ha 6.0-s PowerShell verziót használ, kövesse a [macOS és Linux rendszerekre vonatkozó telepítési utasításokat](/powershell/azure/install-az-ps).

## <a name="install-the-azure-powershell-module"></a>Az Azure PowerShell-modul telepítése

Megemelt jogosultsági szint szükséges a modulok PowerShell-galériából való telepítéséhez. Az Azure PowerShell telepítéséhez futtassa a következő parancsot egy emelt szintű munkamenetben:

```powershell-interactive
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
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

A telepítés folytatásához válassza a `Yes` vagy a `Yes to All` lehetőséget.

Az `AzureRM` modul az Azure PowerShell-parancsmagok összesített modulja. A modul telepítésével letölti az összes elérhető Azure Resource Manager-modult, és használatra elérhetővé teszi a parancsmagjaikat.

## <a name="sign-in"></a>Bejelentkezés

Az Azure PowerShell használatának megkezdéséhez be kell tölteni az `AzureRM` modult az aktuális PowerShell-munkamenetbe az [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) parancsmaggal, majd be kell jelentkezni az Azure-beli hitelesítő adatokkal.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Ezeket a lépéseket minden új PowerShell-munkamenet esetében meg kell ismételni. Az `AzureRM` modul automatikus importálásához be kell állítani egy PowerShell-profilt, amelyről a [profilokat ismertető](/powershell/module/microsoft.powershell.core/about/about_profiles) részben tudhat meg többet.
Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a munkamenetek között, tekintse meg a [felhasználói hitelesítő adatok a PowerShell-munkamenetek között történő megőrzését](context-persistence.md) ismertető részt.

## <a name="update-the-azure-powershell-module"></a>Az Azure PowerShell-modul frissítése

Frissítheti az Azure PowerShell-környezetet az [Update-Module](/powershell/module/powershellget/update-module) futtatásával. Ez a parancs __nem__ távolítja el a korábbi verziókat.

```powershell-interactive
Update-Module -Name AzureRM
```

Ha szeretné a rendszerből eltávolítani az Azure PowerShell régebbi verzióit, tekintse meg az [Azure PowerShell-modul eltávolítását](uninstall-azurerm-ps.md) ismertető szakaszt.

## <a name="use-multiple-versions-of-azure-powershell"></a>Az Azure PowerShell több verziójának használata

Lehetőség van az Azure PowerShell több verziójának telepítésére. Előfordulhat, hogy több verzióra van szüksége, ha helyszíni Azure Stack-erőforrásokat használ, vagy a Windows egy régebbi verzióját használja, amely nem frissíthető a PowerShell 5.0-ra, vagy a klasszikus Azure üzemi modellt használja. Régebbi verzió telepítéséhez a telepítéskor adja meg a `-RequiredVersion` argumentumot.

```powershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

Az Azure PowerShell-modul betöltésekor alapértelmezés szerint a legújabb verzió lesz betöltve. Másik verzió betöltéséhez adja meg a `-RequiredVersion` argumentumot.

```powershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a>Visszajelzés küldése

Ha hibát észlel az Azure PowerShell használata közben, [jelentse be a problémát a GitHubon](https://github.com/Azure/azure-powershell/issues).
A parancssorból a [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) parancsmaggal küldhet visszajelzést.

## <a name="next-steps"></a>Következő lépések

Az Azure PowerShell használatának megkezdéséhez tekintse meg az [Azure PowerShell használatának első lépéseit](get-started-azureps.md) ismertető szakaszt, amelyből többet tudhat meg a modulról és annak funkcióiról.
