---
title: Az Azure PowerShell telepítése macOS vagy Linux rendszeren
description: Az Azure PowerShell telepítése macOS vagy Linux rendszeren.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 47611281f67d68c9fc2686e0c6156b060a225158
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/29/2018
ms.locfileid: "52586683"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a>Az Azure PowerShell telepítése macOS vagy Linux rendszeren

Nem Windows rendszerű platformokon az Azure PowerShell futtatható a PowerShell Core 6-os verziójában. A PowerShell e verziója bármely, .NET Core-t támogató platformon történő használatra készült. Az ilyen platformokon történő használathoz elérhető az Azure PowerShell egy speciális .NET Core-verziója.

> [!NOTE]
> Jelenleg a PowerShell Core 6-os verziója és a .NET Core-hoz készült Azure PowerShell csak bétaverzióban érhető el.
> A termékek korlátozott támogatással rendelkeznek. Ha problémákba ütközik vagy hibát észlel, jelentse be a problémát a GitHubon.
>
> * [A PowerShell Core 6-os verziójának problémái](https://github.com/PowerShell/PowerShell/issues)
> * [Az Azure PowerShell problémái](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a>A PowerShell Core telepítése

A PowerShell Core telepítési útmutatása eltér a macOS- és a Linux-disztribúciók esetében.
Részletes útmutatásokat a következő cikkekben talál:

* [A PowerShell Core telepítése macOS rendszeren](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [A PowerShell Core telepítése Linux rendszeren](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a>A .NET Core-hoz készült Azure PowerShell telepítése

A PowerShell Core tartalmazza az előre telepített PowerShellGet modult. Modulok a PowerShellben történő telepítéséhez megemelt jogosultsági szint szükséges, ezért a munkamenetet superuser felhasználóként kell elindítani:

```bash
sudo pwsh
```

Az Azure PowerShell telepítéséhez futtassa az alábbi parancsot:

```powershell-interactive
Install-Module AzureRM.NetCore
```

> [!IMPORTANT]
> A más cikkekben ismertetett `AzureRM` modul nem a .NET Core-hoz készült, és nem fog működni a PowerShell Core-ral. Az `AzureRM` és az `AzureRM.NetCore` is ugyanazokat a parancsmagneveket használja, csak az összesített modul neve tér el, valamint az, hogy a .NET melyik verzióján lettek létrehozva.

Alapértelmezés szerint a PowerShell-galéria nincs konfigurálva a PowerShellGet megbízható adattáraként. A PSGallery első használatakor a következő üzenet jelenik meg:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

A telepítés folytatásához válassza a `Yes` vagy a `Yes to All` lehetőséget.

## <a name="sign-in"></a>Bejelentkezés

Az Azure PowerShell használatának megkezdéséhez be kell tölteni az `AzureRM.Netcore` modult a PowerShell-munkamenetbe az [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) parancsmaggal, majd be kell jelentkezni az Azure-beli hitelesítő adatokkal. A modul importálásához __nincs__ szükség megemelt jogosultsági szintre.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM.Netcore
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Ezeket a lépéseket minden új PowerShell-munkamenet esetében meg kell ismételni. Az `AzureRM` modul automatikus importálásához be kell állítani egy PowerShell-profilt, amelyről a [profilokat ismertető](/powershell/module/microsoft.powershell.core/about/about_profiles) részben tudhat meg többet.
macOS és Linux rendszeren a `$Profile` környezeti változó segítségével használja a profilját. Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a munkamenetek között, tekintse meg a [felhasználói hitelesítő adatok a PowerShell-munkamenetek között történő megőrzését](context-persistence.md) ismertető részt.

## <a name="available-cmdlets"></a>Elérhető parancsmagok

A .NET Core-hoz elérhető Azure PowerShell-modulok még fejlesztés alatt állnak. Ezek a modulok nem tartalmazzák a modulok Windows verziójához elérhető teljes parancsmagkészletét. Az AzureRM.Netcore-modulokban az alábbi funkciók érhetők el:

* Fiókkezelés
  * Bejelentkezés Microsoft-fiókkal, vállalati fiókkal vagy szolgáltatásnévvel a Microsoft Azure Active Directoryn keresztül
  * Hitelesítő adatokat mentése lemezre a Save-AzureRmContext parancsmaggal és a mentett hitelesítő adatok betöltése az Import-AzureRmContext parancsmaggal
* Környezet
  * Különböző nem beépített Microsoft Azure-környezetek beszerzése
  * Testre szabott környezetek (például az Azure Stack- vagy a Windows Azure Pack-környezetek) hozzáadása/beállítása/eltávolítása
* Felügyeletisík-parancsmagok az Azure-szolgáltatásokhoz a Resource Manager és a Service Manager felületeinek használatával.
  * Virtuális gép
  * App Service (webhelyek)
  * SQL Database
  * Storage
  * Network (Hálózat)

## <a name="next-steps"></a>További lépések

Az Azure PowerShell használatával kapcsolatos további információkért tekintse meg az [Ismerkedés az Azure PowerShell szolgáltatással](get-started-azureps.md) című cikket.
