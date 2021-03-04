---
title: Azure PowerShell használata a Docker-ben
description: A Docker-rendszerképben előre telepített Azure PowerShell használata.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/20/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 48935f15241ec965adf4c34d2c17aa670110585a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101881935"
---
# <a name="using-azure-powershell-in-docker"></a><span data-ttu-id="bce43-103">Azure PowerShell használata a Docker-ben</span><span class="sxs-lookup"><span data-stu-id="bce43-103">Using Azure PowerShell in Docker</span></span>

<span data-ttu-id="bce43-104">A Docker-rendszerképeket a Azure PowerShell előre telepítettével tesszük közzé.</span><span class="sxs-lookup"><span data-stu-id="bce43-104">We are publishing Docker images with Azure PowerShell preinstalled.</span></span> <span data-ttu-id="bce43-105">Ez a cikk bemutatja, hogyan kezdheti el a Azure PowerShell használatát a Docker-tárolóban.</span><span class="sxs-lookup"><span data-stu-id="bce43-105">This article shows you how to get started using Azure PowerShell in the Docker container.</span></span>

## <a name="finding-available-images"></a><span data-ttu-id="bce43-106">Elérhető rendszerképek keresése</span><span class="sxs-lookup"><span data-stu-id="bce43-106">Finding available images</span></span>

<span data-ttu-id="bce43-107">A kiadott képekhez a Docker 17,05-es vagy újabb verziója szükséges.</span><span class="sxs-lookup"><span data-stu-id="bce43-107">The released images require Docker 17.05 or newer.</span></span> <span data-ttu-id="bce43-108">Azt is feltételezi, hogy a Docker `sudo` -t vagy helyi rendszergazdai jogosultságokat nem lehet futtatni.</span><span class="sxs-lookup"><span data-stu-id="bce43-108">It is also expected that you are able to run Docker without `sudo` or local administrative rights.</span></span> <span data-ttu-id="bce43-109">A megfelelő telepítéshez kövesse a Docker hivatalos [utasításait][install] `docker` .</span><span class="sxs-lookup"><span data-stu-id="bce43-109">Please follow Docker's official [instructions][install] to install `docker` correctly.</span></span>

<span data-ttu-id="bce43-110">A tároló legújabb képe a PowerShell legújabb verzióját és a legújabb Azure PowerShell az az modul által támogatott modulokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="bce43-110">The latest container image contains the latest version of PowerShell and the latest Azure PowerShell modules supported with the Az module.</span></span>

<span data-ttu-id="bce43-111">Az az modul minden egyes új kiadásához a következő operációs rendszerekhez tartozó rendszerképet szabadítunk fel:</span><span class="sxs-lookup"><span data-stu-id="bce43-111">For each new release of the Az module we are releasing an image for the following operating systems:</span></span>

- <span data-ttu-id="bce43-112">Ubuntu 18,04 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bce43-112">Ubuntu 18.04 (default)</span></span>
- <span data-ttu-id="bce43-113">Debian 9</span><span class="sxs-lookup"><span data-stu-id="bce43-113">Debian 9</span></span>
- <span data-ttu-id="bce43-114">CentOs 7</span><span class="sxs-lookup"><span data-stu-id="bce43-114">CentOs 7</span></span>

<span data-ttu-id="bce43-115">Az elérhető lemezképek teljes listája megtalálható a [Docker-rendszerkép][az image] oldalán.</span><span class="sxs-lookup"><span data-stu-id="bce43-115">A full list of available images can be found on our [Docker image][az image] page.</span></span>

## <a name="using-azure-powershell-in-a-container"></a><span data-ttu-id="bce43-116">Azure PowerShell használata tárolóban</span><span class="sxs-lookup"><span data-stu-id="bce43-116">Using Azure PowerShell in a container</span></span>

<span data-ttu-id="bce43-117">A következő lépések a rendszerkép letöltéséhez és az interaktív PowerShell-munkamenet elindításához szükséges Docker-parancsokat mutatják be.</span><span class="sxs-lookup"><span data-stu-id="bce43-117">The following steps show the Docker commands required to download the image and start an interactive PowerShell session.</span></span>

