---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnGateway.md
ms.openlocfilehash: f1e7b829856558f438793a921154aa3f04666ff8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495056"
---
# <span data-ttu-id="c7a44-101">Get-AzureRmVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c7a44-101">Get-AzureRmVpnGateway</span></span>

## <span data-ttu-id="c7a44-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c7a44-102">SYNOPSIS</span></span>
<span data-ttu-id="c7a44-103">A ResourceGroupName és a GatewayName segítségével kap egy VpnGateway-erőforrást, vagy felsorolja az összes átjárót a ResourceGroupName vagy a SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="c7a44-103">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7a44-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c7a44-104">SYNTAX</span></span>

### <span data-ttu-id="c7a44-105">ListBySubscriptionId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c7a44-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7a44-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7a44-106">ListByResourceGroupName</span></span>
```
Get-AzureRmVpnGateway -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7a44-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c7a44-107">DESCRIPTION</span></span>
<span data-ttu-id="c7a44-108">A ResourceGroupName és a GatewayName segítségével kap egy VpnGateway-erőforrást, vagy felsorolja az összes átjárót a ResourceGroupName vagy a SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="c7a44-108">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="c7a44-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c7a44-109">EXAMPLES</span></span>

### <span data-ttu-id="c7a44-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c7a44-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="c7a44-111">A fenti létrehoz egy erőforráscsoport, virtuális WAN, virtuális hálózat, virtuális hub a Nyugat-amerikai "testRG" erőforráscsoport az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="c7a44-111">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="c7a44-112">Ezt követően egy VPN-átjáró jön létre a virtuális központban, 2 léptékű egységgel.</span><span class="sxs-lookup"><span data-stu-id="c7a44-112">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="c7a44-113">Ezt követően a VpnGateway a resourceGroupName és az átjáró nevével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c7a44-113">It then gets the VpnGateway using its resourceGroupName and the gateway name.</span></span>

## <span data-ttu-id="c7a44-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c7a44-114">PARAMETERS</span></span>

### <span data-ttu-id="c7a44-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7a44-115">-DefaultProfile</span></span>
<span data-ttu-id="c7a44-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c7a44-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7a44-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c7a44-117">-Name</span></span>
<span data-ttu-id="c7a44-118">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="c7a44-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7a44-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7a44-119">-ResourceGroupName</span></span>
<span data-ttu-id="c7a44-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="c7a44-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7a44-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7a44-121">CommonParameters</span></span>
<span data-ttu-id="c7a44-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c7a44-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7a44-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7a44-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7a44-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7a44-124">INPUTS</span></span>

### <span data-ttu-id="c7a44-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c7a44-125">System.String</span></span>

## <span data-ttu-id="c7a44-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7a44-126">OUTPUTS</span></span>

### <span data-ttu-id="c7a44-127">Microsoft. Azure. commands. Network. models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c7a44-127">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="c7a44-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c7a44-128">NOTES</span></span>

## <span data-ttu-id="c7a44-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7a44-129">RELATED LINKS</span></span>
