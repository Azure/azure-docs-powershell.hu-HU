---
title: Az Azure PowerShell telepítésének egyéb módjai | Microsoft Docs
description: Az Azure PowerShell telepítése az MSI-csomag vagy a Webplatform-telepítő használatával.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/06/2017
ms.openlocfilehash: 3f8963c98b26f971c1259dc89d5da1f35ce3015a
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/14/2020
ms.locfileid: "83386697"
---
# <a name="other-installation-methods"></a>Egyéb telepítési módszerek

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Az Azure PowerShell többféle módszerrel telepíthető. Az előnyben részesített módszer a PowerShellGet használata a PowerShell-galériával. Az Azure PowerShell a Windows rendszeren a Webplatform-telepítő (WebPI) vagy a GitHubról elérhető MSI-fájl használatával telepíthető.

## <a name="install-on-windows-using-the-web-platform-installer"></a>Telepítés Windows rendszeren a Webplatform-telepítővel

A legújabb Azure PowerShell ugyanúgy telepíthető a WebPI-ről, ahogy a korábbi verziók.
Töltse le az [Azure PowerShell WebPI csomagot](https://aka.ms/webpi-azps), és indítsa el a telepítést.

> [!NOTE]
> Ha korábban már telepített Azure-modulokat a PowerShell-galériából, a telepítő automatikusan eltávolítja őket. Ez egyszerűbbé teszi a környezetet, mivel így biztosítható, hogy csak egy Azure PowerShell-verzió lesz telepítve. Léteznek azonban olyan forgatókönyvek, amikor több telepített verzióra lehet szüksége egy időben.
>
> A PowerShell-galéria moduljai a következő helyen települnek: `$env:ProgramFiles\WindowsPowerShell\Modules`. A WebPI telepítője ezzel szemben a következő helyen telepíti az Azure-modulokat: `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.
>
> Ha hiba merül fel a telepítés során, törölje manuálisan az Azure\* mappákat a `$env:ProgramFiles\WindowsPowerShell\Modules` mappából, és próbálkozzon újra a telepítéssel.

A telepítés befejeztével a `$env:PSModulePath` beállításnak tartalmaznia kell az Azure PowerShell-parancsmagokat tartalmazó könyvtárakat. A következő paranccsal ellenőrizheti, hogy az Azure PowerShell megfelelően van-e telepítve.

```powershell-interactive
# To make sure the Azure PowerShell module is available after you install
Get-InstalledModule -Name AzureRM -AllVersions | Select-Object Name, Version, Path
```

> [!NOTE]
> Létezik egy ismert hiba, amely a WebPI telepítésekor léphet fel. Ha a számítógépet a rendszerfrissítések és egyéb telepítések miatt újra kell indítani, előfordulhat, hogy az `$env:PSModulePath` frissítései nem tartalmazzák az Azure PowerShell telepítési útvonalát.

A parancsmagok telepítés utáni betöltése vagy végrehajtása során a következő hibaüzenet jelenhet meg:

```output
PS C:\> Login-AzureRmAccount
Login-AzureRmAccount : The term 'Login-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Login-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Login-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

Ez a hiba a gép újraindításával vagy a modul teljes útvonallal való importálásával javítható. Például:

```powershell-interactive
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-on-windows-using-the-msi-package"></a>Telepítés Windows rendszeren az MSI-csomaggal

Az Azure PowerShell telepíthető a [GitHubról](https://github.com/Azure/azure-powershell/releases/latest) elérhető MSI-fájllal is. Ha az Azure-modulok korábbi verziói már telepítve vannak, a telepítő automatikusan eltávolítja őket. Az MSI-csomag a(z) `$env:ProgramFiles\WindowsPowerShell\Modules` helyre telepíti a modulokat, azonban nem hoz létre verzióspecifikus mappákat.

