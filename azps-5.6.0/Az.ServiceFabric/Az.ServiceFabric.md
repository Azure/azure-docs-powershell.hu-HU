---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: b35ba1bcd976bbc563dd8e3ad6640279a5a8a1dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924426"
---
# Az.ServiceFabric modul
## Leírás
Azure Service Fabric modul, automatizálhatja a két végű műveleteket, például a biztonságos fürt létrehozását, a fürttanúsítványok használatát, a csomópontok hozzáadását vagy a fürtből való eltávolítást stb. Az alábbiakban felsoroljuk az összes művelet teljes listáját.

## Az.ServiceFabric parancsmagok
### [Add-AzServiceFabricClientCertificate](Add-AzServiceFabricClientCertificate.md)
Ügyfél-hitelesítési célokból adjon hozzá általános nevet vagy thumbprint-et a fürthöz.

### [Add-AzServiceFabricClusterCertificate](Add-AzServiceFabricClusterCertificate.md)
Vegyen fel egy másodlagos fürt tanúsítványát a fürtbe.

### [Add-AzServiceFabricManagedClusterClientCertificate](Add-AzServiceFabricManagedClusterClientCertificate.md)
Adja hozzá a tanúsítvány általános nevét vagy thumbprint-ját a fürthöz. Ez a módszer ismét regisztrálja a tanúsítványt, ügyfél-hitelesítési célokra.

### [Add-AzServiceFabricManagedNodeTypeVMExtension](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
Adja hozzá a vm bővítményt a csomóponttípushoz.

### [Add-AzServiceFabricManagedNodeTypeVMSecret](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
Adja hozzá a tanúsítvány titkos nevét a csomóponttípushoz.

### [Add-AzServiceFabricNode](Add-AzServiceFabricNode.md)
Csomópontok hozzáadása a fürt adott csomóponttípushoz.

### [Add-AzServiceFabricNodeType](Add-AzServiceFabricNodeType.md)
Új csomóponttípus hozzáadása a meglévő fürthöz.

### [Get-AzServiceFabricApplication](Get-AzServiceFabricApplication.md)
A Service Fabric alkalmazás részleteinek megtekintése.

### [Get-AzServiceFabricApplicationType](Get-AzServiceFabricApplicationType.md)
A Service Fabric alkalmazás típusának részleteinek lekérte.

### [Get-AzServiceFabricApplicationTypeVersion](Get-AzServiceFabricApplicationTypeVersion.md)
A Service Fabric alkalmazás verziószámának részletei.

### [Get-AzServiceFabricCluster](Get-AzServiceFabricCluster.md)
A fürterőforrás részleteinek megtekintése.

### [Get-AzServiceFabricManagedCluster](Get-AzServiceFabricManagedCluster.md)
A felügyelt fürterőforrás részleteinek megtekintése.

### [Get-AzServiceFabricManagedNodeType](Get-AzServiceFabricManagedNodeType.md)
A felügyelt csomópont típusú erőforrás részleteinek lekérte.

### [Get-AzServiceFabricService](Get-AzServiceFabricService.md)
A Service Fabric szolgáltatás részleteinek lekérte a megadott alkalmazás és fürt alatt.

### [New-AzServiceFabricApplication](New-AzServiceFabricApplication.md)
Hozzon létre új service fabric application under the specified resource group and cluster.

### [New-AzServiceFabricApplicationType](New-AzServiceFabricApplicationType.md)
Hozzon létre új service fabric application type under the specified resource group and cluster.

### [New-AzServiceFabricApplicationTypeVersion](New-AzServiceFabricApplicationTypeVersion.md)
Új alkalmazástípus-verzió létrehozása a megadott erőforráscsoport és fürt alatt.

### [New-AzServiceFabricCluster](New-AzServiceFabricCluster.md)
Ez a parancs az Ön által vagy a rendszer által létrehozott önaírt tanúsítványokat használja egy új szolgáltatás-hálócsoport beállítására. Használhat alapértelmezett sablont vagy egyéni sablont, amit Ön biztosít. Megadhatja azt a mappát, amelybe exportálhatja az önaírt tanúsítványokat, vagy később lehívhatja őket a kulcstárból.

### [New-AzServiceFabricManagedCluster](New-AzServiceFabricManagedCluster.md)
Hozzon létre új felügyelt fürtöt.

### [New-AzServiceFabricManagedNodeType](New-AzServiceFabricManagedNodeType.md)
Új csomóponttípus-erőforrás létrehozása

