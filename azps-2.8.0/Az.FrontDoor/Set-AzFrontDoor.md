---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/set-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
ms.openlocfilehash: 57f1bf57495e75167a1936799c24aff5e6387722
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666401"
---
# <span data-ttu-id="c8d8b-101">Set-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="c8d8b-101">Set-AzFrontDoor</span></span>

## <span data-ttu-id="c8d8b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c8d8b-102">SYNOPSIS</span></span>
<span data-ttu-id="c8d8b-103">Első ajtós terheléselosztás frissítése</span><span class="sxs-lookup"><span data-stu-id="c8d8b-103">Update a Front Door load balancer</span></span>

## <span data-ttu-id="c8d8b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c8d8b-104">SYNTAX</span></span>

### <span data-ttu-id="c8d8b-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c8d8b-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8d8b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8d8b-106">ByObjectParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c8d8b-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8d8b-107">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c8d8b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c8d8b-108">DESCRIPTION</span></span>
<span data-ttu-id="c8d8b-109">A **set-AzFrontDoor** parancsmag az első ajtós terheléselosztást frissíti.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-109">The **Set-AzFrontDoor** cmdlet updates a Front Door load balancer.</span></span> <span data-ttu-id="c8d8b-110">Ha nem adja meg a bemeneti paramétereket, a program a meglévő bejárati ajtótól származó régi paramétereket fogja használni.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-110">If input parameters are not provided, old parameters from the existing Front Door will be used.</span></span>

## <span data-ttu-id="c8d8b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c8d8b-111">EXAMPLES</span></span>

### <span data-ttu-id="c8d8b-112">Példa 1: a meglévő bejárati ajtó frissítése a FrontDoorName és a ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-112">Example 1: update an existing Front Door with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Set-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "resourceGroup1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

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
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="c8d8b-113">frissít egy meglévő FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-113">update an existing FrontDoor.</span></span>

### <span data-ttu-id="c8d8b-114">2. példa: meglévő bejárati ajtó frissítése a PSFrontDoor objektummal.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-114">Example 2: update an existing Front Door with PSFrontDoor object.</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

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
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoor1
```

<span data-ttu-id="c8d8b-115">frissít egy meglévő FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-115">update an existing FrontDoor.</span></span>

### <span data-ttu-id="c8d8b-116">3. példa: meglévő bejárati ajtó frissítése a ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8d8b-116">Example 3: update an existing Front Door with ResourceId</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -ResourceId {resourceId} -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

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
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoor1
```

<span data-ttu-id="c8d8b-117">frissít egy meglévő FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-117">update an existing FrontDoor.</span></span>

## <span data-ttu-id="c8d8b-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c8d8b-118">PARAMETERS</span></span>

### <span data-ttu-id="c8d8b-119">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="c8d8b-119">-BackendPool</span></span>
<span data-ttu-id="c8d8b-120">A Backendpools elérhető az útválasztási szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-120">Backendpools available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8d8b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8d8b-121">-DefaultProfile</span></span>
<span data-ttu-id="c8d8b-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8d8b-123">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="c8d8b-123">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="c8d8b-124">Szeretné-e letiltani a hitelesítő név jelölőnégyzetet HTTPS-kéréseken az összes backend-készletre.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-124">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="c8d8b-125">Nincs hatással a nem HTTPS-kérésekre.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-125">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="c8d8b-126">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="c8d8b-126">-EnabledState</span></span>
<span data-ttu-id="c8d8b-127">A bejárati ajtó kiegyenlítő működési állapota</span><span class="sxs-lookup"><span data-stu-id="c8d8b-127">Operational status of the Front Door load balancer.</span></span>

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

### <span data-ttu-id="c8d8b-128">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="c8d8b-128">-FrontendEndpoint</span></span>
<span data-ttu-id="c8d8b-129">Az útválasztási szabályokhoz elérhető felületi végpontok.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-129">Frontend endpoints available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8d8b-130">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="c8d8b-130">-HealthProbeSetting</span></span>
<span data-ttu-id="c8d8b-131">A bejárati ajtóval társított állapot-szonda beállításai.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-131">Health probe settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8d8b-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8d8b-132">-InputObject</span></span>
<span data-ttu-id="c8d8b-133">A frissíteni kívánt bejárati ajtó objektuma.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-133">The Front Door object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8d8b-134">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="c8d8b-134">-LoadBalancingSetting</span></span>
<span data-ttu-id="c8d8b-135">A bejárati ajtóval társított terheléselosztási beállítások.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-135">Load balancing settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8d8b-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c8d8b-136">-Name</span></span>
<span data-ttu-id="c8d8b-137">A frissítendő bejárati ajtó neve.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-137">The name of the Front Door to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8d8b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8d8b-138">-ResourceGroupName</span></span>
<span data-ttu-id="c8d8b-139">Az az erőforráscsoport, amelyhez az első ajtó tartozik.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-139">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8d8b-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8d8b-140">-ResourceId</span></span>
<span data-ttu-id="c8d8b-141">A frissítendő bejárati ajtó erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="c8d8b-141">Resource Id of the Front Door to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8d8b-142">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="c8d8b-142">-RoutingRule</span></span>
<span data-ttu-id="c8d8b-143">Az FrontDoor társított útválasztási szabályok</span><span class="sxs-lookup"><span data-stu-id="c8d8b-143">Routing rules associated with this FrontDoor</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8d8b-144">-Címke</span><span class="sxs-lookup"><span data-stu-id="c8d8b-144">-Tag</span></span>
<span data-ttu-id="c8d8b-145">A címkéket társítja a FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-145">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="c8d8b-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c8d8b-146">-Confirm</span></span>
<span data-ttu-id="c8d8b-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8d8b-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8d8b-148">-WhatIf</span></span>
<span data-ttu-id="c8d8b-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8d8b-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8d8b-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8d8b-151">CommonParameters</span></span>
<span data-ttu-id="c8d8b-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c8d8b-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8d8b-153">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c8d8b-153">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8d8b-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8d8b-154">INPUTS</span></span>

### <span data-ttu-id="c8d8b-155">Microsoft. Azure. Command. FrontDoor. models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="c8d8b-155">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="c8d8b-156">System. String</span><span class="sxs-lookup"><span data-stu-id="c8d8b-156">System.String</span></span>

## <span data-ttu-id="c8d8b-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8d8b-157">OUTPUTS</span></span>

### <span data-ttu-id="c8d8b-158">Microsoft. Azure. Command. FrontDoor. models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="c8d8b-158">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="c8d8b-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c8d8b-159">NOTES</span></span>

## <span data-ttu-id="c8d8b-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8d8b-160">RELATED LINKS</span></span>

<span data-ttu-id="c8d8b-161">[Új – AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [Új – AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [Új – AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [Új – AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [Új – AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [Új – AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="c8d8b-161">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>
