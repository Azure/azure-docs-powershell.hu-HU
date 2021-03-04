---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
ms.openlocfilehash: f3a5b61561b0886af32aa13103f3234098c76357
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931177"
---
# <span data-ttu-id="c0890-101">New-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="c0890-101">New-AzFrontDoor</span></span>

## <span data-ttu-id="c0890-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0890-102">SYNOPSIS</span></span>
<span data-ttu-id="c0890-103">Új Azure Front Door terheléselosztási rendszer létrehozása</span><span class="sxs-lookup"><span data-stu-id="c0890-103">Create a new Azure Front Door load balancer</span></span>

## <span data-ttu-id="c0890-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c0890-104">SYNTAX</span></span>

### <span data-ttu-id="c0890-105">ByFieldsWithBackendPoolsSettingParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c0890-105">ByFieldsWithBackendPoolsSettingParameterSet (Default)</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-BackendPoolsSetting <PSBackendPoolsSetting>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0890-106">ByFieldsWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0890-106">ByFieldsWithCertificateNameCheckParameterSet</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0890-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c0890-107">DESCRIPTION</span></span>
<span data-ttu-id="c0890-108">A **New-AzFrontDoor** parancsmag létrehoz egy új Azure Front Door terheléselegyenlőt a megadott erőforráscsoportban az aktuális előfizetés alatt</span><span class="sxs-lookup"><span data-stu-id="c0890-108">The **New-AzFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <span data-ttu-id="c0890-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c0890-109">EXAMPLES</span></span>

### <span data-ttu-id="c0890-110">1. példa: A megadott paraméterek alapján hozzon létre front door-t.</span><span class="sxs-lookup"><span data-stu-id="c0890-110">Example 1: Create a Front Door based on given parameters.</span></span>
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

<span data-ttu-id="c0890-111">Hozzon létre egy előtéti adát a megadott paraméterek alapján.</span><span class="sxs-lookup"><span data-stu-id="c0890-111">Create a Front Door based on given parameters.</span></span>

## <span data-ttu-id="c0890-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0890-112">PARAMETERS</span></span>

### <span data-ttu-id="c0890-113">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="c0890-113">-BackendPool</span></span>
<span data-ttu-id="c0890-114">Az útválasztási szabályhoz rendelkezésre álló backendpools.</span><span class="sxs-lookup"><span data-stu-id="c0890-114">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="c0890-115">-BackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="c0890-115">-BackendPoolsSetting</span></span>
<span data-ttu-id="c0890-116">Az összes backendPools beállításai</span><span class="sxs-lookup"><span data-stu-id="c0890-116">Settings for all backendPools</span></span>

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

### <span data-ttu-id="c0890-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0890-117">-DefaultProfile</span></span>
<span data-ttu-id="c0890-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c0890-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0890-119">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="c0890-119">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="c0890-120">Letiltja-e a tanúsítványnév-ellenőrzést a HTTPS-kérelmekben az összes háttérkészletben.</span><span class="sxs-lookup"><span data-stu-id="c0890-120">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="c0890-121">Nincs hatása a nem HTTPS-ről való kérelmekre.</span><span class="sxs-lookup"><span data-stu-id="c0890-121">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="c0890-122">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="c0890-122">-EnabledState</span></span>
<span data-ttu-id="c0890-123">A Front Door terheléselosztási eszköz EnabledState szolgáltatása.</span><span class="sxs-lookup"><span data-stu-id="c0890-123">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="c0890-124">Az alapértelmezett érték engedélyezve van</span><span class="sxs-lookup"><span data-stu-id="c0890-124">Default value is Enabled</span></span>

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

### <span data-ttu-id="c0890-125">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0890-125">-FrontendEndpoint</span></span>
<span data-ttu-id="c0890-126">Útválasztási szabályhoz elérhető előlapi végpontok.</span><span class="sxs-lookup"><span data-stu-id="c0890-126">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="c0890-127">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="c0890-127">-HealthProbeSetting</span></span>
<span data-ttu-id="c0890-128">Az ehhez a Front Door-példányhoz társított állapotbeállítások.</span><span class="sxs-lookup"><span data-stu-id="c0890-128">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="c0890-129">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="c0890-129">-LoadBalancingSetting</span></span>
<span data-ttu-id="c0890-130">Az ehhez a Front Door-példányhoz társított terheléselosztási beállítások.</span><span class="sxs-lookup"><span data-stu-id="c0890-130">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="c0890-131">-Name</span><span class="sxs-lookup"><span data-stu-id="c0890-131">-Name</span></span>
<span data-ttu-id="c0890-132">Front Door name.</span><span class="sxs-lookup"><span data-stu-id="c0890-132">Front Door name.</span></span>

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

### <span data-ttu-id="c0890-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0890-133">-ResourceGroupName</span></span>
<span data-ttu-id="c0890-134">Az erőforráscsoport neve, amelyből a front door lesz létrehozva.</span><span class="sxs-lookup"><span data-stu-id="c0890-134">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="c0890-135">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="c0890-135">-RoutingRule</span></span>
<span data-ttu-id="c0890-136">Routing rules associated with this FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c0890-136">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="c0890-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="c0890-137">-Tag</span></span>
<span data-ttu-id="c0890-138">A Címkék a FrontDoor címkével vannak társítva.</span><span class="sxs-lookup"><span data-stu-id="c0890-138">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="c0890-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0890-139">-Confirm</span></span>
<span data-ttu-id="c0890-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c0890-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0890-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0890-141">-WhatIf</span></span>
<span data-ttu-id="c0890-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c0890-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0890-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c0890-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0890-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0890-144">CommonParameters</span></span>
<span data-ttu-id="c0890-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0890-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0890-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0890-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0890-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c0890-147">INPUTS</span></span>

### <span data-ttu-id="c0890-148">Nincs</span><span class="sxs-lookup"><span data-stu-id="c0890-148">None</span></span>
## <span data-ttu-id="c0890-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0890-149">OUTPUTS</span></span>

### <span data-ttu-id="c0890-150">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="c0890-150">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
## <span data-ttu-id="c0890-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c0890-151">NOTES</span></span>

## <span data-ttu-id="c0890-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0890-152">RELATED LINKS</span></span>

<span data-ttu-id="c0890-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="c0890-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>