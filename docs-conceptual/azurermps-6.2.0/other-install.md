---
title: Az Azure PowerShell telepítésének egyéb módjai
description: Az Azure PowerShell telepítése az MSI-csomag vagy a Webplatform-telepítő használatával.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 0919583d9cb05a75fae3b812eed84109be8b28aa
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323322"
---
# <a name="other-installation-methods"></a>Egyéb telepítési módszerek

Ez a cikk az Azure PowerShell MSI-vel vagy Webplatform-telepítővel (WebPI) való telepítését ismerteti. Az Azure PowerShell futtatható egy Docker-tárolóból is. Csak akkor alkalmazza ezeket a telepítési módszereket, ha a rendszer számára szükséges. Az Azure PowerShell telepítésének szokványos módszere a PowerShellGet segítségével való telepítés. Útmutatás az Azure PowerShell PowerShellGet segítségével való telepítéséhez: [Az Azure PowerShell telepítése a PowerShellGet segítségével](install-azurerm-ps.md).

Ha Linux- vagy macOS-környezetben végzi a telepítést, tekintse meg [Az Azure PowerShell telepítése macOS vagy Linux rendszeren](install-azurermps-maclinux.md) szakaszt.

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a>Telepítés vagy frissítés Windows rendszeren a Webplatform-telepítővel

A legújabb Azure PowerShell ugyanúgy telepíthető a WebPI-ről, ahogy a korábbi verziók.
Töltse le az [Azure PowerShell WebPI csomagot](http://aka.ms/webpi-azps), és indítsa el a telepítést.

> [!NOTE]
> Ha korábban már telepített Azure-modulokat a PowerShell-galériából, a telepítő automatikusan eltávolítja őket. Ez egyszerűbbé teszi a környezetet, mivel így biztosítható, hogy csak egy Azure PowerShell-verzió lesz telepítve. Léteznek azonban olyan forgatókönyvek, amikor több telepített verzióra lehet szüksége egy időben.
>
> A PowerShell-galéria moduljai a következő helyen települnek: `$env:ProgramFiles\WindowsPowerShell\Modules`. A WebPI telepítője ezzel szemben a következő helyen telepíti az Azure-modulokat: `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.
>
> Ha hiba merül fel a telepítés során, törölje manuálisan az `Azure*` mappákat a `$env:ProgramFiles\WindowsPowerShell\Modules` mappából, és próbálkozzon újra a telepítéssel.

A telepítés befejeztével a `$env:PSModulePath` beállításnak tartalmaznia kell az Azure PowerShell-parancsmagokat tartalmazó könyvtárakat. A következő paranccsal ellenőrizheti, hogy az Azure PowerShell megfelelően van-e telepítve:

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> Létezik egy ismert hiba, amely a WebPI telepítésekor léphet fel. Ha a számítógépet a rendszerfrissítések és egyéb telepítések miatt újra kell indítani, előfordulhat, hogy az `$env:PSModulePath` frissítései nem tartalmazzák az Azure PowerShell telepítési útvonalát.

A parancsmagok telepítés utáni betöltése vagy végrehajtása során a következő hibaüzenet jelenhet meg:

```
PS C:\> Connect-AzureRmAccount
Connect-AzureRmAccount : The term 'Connect-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Connect-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Connect-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

Ez a hiba a gép újraindításával vagy a modul teljes útvonallal való importálásával javítható.

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Telepítés vagy frissítés Windows rendszeren az MSI-csomaggal

Az Azure PowerShell telepíthető a [GitHubról](https://aka.ms/azps-release) elérhető MSI-fájllal is. Ha az Azure-modulok korábbi verziói már telepítve vannak, a telepítő automatikusan eltávolítja őket. Az MSI-csomag a(z) `$env:ProgramFiles\WindowsPowerShell\Modules` helyre telepíti a modulokat, azonban nem hoz létre verzióspecifikus mappákat.

## <a name="run-in-a-docker-container"></a>Futtatás Docker-tárolóban

Elérhetők az Azure PowerShellhez előre konfigurált Docker-rendszerképek. Kétféle tároló érhető el: azok, amelyek a hagyományos PowerShellt futtatják Windows rendszeren, és egy olyan, amely a PowerShell Core-t futtatja Windows vagy Linux rendszeren.

| Környezet | Docker-rendszerkép |
|-------------|--------------|
| PowerShell Windows rendszeren | [azuresdk/azure-powershell](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| PowerShell Core Windows rendszeren | [azuresdk/azure-powershell-core:nanoserver](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| PowerShell Core Linux rendszeren | [azuresdk/azure-powershell-core:latest](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

Ezen tárolók futtatásához a `docker run -it $ImageName` parancs segítségével kap egy interaktív terminált. A PowerShell Core Linux-tárolón történő futtatásához például használja a következőt:

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> Ha Windows-tárolót szeretne futtatni a Dockerben, a gazdagép operációs rendszerének Windowsnak kell lennie, és a Dockert úgy kell beállítani, hogy Windows-tárolókat futtasson. További információk a Windows- és Linux-környezet közötti váltáshoz a Dockerben: [Váltás Windows- és Linux-tárolók között](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).