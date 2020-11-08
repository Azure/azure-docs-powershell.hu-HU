---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
ms.openlocfilehash: 3f08ada3dd485a1e18bb6f0a91037ba1df0b5f25
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017766"
---
# <span data-ttu-id="ef78c-101">New-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="ef78c-101">New-AzFrontDoor</span></span>

## <span data-ttu-id="ef78c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ef78c-102">SYNOPSIS</span></span>
<span data-ttu-id="ef78c-103">Új Azure bejárati ajtó kiegyenlítő létrehozása</span><span class="sxs-lookup"><span data-stu-id="ef78c-103">Create a new Azure Front Door load balancer</span></span>

## <span data-ttu-id="ef78c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ef78c-104">SYNTAX</span></span>

### <span data-ttu-id="ef78c-105">ByFieldsWithBackendPoolsSettingParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ef78c-105">ByFieldsWithBackendPoolsSettingParameterSet (Default)</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-BackendPoolsSetting <PSBackendPoolsSetting>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef78c-106">ByFieldsWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef78c-106">ByFieldsWithCertificateNameCheckParameterSet</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef78c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ef78c-107">DESCRIPTION</span></span>
<span data-ttu-id="ef78c-108">A **New-AzFrontDoor** parancsmag új Azure betárcsázós betöltőt hoz létre a megadott erőforrás-csoportban a jelenlegi előfizetés csoportban.</span><span class="sxs-lookup"><span data-stu-id="ef78c-108">The **New-AzFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <span data-ttu-id="ef78c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ef78c-109">EXAMPLES</span></span>

### <span data-ttu-id="ef78c-110">Példa 1: bejárati ajtó létrehozása megadott paraméterek alapján.</span><span class="sxs-lookup"><span data-stu-id="ef78c-110">Example 1: Create a Front Door based on given parameters.</span></span>
```powershell
PS C:\> New-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
BackendPoolsSetting         : {backendPoolsSetting1}
EnforceCertificateNameCheck : {backendPoolsSetting1.EnforceCertificateNameCheck}
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/rg1/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="ef78c-111">Bejárati ajtót hozhat létre a megadott paraméterek alapján.</span><span class="sxs-lookup"><span data-stu-id="ef78c-111">Create a Front Door based on given parameters.</span></span>

## <span data-ttu-id="ef78c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ef78c-112">PARAMETERS</span></span>

### <span data-ttu-id="ef78c-113">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="ef78c-113">-BackendPool</span></span>
<span data-ttu-id="ef78c-114">A Backendpools elérhető az útválasztási szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="ef78c-114">Backendpools available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef78c-115">-BackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="ef78c-115">-BackendPoolsSetting</span></span>
<span data-ttu-id="ef78c-116">Az összes backendPools beállításai</span><span class="sxs-lookup"><span data-stu-id="ef78c-116">Settings for all backendPools</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting
Parameter Sets: ByFieldsWithBackendPoolsSettingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef78c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef78c-117">-DefaultProfile</span></span>
<span data-ttu-id="ef78c-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef78c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef78c-119">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="ef78c-119">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="ef78c-120">Szeretné-e letiltani a hitelesítő név jelölőnégyzetet HTTPS-kéréseken az összes backend-készletre.</span><span class="sxs-lookup"><span data-stu-id="ef78c-120">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="ef78c-121">Nincs hatással a nem HTTPS-kérésekre.</span><span class="sxs-lookup"><span data-stu-id="ef78c-121">No effect on non-HTTPS requests.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFieldsWithCertificateNameCheckParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef78c-122">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="ef78c-122">-EnabledState</span></span>
<span data-ttu-id="ef78c-123">Az első ajtó EnabledState</span><span class="sxs-lookup"><span data-stu-id="ef78c-123">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="ef78c-124">Az alapértelmezett érték engedélyezve</span><span class="sxs-lookup"><span data-stu-id="ef78c-124">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef78c-125">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="ef78c-125">-FrontendEndpoint</span></span>
<span data-ttu-id="ef78c-126">Az útválasztási szabályokhoz elérhető felületi végpontok.</span><span class="sxs-lookup"><span data-stu-id="ef78c-126">Frontend endpoints available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef78c-127">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="ef78c-127">-HealthProbeSetting</span></span>
<span data-ttu-id="ef78c-128">A bejárati ajtóval társított állapot-szonda beállításai.</span><span class="sxs-lookup"><span data-stu-id="ef78c-128">Health probe settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef78c-129">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="ef78c-129">-LoadBalancingSetting</span></span>
<span data-ttu-id="ef78c-130">A bejárati ajtóval társított terheléselosztási beállítások.</span><span class="sxs-lookup"><span data-stu-id="ef78c-130">Load balancing settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef78c-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ef78c-131">-Name</span></span>
<span data-ttu-id="ef78c-132">A bejárati ajtó neve.</span><span class="sxs-lookup"><span data-stu-id="ef78c-132">Front Door name.</span></span>

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

### <span data-ttu-id="ef78c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef78c-133">-ResourceGroupName</span></span>
<span data-ttu-id="ef78c-134">Az erőforráscsoport neve, amelybe az első ajtó jön létre.</span><span class="sxs-lookup"><span data-stu-id="ef78c-134">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="ef78c-135">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="ef78c-135">-RoutingRule</span></span>
<span data-ttu-id="ef78c-136">Az FrontDoor társított útválasztási szabályok</span><span class="sxs-lookup"><span data-stu-id="ef78c-136">Routing rules associated with this FrontDoor</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef78c-137">-Címke</span><span class="sxs-lookup"><span data-stu-id="ef78c-137">-Tag</span></span>
<span data-ttu-id="ef78c-138">A címkéket társítja a FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="ef78c-138">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="ef78c-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ef78c-139">-Confirm</span></span>
<span data-ttu-id="ef78c-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ef78c-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef78c-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef78c-141">-WhatIf</span></span>
<span data-ttu-id="ef78c-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ef78c-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef78c-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ef78c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef78c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef78c-144">CommonParameters</span></span>
<span data-ttu-id="ef78c-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ef78c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef78c-146">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ef78c-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef78c-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef78c-147">INPUTS</span></span>

### <span data-ttu-id="ef78c-148">Nincs</span><span class="sxs-lookup"><span data-stu-id="ef78c-148">None</span></span>
## <span data-ttu-id="ef78c-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef78c-149">OUTPUTS</span></span>

### <span data-ttu-id="ef78c-150">Microsoft. Azure. Command. FrontDoor. models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="ef78c-150">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
## <span data-ttu-id="ef78c-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ef78c-151">NOTES</span></span>

## <span data-ttu-id="ef78c-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef78c-152">RELATED LINKS</span></span>

<span data-ttu-id="ef78c-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [Új – AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [Új – AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [Új – AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [Új – AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [Új – AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="ef78c-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>