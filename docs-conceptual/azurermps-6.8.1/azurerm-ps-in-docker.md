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
ms.sourcegitcommit: dca906e73e943aac207cee23b79915773419c673
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/30/2018
ms.locfileid: "43250401"
---
# <a name="run-azure-powershell-in-a-docker-container"></a><span data-ttu-id="289bc-103">Az Azure PowerShell futtatása Docker-tárolóban</span><span class="sxs-lookup"><span data-stu-id="289bc-103">Run Azure PowerShell in a Docker container</span></span>

<span data-ttu-id="289bc-104">Az Azure PowerShell hordozható környezetben való futtatásának megkönnyítése érdekében a Microsoft olyan Docker-rendszerképeket tesz közzé, amelyeken az Azure PowerShell már telepítve van.</span><span class="sxs-lookup"><span data-stu-id="289bc-104">To make running Azure PowerShell in portable environments easy, Microsoft publishes Docker images with Azure PowerShell pre-installed.</span></span> <span data-ttu-id="289bc-105">Ezek a rendszerképek elérhetők PowerShell Core-t futtató Linux-vendégrendszert, illetve PowerShell Core-t vagy PowerShell 5-öt futtató Windows-vendégrendszert futtató változatban.</span><span class="sxs-lookup"><span data-stu-id="289bc-105">These images offer a Linux guest running PowerShell Core, or a Windows guest with either PowerShell Core or PowerShell 5.</span></span>

| <span data-ttu-id="289bc-106">Környezet</span><span class="sxs-lookup"><span data-stu-id="289bc-106">Environment</span></span> | <span data-ttu-id="289bc-107">Docker-rendszerkép</span><span class="sxs-lookup"><span data-stu-id="289bc-107">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="289bc-108">PowerShell Windows rendszeren</span><span class="sxs-lookup"><span data-stu-id="289bc-108">PowerShell on Windows</span></span> | [<span data-ttu-id="289bc-109">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="289bc-109">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="289bc-110">PowerShell Core Windows rendszeren</span><span class="sxs-lookup"><span data-stu-id="289bc-110">PowerShell Core on Windows</span></span> | [<span data-ttu-id="289bc-111">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="289bc-111">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="289bc-112">PowerShell Core Linux rendszeren</span><span class="sxs-lookup"><span data-stu-id="289bc-112">PowerShell Core on Linux</span></span> | [<span data-ttu-id="289bc-113">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="289bc-113">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="289bc-114">Ezen tárolók futtatásához a `docker run -it $ImageName` parancs segítségével kap egy interaktív terminált.</span><span class="sxs-lookup"><span data-stu-id="289bc-114">To run any of these containers, you use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="289bc-115">A PowerShell Core Linux-tárolón történő futtatásához például használja a következőt:</span><span class="sxs-lookup"><span data-stu-id="289bc-115">For example, to run the PowerShell Core on Linux container, use:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="289bc-116">Ha Windows-tárolót szeretne futtatni a Dockerben, a gazdagép operációs rendszerének Windowsnak kell lennie, és a Dockert úgy kell beállítani, hogy Windows-tárolókat futtasson.</span><span class="sxs-lookup"><span data-stu-id="289bc-116">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="289bc-117">További információk a Windows- és Linux-környezet közötti váltáshoz a Dockerben: [Váltás Windows- és Linux-tárolók között](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span><span class="sxs-lookup"><span data-stu-id="289bc-117">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>

## <a name="use-a-powershell-core-container"></a><span data-ttu-id="289bc-118">PowerShell Core-tároló használata</span><span class="sxs-lookup"><span data-stu-id="289bc-118">Use a PowerShell Core container</span></span>

<span data-ttu-id="289bc-119">A PowerShell Core-tárolókhoz a PowerShell Core 6-os verziója és az `AzureRM.NetCore` modul előre telepítve van.</span><span class="sxs-lookup"><span data-stu-id="289bc-119">The PowerShell Core containers come with PowerShell Core v6 and the `AzureRM.NetCore` module pre-installed.</span></span> <span data-ttu-id="289bc-120">Futtassa az [Import-Module](/powershell/module/microsoft.powershell.core/import-module) parancsmagot, majd jelentkezzen be Azure-fiókjával:</span><span class="sxs-lookup"><span data-stu-id="289bc-120">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a><span data-ttu-id="289bc-121">A Windows-tároló használata a PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="289bc-121">Use the Windows container with PowerShell</span></span>

<span data-ttu-id="289bc-122">A Windows-tároló tartalmazza az előre telepített `AzureRM` modult.</span><span class="sxs-lookup"><span data-stu-id="289bc-122">The Windows container has the `AzureRM` module pre-installed.</span></span> <span data-ttu-id="289bc-123">Futtassa az [Import-Module](/powershell/module/microsoft.powershell.core/import-module) parancsmagot, majd jelentkezzen be Azure-fiókjával:</span><span class="sxs-lookup"><span data-stu-id="289bc-123">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```
