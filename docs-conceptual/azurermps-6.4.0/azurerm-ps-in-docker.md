---
title: Az Azure PowerShell futtatása Docker-tárolóban
description: Útmutatás az Azure PowerShell Docker-tárolóban történő futtatásához.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: b224beb95809d0e48c6f1dd5985de45b3b4df816
ms.sourcegitcommit: de0e60800df1add9f3400166faacca202ef567d9
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/03/2018
ms.locfileid: "37406359"
---
## <a name="run-azure-powershell-in-a-docker-container"></a>Az Azure PowerShell futtatása Docker-tárolóban

Az Azure PowerShellhez előre konfigurált Docker-rendszerképek érhetők el. Kétféle tároló érhető el: azok, amelyek a hagyományos PowerShellt futtatják Windows rendszeren, valamint egy olyan, amely a PowerShell Core-t futtatja Windows vagy Linux rendszeren.

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

## <a name="use-a-powershell-core-container"></a>PowerShell Core-tároló használata

A PowerShell Core-tárolókhoz a PowerShell Core 6-os verziója és az `AzureRM.NetCore` modul előre telepítve van. Futtassa az [Import-Module](/powershell/module/microsoft.powershell.core/import-module) parancsmagot, majd jelentkezzen be Azure-fiókjával:

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a>A Windows-tároló használata a PowerShell-lel

A Windows-tároló tartalmazza az előre telepített `AzureRM` modult. Futtassa az [Import-Module](/powershell/module/microsoft.powershell.core/import-module) parancsmagot, majd jelentkezzen be Azure-fiókjával:

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```