1. <span data-ttu-id="bce43-118">Töltse le a legújabb Azure-PowerShell-rendszerképet.</span><span class="sxs-lookup"><span data-stu-id="bce43-118">Download the latest azure-powershell image.</span></span>

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. <span data-ttu-id="bce43-119">Futtassa az Azure-PowerShell-tárolót interaktív módban:</span><span class="sxs-lookup"><span data-stu-id="bce43-119">Run the azure-powershell container in interactive mode:</span></span>

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

<span data-ttu-id="bce43-120">A Windows Docker-gazdagépek esetében engedélyeznie kell a Docker-fájlmegosztás használatát, hogy a Windows rendszerű helyi meghajtók megoszthatók legyenek a Linux-tárolókkal.</span><span class="sxs-lookup"><span data-stu-id="bce43-120">For Windows Docker hosts, you must enable Docker File Sharing to allow local drives on Windows to be shared with Linux containers.</span></span> <span data-ttu-id="bce43-121">További információ: a [Windows Docker szolgáltatásának első lépései][file-sharing].</span><span class="sxs-lookup"><span data-stu-id="bce43-121">For more information see [Get started with Docker for Windows][file-sharing].</span></span>

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a><span data-ttu-id="bce43-122">Az Azure-PowerShell-tároló interaktív futtatása gazdagép-hitelesítés használatával</span><span class="sxs-lookup"><span data-stu-id="bce43-122">Run the azure-powershell container interactively using host authentication</span></span>

<span data-ttu-id="bce43-123">Ha már telepítve van Azure PowerShell a Docker-t futtató rendszeren, akkor előfordulhat, hogy gyorsítótárazott Azure-beli hitelesítő adatokkal rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="bce43-123">If you have Azure PowerShell already installed on the system hosting Docker, you may have cached Azure credentials.</span></span> <span data-ttu-id="bce43-124">Ezeket a hitelesítő adatokat a Docker-tárolóban futó PowerShell-munkamenetben lehet használni.</span><span class="sxs-lookup"><span data-stu-id="bce43-124">These credentials can be used in the PowerShell session running in the Docker container.</span></span>

<span data-ttu-id="bce43-125">Alapértelmezés szerint a gyorsítótárazott hitelesítő adatok a `$HOME/.Azure` gazdagép könyvtárában találhatók.</span><span class="sxs-lookup"><span data-stu-id="bce43-125">By default, the cached credentials are in `$HOME/.Azure` directory on your host.</span></span> <span data-ttu-id="bce43-126">A Docker szolgáltatásnak hozzáféréssel kell rendelkeznie ehhez a helyhez a hitelesítő adatok eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="bce43-126">The Docker service must have access to this location to access the credentials.</span></span> <span data-ttu-id="bce43-127">A következő parancs elindítja a tárolót a csatlakoztatott hitelesítőadat-gyorsítótárral, és elindítja az interaktív PowerShell-munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="bce43-127">The following command starts the container with the credential cache mounted and starts an interactive PowerShell session.</span></span>

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a><span data-ttu-id="bce43-128">A rendszerkép eltávolítása, ha már nincs rá szükség</span><span class="sxs-lookup"><span data-stu-id="bce43-128">Remove the image when no longer needed</span></span>

<span data-ttu-id="bce43-129">A következő parancs használatával törölheti a Docker-tárolót, ha már nincs rá szüksége.</span><span class="sxs-lookup"><span data-stu-id="bce43-129">The following command is used to delete the Docker container when you no longer need it.</span></span>

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a><span data-ttu-id="bce43-130">Következő lépések</span><span class="sxs-lookup"><span data-stu-id="bce43-130">Next steps</span></span>

<span data-ttu-id="bce43-131">Az Azure PowerShell-modulokról és azok funkcióiról az [Azure PowerShell használatának első lépéseit](get-started-azureps.md) ismertető szakaszban talál további információt.</span><span class="sxs-lookup"><span data-stu-id="bce43-131">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell
[file-sharing]: https://docs.docker.com/docker-for-windows/#file-sharing
