---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 5d963384d08dfed2e7e8516b892d2a3680c9332c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014292"
---
# Az. ServiceFabric modul
## Leírás
Azure Service Fabric modul, amellyel automatizálhatja a végpontos műveleteket (például biztonságos fürtöket), a fürtcsomópontok felett, illetve csomópontok hozzáadását és eltávolítását a fürtből stb. Az összes művelet teljes listája alább látható.

## Az. ServiceFabric parancsmagok

### [Add-AzServiceFabricClientCertificate](Add-AzServiceFabricClientCertificate.md)
Az ügyfél-hitelesítéshez adjon meg köznapi nevet vagy ujjlenyomatot a fürthöz.

### [Add-AzServiceFabricClusterCertificate](Add-AzServiceFabricClusterCertificate.md)
Másodlagos fürtcsomópont hozzáadása a fürthöz.

### [Add-AzServiceFabricNode](Add-AzServiceFabricNode.md)
Csomópontok hozzáadása a fürt adott csomópont-típusához

### [Add-AzServiceFabricNodeType](Add-AzServiceFabricNodeType.md)
Új csomópont-típus felvétele a meglévő fürtbe.

### [Get-AzServiceFabricApplication](Get-AzServiceFabricApplication.md)
A Service Fabric alkalmazás részleteinek beszerzése

### [Get-AzServiceFabricApplicationType](Get-AzServiceFabricApplicationType.md)
A szolgáltatás anyagának beszerzése alkalmazás típusa – részletek

### [Get-AzServiceFabricApplicationTypeVersion](Get-AzServiceFabricApplicationTypeVersion.md)
A szolgáltatás típusa: az alkalmazás típusa – verzió részletei.

### [Get-AzServiceFabricCluster](Get-AzServiceFabricCluster.md)
A fürterőforrás részleteinek beszerzése

### [Get-AzServiceFabricService](Get-AzServiceFabricService.md)
A szolgáltatás szerkezete szolgáltatás adatai a megadott alkalmazásban és fürtben.

### [Új – AzServiceFabricApplication](New-AzServiceFabricApplication.md)
Új szolgáltatási anyag alkalmazása a megadott erőforráscsoport és fürt csoportban

### [Új – AzServiceFabricApplicationType](New-AzServiceFabricApplicationType.md)
Új szolgáltatásból álló anyag típusú alkalmazás létrehozása a megadott erőforráscsoport és fürt csoportban

### [Új – AzServiceFabricApplicationTypeVersion](New-AzServiceFabricApplicationTypeVersion.md)
Új alkalmazás típusú verzió létrehozása a megadott erőforráscsoport és fürt csoportban

### [Új – AzServiceFabricCluster](New-AzServiceFabricCluster.md)
Ez a parancs az Ön által megadott vagy a rendszer által létrehozott tanúsítványokat használja az új Service Fabric-fürt beállításához. Használhatja az Ön által megadott alapértelmezett sablont vagy egyéni sablont. Megadhatja, hogy milyen mappa esetén szeretné exportálni az önaláírt tanúsítványokat, vagy később beolvassa őket a fő boltozatról. 

### [Új – AzServiceFabricService](New-AzServiceFabricService.md)
Új szolgáltatási anyag szolgáltatás létrehozása a megadott alkalmazásban és fürtben.

### [Remove-AzServiceFabricApplication](Remove-AzServiceFabricApplication.md)
Alkalmazás eltávolítása a fürtből Ezzel eltávolítja a program az alkalmazás alatti összes szolgáltatást.

### [Remove-AzServiceFabricApplicationType](Remove-AzServiceFabricApplicationType.md)
A szolgáltatás eltávolítása: az alkalmazás típusa a fürtben. Ezzel a beállítással a program eltávolítja az összes típusú verziót az erőforrásból.

### [Remove-AzServiceFabricApplicationTypeVersion](Remove-AzServiceFabricApplicationTypeVersion.md)
A szolgáltatás eltávolítása: az alkalmazás típusának verziója a fürtből

### [Remove-AzServiceFabricClientCertificate](Remove-AzServiceFabricClientCertificate.md)
Ügyféltanúsítvány (ok) vagy tanúsítvány tárgya (i) eltávolítása a fürt ügyfél-hitelesítéséhez használatos.

### [Remove-AzServiceFabricClusterCertificate](Remove-AzServiceFabricClusterCertificate.md)
A fürt biztonságához használt fürtcsomópontok eltávolítása

### [Remove-AzServiceFabricNode](Remove-AzServiceFabricNode.md)
Csomópontok eltávolítása a megadott csomópont-típusból egy fürtből

### [Remove-AzServiceFabricNodeType](Remove-AzServiceFabricNodeType.md)
Teljes csomópont-típus eltávolítása a fürtből

### [Remove-AzServiceFabricService](Remove-AzServiceFabricService.md)
Szolgáltatás eltávolítása a fürtből

### [Remove-AzServiceFabricSetting](Remove-AzServiceFabricSetting.md)
Egy vagy több szolgáltatási anyag beállítás eltávolítása a fürtből

### [Set-AzServiceFabricSetting](Set-AzServiceFabricSetting.md)
Egy vagy több szolgáltatási szerkezet beállításainak hozzáadása vagy frissítése a fürthöz.

### [Set-AzServiceFabricUpgradeType](Set-AzServiceFabricUpgradeType.md)
Módosítsa a szolgáltatás szerkezetének frissítési típusát a fürtben.

### [Update-AzServiceFabricApplication](Update-AzServiceFabricApplication.md)
A szolgáltatás szövet-alkalmazásának frissítése Ez lehetővé teszi az alkalmazás paramétereinek frissítését és/vagy az alkalmazás típusának frissítését, amely elindítja az alkalmazások frissítését.

### [Update-AzServiceFabricDurability](Update-AzServiceFabricDurability.md)
Módosítsa a VmSku tartóssági rétegét vagy egy csomópont típusát.

### [Update-AzServiceFabricReliability](Update-AzServiceFabricReliability.md)
A fürt elsődleges csomópont-típusának megbízhatósági szintjeinek frissítése

