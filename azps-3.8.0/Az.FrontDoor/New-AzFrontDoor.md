---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
ms.openlocfilehash: 3f08ada3dd485a1e18bb6f0a91037ba1df0b5f25
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845522"
---
# <span data-ttu-id="1c27f-101">New-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="1c27f-101">New-AzFrontDoor</span></span>

## <span data-ttu-id="1c27f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1c27f-102">SYNOPSIS</span></span>
<span data-ttu-id="1c27f-103">Új Azure bejárati ajtó kiegyenlítő létrehozása</span><span class="sxs-lookup"><span data-stu-id="1c27f-103">Create a new Azure Front Door load balancer</span></span>

## <span data-ttu-id="1c27f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1c27f-104">SYNTAX</span></span>

### <span data-ttu-id="1c27f-105">ByFieldsWithBackendPoolsSettingParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1c27f-105">ByFieldsWithBackendPoolsSettingParameterSet (Default)</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-BackendPoolsSetting <PSBackendPoolsSetting>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c27f-106">ByFieldsWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c27f-106">ByFieldsWithCertificateNameCheckParameterSet</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c27f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1c27f-107">DESCRIPTION</span></span>
<span data-ttu-id="1c27f-108">A **New-AzFrontDoor** parancsmag új Azure betárcsázós betöltőt hoz létre a megadott erőforrás-csoportban a jelenlegi előfizetés csoportban.</span><span class="sxs-lookup"><span data-stu-id="1c27f-108">The **New-AzFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <span data-ttu-id="1c27f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1c27f-109">EXAMPLES</span></span>

### <span data-ttu-id="1c27f-110">Példa 1: bejárati ajtó létrehozása megadott paraméterek alapján.</span><span class="sxs-lookup"><span data-stu-id="1c27f-110">Example 1: Create a Front Door based on given parameters.</span></span>
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

<span data-ttu-id="1c27f-111">Bejárati ajtót hozhat létre a megadott paraméterek alapján.</span><span class="sxs-lookup"><span data-stu-id="1c27f-111">Create a Front Door based on given parameters.</span></span>

## <span data-ttu-id="1c27f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1c27f-112">PARAMETERS</span></span>

### <span data-ttu-id="1c27f-113">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="1c27f-113">-BackendPool</span></span>
<span data-ttu-id="1c27f-114">A Backendpools elérhető az útválasztási szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="1c27f-114">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="1c27f-115">-BackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="1c27f-115">-BackendPoolsSetting</span></span>
<span data-ttu-id="1c27f-116">Az összes backendPools beállításai</span><span class="sxs-lookup"><span data-stu-id="1c27f-116">Settings for all backendPools</span></span>

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

### <span data-ttu-id="1c27f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c27f-117">-DefaultProfile</span></span>
<span data-ttu-id="1c27f-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1c27f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c27f-119">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="1c27f-119">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="1c27f-120">Szeretné-e letiltani a hitelesítő név jelölőnégyzetet HTTPS-kéréseken az összes backend-készletre.</span><span class="sxs-lookup"><span data-stu-id="1c27f-120">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="1c27f-121">Nincs hatással a nem HTTPS-kérésekre.</span><span class="sxs-lookup"><span data-stu-id="1c27f-121">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="1c27f-122">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="1c27f-122">-EnabledState</span></span>
<span data-ttu-id="1c27f-123">Az első ajtó EnabledState</span><span class="sxs-lookup"><span data-stu-id="1c27f-123">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="1c27f-124">Az alapértelmezett érték engedélyezve</span><span class="sxs-lookup"><span data-stu-id="1c27f-124">Default value is Enabled</span></span>

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

### <span data-ttu-id="1c27f-125">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c27f-125">-FrontendEndpoint</span></span>
<span data-ttu-id="1c27f-126">Az útválasztási szabályokhoz elérhető felületi végpontok.</span><span class="sxs-lookup"><span data-stu-id="1c27f-126">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="1c27f-127">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="1c27f-127">-HealthProbeSetting</span></span>
<span data-ttu-id="1c27f-128">A bejárati ajtóval társított állapot-szonda beállításai.</span><span class="sxs-lookup"><span data-stu-id="1c27f-128">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="1c27f-129">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="1c27f-129">-LoadBalancingSetting</span></span>
<span data-ttu-id="1c27f-130">A bejárati ajtóval társított terheléselosztási beállítások.</span><span class="sxs-lookup"><span data-stu-id="1c27f-130">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="1c27f-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1c27f-131">-Name</span></span>
<span data-ttu-id="1c27f-132">A bejárati ajtó neve.</span><span class="sxs-lookup"><span data-stu-id="1c27f-132">Front Door name.</span></span>

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

### <span data-ttu-id="1c27f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c27f-133">-ResourceGroupName</span></span>
<span data-ttu-id="1c27f-134">Az erőforráscsoport neve, amelybe az első ajtó jön létre.</span><span class="sxs-lookup"><span data-stu-id="1c27f-134">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="1c27f-135">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="1c27f-135">-RoutingRule</span></span>
<span data-ttu-id="1c27f-136">Az FrontDoor társított útválasztási szabályok</span><span class="sxs-lookup"><span data-stu-id="1c27f-136">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="1c27f-137">-Címke</span><span class="sxs-lookup"><span data-stu-id="1c27f-137">-Tag</span></span>
<span data-ttu-id="1c27f-138">A címkéket társítja a FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="1c27f-138">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="1c27f-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1c27f-139">-Confirm</span></span>
<span data-ttu-id="1c27f-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1c27f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c27f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c27f-141">-WhatIf</span></span>
<span data-ttu-id="1c27f-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1c27f-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c27f-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1c27f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c27f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c27f-144">CommonParameters</span></span>
<span data-ttu-id="1c27f-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1c27f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c27f-146">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1c27f-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c27f-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c27f-147">INPUTS</span></span>

### <span data-ttu-id="1c27f-148">Nincs</span><span class="sxs-lookup"><span data-stu-id="1c27f-148">None</span></span>
## <span data-ttu-id="1c27f-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c27f-149">OUTPUTS</span></span>

### <span data-ttu-id="1c27f-150">Microsoft. Azure. Command. FrontDoor. models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="1c27f-150">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
## <span data-ttu-id="1c27f-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1c27f-151">NOTES</span></span>

## <span data-ttu-id="1c27f-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1c27f-152">RELATED LINKS</span></span>

<span data-ttu-id="1c27f-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [Új – AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [Új – AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [Új – AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [Új – AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [Új – AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="1c27f-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>