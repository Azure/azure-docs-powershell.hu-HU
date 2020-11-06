---
Module Name: AzureRM.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
ms.openlocfilehash: 0bd157b8df4cca37c92a4d4f2984011dbd924e34
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93490056"
---
# AzureRM. ServiceFabric modul
## Leírás
Azure Service Fabric modul, amellyel automatizálhatja a végpontos műveleteket (például biztonságos fürtöket), a fürtcsomópontok felett, illetve csomópontok hozzáadását és eltávolítását a fürtből stb. Az összes művelet teljes listája alább látható.

## AzureRM. ServiceFabric parancsmagok
### [Add-AzureRmServiceFabricApplicationCertificate](Add-AzureRmServiceFabricApplicationCertificate.md)
Vegyen fel egy új tanúsítványt a fürtöt alkotó virtuális gép Méretarányi készletéhez. A tanúsítvány az alkalmazási tanúsítványként való használatra szolgál.

### [Add-AzureRmServiceFabricClientCertificate](Add-AzureRmServiceFabricClientCertificate.md)
Az ügyfél-hitelesítéshez adjon meg köznapi nevet vagy ujjlenyomatot a fürthöz.

### [Add-AzureRmServiceFabricClusterCertificate](Add-AzureRmServiceFabricClusterCertificate.md)
Másodlagos fürtcsomópont hozzáadása a fürthöz.

### [Add-AzureRmServiceFabricNode](Add-AzureRmServiceFabricNode.md)
Csomópontok hozzáadása a fürt adott csomópont-típusához

### [Add-AzureRmServiceFabricNodeType](Add-AzureRmServiceFabricNodeType.md)
Új csomópont-típus felvétele a meglévő fürtbe.

### [Get-AzureRmServiceFabricCluster](Get-AzureRmServiceFabricCluster.md)
A fürterőforrás részleteinek beszerzése

### [Új – AzureRmServiceFabricCluster](New-AzureRmServiceFabricCluster.md)
Ez a parancs az Ön által megadott vagy a rendszer által létrehozott tanúsítványokat használja az új Service Fabric-fürt beállításához. Használhatja az Ön által megadott alapértelmezett sablont vagy egyéni sablont. Megadhatja, hogy milyen mappa esetén szeretné exportálni az önaláírt tanúsítványokat, vagy később beolvassa őket a fő boltozatról. 

### [Remove-AzureRmServiceFabricClientCertificate](Remove-AzureRmServiceFabricClientCertificate.md)
Ügyféltanúsítvány (ok) vagy tanúsítvány tárgya (i) eltávolítása a fürt ügyfél-hitelesítéséhez használatos.

### [Remove-AzureRmServiceFabricClusterCertificate](Remove-AzureRmServiceFabricClusterCertificate.md)
A fürt biztonságához használt fürtcsomópontok eltávolítása

### [Remove-AzureRmServiceFabricNode](Remove-AzureRmServiceFabricNode.md)
Csomópontok eltávolítása a megadott csomópont-típusból egy fürtből

### [Remove-AzureRmServiceFabricNodeType](Remove-AzureRmServiceFabricNodeType.md)
Teljes csomópont-típus eltávolítása a fürtből

### [Remove-AzureRmServiceFabricSetting](Remove-AzureRmServiceFabricSetting.md)
Egy vagy több szolgáltatási anyag beállítás eltávolítása a fürtből

### [Set-AzureRmServiceFabricSetting](Set-AzureRmServiceFabricSetting.md)
Egy vagy több szolgáltatási szerkezet beállításainak hozzáadása vagy frissítése a fürthöz.

### [Set-AzureRmServiceFabricUpgradeType](Set-AzureRmServiceFabricUpgradeType.md)
Módosítsa a szolgáltatás szerkezetének frissítési típusát a fürtben.

### [Update-AzureRmServiceFabricDurability](Update-AzureRmServiceFabricDurability.md)
Módosítsa a VmSku tartóssági rétegét vagy egy csomópont típusát.

### [Update-AzureRmServiceFabricReliability](Update-AzureRmServiceFabricReliability.md)
A fürt elsődleges csomópont-típusának megbízhatósági szintjeinek frissítése

