---
title: Az Azure PowerShell futtatása Docker-tárolóban
description: Útmutatás az Azure PowerShell Docker-tárolóban történő futtatásához.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: 27ac176d8bd0b142b7740b2ba6793edb500a8af3
ms.sourcegitcommit: 9cb98f055a0525c2061f65149965d5e7c3e03ddc
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/30/2018
ms.locfileid: "43117745"
---
# <a name="run-azure-powershell-in-a-docker-container"></a>Az Azure PowerShell futtatása Docker-tárolóban

Az Azure PowerShell hordozható környezetben való futtatásának megkönnyítése érdekében a Microsoft olyan Docker-rendszerképeket tesz közzé, amelyeken az Azure PowerShell már telepítve van. Ezek a rendszerképek elérhetők PowerShell Core-t futtató Linux-vendégrendszert, illetve PowerShell Core-t vagy PowerShell 5-öt futtató Windows-vendégrendszert futtató változatban.

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
