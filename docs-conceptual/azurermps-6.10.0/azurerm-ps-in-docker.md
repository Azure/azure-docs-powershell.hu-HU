---
title: Az Azure PowerShell futtatása Docker-tárolóban
description: Útmutatás az Azure PowerShell Docker-tárolóban történő futtatásához.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 0ed8f50abbcb2aa00192196f19004446dc696b5d
ms.sourcegitcommit: a749eb729f583c9d0dd86141bbd04984d77ae9ab
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/11/2018
ms.locfileid: "48882101"
---
# <a name="run-azure-powershell-in-a-docker-container"></a>Az Azure PowerShell futtatása Docker-tárolóban

A Microsoft olyan Docker-rendszerképeket tesz közzé, amelyeken az Azure PowerShell már telepítve van. Ezek a rendszerképek lehetővé teszik az Azure PowerShell-lel való kísérletezést, illetve a PowerShell elkülönített környezetben történő futtatását. Bizonyos rendszerképek a PowerShell Core-t és PowerShell 5-öt is futtatják. 

| Környezet | Docker-rendszerkép |
|-------------|--------------|
| PowerShell Windows rendszeren | [azuresdk/azure-powershell](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| PowerShell Core Windows rendszeren | [azuresdk/azure-powershell-core:nanoserver](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| PowerShell Core Linux rendszeren | [azuresdk/azure-powershell-core:latest](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

Ezen tárolók futtatásához a `docker run -it $ImageName` parancs segítségével kap egy interaktív terminált. A Linux-tároló PowerShell Core használatával történő futtatásához például használja a következőt:

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
