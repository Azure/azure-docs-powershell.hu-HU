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
# <a name="using-azure-powershell-in-docker"></a>Azure PowerShell használata a Docker-ben

A Docker-rendszerképeket a Azure PowerShell előre telepítettével tesszük közzé. Ez a cikk bemutatja, hogyan kezdheti el a Azure PowerShell használatát a Docker-tárolóban.

## <a name="finding-available-images"></a>Elérhető rendszerképek keresése

A kiadott képekhez a Docker 17,05-es vagy újabb verziója szükséges. Azt is feltételezi, hogy a Docker `sudo` -t vagy helyi rendszergazdai jogosultságokat nem lehet futtatni. A megfelelő telepítéshez kövesse a Docker hivatalos [utasításait][install] `docker` .

A tároló legújabb képe a PowerShell legújabb verzióját és a legújabb Azure PowerShell az az modul által támogatott modulokat tartalmazza.

Az az modul minden egyes új kiadásához a következő operációs rendszerekhez tartozó rendszerképet szabadítunk fel:

- Ubuntu 18,04 (alapértelmezett)
- Debian 9
- CentOs 7

Az elérhető lemezképek teljes listája megtalálható a [Docker-rendszerkép][az image] oldalán.

## <a name="using-azure-powershell-in-a-container"></a>Azure PowerShell használata tárolóban

A következő lépések a rendszerkép letöltéséhez és az interaktív PowerShell-munkamenet elindításához szükséges Docker-parancsokat mutatják be.

1. Töltse le a legújabb Azure-PowerShell-rendszerképet.

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. Futtassa az Azure-PowerShell-tárolót interaktív módban:

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

A Windows Docker-gazdagépek esetében engedélyeznie kell a Docker-fájlmegosztás használatát, hogy a Windows rendszerű helyi meghajtók megoszthatók legyenek a Linux-tárolókkal. További információ: a [Windows Docker szolgáltatásának első lépései][file-sharing].

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a>Az Azure-PowerShell-tároló interaktív futtatása gazdagép-hitelesítés használatával

Ha már telepítve van Azure PowerShell a Docker-t futtató rendszeren, akkor előfordulhat, hogy gyorsítótárazott Azure-beli hitelesítő adatokkal rendelkezik. Ezeket a hitelesítő adatokat a Docker-tárolóban futó PowerShell-munkamenetben lehet használni.

Alapértelmezés szerint a gyorsítótárazott hitelesítő adatok a `$HOME/.Azure` gazdagép könyvtárában találhatók. A Docker szolgáltatásnak hozzáféréssel kell rendelkeznie ehhez a helyhez a hitelesítő adatok eléréséhez. A következő parancs elindítja a tárolót a csatlakoztatott hitelesítőadat-gyorsítótárral, és elindítja az interaktív PowerShell-munkamenetet.

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a>A rendszerkép eltávolítása, ha már nincs rá szükség

A következő parancs használatával törölheti a Docker-tárolót, ha már nincs rá szüksége.

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a>Következő lépések

Az Azure PowerShell-modulokról és azok funkcióiról az [Azure PowerShell használatának első lépéseit](get-started-azureps.md) ismertető szakaszban talál további információt.

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell
[file-sharing]: https://docs.docker.com/docker-for-windows/#file-sharing
