---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/update-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
ms.openlocfilehash: 9c9ec2f2a48d3bc94ef0e0ab72b5b2bf4edd9045
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005349"
---
# <span data-ttu-id="f536a-101">Update-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="f536a-101">Update-AzSpringCloud</span></span>

## <span data-ttu-id="f536a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f536a-102">SYNOPSIS</span></span>
<span data-ttu-id="f536a-103">Művelet egy kilépő szolgáltatás frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="f536a-103">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="f536a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f536a-104">SYNTAX</span></span>

### <span data-ttu-id="f536a-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f536a-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f536a-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f536a-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloud -InputObject <ISpringCloudIdentity> [-GitPropertyUri <String>] [-Location <String>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>] [-TraceAppInsightInstrumentationKey <String>]
 [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f536a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f536a-107">DESCRIPTION</span></span>
<span data-ttu-id="f536a-108">Művelet egy kilépő szolgáltatás frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="f536a-108">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="f536a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f536a-109">EXAMPLES</span></span>

### <span data-ttu-id="f536a-110">1. példa: A Tavaszi felhőszolgáltatás frissítése név szerint.</span><span class="sxs-lookup"><span data-stu-id="f536a-110">Example 1: Update Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Update-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
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

<span data-ttu-id="f536a-111">Frissítse a Tavaszi felhőszolgáltatást név szerint.</span><span class="sxs-lookup"><span data-stu-id="f536a-111">Update Spring Cloud Service by name.</span></span>

### <span data-ttu-id="f536a-112">2. példa: A tavaszi felhőszolgáltatás frissítése a pipe-ból.</span><span class="sxs-lookup"><span data-stu-id="f536a-112">Example 2: Update Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service | Update-AzSpringCloud
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

<span data-ttu-id="f536a-113">Frissítse a spring cloud service-et a pipe-ból.</span><span class="sxs-lookup"><span data-stu-id="f536a-113">Update Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="f536a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f536a-114">PARAMETERS</span></span>

### <span data-ttu-id="f536a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f536a-115">-AsJob</span></span>
<span data-ttu-id="f536a-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="f536a-116">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f536a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f536a-117">-DefaultProfile</span></span>
<span data-ttu-id="f536a-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f536a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f536a-119">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="f536a-119">-GitPropertyUri</span></span>
<span data-ttu-id="f536a-120">A tárház URI-ja</span><span class="sxs-lookup"><span data-stu-id="f536a-120">URI of the repository</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f536a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f536a-121">-InputObject</span></span>
<span data-ttu-id="f536a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="f536a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f536a-123">-Location</span><span class="sxs-lookup"><span data-stu-id="f536a-123">-Location</span></span>
<span data-ttu-id="f536a-124">Az erőforrás FÖLDRAJZI helye.</span><span class="sxs-lookup"><span data-stu-id="f536a-124">The GEO location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f536a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f536a-125">-Name</span></span>
<span data-ttu-id="f536a-126">A Szolgáltatás erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f536a-126">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f536a-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f536a-127">-NoWait</span></span>
<span data-ttu-id="f536a-128">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="f536a-128">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f536a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f536a-129">-ResourceGroupName</span></span>
<span data-ttu-id="f536a-130">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f536a-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f536a-131">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="f536a-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f536a-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f536a-132">-SkuName</span></span>
<span data-ttu-id="f536a-133">A termékváltozat neve</span><span class="sxs-lookup"><span data-stu-id="f536a-133">Name of the Sku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f536a-134">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="f536a-134">-SkuTier</span></span>
<span data-ttu-id="f536a-135">A termékváltozat rétege</span><span class="sxs-lookup"><span data-stu-id="f536a-135">Tier of the Sku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f536a-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f536a-136">-SubscriptionId</span></span>
<span data-ttu-id="f536a-137">Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="f536a-137">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f536a-138">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="f536a-138">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f536a-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="f536a-139">-Tag</span></span>
<span data-ttu-id="f536a-140">A szolgáltatás címkéi, amelyek az erőforrást leíró kulcsérték-párok listáját jelentik.</span><span class="sxs-lookup"><span data-stu-id="f536a-140">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f536a-141">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="f536a-141">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="f536a-142">Target application insight instrumentation key</span><span class="sxs-lookup"><span data-stu-id="f536a-142">Target application insight instrumentation key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f536a-143">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="f536a-143">-TraceEnabled</span></span>
<span data-ttu-id="f536a-144">Azt jelzi, hogy engedélyezi-e a nyomkövetési funkciót</span><span class="sxs-lookup"><span data-stu-id="f536a-144">Indicates whether enable the tracing functionality</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f536a-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f536a-145">-Confirm</span></span>
<span data-ttu-id="f536a-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f536a-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f536a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f536a-147">-WhatIf</span></span>
<span data-ttu-id="f536a-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f536a-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f536a-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f536a-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f536a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f536a-150">CommonParameters</span></span>
<span data-ttu-id="f536a-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f536a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f536a-152">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f536a-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f536a-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f536a-153">INPUTS</span></span>

### <span data-ttu-id="f536a-154">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="f536a-154">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="f536a-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f536a-155">OUTPUTS</span></span>

### <span data-ttu-id="f536a-156">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span><span class="sxs-lookup"><span data-stu-id="f536a-156">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="f536a-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f536a-157">NOTES</span></span>

<span data-ttu-id="f536a-158">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f536a-158">ALIASES</span></span>

<span data-ttu-id="f536a-159">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="f536a-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f536a-160">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="f536a-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f536a-161">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f536a-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f536a-162">INPUTOBJECT: <ISpringCloudIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="f536a-162">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f536a-163">`[AppName <String>]`: Az apperőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f536a-163">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="f536a-164">`[BindingName <String>]`: A Kötés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f536a-164">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="f536a-165">`[CertificateName <String>]`: A tanúsítványforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f536a-165">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="f536a-166">`[DeploymentName <String>]`: A Központi telepítés erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f536a-166">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="f536a-167">`[DomainName <String>]`: Az egyéni tartományerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f536a-167">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="f536a-168">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="f536a-168">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f536a-169">`[Location <String>]`: a régió</span><span class="sxs-lookup"><span data-stu-id="f536a-169">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="f536a-170">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f536a-170">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="f536a-171">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="f536a-171">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="f536a-172">`[ServiceName <String>]`: A Szolgáltatás erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f536a-172">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="f536a-173">`[SubscriptionId <String>]`: Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="f536a-173">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="f536a-174">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="f536a-174">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f536a-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f536a-175">RELATED LINKS</span></span>

