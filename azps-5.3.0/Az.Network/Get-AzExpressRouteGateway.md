---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
ms.openlocfilehash: 597b6fcff647b1b2032f0a1ac5d11961b9d1e959
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469314"
---
# <span data-ttu-id="b96ea-101">Get-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="b96ea-101">Get-AzExpressRouteGateway</span></span>

## <span data-ttu-id="b96ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b96ea-102">SYNOPSIS</span></span>
<span data-ttu-id="b96ea-103">ExpressRouteGateway-erőforrást kap a ResourceGroupName és a GatewayName OR használatával, és felsorolja az összes átjárót a ResourceGroupName vagy az SubscriptionId szerint.</span><span class="sxs-lookup"><span data-stu-id="b96ea-103">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="b96ea-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b96ea-104">SYNTAX</span></span>

### <span data-ttu-id="b96ea-105">ListBySubscriptionId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b96ea-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzExpressRouteGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b96ea-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b96ea-106">ListByResourceGroupName</span></span>
```
Get-AzExpressRouteGateway [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b96ea-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="b96ea-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b96ea-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b96ea-108">DESCRIPTION</span></span>
<span data-ttu-id="b96ea-109">ExpressRouteGateway-erőforrást kap a ResourceGroupName és a GatewayName OR használatával, és felsorolja az összes átjárót a ResourceGroupName vagy az SubscriptionId szerint.</span><span class="sxs-lookup"><span data-stu-id="b96ea-109">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="b96ea-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b96ea-110">EXAMPLES</span></span>

### <span data-ttu-id="b96ea-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="b96ea-111">Example 1</span></span>

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

<span data-ttu-id="b96ea-112">A fenti létrehoz egy erőforráscsoportot (Virtual WAN, Virtual Network, Virtual Hub in West Central US, Virtual Hub in West Central US in "testRG" resource group in Azure.</span><span class="sxs-lookup"><span data-stu-id="b96ea-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="b96ea-113">Ezután létrejön egy ExpressRoute-átjáró a virtuális központban 2 méretarányú egységben.</span><span class="sxs-lookup"><span data-stu-id="b96ea-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="b96ea-114">Ezt követően az ExpressRouteGateway az erőforrásCsoportneve és az átjáró neve segítségével jut hozzá.</span><span class="sxs-lookup"><span data-stu-id="b96ea-114">It then gets the ExpressRouteGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="b96ea-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="b96ea-115">Example 2</span></span>

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

<span data-ttu-id="b96ea-116">Ez a parancs az összes Olyan ExpressRouteGatewayt beszerzi, amely a "teszt" kifejezéssel kezdődik</span><span class="sxs-lookup"><span data-stu-id="b96ea-116">This command will get all ExpressRouteGateways that start with "test"</span></span>

## <span data-ttu-id="b96ea-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b96ea-117">PARAMETERS</span></span>

### <span data-ttu-id="b96ea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b96ea-118">-DefaultProfile</span></span>
<span data-ttu-id="b96ea-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b96ea-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b96ea-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b96ea-120">-Name</span></span>
<span data-ttu-id="b96ea-121">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="b96ea-121">The resource name.</span></span>

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

### <span data-ttu-id="b96ea-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b96ea-122">-ResourceGroupName</span></span>
<span data-ttu-id="b96ea-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b96ea-123">The resource group name.</span></span>

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

### <span data-ttu-id="b96ea-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b96ea-124">-ResourceId</span></span>
<span data-ttu-id="b96ea-125">Az expressRouteGateway törölt Azure-erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="b96ea-125">The Azure resource ID for the expressRouteGateway to be deleted.</span></span>

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

### <span data-ttu-id="b96ea-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b96ea-126">CommonParameters</span></span>
<span data-ttu-id="b96ea-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b96ea-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b96ea-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b96ea-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b96ea-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b96ea-129">INPUTS</span></span>

### <span data-ttu-id="b96ea-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b96ea-130">System.String</span></span>

## <span data-ttu-id="b96ea-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b96ea-131">OUTPUTS</span></span>

### <span data-ttu-id="b96ea-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="b96ea-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="b96ea-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b96ea-133">NOTES</span></span>

## <span data-ttu-id="b96ea-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b96ea-134">RELATED LINKS</span></span>
