---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
ms.openlocfilehash: cea5b69b279b6f7f7a8e783d4ed328237377c18f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666428"
---
# <span data-ttu-id="b467a-101">New-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="b467a-101">New-AzFrontDoor</span></span>

## <span data-ttu-id="b467a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b467a-102">SYNOPSIS</span></span>
<span data-ttu-id="b467a-103">Új Azure bejárati ajtó kiegyenlítő létrehozása</span><span class="sxs-lookup"><span data-stu-id="b467a-103">Create a new Azure Front Door load balancer</span></span>

## <span data-ttu-id="b467a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b467a-104">SYNTAX</span></span>

```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b467a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b467a-105">DESCRIPTION</span></span>
<span data-ttu-id="b467a-106">A **New-AzFrontDoor** parancsmag új Azure betárcsázós betöltőt hoz létre a megadott erőforrás-csoportban a jelenlegi előfizetés csoportban.</span><span class="sxs-lookup"><span data-stu-id="b467a-106">The **New-AzFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <span data-ttu-id="b467a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b467a-107">EXAMPLES</span></span>

### <span data-ttu-id="b467a-108">Példa 1: bejárati ajtó létrehozása megadott paraméterek alapján.</span><span class="sxs-lookup"><span data-stu-id="b467a-108">Example 1: Create a Front Door based on given parameters.</span></span>
```powershell
PS C:\> New-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
EnforceCertificateNameCheck : Enabled
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

<span data-ttu-id="b467a-109">Bejárati ajtót hozhat létre a megadott paraméterek alapján.</span><span class="sxs-lookup"><span data-stu-id="b467a-109">Create a Front Door based on given parameters.</span></span>

## <span data-ttu-id="b467a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b467a-110">PARAMETERS</span></span>

### <span data-ttu-id="b467a-111">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="b467a-111">-BackendPool</span></span>
<span data-ttu-id="b467a-112">A Backendpools elérhető az útválasztási szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="b467a-112">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="b467a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b467a-113">-DefaultProfile</span></span>
<span data-ttu-id="b467a-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b467a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b467a-115">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="b467a-115">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="b467a-116">Szeretné-e letiltani a hitelesítő név jelölőnégyzetet HTTPS-kéréseken az összes backend-készletre.</span><span class="sxs-lookup"><span data-stu-id="b467a-116">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="b467a-117">Nincs hatással a nem HTTPS-kérésekre.</span><span class="sxs-lookup"><span data-stu-id="b467a-117">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="b467a-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="b467a-118">-EnabledState</span></span>
<span data-ttu-id="b467a-119">Az első ajtó EnabledState</span><span class="sxs-lookup"><span data-stu-id="b467a-119">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="b467a-120">Az alapértelmezett érték engedélyezve</span><span class="sxs-lookup"><span data-stu-id="b467a-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="b467a-121">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="b467a-121">-FrontendEndpoint</span></span>
<span data-ttu-id="b467a-122">Az útválasztási szabályokhoz elérhető felületi végpontok.</span><span class="sxs-lookup"><span data-stu-id="b467a-122">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="b467a-123">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="b467a-123">-HealthProbeSetting</span></span>
<span data-ttu-id="b467a-124">A bejárati ajtóval társított állapot-szonda beállításai.</span><span class="sxs-lookup"><span data-stu-id="b467a-124">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="b467a-125">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="b467a-125">-LoadBalancingSetting</span></span>
<span data-ttu-id="b467a-126">A bejárati ajtóval társított terheléselosztási beállítások.</span><span class="sxs-lookup"><span data-stu-id="b467a-126">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="b467a-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b467a-127">-Name</span></span>
<span data-ttu-id="b467a-128">A bejárati ajtó neve.</span><span class="sxs-lookup"><span data-stu-id="b467a-128">Front Door name.</span></span>

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

### <span data-ttu-id="b467a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b467a-129">-ResourceGroupName</span></span>
<span data-ttu-id="b467a-130">Az erőforráscsoport neve, amelybe az első ajtó jön létre.</span><span class="sxs-lookup"><span data-stu-id="b467a-130">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="b467a-131">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="b467a-131">-RoutingRule</span></span>
<span data-ttu-id="b467a-132">Az FrontDoor társított útválasztási szabályok</span><span class="sxs-lookup"><span data-stu-id="b467a-132">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="b467a-133">-Címke</span><span class="sxs-lookup"><span data-stu-id="b467a-133">-Tag</span></span>
<span data-ttu-id="b467a-134">A címkéket társítja a FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="b467a-134">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="b467a-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b467a-135">-Confirm</span></span>
<span data-ttu-id="b467a-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b467a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b467a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b467a-137">-WhatIf</span></span>
<span data-ttu-id="b467a-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b467a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b467a-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b467a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b467a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b467a-140">CommonParameters</span></span>
<span data-ttu-id="b467a-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b467a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b467a-142">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b467a-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b467a-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b467a-143">INPUTS</span></span>

### <span data-ttu-id="b467a-144">Nincs</span><span class="sxs-lookup"><span data-stu-id="b467a-144">None</span></span>

## <span data-ttu-id="b467a-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b467a-145">OUTPUTS</span></span>

### <span data-ttu-id="b467a-146">Microsoft. Azure. Command. FrontDoor. models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="b467a-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="b467a-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b467a-147">NOTES</span></span>

## <span data-ttu-id="b467a-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b467a-148">RELATED LINKS</span></span>

<span data-ttu-id="b467a-149">[Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [Új – AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [Új – AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [Új – AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [Új – AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [Új – AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="b467a-149">[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>