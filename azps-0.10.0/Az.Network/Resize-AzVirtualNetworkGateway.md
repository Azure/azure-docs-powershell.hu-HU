---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: bd42d7cec30b7d42dcb1cdb3657f6681bf2cb6b0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843722"
---
# <span data-ttu-id="a95e4-101">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a95e4-101">Resize-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="a95e4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a95e4-102">SYNOPSIS</span></span>
<span data-ttu-id="a95e4-103">Egy meglévő virtuális hálózati átjáró átméretezése.</span><span class="sxs-lookup"><span data-stu-id="a95e4-103">Resizes an existing virtual network gateway.</span></span>

## <span data-ttu-id="a95e4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a95e4-104">SYNTAX</span></span>

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a95e4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a95e4-105">DESCRIPTION</span></span>
<span data-ttu-id="a95e4-106">Az **átméretezés-AzVirtualNetworkGateway** parancsmag lehetővé teszi a virtuális hálózati átjáró készletezési egységének (SKU) módosítását.</span><span class="sxs-lookup"><span data-stu-id="a95e4-106">The **Resize-AzVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="a95e4-107">A SKU határozza meg az átjáró funkcióit, így például az átviteli sebességet és az engedélyezett IP-alagutak maximális számát.</span><span class="sxs-lookup"><span data-stu-id="a95e4-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="a95e4-108">Az Azure támogatja az alapvető, normál, nagy teljesítményű, VpnGw1, VpnGw2 és VpnGw3 SKU-ket (más néven kicsi, közepes és nagy méretű SKU).</span><span class="sxs-lookup"><span data-stu-id="a95e4-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2 and VpnGw3 SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="a95e4-109">Az egyes SKU-típusok képességeiről további információt a című témakörben találhat https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .</span><span class="sxs-lookup"><span data-stu-id="a95e4-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>

<span data-ttu-id="a95e4-110">Tartsa szem előtt, hogy a SKU az árak és a funkciók között eltérő.</span><span class="sxs-lookup"><span data-stu-id="a95e4-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="a95e4-111">További információ: https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .</span><span class="sxs-lookup"><span data-stu-id="a95e4-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="a95e4-112">Példák</span><span class="sxs-lookup"><span data-stu-id="a95e4-112">EXAMPLES</span></span>

### <span data-ttu-id="a95e4-113">Példa 1: virtuális hálózati átjáró méretének módosítása</span><span class="sxs-lookup"><span data-stu-id="a95e4-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="a95e4-114">Ez a példa a ContosoVirtualGateway nevű virtuális hálózati átjáró méretét módosítja.</span><span class="sxs-lookup"><span data-stu-id="a95e4-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="a95e4-115">Az első parancs egy objektumra mutató hivatkozást hoz létre a ContosoVirtualGateway-hoz; Ez az objektum hivatkozás a $Gateway nevű változóban tárolódik.</span><span class="sxs-lookup"><span data-stu-id="a95e4-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="a95e4-116">A második parancs ezt követően a **Resize-AzVirtualNetworkGateway** parancsmagot használja az *GatewaySku* tulajdonság egyszerű értékre való beállításához.</span><span class="sxs-lookup"><span data-stu-id="a95e4-116">The second command then uses the **Resize-AzVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="a95e4-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a95e4-117">PARAMETERS</span></span>

### <span data-ttu-id="a95e4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a95e4-118">-DefaultProfile</span></span>
<span data-ttu-id="a95e4-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a95e4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95e4-120">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="a95e4-120">-GatewaySku</span></span>
<span data-ttu-id="a95e4-121">Az átjáró új típusú SKU-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a95e4-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="a95e4-122">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a95e4-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a95e4-123">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="a95e4-123">Basic</span></span>
- <span data-ttu-id="a95e4-124">Standard</span><span class="sxs-lookup"><span data-stu-id="a95e4-124">Standard</span></span>
- <span data-ttu-id="a95e4-125">Nagy teljesítmény</span><span class="sxs-lookup"><span data-stu-id="a95e4-125">High Performance</span></span>
- <span data-ttu-id="a95e4-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="a95e4-126">VpnGw1</span></span>
- <span data-ttu-id="a95e4-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="a95e4-127">VpnGw2</span></span>
- <span data-ttu-id="a95e4-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="a95e4-128">VpnGw3</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a95e4-129">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a95e4-129">-VirtualNetworkGateway</span></span>
<span data-ttu-id="a95e4-130">Az átméretezni kívánt virtuális hálózati átjáróra mutató objektum hivatkozását adja meg.</span><span class="sxs-lookup"><span data-stu-id="a95e4-130">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="a95e4-131">Az objektum hivatkozását létrehozhatja a Get-AzVirtualNetworkGateway használatával, és megadhatja az átjáró nevét.</span><span class="sxs-lookup"><span data-stu-id="a95e4-131">You can create this object reference by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a95e4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a95e4-132">CommonParameters</span></span>
<span data-ttu-id="a95e4-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a95e4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a95e4-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a95e4-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a95e4-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a95e4-135">INPUTS</span></span>

###  
<span data-ttu-id="a95e4-136">Ez a parancsmag a **Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway** objektum pipeline-példányait fogadja el.</span><span class="sxs-lookup"><span data-stu-id="a95e4-136">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="a95e4-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a95e4-137">OUTPUTS</span></span>

###  
<span data-ttu-id="a95e4-138">Ez a parancsmag módosítja a **Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway** objektum meglévő példányait.</span><span class="sxs-lookup"><span data-stu-id="a95e4-138">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="a95e4-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a95e4-139">NOTES</span></span>
<span data-ttu-id="a95e4-140">Az alap/normál/HighPerformance SKU-ról nem lehet átméretezni az új VpnGw1/VpnGw2/VpnGw3 SKU-ra.</span><span class="sxs-lookup"><span data-stu-id="a95e4-140">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="a95e4-141">Lásd: https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways utasítások.</span><span class="sxs-lookup"><span data-stu-id="a95e4-141">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="a95e4-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a95e4-142">RELATED LINKS</span></span>

[<span data-ttu-id="a95e4-143">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="a95e4-143">Get-AzVpnClientPackage</span></span>](./Get-AzVpnClientPackage.md)

[<span data-ttu-id="a95e4-144">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a95e4-144">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="a95e4-145">Set-AzVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="a95e4-145">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)


