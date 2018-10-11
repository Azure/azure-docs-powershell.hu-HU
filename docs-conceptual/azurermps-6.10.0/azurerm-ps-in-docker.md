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
# <a name="run-azure-powershell-in-a-docker-container"></a><span data-ttu-id="7bd7c-103">Az Azure PowerShell futtatása Docker-tárolóban</span><span class="sxs-lookup"><span data-stu-id="7bd7c-103">Run Azure PowerShell in a Docker container</span></span>

<span data-ttu-id="7bd7c-104">A Microsoft olyan Docker-rendszerképeket tesz közzé, amelyeken az Azure PowerShell már telepítve van.</span><span class="sxs-lookup"><span data-stu-id="7bd7c-104">Microsoft publishes Docker images with Azure PowerShell pre-installed.</span></span> <span data-ttu-id="7bd7c-105">Ezek a rendszerképek lehetővé teszik az Azure PowerShell-lel való kísérletezést, illetve a PowerShell elkülönített környezetben történő futtatását.</span><span class="sxs-lookup"><span data-stu-id="7bd7c-105">These images allow for experimenting with Azure PowerShell or running it in an isolated environment.</span></span> <span data-ttu-id="7bd7c-106">Bizonyos rendszerképek a PowerShell Core-t és PowerShell 5-öt is futtatják.</span><span class="sxs-lookup"><span data-stu-id="7bd7c-106">There are images running both PowerShell Core and PowerShell 5.</span></span> 

| <span data-ttu-id="7bd7c-107">Környezet</span><span class="sxs-lookup"><span data-stu-id="7bd7c-107">Environment</span></span> | <span data-ttu-id="7bd7c-108">Docker-rendszerkép</span><span class="sxs-lookup"><span data-stu-id="7bd7c-108">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="7bd7c-109">PowerShell Windows rendszeren</span><span class="sxs-lookup"><span data-stu-id="7bd7c-109">PowerShell on Windows</span></span> | [<span data-ttu-id="7bd7c-110">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="7bd7c-110">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="7bd7c-111">PowerShell Core Windows rendszeren</span><span class="sxs-lookup"><span data-stu-id="7bd7c-111">PowerShell Core on Windows</span></span> | [<span data-ttu-id="7bd7c-112">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="7bd7c-112">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="7bd7c-113">PowerShell Core Linux rendszeren</span><span class="sxs-lookup"><span data-stu-id="7bd7c-113">PowerShell Core on Linux</span></span> | [<span data-ttu-id="7bd7c-114">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="7bd7c-114">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="7bd7c-115">Ezen tárolók futtatásához a `docker run -it $ImageName` parancs segítségével kap egy interaktív terminált.</span><span class="sxs-lookup"><span data-stu-id="7bd7c-115">To run any of these containers, use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="7bd7c-116">A Linux-tároló PowerShell Core használatával történő futtatásához például használja a következőt:</span><span class="sxs-lookup"><span data-stu-id="7bd7c-116">For example, to run a Linux container with PowerShell Core:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="7bd7c-117">Ha Windows-tárolót szeretne futtatni a Dockerben, a gazdagép operációs rendszerének Windowsnak kell lennie, és a Dockert úgy kell beállítani, hogy Windows-tárolókat futtasson.</span><span class="sxs-lookup"><span data-stu-id="7bd7c-117">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="7bd7c-118">További információk a Windows- és Linux-környezet közötti váltáshoz a Dockerben: [Váltás Windows- és Linux-tárolók között](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span><span class="sxs-lookup"><span data-stu-id="7bd7c-118">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>

## <a name="use-a-powershell-core-container"></a><span data-ttu-id="7bd7c-119">PowerShell Core-tároló használata</span><span class="sxs-lookup"><span data-stu-id="7bd7c-119">Use a PowerShell Core container</span></span>

<span data-ttu-id="7bd7c-120">A PowerShell Core-tárolókhoz a PowerShell Core 6-os verziója és az `AzureRM.NetCore` modul előre telepítve van.</span><span class="sxs-lookup"><span data-stu-id="7bd7c-120">The PowerShell Core containers come with PowerShell Core v6 and the `AzureRM.NetCore` module pre-installed.</span></span> <span data-ttu-id="7bd7c-121">Futtassa az [Import-Module](/powershell/module/microsoft.powershell.core/import-module) parancsmagot, majd jelentkezzen be Azure-fiókjával:</span><span class="sxs-lookup"><span data-stu-id="7bd7c-121">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a><span data-ttu-id="7bd7c-122">A Windows-tároló használata a PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="7bd7c-122">Use the Windows container with PowerShell</span></span>

<span data-ttu-id="7bd7c-123">A Windows-tároló tartalmazza az előre telepített `AzureRM` modult.</span><span class="sxs-lookup"><span data-stu-id="7bd7c-123">The Windows container has the `AzureRM` module pre-installed.</span></span> <span data-ttu-id="7bd7c-124">Futtassa az [Import-Module](/powershell/module/microsoft.powershell.core/import-module) parancsmagot, majd jelentkezzen be Azure-fiókjával:</span><span class="sxs-lookup"><span data-stu-id="7bd7c-124">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```
