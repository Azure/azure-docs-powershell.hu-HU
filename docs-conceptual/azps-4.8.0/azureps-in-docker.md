---
title: Az Azure PowerShell használata a Dockerben
description: Útmutatás a Docker-rendszerképekben előre telepített Azure PowerShell használatához.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/20/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 48935f15241ec965adf4c34d2c17aa670110585a
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/06/2020
ms.locfileid: "93410156"
---
# <a name="using-azure-powershell-in-docker"></a><span data-ttu-id="3569f-103">Az Azure PowerShell használata a Dockerben</span><span class="sxs-lookup"><span data-stu-id="3569f-103">Using Azure PowerShell in Docker</span></span>

<span data-ttu-id="3569f-104">A Docker-rendszerképeket előre telepített Azure PowerShell-lel tesszük közzé.</span><span class="sxs-lookup"><span data-stu-id="3569f-104">We are publishing Docker images with Azure PowerShell preinstalled.</span></span> <span data-ttu-id="3569f-105">Ez a cikk bemutatja, hogyan kezdheti meg az Azure PowerShell használatát a Docker-tárolóban.</span><span class="sxs-lookup"><span data-stu-id="3569f-105">This article shows you how to get started using Azure PowerShell in the Docker container.</span></span>

## <a name="finding-available-images"></a><span data-ttu-id="3569f-106">Az elérhető rendszerképek keresése</span><span class="sxs-lookup"><span data-stu-id="3569f-106">Finding available images</span></span>

<span data-ttu-id="3569f-107">A kiadott rendszerképekhez a Docker 17.05-ös vagy újabb verziója szükséges.</span><span class="sxs-lookup"><span data-stu-id="3569f-107">The released images require Docker 17.05 or newer.</span></span> <span data-ttu-id="3569f-108">Emellett képesnek kell lennie a Docker `sudo` vagy helyi rendszergazdai jogosultságok nélkül történő futtatására.</span><span class="sxs-lookup"><span data-stu-id="3569f-108">It is also expected that you are able to run Docker without `sudo` or local administrative rights.</span></span> <span data-ttu-id="3569f-109">Kövesse a Docker hivatalos [útmutatását][install] a `docker` megfelelő telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="3569f-109">Please follow Docker's official [instructions][install] to install `docker` correctly.</span></span>

<span data-ttu-id="3569f-110">A legfrissebb tárolórendszerkép tartalmazza a legújabb PowerShell-verziót és azokat a legújabb Azure PowerShell-modulokat, amelyeket az Az modul támogat.</span><span class="sxs-lookup"><span data-stu-id="3569f-110">The latest container image contains the latest version of PowerShell and the latest Azure PowerShell modules supported with the Az module.</span></span>

<span data-ttu-id="3569f-111">Az Az modul minden egyes új kiadása esetében kiadunk egy-egy rendszerképet a következő operációs rendszerekhez:</span><span class="sxs-lookup"><span data-stu-id="3569f-111">For each new release of the Az module we are releasing an image for the following operating systems:</span></span>

- <span data-ttu-id="3569f-112">Ubuntu 18.04 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3569f-112">Ubuntu 18.04 (default)</span></span>
- <span data-ttu-id="3569f-113">Debian 9</span><span class="sxs-lookup"><span data-stu-id="3569f-113">Debian 9</span></span>
- <span data-ttu-id="3569f-114">CentOs 7</span><span class="sxs-lookup"><span data-stu-id="3569f-114">CentOs 7</span></span>

<span data-ttu-id="3569f-115">Az elérhető rendszerképek teljes listája a [Docker-rendszerképeket][az image] tartalmazó oldalunkon található meg.</span><span class="sxs-lookup"><span data-stu-id="3569f-115">A full list of available images can be found on our [Docker image][az image] page.</span></span>

## <a name="using-azure-powershell-in-a-container"></a><span data-ttu-id="3569f-116">Az Azure PowerShell használata tárolóban</span><span class="sxs-lookup"><span data-stu-id="3569f-116">Using Azure PowerShell in a container</span></span>

