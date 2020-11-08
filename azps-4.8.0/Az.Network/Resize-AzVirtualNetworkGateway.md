---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: dd48af6a0f20cafea5911adb629a83323faa94a6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184792"
---
# <span data-ttu-id="fd57f-101">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fd57f-101">Resize-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="fd57f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fd57f-102">SYNOPSIS</span></span>
<span data-ttu-id="fd57f-103">Egy meglévő virtuális hálózati átjáró átméretezése.</span><span class="sxs-lookup"><span data-stu-id="fd57f-103">Resizes an existing virtual network gateway.</span></span>

## <span data-ttu-id="fd57f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fd57f-104">SYNTAX</span></span>

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd57f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fd57f-105">DESCRIPTION</span></span>
<span data-ttu-id="fd57f-106">Az **átméretezés-AzVirtualNetworkGateway** parancsmag lehetővé teszi a virtuális hálózati átjáró készletezési egységének (SKU) módosítását.</span><span class="sxs-lookup"><span data-stu-id="fd57f-106">The **Resize-AzVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="fd57f-107">A SKU határozza meg az átjáró funkcióit, így például az átviteli sebességet és az engedélyezett IP-alagutak maximális számát.</span><span class="sxs-lookup"><span data-stu-id="fd57f-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="fd57f-108">Az Azure támogatja az alapvető, normál, nagy teljesítményű, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ, (néha kicsi, közepes és nagy méretű SKU) használatát.</span><span class="sxs-lookup"><span data-stu-id="fd57f-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="fd57f-109">Az egyes SKU-típusok képességeiről további információt a című témakörben találhat https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .</span><span class="sxs-lookup"><span data-stu-id="fd57f-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>
<span data-ttu-id="fd57f-110">Tartsa szem előtt, hogy a SKU az árak és a funkciók között eltérő.</span><span class="sxs-lookup"><span data-stu-id="fd57f-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="fd57f-111">További információ: https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .</span><span class="sxs-lookup"><span data-stu-id="fd57f-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="fd57f-112">Példák</span><span class="sxs-lookup"><span data-stu-id="fd57f-112">EXAMPLES</span></span>

### <span data-ttu-id="fd57f-113">Példa 1: virtuális hálózati átjáró méretének módosítása</span><span class="sxs-lookup"><span data-stu-id="fd57f-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="fd57f-114">Ez a példa a ContosoVirtualGateway nevű virtuális hálózati átjáró méretét módosítja.</span><span class="sxs-lookup"><span data-stu-id="fd57f-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="fd57f-115">Az első parancs egy objektumra mutató hivatkozást hoz létre a ContosoVirtualGateway-hoz; Ez az objektum hivatkozás a $Gateway nevű változóban tárolódik.</span><span class="sxs-lookup"><span data-stu-id="fd57f-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="fd57f-116">A második parancs ezt követően a **Resize-AzVirtualNetworkGateway** parancsmagot használja az *GatewaySku* tulajdonság egyszerű értékre való beállításához.</span><span class="sxs-lookup"><span data-stu-id="fd57f-116">The second command then uses the **Resize-AzVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="fd57f-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fd57f-117">PARAMETERS</span></span>

