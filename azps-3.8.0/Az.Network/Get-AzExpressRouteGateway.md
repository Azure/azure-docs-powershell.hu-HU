---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
ms.openlocfilehash: 597b6fcff647b1b2032f0a1ac5d11961b9d1e959
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013360"
---
# <span data-ttu-id="1242b-101">Get-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="1242b-101">Get-AzExpressRouteGateway</span></span>

## <span data-ttu-id="1242b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1242b-102">SYNOPSIS</span></span>
<span data-ttu-id="1242b-103">A ResourceGroupName és a GatewayName segítségével kap egy ExpressRouteGateway-erőforrást, vagy felsorolja az összes átjárót a ResourceGroupName vagy a SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="1242b-103">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="1242b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1242b-104">SYNTAX</span></span>

### <span data-ttu-id="1242b-105">ListBySubscriptionId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1242b-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzExpressRouteGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1242b-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1242b-106">ListByResourceGroupName</span></span>
```
Get-AzExpressRouteGateway [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1242b-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="1242b-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1242b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1242b-108">DESCRIPTION</span></span>
<span data-ttu-id="1242b-109">A ResourceGroupName és a GatewayName segítségével kap egy ExpressRouteGateway-erőforrást, vagy felsorolja az összes átjárót a ResourceGroupName vagy a SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="1242b-109">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="1242b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1242b-110">EXAMPLES</span></span>

### <span data-ttu-id="1242b-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1242b-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"

ResourceGroupName   : testRG
Name                : testExpressRoutegw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="1242b-112">A fenti létrehoz egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub a Nyugat-középen amerikai "testRG" erőforráscsoport az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="1242b-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="1242b-113">Ezt követően egy ExpressRoute átjáró jön létre a virtuális központban, 2 léptékű egységgel.</span><span class="sxs-lookup"><span data-stu-id="1242b-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="1242b-114">Ezt követően a ExpressRouteGateway a resourceGroupName és az átjáró nevével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1242b-114">It then gets the ExpressRouteGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="1242b-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="1242b-115">Example 2</span></span>

```powershell
PS C:\> Get-AzExpressRouteGateway -Name test*

ResourceGroupName   : testRG
Name                : testExpressRoutegw1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw1
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded

ResourceGroupName   : testRG
Name                : testExpressRoutegw2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw2
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="1242b-116">Ez a parancs a "teszt" kezdetű összes ExpressRouteGateways fogja kapni</span><span class="sxs-lookup"><span data-stu-id="1242b-116">This command will get all ExpressRouteGateways that start with "test"</span></span>

## <span data-ttu-id="1242b-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1242b-117">PARAMETERS</span></span>

### <span data-ttu-id="1242b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1242b-118">-DefaultProfile</span></span>
<span data-ttu-id="1242b-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1242b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1242b-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1242b-120">-Name</span></span>
<span data-ttu-id="1242b-121">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="1242b-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, ExpressRouteGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="1242b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1242b-122">-ResourceGroupName</span></span>
<span data-ttu-id="1242b-123">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="1242b-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="1242b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1242b-124">-ResourceId</span></span>
<span data-ttu-id="1242b-125">A törlendő expressRouteGateway Azure Resource AZONOSÍTÓja.</span><span class="sxs-lookup"><span data-stu-id="1242b-125">The Azure resource ID for the expressRouteGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: expressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1242b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1242b-126">CommonParameters</span></span>
<span data-ttu-id="1242b-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1242b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1242b-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1242b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1242b-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1242b-129">INPUTS</span></span>

### <span data-ttu-id="1242b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1242b-130">System.String</span></span>

## <span data-ttu-id="1242b-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1242b-131">OUTPUTS</span></span>

### <span data-ttu-id="1242b-132">Microsoft. Azure. commands. Network. models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="1242b-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="1242b-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1242b-133">NOTES</span></span>

## <span data-ttu-id="1242b-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1242b-134">RELATED LINKS</span></span>
