---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/new-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
ms.openlocfilehash: d5b8d521c72b553143f75b0911cb9b933b0795e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150635"
---
# <span data-ttu-id="491b6-101">New-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="491b6-101">New-AzSpringCloud</span></span>

## <span data-ttu-id="491b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="491b6-102">SYNOPSIS</span></span>
<span data-ttu-id="491b6-103">Hozzon létre egy új szolgáltatást, vagy frissítsen egy kilépő szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="491b6-103">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="491b6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="491b6-104">SYNTAX</span></span>

```
New-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="491b6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="491b6-105">DESCRIPTION</span></span>
<span data-ttu-id="491b6-106">Hozzon létre egy új szolgáltatást, vagy frissítsen egy kilépő szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="491b6-106">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="491b6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="491b6-107">EXAMPLES</span></span>

### <span data-ttu-id="491b6-108">1. példa: Tavaszi felhőszolgáltatás létrehozása.</span><span class="sxs-lookup"><span data-stu-id="491b6-108">Example 1: Create a spring cloud service.</span></span>
```powershell
PS C:\> New-AzSpringCloud -ResourceGroupName spring-cloud-rp -name spring-cloud-service -Location eastus

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

<span data-ttu-id="491b6-109">Létrehozhat egy tavaszi felhőszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="491b6-109">Create a spring cloud service.</span></span>

## <span data-ttu-id="491b6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="491b6-110">PARAMETERS</span></span>

### <span data-ttu-id="491b6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="491b6-111">-AsJob</span></span>
<span data-ttu-id="491b6-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="491b6-112">Run the command as a job</span></span>

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

### <span data-ttu-id="491b6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="491b6-113">-DefaultProfile</span></span>
<span data-ttu-id="491b6-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="491b6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="491b6-115">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="491b6-115">-GitPropertyUri</span></span>
<span data-ttu-id="491b6-116">A tárház URI-ja</span><span class="sxs-lookup"><span data-stu-id="491b6-116">URI of the repository</span></span>

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

### <span data-ttu-id="491b6-117">-Location</span><span class="sxs-lookup"><span data-stu-id="491b6-117">-Location</span></span>
<span data-ttu-id="491b6-118">Az erőforrás FÖLDRAJZI helye.</span><span class="sxs-lookup"><span data-stu-id="491b6-118">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="491b6-119">-Name</span><span class="sxs-lookup"><span data-stu-id="491b6-119">-Name</span></span>
<span data-ttu-id="491b6-120">A Szolgáltatás erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="491b6-120">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="491b6-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="491b6-121">-NoWait</span></span>
<span data-ttu-id="491b6-122">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="491b6-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="491b6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="491b6-123">-ResourceGroupName</span></span>
<span data-ttu-id="491b6-124">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="491b6-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="491b6-125">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="491b6-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="491b6-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="491b6-126">-SkuName</span></span>
<span data-ttu-id="491b6-127">A termékváltozat neve</span><span class="sxs-lookup"><span data-stu-id="491b6-127">Name of the Sku</span></span>

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

### <span data-ttu-id="491b6-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="491b6-128">-SkuTier</span></span>
<span data-ttu-id="491b6-129">A termékváltozat rétege</span><span class="sxs-lookup"><span data-stu-id="491b6-129">Tier of the Sku</span></span>

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

### <span data-ttu-id="491b6-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="491b6-130">-SubscriptionId</span></span>
<span data-ttu-id="491b6-131">Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="491b6-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="491b6-132">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="491b6-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="491b6-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="491b6-133">-Tag</span></span>
<span data-ttu-id="491b6-134">A szolgáltatás címkéi, amelyek az erőforrást leíró kulcsérték-párok listáját jelentik.</span><span class="sxs-lookup"><span data-stu-id="491b6-134">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="491b6-135">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="491b6-135">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="491b6-136">Target application insight instrumentation key</span><span class="sxs-lookup"><span data-stu-id="491b6-136">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="491b6-137">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="491b6-137">-TraceEnabled</span></span>
<span data-ttu-id="491b6-138">Azt jelzi, hogy engedélyezi-e a nyomkövetési funkciót</span><span class="sxs-lookup"><span data-stu-id="491b6-138">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="491b6-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="491b6-139">-Confirm</span></span>
<span data-ttu-id="491b6-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="491b6-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="491b6-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="491b6-141">-WhatIf</span></span>
<span data-ttu-id="491b6-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="491b6-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="491b6-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="491b6-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="491b6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="491b6-144">CommonParameters</span></span>
<span data-ttu-id="491b6-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="491b6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="491b6-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="491b6-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="491b6-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="491b6-147">INPUTS</span></span>

## <span data-ttu-id="491b6-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="491b6-148">OUTPUTS</span></span>

### <span data-ttu-id="491b6-149">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span><span class="sxs-lookup"><span data-stu-id="491b6-149">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="491b6-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="491b6-150">NOTES</span></span>

<span data-ttu-id="491b6-151">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="491b6-151">ALIASES</span></span>

## <span data-ttu-id="491b6-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="491b6-152">RELATED LINKS</span></span>

