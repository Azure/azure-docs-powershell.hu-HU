---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
ms.openlocfilehash: b6537b9b8501aa2ec0aa76c9ede080893bf136ee
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195090"
---
# <span data-ttu-id="80982-101">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="80982-101">Get-AzVpnGateway</span></span>

## <span data-ttu-id="80982-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="80982-102">SYNOPSIS</span></span>
<span data-ttu-id="80982-103">A ResourceGroupName és a GatewayName segítségével kap egy VpnGateway-erőforrást, vagy felsorolja az összes átjárót a ResourceGroupName vagy a SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="80982-103">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="80982-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="80982-104">SYNTAX</span></span>

### <span data-ttu-id="80982-105">ListBySubscriptionId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="80982-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80982-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80982-106">ListByResourceGroupName</span></span>
```
Get-AzVpnGateway [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="80982-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="80982-107">DESCRIPTION</span></span>
<span data-ttu-id="80982-108">A ResourceGroupName és a GatewayName segítségével kap egy VpnGateway-erőforrást, vagy felsorolja az összes átjárót a ResourceGroupName vagy a SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="80982-108">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="80982-109">Példák</span><span class="sxs-lookup"><span data-stu-id="80982-109">EXAMPLES</span></span>

### <span data-ttu-id="80982-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="80982-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
IpConfigurations    : {Instance0, Instance1}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="80982-111">A fenti létrehoz egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub a Nyugat-amerikai "testRG" erőforráscsoport az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="80982-111">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="80982-112">Ezt követően egy VPN-átjáró jön létre a virtuális központban, 2 léptékű egységgel.</span><span class="sxs-lookup"><span data-stu-id="80982-112">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="80982-113">Ezt követően a VpnGateway a resourceGroupName és az átjáró nevével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="80982-113">It then gets the VpnGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="80982-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="80982-114">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnGateway -Name test*

ResourceGroupName   : testRG
Name                : test1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/test1
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
IpConfigurations    : {Instance0, Instance1}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded

ResourceGroupName   : testRG
Name                : test2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/test2
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
IpConfigurations    : {Instance0, Instance1}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="80982-115">Ez a parancsmag a "teszt" kezdetű összes átjárót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="80982-115">This cmdlet gets all Gateways that start with "test".</span></span>

## <span data-ttu-id="80982-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="80982-116">PARAMETERS</span></span>

### <span data-ttu-id="80982-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80982-117">-DefaultProfile</span></span>
<span data-ttu-id="80982-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="80982-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80982-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="80982-119">-Name</span></span>
<span data-ttu-id="80982-120">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="80982-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="80982-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80982-121">-ResourceGroupName</span></span>
<span data-ttu-id="80982-122">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="80982-122">The resource group name.</span></span>

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

### <span data-ttu-id="80982-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80982-123">CommonParameters</span></span>
<span data-ttu-id="80982-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="80982-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80982-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="80982-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80982-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="80982-126">INPUTS</span></span>

### <span data-ttu-id="80982-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="80982-127">None</span></span>

## <span data-ttu-id="80982-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="80982-128">OUTPUTS</span></span>

### <span data-ttu-id="80982-129">Microsoft. Azure. commands. Network. models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="80982-129">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="80982-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="80982-130">NOTES</span></span>

## <span data-ttu-id="80982-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="80982-131">RELATED LINKS</span></span>

[<span data-ttu-id="80982-132">Új – AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="80982-132">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="80982-133">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="80982-133">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="80982-134">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="80982-134">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
