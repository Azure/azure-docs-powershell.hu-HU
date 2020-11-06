---
<span data-ttu-id="70799-101">külső súgófájl: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml modul neve: AzureRM. FrontDoor online verzió: a megfelelő URL-címnek a következőnek kell lennie: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoor Schema: 2.0.0 content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md</span><span class="sxs-lookup"><span data-stu-id="70799-101">external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml Module Name: AzureRM.FrontDoor online version: The corresponding URL should be the following: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoor schema: 2.0.0 content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md</span></span>
---

# <a name="new-azurermfrontdoor"></a><span data-ttu-id="70799-102">New-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="70799-102">New-AzureRmFrontDoor</span></span>

## <a name="synopsis"></a><span data-ttu-id="70799-103">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="70799-103">SYNOPSIS</span></span>
<span data-ttu-id="70799-104">Új Azure bejárati ajtó kiegyenlítő létrehozása</span><span class="sxs-lookup"><span data-stu-id="70799-104">Create a new Azure Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <a name="syntax"></a><span data-ttu-id="70799-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="70799-105">SYNTAX</span></span>

```
New-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <a name="description"></a><span data-ttu-id="70799-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="70799-106">DESCRIPTION</span></span>
<span data-ttu-id="70799-107">A **New-AzureRmFrontDoor** parancsmag új Azure betárcsázós betöltőt hoz létre a megadott erőforrás-csoportban a jelenlegi előfizetés csoportban.</span><span class="sxs-lookup"><span data-stu-id="70799-107">The **New-AzureRmFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <a name="examples"></a><span data-ttu-id="70799-108">Példák</span><span class="sxs-lookup"><span data-stu-id="70799-108">EXAMPLES</span></span>

### <a name="example-1-create-a-front-door-based-on-given-parameters"></a><span data-ttu-id="70799-109">Példa 1: bejárati ajtó létrehozása megadott paraméterek alapján.</span><span class="sxs-lookup"><span data-stu-id="70799-109">Example 1: Create a Front Door based on given parameters.</span></span>
```powershell
PS C:\> New-AzureRmFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

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
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="70799-110">Bejárati ajtót hozhat létre a megadott paraméterek alapján.</span><span class="sxs-lookup"><span data-stu-id="70799-110">Create a Front Door based on given parameters.</span></span>

## <a name="parameters"></a><span data-ttu-id="70799-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="70799-111">PARAMETERS</span></span>

### <a name="-backendpool"></a><span data-ttu-id="70799-112">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="70799-112">-BackendPool</span></span>
<span data-ttu-id="70799-113">A Backendpools elérhető az útválasztási szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="70799-113">Backendpools available to routing rule.</span></span>

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

### <a name="-defaultprofile"></a><span data-ttu-id="70799-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70799-114">-DefaultProfile</span></span>
<span data-ttu-id="70799-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="70799-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <a name="-enabledstate"></a><span data-ttu-id="70799-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="70799-116">-EnabledState</span></span>
<span data-ttu-id="70799-117">Az első ajtó EnabledState</span><span class="sxs-lookup"><span data-stu-id="70799-117">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="70799-118">Az alapértelmezett érték engedélyezve</span><span class="sxs-lookup"><span data-stu-id="70799-118">Default value is Enabled</span></span>

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

### <a name="-frontendendpoint"></a><span data-ttu-id="70799-119">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="70799-119">-FrontendEndpoint</span></span>
<span data-ttu-id="70799-120">Az útválasztási szabályokhoz elérhető felületi végpontok.</span><span class="sxs-lookup"><span data-stu-id="70799-120">Frontend endpoints available to routing rule.</span></span>

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

### <a name="-healthprobesetting"></a><span data-ttu-id="70799-121">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="70799-121">-HealthProbeSetting</span></span>
<span data-ttu-id="70799-122">A bejárati ajtóval társított állapot-szonda beállításai.</span><span class="sxs-lookup"><span data-stu-id="70799-122">Health probe settings associated with this Front Door instance.</span></span>

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

### <a name="-loadbalancingsetting"></a><span data-ttu-id="70799-123">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="70799-123">-LoadBalancingSetting</span></span>
<span data-ttu-id="70799-124">A bejárati ajtóval társított terheléselosztási beállítások.</span><span class="sxs-lookup"><span data-stu-id="70799-124">Load balancing settings associated with this Front Door instance.</span></span>

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

### <a name="-name"></a><span data-ttu-id="70799-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="70799-125">-Name</span></span>
<span data-ttu-id="70799-126">A bejárati ajtó neve.</span><span class="sxs-lookup"><span data-stu-id="70799-126">Front Door name.</span></span>

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

### <a name="-resourcegroupname"></a><span data-ttu-id="70799-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70799-127">-ResourceGroupName</span></span>
<span data-ttu-id="70799-128">Az erőforráscsoport neve, amelybe az első ajtó jön létre.</span><span class="sxs-lookup"><span data-stu-id="70799-128">The resource group name that the Front Door will be created in.</span></span>

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

### <a name="-routingrule"></a><span data-ttu-id="70799-129">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="70799-129">-RoutingRule</span></span>
<span data-ttu-id="70799-130">Az FrontDoor társított útválasztási szabályok</span><span class="sxs-lookup"><span data-stu-id="70799-130">Routing rules associated with this FrontDoor</span></span>

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

### <a name="-tag"></a><span data-ttu-id="70799-131">-Címke</span><span class="sxs-lookup"><span data-stu-id="70799-131">-Tag</span></span>
<span data-ttu-id="70799-132">A címkéket társítja a FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="70799-132">The tags associate with the FrontDoor.</span></span>

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

### <a name="-confirm"></a><span data-ttu-id="70799-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="70799-133">-Confirm</span></span>
<span data-ttu-id="70799-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="70799-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <a name="-whatif"></a><span data-ttu-id="70799-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70799-135">-WhatIf</span></span>
<span data-ttu-id="70799-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="70799-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70799-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="70799-137">The cmdlet is not run.</span></span>

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

### <a name="commonparameters"></a><span data-ttu-id="70799-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70799-138">CommonParameters</span></span>
<span data-ttu-id="70799-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="70799-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70799-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70799-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <a name="inputs"></a><span data-ttu-id="70799-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="70799-141">INPUTS</span></span>

### <a name="systemstring"></a><span data-ttu-id="70799-142">System. String</span><span class="sxs-lookup"><span data-stu-id="70799-142">System.String</span></span>

## <a name="outputs"></a><span data-ttu-id="70799-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70799-143">OUTPUTS</span></span>

### <a name="microsoftazurecommandsfrontdoormodelspsfrontdoor"></a><span data-ttu-id="70799-144">Microsoft. Azure. Command. FrontDoor. models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="70799-144">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <a name="notes"></a><span data-ttu-id="70799-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="70799-145">NOTES</span></span>

## <a name="related-links"></a><span data-ttu-id="70799-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70799-146">RELATED LINKS</span></span>

<span data-ttu-id="70799-147">[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md) 
 [Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md) 
 [Új – AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md) 
 [Új – AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md) 
 [Új – AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md) 
 [Új – AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md) 
 [Új – AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="70799-147">[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)
[Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)
[New-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md)
[New-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md)
[New-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md)
[New-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md)
[New-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span></span>
