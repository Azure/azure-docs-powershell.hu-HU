---
title: Az Azure PowerShell használata a Dockerben
description: Útmutatás a Docker-rendszerképekben előre telepített Azure PowerShell használatához.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/20/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2b487abeecbffa6cd8b7b64276ab301619348385
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/01/2020
ms.locfileid: "89244534"
---
# <a name="using-azure-powershell-in-docker"></a>Az Azure PowerShell használata a Dockerben

A Docker-rendszerképeket előre telepített Azure PowerShell-lel tesszük közzé. Ez a cikk bemutatja, hogyan kezdheti meg az Azure PowerShell használatát a Docker-tárolóban.

## <a name="finding-available-images"></a>Az elérhető rendszerképek keresése

A kiadott rendszerképekhez a Docker 17.05-ös vagy újabb verziója szükséges. Emellett képesnek kell lennie a Docker `sudo` vagy helyi rendszergazdai jogosultságok nélkül történő futtatására. Kövesse a Docker hivatalos [útmutatását][install] a `docker` megfelelő telepítéséhez.

A legfrissebb tárolórendszerkép tartalmazza a legújabb PowerShell-verziót és azokat a legújabb Azure PowerShell-modulokat, amelyeket az Az modul támogat.

Az Az modul minden egyes új kiadása esetében kiadunk egy-egy rendszerképet a következő operációs rendszerekhez:

- Ubuntu 18.04 (alapértelmezett)
- Debian 9
- CentOs 7

Az elérhető rendszerképek teljes listája a [Docker-rendszerképeket][az image] tartalmazó oldalunkon található meg.

## <a name="using-azure-powershell-in-a-container"></a>Az Azure PowerShell használata tárolóban

Az alábbi lépések bemutatják a rendszerkép letöltéséhez és egy interaktív PowerShell-munkamenet elindításához szükséges Docker-parancsokat.

1. Töltse le a legújabb azure-powershell rendszerképet.

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. Futtassa az azure-powershell tárolót interaktív módban:

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

A Windows Docker-gazdagépek esetében engedélyeznie kell a Docker-fájlmegosztás használatát, hogy a Windows rendszerű helyi meghajtók megoszthatók legyenek a Linux-tárolókkal. További információkért lásd [a Windowshoz készült Docker használatát bemutató részt][file-sharing].

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a>Az azure-powershell tároló interaktív futtatása gazdagép-hitelesítéssel

Ha az Azure PowerShell már telepítve lett a Dockert futtató rendszeren, lehet, hogy már gyorsítótárazta az Azure-beli hitelesítő adatokat. Ezek a hitelesítő adatok használhatók a Docker-tárolóban futó PowerShell-munkamenetben.

Alapértelmezés szerint a gyorsítótárazott hitelesítő adatok a gazdagép `$HOME/.Azure` könyvtárában találhatók. A Docker szolgáltatásnak hozzáféréssel kell rendelkeznie ehhez a helyhez a hitelesítő adatok eléréséhez. Az alábbi parancs elindítja a tárolót a csatolt hitelesítőadat-gyorsítótárral, majd elindít egy interaktív PowerShell-munkamenetet.

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a>A már nem szükséges rendszerkép eltávolítása

Az alábbi paranccsal törölheti a Docker-tárolót, ha már nincs rá szüksége.

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
