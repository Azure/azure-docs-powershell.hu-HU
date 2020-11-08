---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/update-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
ms.openlocfilehash: 361ba47486d7cc506e918ea279129110306e415f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185221"
---
# <span data-ttu-id="930f5-101">Update-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="930f5-101">Update-AzSpringCloud</span></span>

## <span data-ttu-id="930f5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="930f5-102">SYNOPSIS</span></span>
<span data-ttu-id="930f5-103">Művelet a kilépési szolgáltatás frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="930f5-103">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="930f5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="930f5-104">SYNTAX</span></span>

### <span data-ttu-id="930f5-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="930f5-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="930f5-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="930f5-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloud -InputObject <ISpringCloudIdentity> [-GitPropertyUri <String>] [-Location <String>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>] [-TraceAppInsightInstrumentationKey <String>]
 [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="930f5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="930f5-107">DESCRIPTION</span></span>
<span data-ttu-id="930f5-108">Művelet a kilépési szolgáltatás frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="930f5-108">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="930f5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="930f5-109">EXAMPLES</span></span>

### <span data-ttu-id="930f5-110">1. példa: a tavaszi Felhőbeli szolgáltatás frissítése név szerint.</span><span class="sxs-lookup"><span data-stu-id="930f5-110">Example 1: Update Spring Cloud Service by name.</span></span>
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

<span data-ttu-id="930f5-111">Frissítse a tavaszi felhő szolgáltatását név szerint.</span><span class="sxs-lookup"><span data-stu-id="930f5-111">Update Spring Cloud Service by name.</span></span>

### <span data-ttu-id="930f5-112">2. példa: a tavaszi felhő szolgáltatás frissítése a pipe-ról</span><span class="sxs-lookup"><span data-stu-id="930f5-112">Example 2: Update Spring Cloud Service from pipe.</span></span>
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

<span data-ttu-id="930f5-113">Frissítse a tavaszi felhő szolgáltatását a pipe-ról.</span><span class="sxs-lookup"><span data-stu-id="930f5-113">Update Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="930f5-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="930f5-114">PARAMETERS</span></span>

### <span data-ttu-id="930f5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="930f5-115">-AsJob</span></span>
<span data-ttu-id="930f5-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="930f5-116">Run the command as a job</span></span>

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

### <span data-ttu-id="930f5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="930f5-117">-DefaultProfile</span></span>
<span data-ttu-id="930f5-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="930f5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="930f5-119">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="930f5-119">-GitPropertyUri</span></span>
<span data-ttu-id="930f5-120">A tárház URI-ja</span><span class="sxs-lookup"><span data-stu-id="930f5-120">URI of the repository</span></span>

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

### <span data-ttu-id="930f5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="930f5-121">-InputObject</span></span>
<span data-ttu-id="930f5-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="930f5-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="930f5-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="930f5-123">-Location</span></span>
<span data-ttu-id="930f5-124">Az erőforrás földrajzi helye.</span><span class="sxs-lookup"><span data-stu-id="930f5-124">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="930f5-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="930f5-125">-Name</span></span>
<span data-ttu-id="930f5-126">A szolgáltatás erőforrásának neve.</span><span class="sxs-lookup"><span data-stu-id="930f5-126">The name of the Service resource.</span></span>

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

### <span data-ttu-id="930f5-127">-Várva</span><span class="sxs-lookup"><span data-stu-id="930f5-127">-NoWait</span></span>
<span data-ttu-id="930f5-128">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="930f5-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="930f5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="930f5-129">-ResourceGroupName</span></span>
<span data-ttu-id="930f5-130">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="930f5-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="930f5-131">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="930f5-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="930f5-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="930f5-132">-SkuName</span></span>
<span data-ttu-id="930f5-133">A SKU neve</span><span class="sxs-lookup"><span data-stu-id="930f5-133">Name of the Sku</span></span>

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

### <span data-ttu-id="930f5-134">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="930f5-134">-SkuTier</span></span>
<span data-ttu-id="930f5-135">Az SKU rétege</span><span class="sxs-lookup"><span data-stu-id="930f5-135">Tier of the Sku</span></span>

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

### <span data-ttu-id="930f5-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="930f5-136">-SubscriptionId</span></span>
<span data-ttu-id="930f5-137">Megkapja az előfizetés AZONOSÍTÓját, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="930f5-137">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="930f5-138">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="930f5-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="930f5-139">-Címke</span><span class="sxs-lookup"><span data-stu-id="930f5-139">-Tag</span></span>
<span data-ttu-id="930f5-140">A szolgáltatás címkéi, amelyek az erőforrást leíró kulcspárt tartalmazó párok listáját tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="930f5-140">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="930f5-141">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="930f5-141">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="930f5-142">Célalkalmazás Insight Instrumentation-kulcs</span><span class="sxs-lookup"><span data-stu-id="930f5-142">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="930f5-143">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="930f5-143">-TraceEnabled</span></span>
<span data-ttu-id="930f5-144">Azt jelzi, hogy engedélyezve van-e a nyomkövetési funkció?</span><span class="sxs-lookup"><span data-stu-id="930f5-144">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="930f5-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="930f5-145">-Confirm</span></span>
<span data-ttu-id="930f5-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="930f5-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="930f5-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="930f5-147">-WhatIf</span></span>
<span data-ttu-id="930f5-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="930f5-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="930f5-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="930f5-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="930f5-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="930f5-150">CommonParameters</span></span>
<span data-ttu-id="930f5-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="930f5-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="930f5-152">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="930f5-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="930f5-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="930f5-153">INPUTS</span></span>

### <span data-ttu-id="930f5-154">Microsoft. Azure. PowerShell. parancsmagok. SpringCloud. models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="930f5-154">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="930f5-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="930f5-155">OUTPUTS</span></span>

### <span data-ttu-id="930f5-156">Microsoft. Azure. PowerShell. parancsmagok. SpringCloud. modellek. Api20200701. IServiceResource</span><span class="sxs-lookup"><span data-stu-id="930f5-156">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="930f5-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="930f5-157">NOTES</span></span>

<span data-ttu-id="930f5-158">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="930f5-158">ALIASES</span></span>

<span data-ttu-id="930f5-159">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="930f5-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="930f5-160">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="930f5-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="930f5-161">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="930f5-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="930f5-162">INPUTOBJECT <ISpringCloudIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="930f5-162">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="930f5-163">`[AppName <String>]`: Az App-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="930f5-163">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="930f5-164">`[BindingName <String>]`: A kötési erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="930f5-164">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="930f5-165">`[CertificateName <String>]`: A tanúsítvány-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="930f5-165">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="930f5-166">`[DeploymentName <String>]`: A telepítő erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="930f5-166">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="930f5-167">`[DomainName <String>]`: Az egyéni tartomány-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="930f5-167">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="930f5-168">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="930f5-168">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="930f5-169">`[Location <String>]`: a régió</span><span class="sxs-lookup"><span data-stu-id="930f5-169">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="930f5-170">`[ResourceGroupName <String>]`: Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="930f5-170">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="930f5-171">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="930f5-171">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="930f5-172">`[ServiceName <String>]`: A szolgáltatás-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="930f5-172">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="930f5-173">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító előfizetési azonosítót kapja.</span><span class="sxs-lookup"><span data-stu-id="930f5-173">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="930f5-174">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="930f5-174">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="930f5-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="930f5-175">RELATED LINKS</span></span>

