---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/set-azurermfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoor.md
ms.openlocfilehash: 250fa8a5638e1aa9d67d212fd45352c7756d2aef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491917"
---
# <span data-ttu-id="ca306-101">Set-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="ca306-101">Set-AzureRmFrontDoor</span></span>

## <span data-ttu-id="ca306-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ca306-102">SYNOPSIS</span></span>
<span data-ttu-id="ca306-103">Első ajtós terheléselosztás frissítése</span><span class="sxs-lookup"><span data-stu-id="ca306-103">Update a Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca306-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ca306-104">SYNTAX</span></span>

### <span data-ttu-id="ca306-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ca306-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca306-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca306-106">ByObjectParameterSet</span></span>
```
Set-AzureRmFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca306-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca306-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca306-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ca306-108">DESCRIPTION</span></span>
<span data-ttu-id="ca306-109">A **set-AzureRmFrontDoor** parancsmag az első ajtós terheléselosztást frissíti.</span><span class="sxs-lookup"><span data-stu-id="ca306-109">The **Set-AzureRmFrontDoor** cmdlet updates a Front Door load balancer.</span></span> <span data-ttu-id="ca306-110">Ha nem adja meg a bemeneti paramétereket, a program a meglévő bejárati ajtótól származó régi paramétereket fogja használni.</span><span class="sxs-lookup"><span data-stu-id="ca306-110">If input parameters are not provided, old parameters from the existing Front Door will be used.</span></span>

## <span data-ttu-id="ca306-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ca306-111">EXAMPLES</span></span>

### <span data-ttu-id="ca306-112">Példa 1: a meglévő bejárati ajtó frissítése a FrontDoorName és a ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="ca306-112">Example 1: update an existing Front Door with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoor -Name "frontDoor1" -ResourceGroupName "resourceGroup1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="ca306-113">frissít egy meglévő FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="ca306-113">update an existing FrontDoor.</span></span>

### <span data-ttu-id="ca306-114">2. példa: meglévő bejárati ajtó frissítése a PSFrontDoor objektummal.</span><span class="sxs-lookup"><span data-stu-id="ca306-114">Example 2: update an existing Front Door with PSFrontDoor object.</span></span>
```powershell
PS C:\>  Set-AzureRmFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="ca306-115">frissít egy meglévő FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="ca306-115">update an existing FrontDoor.</span></span>

### <span data-ttu-id="ca306-116">3. példa: meglévő bejárati ajtó frissítése a ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca306-116">Example 3: update an existing Front Door with ResourceId</span></span>
```powershell
PS C:\>  Set-AzureRmFrontDoor -ResourceId {resourceId} -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="ca306-117">frissít egy meglévő FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="ca306-117">update an existing FrontDoor.</span></span>

## <span data-ttu-id="ca306-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ca306-118">PARAMETERS</span></span>

### <span data-ttu-id="ca306-119">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="ca306-119">-BackendPool</span></span>
<span data-ttu-id="ca306-120">A Backendpools elérhető az útválasztási szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="ca306-120">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="ca306-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca306-121">-DefaultProfile</span></span>
<span data-ttu-id="ca306-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ca306-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca306-123">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="ca306-123">-EnabledState</span></span>
<span data-ttu-id="ca306-124">A bejárati ajtó kiegyenlítő működési állapota</span><span class="sxs-lookup"><span data-stu-id="ca306-124">Operational status of the Front Door load balancer.</span></span>

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

### <span data-ttu-id="ca306-125">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="ca306-125">-FrontendEndpoint</span></span>
<span data-ttu-id="ca306-126">Az útválasztási szabályokhoz elérhető felületi végpontok.</span><span class="sxs-lookup"><span data-stu-id="ca306-126">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="ca306-127">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="ca306-127">-HealthProbeSetting</span></span>
<span data-ttu-id="ca306-128">A bejárati ajtóval társított állapot-szonda beállításai.</span><span class="sxs-lookup"><span data-stu-id="ca306-128">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="ca306-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca306-129">-InputObject</span></span>
<span data-ttu-id="ca306-130">A frissíteni kívánt bejárati ajtó objektuma.</span><span class="sxs-lookup"><span data-stu-id="ca306-130">The Front Door object to update.</span></span>

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

### <span data-ttu-id="ca306-131">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="ca306-131">-LoadBalancingSetting</span></span>
<span data-ttu-id="ca306-132">A bejárati ajtóval társított terheléselosztási beállítások.</span><span class="sxs-lookup"><span data-stu-id="ca306-132">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="ca306-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ca306-133">-Name</span></span>
<span data-ttu-id="ca306-134">A frissítendő bejárati ajtó neve.</span><span class="sxs-lookup"><span data-stu-id="ca306-134">The name of the Front Door to update.</span></span>

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

### <span data-ttu-id="ca306-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca306-135">-ResourceGroupName</span></span>
<span data-ttu-id="ca306-136">Az az erőforráscsoport, amelyhez az első ajtó tartozik.</span><span class="sxs-lookup"><span data-stu-id="ca306-136">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="ca306-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca306-137">-ResourceId</span></span>
<span data-ttu-id="ca306-138">A frissítendő bejárati ajtó erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="ca306-138">Resource Id of the Front Door to update</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca306-139">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="ca306-139">-RoutingRule</span></span>
<span data-ttu-id="ca306-140">Az FrontDoor társított útválasztási szabályok</span><span class="sxs-lookup"><span data-stu-id="ca306-140">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="ca306-141">-Címke</span><span class="sxs-lookup"><span data-stu-id="ca306-141">-Tag</span></span>
<span data-ttu-id="ca306-142">A címkéket társítja a FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="ca306-142">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="ca306-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ca306-143">-Confirm</span></span>
<span data-ttu-id="ca306-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ca306-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca306-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca306-145">-WhatIf</span></span>
<span data-ttu-id="ca306-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ca306-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca306-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ca306-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca306-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca306-148">CommonParameters</span></span>
<span data-ttu-id="ca306-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ca306-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca306-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca306-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca306-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca306-151">INPUTS</span></span>

### <span data-ttu-id="ca306-152">Microsoft. Azure. Command. FrontDoor. models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="ca306-152">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="ca306-153">System. String</span><span class="sxs-lookup"><span data-stu-id="ca306-153">System.String</span></span>

## <span data-ttu-id="ca306-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca306-154">OUTPUTS</span></span>

### <span data-ttu-id="ca306-155">Microsoft. Azure. Command. FrontDoor. models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="ca306-155">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="ca306-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ca306-156">NOTES</span></span>

## <span data-ttu-id="ca306-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca306-157">RELATED LINKS</span></span>

<span data-ttu-id="ca306-158">[Új – AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md) 
 [Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md) 
 [Új – AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md) 
 [Új – AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md) 
 [Új – AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md) 
 [Új – AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md) 
 [Új – AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="ca306-158">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)
[Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)
[New-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md)
[New-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md)
[New-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md)
[New-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md)
[New-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span></span>
