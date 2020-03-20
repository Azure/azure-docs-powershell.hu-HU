---
title: Az Azure PowerShell használata a Dockerben
description: Útmutatás a Docker-rendszerképekben előre telepített Azure PowerShell használatához.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: a5746b71cfc41f7c6283b0e95b0940ca4b594ec7
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "79402680"
---
# <a name="using-azure-powershell-in-docker"></a><span data-ttu-id="8099e-103">Az Azure PowerShell használata a Dockerben</span><span class="sxs-lookup"><span data-stu-id="8099e-103">Using Azure PowerShell in Docker</span></span>

<span data-ttu-id="8099e-104">A Docker-rendszerképeket előre telepített Azure PowerShell-lel tesszük közzé.</span><span class="sxs-lookup"><span data-stu-id="8099e-104">We are publishing Docker images with Azure PowerShell preinstalled.</span></span> <span data-ttu-id="8099e-105">Ez a cikk bemutatja, hogyan kezdheti meg az Azure PowerShell használatát a Docker-tárolóban.</span><span class="sxs-lookup"><span data-stu-id="8099e-105">This article shows you how to get started using Azure PowerShell in the Docker container.</span></span>

## <a name="finding-available-images"></a><span data-ttu-id="8099e-106">Az elérhető rendszerképek keresése</span><span class="sxs-lookup"><span data-stu-id="8099e-106">Finding available images</span></span>

<span data-ttu-id="8099e-107">A kiadott rendszerképekhez a Docker 17.05-ös vagy újabb verziója szükséges.</span><span class="sxs-lookup"><span data-stu-id="8099e-107">The released images require Docker 17.05 or newer.</span></span> <span data-ttu-id="8099e-108">Emellett képesnek kell lennie a Docker `sudo` vagy helyi rendszergazdai jogosultságok nélkül történő futtatására.</span><span class="sxs-lookup"><span data-stu-id="8099e-108">It is also expected that you are able to run Docker without `sudo` or local administrative rights.</span></span> <span data-ttu-id="8099e-109">Kövesse a Docker hivatalos [útmutatását][install] a `docker` megfelelő telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="8099e-109">Please follow Docker's official [instructions][install] to install `docker` correctly.</span></span>

<span data-ttu-id="8099e-110">A kiadott tárolók létrehozása a hivatalos PowerShell-tárolókból történik, majd hozzáadjuk az Az modult rétegként.</span><span class="sxs-lookup"><span data-stu-id="8099e-110">The released containers are built from the official PowerShell containers, then the Az module added as a layer.</span></span>

<span data-ttu-id="8099e-111">A legújabb stabil rendszerképek az alábbiak:</span><span class="sxs-lookup"><span data-stu-id="8099e-111">The latest stable image includes:</span></span>

- <span data-ttu-id="8099e-112">Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="8099e-112">Ubuntu 18.04</span></span>
- <span data-ttu-id="8099e-113">PowerShell 6.2.4-es verzió</span><span class="sxs-lookup"><span data-stu-id="8099e-113">PowerShell version 6.2.4</span></span>
- <span data-ttu-id="8099e-114">Az Azure PowerShell legutóbbi Az modulja</span><span class="sxs-lookup"><span data-stu-id="8099e-114">Azure PowerShell most current Az module</span></span>

<span data-ttu-id="8099e-115">Az elérhető rendszerképek teljes listája a [Docker-rendszerképeket][az image] tartalmazó oldalunkon található meg.</span><span class="sxs-lookup"><span data-stu-id="8099e-115">A full list of available images can be found on our [Docker image][az image] page.</span></span>

## <a name="using-azure-powershell-in-a-container"></a><span data-ttu-id="8099e-116">Az Azure PowerShell használata tárolóban</span><span class="sxs-lookup"><span data-stu-id="8099e-116">Using Azure PowerShell in a container</span></span>

<span data-ttu-id="8099e-117">Az alábbi lépések bemutatják a rendszerkép letöltéséhez és egy interaktív PowerShell-munkamenet elindításához szükséges Docker-parancsokat.</span><span class="sxs-lookup"><span data-stu-id="8099e-117">The following steps show the Docker commands required to download the image and start an interactive PowerShell session.</span></span>

1. <span data-ttu-id="8099e-118">Töltse le a legújabb azure-powershell rendszerképet.</span><span class="sxs-lookup"><span data-stu-id="8099e-118">Download the latest azure-powershell image.</span></span>

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. <span data-ttu-id="8099e-119">Futtassa az azure-powershell tárolót interaktív módban:</span><span class="sxs-lookup"><span data-stu-id="8099e-119">Run the azure-powershell container in interactive mode:</span></span>

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a><span data-ttu-id="8099e-120">Az azure-powershell tároló interaktív futtatása gazdagép-hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="8099e-120">Run the azure-powershell container interactively using host authentication</span></span>

<span data-ttu-id="8099e-121">Ha az Azure PowerShell már telepítve lett a Dockert futtató rendszeren, lehet, hogy már gyorsítótárazta az Azure-beli hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="8099e-121">If you have Azure PowerShell already installed on the system hosting Docker, you may have cached Azure credentials.</span></span> <span data-ttu-id="8099e-122">Ezek a hitelesítő adatok használhatók a Docker-tárolóban futó PowerShell-munkamenetben.</span><span class="sxs-lookup"><span data-stu-id="8099e-122">These credentials can be used in the PowerShell session running in the Docker container.</span></span>

<span data-ttu-id="8099e-123">Alapértelmezés szerint a gyorsítótárazott hitelesítő adatok a gazdagép `$HOME/.Azure` könyvtárában találhatók.</span><span class="sxs-lookup"><span data-stu-id="8099e-123">By default, the cached credentials are in `$HOME/.Azure` directory on your host.</span></span> <span data-ttu-id="8099e-124">A Docker szolgáltatásnak hozzáféréssel kell rendelkeznie ehhez a helyhez a hitelesítő adatok eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="8099e-124">The Docker service must have access to this location to access the credentials.</span></span> <span data-ttu-id="8099e-125">Az alábbi parancs elindítja a tárolót a csatolt hitelesítőadat-gyorsítótárral, majd elindít egy interaktív PowerShell-munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="8099e-125">The following command starts the container with the credential cache mounted and starts an interactive PowerShell session.</span></span>

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a><span data-ttu-id="8099e-126">A már nem szükséges rendszerkép eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8099e-126">Remove the image when no longer needed</span></span>

<span data-ttu-id="8099e-127">Az alábbi paranccsal törölheti a Docker-tárolót, ha már nincs rá szüksége.</span><span class="sxs-lookup"><span data-stu-id="8099e-127">The following command is used to delete the Docker container when you no longer need it.</span></span>

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a><span data-ttu-id="8099e-128">További lépések</span><span class="sxs-lookup"><span data-stu-id="8099e-128">Next steps</span></span>

<span data-ttu-id="8099e-129">Az Azure PowerShell-modulokról és azok funkcióiról az [Azure PowerShell használatának első lépéseit](get-started-azureps.md) ismertető szakaszban talál további információt.</span><span class="sxs-lookup"><span data-stu-id="8099e-129">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell