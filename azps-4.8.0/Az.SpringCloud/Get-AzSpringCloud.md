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
# <span data-ttu-id="e534a-101">Get-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="e534a-101">Get-AzSpringCloud</span></span>

## <span data-ttu-id="e534a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e534a-102">SYNOPSIS</span></span>
<span data-ttu-id="e534a-103">Szerezzen be egy szolgáltatást és annak tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="e534a-103">Get a Service and its properties.</span></span>

## <span data-ttu-id="e534a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e534a-104">SYNTAX</span></span>

### <span data-ttu-id="e534a-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e534a-105">List (Default)</span></span>
```
Get-AzSpringCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e534a-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="e534a-106">Get</span></span>
```
Get-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e534a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e534a-107">GetViaIdentity</span></span>
```
Get-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e534a-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="e534a-108">List1</span></span>
```
Get-AzSpringCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e534a-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="e534a-109">DESCRIPTION</span></span>
<span data-ttu-id="e534a-110">Szerezzen be egy szolgáltatást és annak tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="e534a-110">Get a Service and its properties.</span></span>

## <span data-ttu-id="e534a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="e534a-111">EXAMPLES</span></span>

### <span data-ttu-id="e534a-112">Példa 1: a tavaszi Felhőbeli szolgáltatás beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="e534a-112">Example 1: Get Spring Cloud Service by name</span></span>
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

<span data-ttu-id="e534a-113">A tavaszi felhő szolgáltatás beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="e534a-113">Get Spring Cloud Service by name</span></span>

### <span data-ttu-id="e534a-114">2. példa: a tavaszi felhő-szolgáltatás listázása az erőforráscsoport alatt.</span><span class="sxs-lookup"><span data-stu-id="e534a-114">Example 2: List all the spring cloud service under the resource group.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg
Location Name                Type
-------- ----                ----
eastus   spring-cloud-rg Microsoft.AppPlatform/Spring
```

<span data-ttu-id="e534a-115">Felsorolhatja az összes tavaszi felhő-szolgáltatást az erőforrás csoportban.</span><span class="sxs-lookup"><span data-stu-id="e534a-115">List all the spring cloud service under the resource group.</span></span>

## <span data-ttu-id="e534a-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e534a-116">PARAMETERS</span></span>

### <span data-ttu-id="e534a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e534a-117">-DefaultProfile</span></span>
<span data-ttu-id="e534a-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e534a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e534a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e534a-119">-InputObject</span></span>
<span data-ttu-id="e534a-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e534a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e534a-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e534a-121">-Name</span></span>
<span data-ttu-id="e534a-122">A szolgáltatás erőforrásának neve.</span><span class="sxs-lookup"><span data-stu-id="e534a-122">The name of the Service resource.</span></span>

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

### <span data-ttu-id="e534a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e534a-123">-ResourceGroupName</span></span>
<span data-ttu-id="e534a-124">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e534a-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e534a-125">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="e534a-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e534a-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e534a-126">-SubscriptionId</span></span>
<span data-ttu-id="e534a-127">Megkapja az előfizetés AZONOSÍTÓját, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="e534a-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e534a-128">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e534a-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e534a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e534a-129">CommonParameters</span></span>
<span data-ttu-id="e534a-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e534a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e534a-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e534a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e534a-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e534a-132">INPUTS</span></span>

### <span data-ttu-id="e534a-133">Microsoft. Azure. PowerShell. parancsmagok. SpringCloud. models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="e534a-133">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="e534a-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e534a-134">OUTPUTS</span></span>

### <span data-ttu-id="e534a-135">Microsoft. Azure. PowerShell. parancsmagok. SpringCloud. modellek. Api20190501Preview. IServiceResource</span><span class="sxs-lookup"><span data-stu-id="e534a-135">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IServiceResource</span></span>

## <span data-ttu-id="e534a-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e534a-136">NOTES</span></span>

<span data-ttu-id="e534a-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e534a-137">ALIASES</span></span>

<span data-ttu-id="e534a-138">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="e534a-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e534a-139">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="e534a-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e534a-140">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="e534a-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e534a-141">INPUTOBJECT <ISpringCloudIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="e534a-141">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e534a-142">`[AppName <String>]`: Az App-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e534a-142">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="e534a-143">`[BindingName <String>]`: A kötési erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e534a-143">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="e534a-144">`[CertificateName <String>]`: A tanúsítvány-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e534a-144">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="e534a-145">`[DeploymentName <String>]`: A telepítő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e534a-145">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="e534a-146">`[DomainName <String>]`: Az egyéni tartomány-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e534a-146">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="e534a-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="e534a-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e534a-148">`[Location <String>]`: a régió</span><span class="sxs-lookup"><span data-stu-id="e534a-148">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="e534a-149">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e534a-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="e534a-150">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="e534a-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="e534a-151">`[ServiceName <String>]`: A szolgáltatás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e534a-151">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="e534a-152">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót kapja.</span><span class="sxs-lookup"><span data-stu-id="e534a-152">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="e534a-153">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e534a-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e534a-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e534a-154">RELATED LINKS</span></span>