### [New-AzServiceFabricService](New-AzServiceFabricService.md)
Hozzon létre új szervizszolgáltatást a megadott alkalmazás és fürt alatt.

### [Remove-AzServiceFabricApplication](Remove-AzServiceFabricApplication.md)
Alkalmazás eltávolítása a fürtből Ezzel eltávolítja az alkalmazás összes szolgáltatását.

### [Remove-AzServiceFabricApplicationType](Remove-AzServiceFabricApplicationType.md)
Távolítsa el a Service fabric egy alkalmazástípust a fürtből. Ezzel eltávolítja az erőforrás összes típusverzióját.

### [Remove-AzServiceFabricApplicationTypeVersion](Remove-AzServiceFabricApplicationTypeVersion.md)
Távolítsa el a service fabric an application type version from the cluster.

### [Remove-AzServiceFabricClientCertificate](Remove-AzServiceFabricClientCertificate.md)
Távolítsa el az ügyfél-tanúsítvány(ok) vagy a tanúsítvány tulajdonosának(ok) nevét az ügyfél-hitelesítéshez a fürtre való ügyfélalkalmazás-hitelesítéshez.

### [Remove-AzServiceFabricClusterCertificate](Remove-AzServiceFabricClusterCertificate.md)
Távolítsa el a fürt tanúsítványát a fürtbiztonság érdekében.

### [Remove-AzServiceFabricManagedCluster](Remove-AzServiceFabricManagedCluster.md)
Fürterőforrás eltávolítása

### [Remove-AzServiceFabricManagedClusterClientCertificate](Remove-AzServiceFabricManagedClusterClientCertificate.md)
Ügyfél tanúsítványának visszaírása thumbprint vagy common name alapján.

### [Remove-AzServiceFabricManagedNodeType](Remove-AzServiceFabricManagedNodeType.md)
Távolítsa el a csomóponttípust vagy a csomóponttípus adott csomópontját.

### [Remove-AzServiceFabricManagedNodeTypeVMExtension](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
Távolítsa el a vm-bővítményt a csomóponttípusból.

### [Remove-AzServiceFabricNode](Remove-AzServiceFabricNode.md)
Csomópontok eltávolítása az adott csomóponttípusból a fürtből.

### [Remove-AzServiceFabricNodeType](Remove-AzServiceFabricNodeType.md)
Teljes csomóponttípus eltávolítása a fürtből.

### [Remove-AzServiceFabricService](Remove-AzServiceFabricService.md)
Szolgáltatás eltávolítása a fürtből.

### [Remove-AzServiceFabricSetting](Remove-AzServiceFabricSetting.md)
Távolítson el egy vagy több Service Fabric-beállítást a fürtből.

### [Restart-AzServiceFabricManagedNodeType](Restart-AzServiceFabricManagedNodeType.md)
Indítsa újra az egyes csomópontokat a csomóponttípusból.

### [Set-AzServiceFabricManagedCluster](Set-AzServiceFabricManagedCluster.md)
A fürterőforrás tulajdonságainak beállítása

### [Set-AzServiceFabricManagedNodeType](Set-AzServiceFabricManagedNodeType.md)
Beállítja a csomóponttípus erőforrástulajdonságokat, vagy reimage-műveleteket futtat a csomóponttípus -Reimage paraméterrel megadott ndes-ján.

### [Set-AzServiceFabricSetting](Set-AzServiceFabricSetting.md)
Vegyen fel vagy frissítsen egy vagy több Service Fabric-beállítást a fürtben.

### [Set-AzServiceFabricUpgradeType](Set-AzServiceFabricUpgradeType.md)
Módosítsa a Service Fabric frissítési típusát a fürthöz.

### [Update-AzServiceFabricApplication](Update-AzServiceFabricApplication.md)
Szervizáru-alkalmazás frissítése. Ez lehetővé teszi az alkalmazásparaméterek frissítését és/vagy az alkalmazástípus verzióját, amely elindít egy alkalmazásfrissítést.

### [Update-AzServiceFabricDurability](Update-AzServiceFabricDurability.md)
Frissítse a fürt egyik csomóponttípusának 10.10-es szintjéhez vagy VmSku-jának frissítéséhez.

### [Update-AzServiceFabricReliability](Update-AzServiceFabricReliability.md)
Frissítse egy fürt elsődleges csomóponttípusának megbízhatósági rétegét.