<span data-ttu-id="3569f-117">Az alábbi lépések bemutatják a rendszerkép letöltéséhez és egy interaktív PowerShell-munkamenet elindításához szükséges Docker-parancsokat.</span><span class="sxs-lookup"><span data-stu-id="3569f-117">The following steps show the Docker commands required to download the image and start an interactive PowerShell session.</span></span>

1. <span data-ttu-id="3569f-118">Töltse le a legújabb azure-powershell rendszerképet.</span><span class="sxs-lookup"><span data-stu-id="3569f-118">Download the latest azure-powershell image.</span></span>

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. <span data-ttu-id="3569f-119">Futtassa az azure-powershell tárolót interaktív módban:</span><span class="sxs-lookup"><span data-stu-id="3569f-119">Run the azure-powershell container in interactive mode:</span></span>

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

<span data-ttu-id="3569f-120">A Windows Docker-gazdagépek esetében engedélyeznie kell a Docker-fájlmegosztás használatát, hogy a Windows rendszerű helyi meghajtók megoszthatók legyenek a Linux-tárolókkal.</span><span class="sxs-lookup"><span data-stu-id="3569f-120">For Windows Docker hosts, you must enable Docker File Sharing to allow local drives on Windows to be shared with Linux containers.</span></span> <span data-ttu-id="3569f-121">További információkért lásd [a Windowshoz készült Docker használatát bemutató részt][file-sharing].</span><span class="sxs-lookup"><span data-stu-id="3569f-121">For more information see [Get started with Docker for Windows][file-sharing].</span></span>

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a><span data-ttu-id="3569f-122">Az azure-powershell tároló interaktív futtatása gazdagép-hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="3569f-122">Run the azure-powershell container interactively using host authentication</span></span>

<span data-ttu-id="3569f-123">Ha az Azure PowerShell már telepítve lett a Dockert futtató rendszeren, lehet, hogy már gyorsítótárazta az Azure-beli hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="3569f-123">If you have Azure PowerShell already installed on the system hosting Docker, you may have cached Azure credentials.</span></span> <span data-ttu-id="3569f-124">Ezek a hitelesítő adatok használhatók a Docker-tárolóban futó PowerShell-munkamenetben.</span><span class="sxs-lookup"><span data-stu-id="3569f-124">These credentials can be used in the PowerShell session running in the Docker container.</span></span>

<span data-ttu-id="3569f-125">Alapértelmezés szerint a gyorsítótárazott hitelesítő adatok a gazdagép `$HOME/.Azure` könyvtárában találhatók.</span><span class="sxs-lookup"><span data-stu-id="3569f-125">By default, the cached credentials are in `$HOME/.Azure` directory on your host.</span></span> <span data-ttu-id="3569f-126">A Docker szolgáltatásnak hozzáféréssel kell rendelkeznie ehhez a helyhez a hitelesítő adatok eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="3569f-126">The Docker service must have access to this location to access the credentials.</span></span> <span data-ttu-id="3569f-127">Az alábbi parancs elindítja a tárolót a csatolt hitelesítőadat-gyorsítótárral, majd elindít egy interaktív PowerShell-munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="3569f-127">The following command starts the container with the credential cache mounted and starts an interactive PowerShell session.</span></span>

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a><span data-ttu-id="3569f-128">A már nem szükséges rendszerkép eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3569f-128">Remove the image when no longer needed</span></span>

<span data-ttu-id="3569f-129">Az alábbi paranccsal törölheti a Docker-tárolót, ha már nincs rá szüksége.</span><span class="sxs-lookup"><span data-stu-id="3569f-129">The following command is used to delete the Docker container when you no longer need it.</span></span>

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a><span data-ttu-id="3569f-130">Következő lépések</span><span class="sxs-lookup"><span data-stu-id="3569f-130">Next steps</span></span>

<span data-ttu-id="3569f-131">Az Azure PowerShell-modulokról és azok funkcióiról az [Azure PowerShell használatának első lépéseit](get-started-azureps.md) ismertető szakaszban talál további információt.</span><span class="sxs-lookup"><span data-stu-id="3569f-131">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell
[file-sharing]: https://docs.docker.com/docker-for-windows/#file-sharing
