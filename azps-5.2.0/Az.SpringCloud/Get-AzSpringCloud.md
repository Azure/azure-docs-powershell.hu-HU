---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
ms.openlocfilehash: 39324dc0f85ca4d6f9c3498fae92c340e2113dad
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336042"
---
# <span data-ttu-id="f6bf6-101">Get-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="f6bf6-101">Get-AzSpringCloud</span></span>

## <span data-ttu-id="f6bf6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6bf6-102">SYNOPSIS</span></span>
<span data-ttu-id="f6bf6-103">Szolgáltatás és tulajdonságainak lekérte.</span><span class="sxs-lookup"><span data-stu-id="f6bf6-103">Get a Service and its properties.</span></span>

## <span data-ttu-id="f6bf6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f6bf6-104">SYNTAX</span></span>

### <span data-ttu-id="f6bf6-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f6bf6-105">List (Default)</span></span>
```
Get-AzSpringCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f6bf6-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="f6bf6-106">Get</span></span>
```
Get-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f6bf6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f6bf6-107">GetViaIdentity</span></span>
```
Get-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f6bf6-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="f6bf6-108">List1</span></span>
```
Get-AzSpringCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6bf6-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f6bf6-109">DESCRIPTION</span></span>
<span data-ttu-id="f6bf6-110">Szolgáltatás és tulajdonságainak lekérte.</span><span class="sxs-lookup"><span data-stu-id="f6bf6-110">Get a Service and its properties.</span></span>

## <span data-ttu-id="f6bf6-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f6bf6-111">EXAMPLES</span></span>

### <span data-ttu-id="f6bf6-112">1. példa: A Spring Cloud Service szolgáltatás lekért neve</span><span class="sxs-lookup"><span data-stu-id="f6bf6-112">Example 1: Get Spring Cloud Service by name</span></span>
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

<span data-ttu-id="f6bf6-113">A Spring Cloud Service szolgáltatás lekért neve</span><span class="sxs-lookup"><span data-stu-id="f6bf6-113">Get Spring Cloud Service by name</span></span>

### <span data-ttu-id="f6bf6-114">2. példa: Sorolja fel az erőforráscsoportban az összes tavaszi felhőszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="f6bf6-114">Example 2: List all the spring cloud service under the resource group.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg
Location Name                Type
-------- ----                ----
eastus   spring-cloud-rg Microsoft.AppPlatform/Spring
```

<span data-ttu-id="f6bf6-115">Sorolja fel a tavaszi felhőszolgáltatást az erőforráscsoport alatt.</span><span class="sxs-lookup"><span data-stu-id="f6bf6-115">List all the spring cloud service under the resource group.</span></span>

## <span data-ttu-id="f6bf6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6bf6-116">PARAMETERS</span></span>

### <span data-ttu-id="f6bf6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6bf6-117">-DefaultProfile</span></span>
<span data-ttu-id="f6bf6-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f6bf6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6bf6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6bf6-119">-InputObject</span></span>
<span data-ttu-id="f6bf6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="f6bf6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f6bf6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f6bf6-121">-Name</span></span>
<span data-ttu-id="f6bf6-122">A Szolgáltatás erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f6bf6-122">The name of the Service resource.</span></span>

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

### <span data-ttu-id="f6bf6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6bf6-123">-ResourceGroupName</span></span>
<span data-ttu-id="f6bf6-124">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f6bf6-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f6bf6-125">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="f6bf6-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="f6bf6-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f6bf6-126">-SubscriptionId</span></span>
<span data-ttu-id="f6bf6-127">Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="f6bf6-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f6bf6-128">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="f6bf6-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f6bf6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6bf6-129">CommonParameters</span></span>
<span data-ttu-id="f6bf6-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6bf6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6bf6-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6bf6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6bf6-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f6bf6-132">INPUTS</span></span>

### <span data-ttu-id="f6bf6-133">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="f6bf6-133">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="f6bf6-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6bf6-134">OUTPUTS</span></span>

### <span data-ttu-id="f6bf6-135">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span><span class="sxs-lookup"><span data-stu-id="f6bf6-135">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="f6bf6-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f6bf6-136">NOTES</span></span>

<span data-ttu-id="f6bf6-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f6bf6-137">ALIASES</span></span>

<span data-ttu-id="f6bf6-138">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="f6bf6-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f6bf6-139">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="f6bf6-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f6bf6-140">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f6bf6-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f6bf6-141">INPUTOBJECT: <ISpringCloudIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="f6bf6-141">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f6bf6-142">`[AppName <String>]`: Az apperőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f6bf6-142">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="f6bf6-143">`[BindingName <String>]`: A Kötés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f6bf6-143">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="f6bf6-144">`[CertificateName <String>]`: A tanúsítványforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f6bf6-144">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="f6bf6-145">`[DeploymentName <String>]`: A Központi telepítés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f6bf6-145">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="f6bf6-146">`[DomainName <String>]`: Az egyéni tartományerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f6bf6-146">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="f6bf6-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="f6bf6-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f6bf6-148">`[Location <String>]`: a régió</span><span class="sxs-lookup"><span data-stu-id="f6bf6-148">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="f6bf6-149">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f6bf6-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="f6bf6-150">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="f6bf6-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="f6bf6-151">`[ServiceName <String>]`: A Szolgáltatás erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f6bf6-151">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="f6bf6-152">`[SubscriptionId <String>]`: Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="f6bf6-152">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="f6bf6-153">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="f6bf6-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f6bf6-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6bf6-154">RELATED LINKS</span></span>

