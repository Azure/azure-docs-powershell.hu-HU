---
title: Az Azure PowerShell futtatása Docker-tárolóban
description: Útmutatás az Azure PowerShell futtatásához Docker-tárolóban.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: b224beb95809d0e48c6f1dd5985de45b3b4df816
ms.sourcegitcommit: 4c775721461210431bd913f28d1f1e6f1976880a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/28/2018
ms.locfileid: "37091599"
---
## <a name="run-azure-powershell-in-a-docker-container"></a><span data-ttu-id="1c6cb-103">Az Azure PowerShell futtatása Docker-tárolóban</span><span class="sxs-lookup"><span data-stu-id="1c6cb-103">Run Azure PowerShell in a Docker container</span></span>

<span data-ttu-id="1c6cb-104">Elérhetők az Azure PowerShellhez előre konfigurált Docker-rendszerképek.</span><span class="sxs-lookup"><span data-stu-id="1c6cb-104">There are a set of Docker images preconfigured with Azure PowerShell.</span></span> <span data-ttu-id="1c6cb-105">Kétféle tároló érhető el: azok, amelyek a hagyományos PowerShellt futtatják Windows rendszeren, és egy olyan, amely a PowerShell Core-t futtatja Windows vagy Linux rendszeren.</span><span class="sxs-lookup"><span data-stu-id="1c6cb-105">Two types of containers are available: Those running traditional PowerShell on Windows, and a container running PowerShell Core on either Windows or Linux.</span></span>

| <span data-ttu-id="1c6cb-106">Környezet</span><span class="sxs-lookup"><span data-stu-id="1c6cb-106">Environment</span></span> | <span data-ttu-id="1c6cb-107">Docker-rendszerkép</span><span class="sxs-lookup"><span data-stu-id="1c6cb-107">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="1c6cb-108">PowerShell Windows rendszeren</span><span class="sxs-lookup"><span data-stu-id="1c6cb-108">PowerShell on Windows</span></span> | [<span data-ttu-id="1c6cb-109">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="1c6cb-109">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="1c6cb-110">PowerShell Core Windows rendszeren</span><span class="sxs-lookup"><span data-stu-id="1c6cb-110">PowerShell Core on Windows</span></span> | [<span data-ttu-id="1c6cb-111">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="1c6cb-111">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="1c6cb-112">PowerShell Core Linux rendszeren</span><span class="sxs-lookup"><span data-stu-id="1c6cb-112">PowerShell Core on Linux</span></span> | [<span data-ttu-id="1c6cb-113">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="1c6cb-113">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="1c6cb-114">Ezen tárolók futtatásához a `docker run -it $ImageName` parancs segítségével kap egy interaktív terminált.</span><span class="sxs-lookup"><span data-stu-id="1c6cb-114">To run any of these containers, you use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="1c6cb-115">A PowerShell Core Linux-tárolón történő futtatásához például használja a következőt:</span><span class="sxs-lookup"><span data-stu-id="1c6cb-115">For example, to run the PowerShell Core on Linux container, use:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="1c6cb-116">Ha Windows-tárolót szeretne futtatni a Dockerben, a gazdagép operációs rendszerének Windowsnak kell lennie, és a Dockert úgy kell beállítani, hogy Windows-tárolókat futtasson.</span><span class="sxs-lookup"><span data-stu-id="1c6cb-116">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="1c6cb-117">További információk a Windows- és Linux-környezet közötti váltáshoz a Dockerben: [Váltás Windows- és Linux-tárolók között](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span><span class="sxs-lookup"><span data-stu-id="1c6cb-117">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>

## <a name="use-a-powershell-core-container"></a><span data-ttu-id="1c6cb-118">PowerShell Core-tároló használata</span><span class="sxs-lookup"><span data-stu-id="1c6cb-118">Use a PowerShell Core container</span></span>

<span data-ttu-id="1c6cb-119">A PowerShell Core-tárolókhoz a PowerShell Core 6-os verziója és az `AzureRM.NetCore` modul előre telepítve van.</span><span class="sxs-lookup"><span data-stu-id="1c6cb-119">The PowerShell Core containers come with PowerShell Core v6 and the `AzureRM.NetCore` module pre-installed.</span></span> <span data-ttu-id="1c6cb-120">Futtassa az [Import-Module](/powershell/module/microsoft.powershell.core/import-module) parancsmagot, majd jelentkezzen be Azure-fiókjával:</span><span class="sxs-lookup"><span data-stu-id="1c6cb-120">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a><span data-ttu-id="1c6cb-121">A Windows-tároló használata a PowerShell-lel</span><span class="sxs-lookup"><span data-stu-id="1c6cb-121">Use the Windows container with PowerShell</span></span>

<span data-ttu-id="1c6cb-122">A Windows-tároló tartalmazza az előre telepített `AzureRM` modult.</span><span class="sxs-lookup"><span data-stu-id="1c6cb-122">The Windows container has the `AzureRM` module pre-installed.</span></span> <span data-ttu-id="1c6cb-123">Futtassa az [Import-Module](/powershell/module/microsoft.powershell.core/import-module) parancsmagot, majd jelentkezzen be Azure-fiókjával:</span><span class="sxs-lookup"><span data-stu-id="1c6cb-123">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```