### <span data-ttu-id="fd57f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd57f-118">-DefaultProfile</span></span>
<span data-ttu-id="fd57f-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd57f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd57f-120">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="fd57f-120">-GatewaySku</span></span>
<span data-ttu-id="fd57f-121">Az átjáró új típusú SKU-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd57f-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="fd57f-122">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="fd57f-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fd57f-123">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="fd57f-123">Basic</span></span>
- <span data-ttu-id="fd57f-124">Standard</span><span class="sxs-lookup"><span data-stu-id="fd57f-124">Standard</span></span>
- <span data-ttu-id="fd57f-125">Nagy teljesítmény</span><span class="sxs-lookup"><span data-stu-id="fd57f-125">High Performance</span></span>
- <span data-ttu-id="fd57f-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="fd57f-126">VpnGw1</span></span>
- <span data-ttu-id="fd57f-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="fd57f-127">VpnGw2</span></span>
- <span data-ttu-id="fd57f-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="fd57f-128">VpnGw3</span></span>
- <span data-ttu-id="fd57f-129">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="fd57f-129">VpnGw1AZ</span></span> 
- <span data-ttu-id="fd57f-130">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="fd57f-130">VpnGw2AZ</span></span> 
- <span data-ttu-id="fd57f-131">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="fd57f-131">VpnGw3AZ</span></span> 
- <span data-ttu-id="fd57f-132">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="fd57f-132">ErGw1AZ</span></span> 
- <span data-ttu-id="fd57f-133">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="fd57f-133">ErGw2AZ</span></span> 
- <span data-ttu-id="fd57f-134">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="fd57f-134">ErGw3AZ</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd57f-135">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fd57f-135">-VirtualNetworkGateway</span></span>
<span data-ttu-id="fd57f-136">Az átméretezni kívánt virtuális hálózati átjáróra mutató objektum hivatkozását adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd57f-136">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="fd57f-137">Az objektum hivatkozását létrehozhatja a Get-AzVirtualNetworkGateway használatával, és megadhatja az átjáró nevét.</span><span class="sxs-lookup"><span data-stu-id="fd57f-137">You can create this object reference by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd57f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd57f-138">CommonParameters</span></span>
<span data-ttu-id="fd57f-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fd57f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd57f-140">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd57f-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd57f-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd57f-141">INPUTS</span></span>

### <span data-ttu-id="fd57f-142">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fd57f-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="fd57f-143">System. String</span><span class="sxs-lookup"><span data-stu-id="fd57f-143">System.String</span></span>

## <span data-ttu-id="fd57f-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd57f-144">OUTPUTS</span></span>

### <span data-ttu-id="fd57f-145">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fd57f-145">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="fd57f-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fd57f-146">NOTES</span></span>
<span data-ttu-id="fd57f-147">Az alap/normál/HighPerformance SKU-ról nem lehet átméretezni az új VpnGw1/VpnGw2/VpnGw3 SKU-ra.</span><span class="sxs-lookup"><span data-stu-id="fd57f-147">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="fd57f-148">A további átméretezés nem engedélyezett a VpnGw1AZ/VpnGw2AZ/VpnGw3AZ vagy a ErGw1AZ/ErGw2AZ/ErGw3AZ.</span><span class="sxs-lookup"><span data-stu-id="fd57f-148">Further resize is not allowed from/to VpnGw1AZ/VpnGw2AZ/VpnGw3AZ or ErGw1AZ/ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="fd57f-149">Az átméretezés csak a SKU "sorozat"-ban engedélyezett, például a VpnGw1AZ átméretezhetők a VpnGw2AZ/VpnGw3AZ és a ErGw1AZ átméretezhetők a ErGw2AZ/ErGw3AZ.</span><span class="sxs-lookup"><span data-stu-id="fd57f-149">Resize is allowed only within the SKU 'series' e.g VpnGw1AZ can be resized to/from VpnGw2AZ/VpnGw3AZ and ErGw1AZ can be resized to/from ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="fd57f-150">Lásd: https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways utasítások.</span><span class="sxs-lookup"><span data-stu-id="fd57f-150">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="fd57f-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd57f-151">RELATED LINKS</span></span>

[<span data-ttu-id="fd57f-152">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fd57f-152">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="fd57f-153">Új – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fd57f-153">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="fd57f-154">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fd57f-154">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="fd57f-155">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fd57f-155">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="fd57f-156">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fd57f-156">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)

[<span data-ttu-id="fd57f-157">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="fd57f-157">Get-AzVpnClientPackage</span></span>](./Get-AzVpnClientPackage.md)

[<span data-ttu-id="fd57f-158">Set-AzVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="fd57f-158">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)
