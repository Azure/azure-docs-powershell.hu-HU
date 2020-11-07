---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: 3a1d9c2f415d56263529fcd66aa1ee9535823bbf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838287"
---
# <span data-ttu-id="d7b8f-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d7b8f-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="d7b8f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7b8f-102">SYNOPSIS</span></span>
<span data-ttu-id="d7b8f-103">A csomag-rögzítési művelet elindítása virtuális hálózati átjáró-kapcsolaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="d7b8f-103">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="d7b8f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7b8f-104">SYNTAX</span></span>

### <span data-ttu-id="d7b8f-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d7b8f-105">ByName (Default)</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7b8f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d7b8f-106">ByInputObject</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7b8f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d7b8f-107">ByResourceId</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7b8f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7b8f-108">DESCRIPTION</span></span>
<span data-ttu-id="d7b8f-109">A csomag-rögzítési művelet elindítása virtuális hálózati átjáró-kapcsolaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="d7b8f-109">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="d7b8f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d7b8f-110">EXAMPLES</span></span>

### <span data-ttu-id="d7b8f-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d7b8f-111">Example 1</span></span>
```powershell
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn"

Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2Site1Cn
Etag              :
Id                :
```
### <span data-ttu-id="d7b8f-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="d7b8f-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"IpSubnetValueAsAny`":true,`"TcpFlags`":-1,`"PortValueAsAny`":true,`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -FilterData $a

Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2Site1Cn
Etag              :
Id                :
```

## <span data-ttu-id="d7b8f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7b8f-113">PARAMETERS</span></span>

### <span data-ttu-id="d7b8f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7b8f-114">-AsJob</span></span>
<span data-ttu-id="d7b8f-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d7b8f-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b8f-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d7b8f-116">-Confirm</span></span>
<span data-ttu-id="d7b8f-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d7b8f-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b8f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7b8f-118">-DefaultProfile</span></span>
<span data-ttu-id="d7b8f-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d7b8f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b8f-120">-FilterData</span><span class="sxs-lookup"><span data-stu-id="d7b8f-120">-FilterData</span></span>
<span data-ttu-id="d7b8f-121">Szűrési lehetőségek a virtuális hálózati átjáró kapcsolaton keresztüli csomagok rögzítésének megkezdéséhez.</span><span class="sxs-lookup"><span data-stu-id="d7b8f-121">Filter options for start packet capture on virtual network gateway connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b8f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7b8f-122">-InputObject</span></span>
<span data-ttu-id="d7b8f-123">A virtuális hálózati átjáró kapcsolat objektuma, ahol a csomag elindítható.</span><span class="sxs-lookup"><span data-stu-id="d7b8f-123">The virtual network gateway connection object where packet capture to be started.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: ByInputObject
Aliases: VirtualNetworkGatewayConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7b8f-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d7b8f-124">-Name</span></span>
<span data-ttu-id="d7b8f-125">A virtuális hálózati átjáró kapcsolatának neve, amelybe a csomagot el kell indítani.</span><span class="sxs-lookup"><span data-stu-id="d7b8f-125">The virtual network gateway connection name where packet capture to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, VirtualNetworkGatewayConnectionName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b8f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7b8f-126">-ResourceGroupName</span></span>
<span data-ttu-id="d7b8f-127">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="d7b8f-127">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b8f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7b8f-128">-ResourceId</span></span>
<span data-ttu-id="d7b8f-129">Az Azure Resource ID a VirtualNetworkGatewayConnection, ahol a csomagot el szeretné indítani.</span><span class="sxs-lookup"><span data-stu-id="d7b8f-129">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7b8f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7b8f-130">-WhatIf</span></span>
<span data-ttu-id="d7b8f-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d7b8f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7b8f-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d7b8f-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b8f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7b8f-133">CommonParameters</span></span>
<span data-ttu-id="d7b8f-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7b8f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7b8f-135">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d7b8f-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7b8f-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7b8f-136">INPUTS</span></span>

### <span data-ttu-id="d7b8f-137">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d7b8f-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="d7b8f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d7b8f-138">System.String</span></span>

## <span data-ttu-id="d7b8f-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7b8f-139">OUTPUTS</span></span>

### <span data-ttu-id="d7b8f-140">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="d7b8f-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="d7b8f-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7b8f-141">NOTES</span></span>

## <span data-ttu-id="d7b8f-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7b8f-142">RELATED LINKS</span></span>
[<span data-ttu-id="d7b8f-143">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d7b8f-143">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>](./Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md)