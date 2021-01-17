---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: dd48af6a0f20cafea5911adb629a83323faa94a6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98481160"
---
# <span data-ttu-id="6f44e-101">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6f44e-101">Resize-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="6f44e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f44e-102">SYNOPSIS</span></span>
<span data-ttu-id="6f44e-103">Átméretez egy meglévő virtuális hálózati átjárót.</span><span class="sxs-lookup"><span data-stu-id="6f44e-103">Resizes an existing virtual network gateway.</span></span>

## <span data-ttu-id="6f44e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6f44e-104">SYNTAX</span></span>

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f44e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6f44e-105">DESCRIPTION</span></span>
<span data-ttu-id="6f44e-106">Az **Resize-AzVirtualNetworkGateway** parancsmag segítségével módosíthatja egy virtuális hálózati átjáró készletezési egységét.</span><span class="sxs-lookup"><span data-stu-id="6f44e-106">The **Resize-AzVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="6f44e-107">Az SKUs meghatározza az átjárók képességeit, többek között az átviteli sebességet és az engedélyezett IP-átjárók maximális számát.</span><span class="sxs-lookup"><span data-stu-id="6f44e-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="6f44e-108">Az Azure alapszintű, szabványos, nagy teljesítményű, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUs (más néven Kis, Közepes és Nagy SKUs) támogatja.</span><span class="sxs-lookup"><span data-stu-id="6f44e-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="6f44e-109">Az egyes termékváltozat-típusokkal kapcsolatos részletes információkért https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ lásd: .</span><span class="sxs-lookup"><span data-stu-id="6f44e-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>
<span data-ttu-id="6f44e-110">Ne feledje, hogy a termékkódja az árazásban és a képességekben is különbözik.</span><span class="sxs-lookup"><span data-stu-id="6f44e-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="6f44e-111">További információ: https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .</span><span class="sxs-lookup"><span data-stu-id="6f44e-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="6f44e-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6f44e-112">EXAMPLES</span></span>

### <span data-ttu-id="6f44e-113">1. példa: Virtuális hálózati átjáró méretének módosítása</span><span class="sxs-lookup"><span data-stu-id="6f44e-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="6f44e-114">Ez a példa módosítja a ContosoVirtualGateway nevű virtuális hálózati átjáró méretét.</span><span class="sxs-lookup"><span data-stu-id="6f44e-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="6f44e-115">Az első parancs a ContosoVirtualGateway objektumhivatkozását hozza létre; Ezt az objektumhivatkozást egy $Gateway.</span><span class="sxs-lookup"><span data-stu-id="6f44e-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="6f44e-116">A második parancs ezután az **Resize-AzVirtualNetworkGateway** parancsmagot használva alapszintűre állíthatja az *ÁtjáróKku* tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="6f44e-116">The second command then uses the **Resize-AzVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="6f44e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f44e-117">PARAMETERS</span></span>

### <span data-ttu-id="6f44e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f44e-118">-DefaultProfile</span></span>
<span data-ttu-id="6f44e-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6f44e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f44e-120">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="6f44e-120">-GatewaySku</span></span>
<span data-ttu-id="6f44e-121">Az átjárók termékváltozatának új típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="6f44e-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="6f44e-122">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="6f44e-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6f44e-123">Alapszintű</span><span class="sxs-lookup"><span data-stu-id="6f44e-123">Basic</span></span>
- <span data-ttu-id="6f44e-124">Normál</span><span class="sxs-lookup"><span data-stu-id="6f44e-124">Standard</span></span>
- <span data-ttu-id="6f44e-125">Nagy teljesítmény</span><span class="sxs-lookup"><span data-stu-id="6f44e-125">High Performance</span></span>
- <span data-ttu-id="6f44e-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="6f44e-126">VpnGw1</span></span>
- <span data-ttu-id="6f44e-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="6f44e-127">VpnGw2</span></span>
- <span data-ttu-id="6f44e-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="6f44e-128">VpnGw3</span></span>
- <span data-ttu-id="6f44e-129">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="6f44e-129">VpnGw1AZ</span></span> 
- <span data-ttu-id="6f44e-130">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="6f44e-130">VpnGw2AZ</span></span> 
- <span data-ttu-id="6f44e-131">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="6f44e-131">VpnGw3AZ</span></span> 
- <span data-ttu-id="6f44e-132">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="6f44e-132">ErGw1AZ</span></span> 
- <span data-ttu-id="6f44e-133">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="6f44e-133">ErGw2AZ</span></span> 
- <span data-ttu-id="6f44e-134">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="6f44e-134">ErGw3AZ</span></span> 

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

### <span data-ttu-id="6f44e-135">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6f44e-135">-VirtualNetworkGateway</span></span>
<span data-ttu-id="6f44e-136">Az átméretezni szükséges virtuális hálózati átjáró objektumhivatkozását adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f44e-136">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="6f44e-137">Ezt az objektumhivatkozást a Get-AzVirtualNetworkGateway és az átjáró nevének megadásával hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="6f44e-137">You can create this object reference by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="6f44e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f44e-138">CommonParameters</span></span>
<span data-ttu-id="6f44e-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f44e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f44e-140">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f44e-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f44e-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6f44e-141">INPUTS</span></span>

### <span data-ttu-id="6f44e-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6f44e-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="6f44e-143">System.String</span><span class="sxs-lookup"><span data-stu-id="6f44e-143">System.String</span></span>

## <span data-ttu-id="6f44e-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f44e-144">OUTPUTS</span></span>

### <span data-ttu-id="6f44e-145">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6f44e-145">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="6f44e-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6f44e-146">NOTES</span></span>
<span data-ttu-id="6f44e-147">Alapszintű/Standard/HighPerformance SKUs-ból nem lehet átméretezni az új VpnGw1/VpnGw2/VpnGw3-SKUs-ra.</span><span class="sxs-lookup"><span data-stu-id="6f44e-147">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="6f44e-148">A vpnGw1AZ/VpnGw2AZ/VpnGw3AZ vagy ErGw1AZ/ErGw2AZ/ErGw2AZ/ErGw3AZ nem engedélyezett további átméretezések.</span><span class="sxs-lookup"><span data-stu-id="6f44e-148">Further resize is not allowed from/to VpnGw1AZ/VpnGw2AZ/VpnGw3AZ or ErGw1AZ/ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="6f44e-149">Az átméretezés csak az SKU "adatsorában" engedélyezett, például a VpnGw1AZ átméretezhetők a VpnGw2AZ/VpnGw3AZ/VpnGw3AZ és az ErGw1AZ termékváltozatba vagy az ErGw2AZ/ErGw3AZ alkalmazásba.</span><span class="sxs-lookup"><span data-stu-id="6f44e-149">Resize is allowed only within the SKU 'series' e.g VpnGw1AZ can be resized to/from VpnGw2AZ/VpnGw3AZ and ErGw1AZ can be resized to/from ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="6f44e-150">Útmutatást https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways itt láthat.</span><span class="sxs-lookup"><span data-stu-id="6f44e-150">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="6f44e-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6f44e-151">RELATED LINKS</span></span>

[<span data-ttu-id="6f44e-152">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6f44e-152">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="6f44e-153">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6f44e-153">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="6f44e-154">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6f44e-154">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="6f44e-155">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6f44e-155">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="6f44e-156">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6f44e-156">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)

[<span data-ttu-id="6f44e-157">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="6f44e-157">Get-AzVpnClientPackage</span></span>](./Get-AzVpnClientPackage.md)

[<span data-ttu-id="6f44e-158">Set-AzVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="6f44e-158">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)
