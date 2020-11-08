---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/new-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
ms.openlocfilehash: c84037fd402e5ecea51cc4f60dcddb1873878f5a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183941"
---
# <span data-ttu-id="d80a1-101">New-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="d80a1-101">New-AzSpringCloud</span></span>

## <span data-ttu-id="d80a1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d80a1-102">SYNOPSIS</span></span>
<span data-ttu-id="d80a1-103">Hozzon létre egy új szolgáltatást, vagy frissítsen egy kilépés szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="d80a1-103">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="d80a1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d80a1-104">SYNTAX</span></span>

```
New-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d80a1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d80a1-105">DESCRIPTION</span></span>
<span data-ttu-id="d80a1-106">Hozzon létre egy új szolgáltatást, vagy frissítsen egy kilépés szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="d80a1-106">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="d80a1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d80a1-107">EXAMPLES</span></span>

### <span data-ttu-id="d80a1-108">1. példa: a tavaszi felhő szolgáltatás létrehozása.</span><span class="sxs-lookup"><span data-stu-id="d80a1-108">Example 1: Create a spring cloud service.</span></span>
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

<span data-ttu-id="d80a1-109">Készítsen egy tavaszi felhő-szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="d80a1-109">Create a spring cloud service.</span></span>

## <span data-ttu-id="d80a1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d80a1-110">PARAMETERS</span></span>

### <span data-ttu-id="d80a1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d80a1-111">-AsJob</span></span>
<span data-ttu-id="d80a1-112">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="d80a1-112">Run the command as a job</span></span>

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

### <span data-ttu-id="d80a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d80a1-113">-DefaultProfile</span></span>
<span data-ttu-id="d80a1-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d80a1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d80a1-115">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="d80a1-115">-GitPropertyUri</span></span>
<span data-ttu-id="d80a1-116">A tárház URI-ja</span><span class="sxs-lookup"><span data-stu-id="d80a1-116">URI of the repository</span></span>

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

### <span data-ttu-id="d80a1-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="d80a1-117">-Location</span></span>
<span data-ttu-id="d80a1-118">Az erőforrás földrajzi helye.</span><span class="sxs-lookup"><span data-stu-id="d80a1-118">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="d80a1-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d80a1-119">-Name</span></span>
<span data-ttu-id="d80a1-120">A szolgáltatás erőforrásának neve.</span><span class="sxs-lookup"><span data-stu-id="d80a1-120">The name of the Service resource.</span></span>

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

### <span data-ttu-id="d80a1-121">-Várva</span><span class="sxs-lookup"><span data-stu-id="d80a1-121">-NoWait</span></span>
<span data-ttu-id="d80a1-122">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="d80a1-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d80a1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d80a1-123">-ResourceGroupName</span></span>
<span data-ttu-id="d80a1-124">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d80a1-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d80a1-125">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="d80a1-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d80a1-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d80a1-126">-SkuName</span></span>
<span data-ttu-id="d80a1-127">A SKU neve</span><span class="sxs-lookup"><span data-stu-id="d80a1-127">Name of the Sku</span></span>

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

### <span data-ttu-id="d80a1-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="d80a1-128">-SkuTier</span></span>
<span data-ttu-id="d80a1-129">Az SKU rétege</span><span class="sxs-lookup"><span data-stu-id="d80a1-129">Tier of the Sku</span></span>

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

### <span data-ttu-id="d80a1-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d80a1-130">-SubscriptionId</span></span>
<span data-ttu-id="d80a1-131">Megkapja az előfizetés AZONOSÍTÓját, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="d80a1-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d80a1-132">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="d80a1-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d80a1-133">-Címke</span><span class="sxs-lookup"><span data-stu-id="d80a1-133">-Tag</span></span>
<span data-ttu-id="d80a1-134">A szolgáltatás címkéi, amelyek az erőforrást leíró kulcspárt tartalmazó párok listáját tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="d80a1-134">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="d80a1-135">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="d80a1-135">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="d80a1-136">Célalkalmazás Insight Instrumentation-kulcs</span><span class="sxs-lookup"><span data-stu-id="d80a1-136">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="d80a1-137">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="d80a1-137">-TraceEnabled</span></span>
<span data-ttu-id="d80a1-138">Azt jelzi, hogy engedélyezve van-e a nyomkövetési funkció?</span><span class="sxs-lookup"><span data-stu-id="d80a1-138">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="d80a1-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d80a1-139">-Confirm</span></span>
<span data-ttu-id="d80a1-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d80a1-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d80a1-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d80a1-141">-WhatIf</span></span>
<span data-ttu-id="d80a1-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d80a1-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d80a1-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d80a1-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d80a1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d80a1-144">CommonParameters</span></span>
<span data-ttu-id="d80a1-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d80a1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d80a1-146">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d80a1-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d80a1-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d80a1-147">INPUTS</span></span>

## <span data-ttu-id="d80a1-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d80a1-148">OUTPUTS</span></span>

### <span data-ttu-id="d80a1-149">Microsoft. Azure. PowerShell. parancsmagok. SpringCloud. modellek. Api20190501Preview. IServiceResource</span><span class="sxs-lookup"><span data-stu-id="d80a1-149">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IServiceResource</span></span>

## <span data-ttu-id="d80a1-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d80a1-150">NOTES</span></span>

<span data-ttu-id="d80a1-151">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d80a1-151">ALIASES</span></span>

## <span data-ttu-id="d80a1-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d80a1-152">RELATED LINKS</span></span>

