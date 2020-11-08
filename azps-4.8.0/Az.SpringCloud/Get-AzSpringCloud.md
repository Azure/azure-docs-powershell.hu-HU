---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
ms.openlocfilehash: e304b9394878c734f51988816ef512158957feab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183944"
---
# Get-AzSpringCloud

## Áttekintés
Szerezzen be egy szolgáltatást és annak tulajdonságait.

## SZINTAXISA

### Lista (alapértelmezett)
```
Get-AzSpringCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Beszerzése
```
Get-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Lista1
```
Get-AzSpringCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## Leírás
Szerezzen be egy szolgáltatást és annak tulajdonságait.

## Példák

### Példa 1: a tavaszi Felhőbeli szolgáltatás beszerzése név alapján
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
ConfigServerPropertiesErrorCode                  :
ConfigServerPropertiesErrorMessage               :
ConfigServerPropertyState                        : Succeeded
GitPropertyHostKey                               :
GitPropertyHostKeyAlgorithm                      :
GitPropertyLabel                                 :
GitPropertyPassword                              :
GitPropertyPrivateKey                            :
GitPropertyRepository                            :
GitPropertySearchPath                            :
GitPropertyStrictHostKeyChecking                 :
GitPropertyUri                                   :
GitPropertyUsername                              :
Id                                               : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service
Location                                         : eastus
Name                                             : spring-cloud-service
NetworkProfileAppNetworkResourceGroup            :
NetworkProfileAppSubnetId                        :
NetworkProfileServiceCidr                        :
NetworkProfileServiceRuntimeNetworkResourceGroup :
NetworkProfileServiceRuntimeSubnetId             :
ProvisioningState                                : Succeeded
ServiceId                                        : e5e964885b4146b1a91e9bfc17971ee5
SkuCapacity                                      :
SkuName                                          : S0
SkuTier                                          : Standard
Tag                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TrackedResourceTags
TraceAppInsightInstrumentationKey                :
TraceEnabled                                     : False
TraceErrorCode                                   :
TraceErrorMessage                                :
TraceState                                       : Succeeded
Type                                             : Microsoft.AppPlatform/Spring
Version                                          : 2
ConfigServerGitProperty                          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerGitProperty
ConfigServerProperty                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerProperties
ConfigServerPropertyConfigServer                 : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerSettings
ConfigServerPropertyError                        : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
NetworkProfile                                   : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.NetworkProfile
Property                                         : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ClusterResourceProperties
Sku                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Sku
Trace                                            : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TraceProperties
TraceError                                       : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
```

A tavaszi felhő szolgáltatás beszerzése név alapján

### 2. példa: a tavaszi felhő-szolgáltatás listázása az erőforráscsoport alatt.
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg
Location Name                Type
-------- ----                ----
eastus   spring-cloud-rg Microsoft.AppPlatform/Spring
```

Felsorolhatja az összes tavaszi felhő-szolgáltatást az erőforrás csoportban.

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (név)
A szolgáltatás erőforrásának neve.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforrást tartalmazó erőforráscsoport neve.
Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Megkapja az előfizetés AZONOSÍTÓját, amely egyedileg azonosítja a Microsoft Azure-előfizetést.
Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### Microsoft. Azure. PowerShell. parancsmagok. SpringCloud. models. ISpringCloudIdentity

## KIMENETEK

### Microsoft. Azure. PowerShell. parancsmagok. SpringCloud. modellek. Api20190501Preview. IServiceResource

## MEGJEGYZI

ALIASOK

KOMPLEX PARAMÉTEREK TULAJDONSÁGAI

Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot. A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.


INPUTOBJECT <ISpringCloudIdentity> : Identity paraméter
  - `[AppName <String>]`: Az App-erőforrás neve.
  - `[BindingName <String>]`: A kötési erőforrás neve.
  - `[CertificateName <String>]`: A tanúsítvány-erőforrás neve.
  - `[DeploymentName <String>]`: A telepítő erőforrás neve.
  - `[DomainName <String>]`: Az egyéni tartomány-erőforrás neve.
  - `[Id <String>]`: Erőforrás-identitás elérési útja
  - `[Location <String>]`: a régió
  - `[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve. Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.
  - `[ServiceName <String>]`: A szolgáltatás-erőforrás neve.
  - `[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót kapja. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.

## KAPCSOLÓDÓ HIVATKOZÁSOK

