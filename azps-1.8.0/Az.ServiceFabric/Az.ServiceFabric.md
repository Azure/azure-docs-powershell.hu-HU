---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 01bf8c630f4fc4d137e98be5b1996eaf47ea3363
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93657867"
---
# Az. ServiceFabric modul
## Leírás
Azure Service Fabric modul, amellyel automatizálhatja a végpontos műveleteket (például biztonságos fürtöket), a fürtcsomópontok felett, illetve csomópontok hozzáadását és eltávolítását a fürtből stb. Az összes művelet teljes listája alább látható.

## Az. ServiceFabric parancsmagok
### [Add-AzServiceFabricApplicationCertificate](Add-AzServiceFabricApplicationCertificate.md)
Vegyen fel egy új tanúsítványt a fürtöt alkotó virtuális gép Méretarányi készletéhez. A tanúsítvány az alkalmazási tanúsítványként való használatra szolgál.

### [Add-AzServiceFabricClientCertificate](Add-AzServiceFabricClientCertificate.md)
Az ügyfél-hitelesítéshez adjon meg köznapi nevet vagy ujjlenyomatot a fürthöz.

### [Add-AzServiceFabricClusterCertificate](Add-AzServiceFabricClusterCertificate.md)
Másodlagos fürtcsomópont hozzáadása a fürthöz.

### [Add-AzServiceFabricNode](Add-AzServiceFabricNode.md)
Csomópontok hozzáadása a fürt adott csomópont-típusához

### [Add-AzServiceFabricNodeType](Add-AzServiceFabricNodeType.md)
Új csomópont-típus felvétele a meglévő fürtbe.

### [Get-AzServiceFabricCluster](Get-AzServiceFabricCluster.md)
A fürterőforrás részleteinek beszerzése

### [Új – AzServiceFabricCluster](New-AzServiceFabricCluster.md)
Ez a parancs az Ön által megadott vagy a rendszer által létrehozott tanúsítványokat használja az új Service Fabric-fürt beállításához. Használhatja az Ön által megadott alapértelmezett sablont vagy egyéni sablont. Megadhatja, hogy milyen mappa esetén szeretné exportálni az önaláírt tanúsítványokat, vagy később beolvassa őket a fő boltozatról. 

### [Remove-AzServiceFabricClientCertificate](Remove-AzServiceFabricClientCertificate.md)
Ügyféltanúsítvány (ok) vagy tanúsítvány tárgya (i) eltávolítása a fürt ügyfél-hitelesítéséhez használatos.

### [Remove-AzServiceFabricClusterCertificate](Remove-AzServiceFabricClusterCertificate.md)
A fürt biztonságához használt fürtcsomópontok eltávolítása

### [Remove-AzServiceFabricNode](Remove-AzServiceFabricNode.md)
Csomópontok eltávolítása a megadott csomópont-típusból egy fürtből

### [Remove-AzServiceFabricNodeType](Remove-AzServiceFabricNodeType.md)
Teljes csomópont-típus eltávolítása a fürtből

### [Remove-AzServiceFabricSetting](Remove-AzServiceFabricSetting.md)
Egy vagy több szolgáltatási anyag beállítás eltávolítása a fürtből

### [Set-AzServiceFabricSetting](Set-AzServiceFabricSetting.md)
Egy vagy több szolgáltatási szerkezet beállításainak hozzáadása vagy frissítése a fürthöz.

### [Set-AzServiceFabricUpgradeType](Set-AzServiceFabricUpgradeType.md)
Módosítsa a szolgáltatás szerkezetének frissítési típusát a fürtben.

### [Update-AzServiceFabricDurability](Update-AzServiceFabricDurability.md)
Módosítsa a VmSku tartóssági rétegét vagy egy csomópont típusát.

### [Update-AzServiceFabricReliability](Update-AzServiceFabricReliability.md)
A fürt elsődleges csomópont-típusának megbízhatósági szintjeinek frissítése

