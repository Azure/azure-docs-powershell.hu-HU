---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: d01fad830b9edcd8eced13a4f1e9317bb4930f9c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94172859"
---
# <span data-ttu-id="91383-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="91383-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="91383-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="91383-102">SYNOPSIS</span></span>
<span data-ttu-id="91383-103">A csomag-rögzítési művelet elindítása virtuális hálózati átjáró-kapcsolaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="91383-103">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="91383-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="91383-104">SYNTAX</span></span>

### <span data-ttu-id="91383-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="91383-105">ByName (Default)</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91383-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="91383-106">ByInputObject</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91383-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="91383-107">ByResourceId</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91383-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="91383-108">DESCRIPTION</span></span>
<span data-ttu-id="91383-109">A csomag-rögzítési művelet elindítása virtuális hálózati átjáró-kapcsolaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="91383-109">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="91383-110">Példák</span><span class="sxs-lookup"><span data-stu-id="91383-110">EXAMPLES</span></span>

### <span data-ttu-id="91383-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="91383-111">Example 1</span></span>
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
### <span data-ttu-id="91383-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="91383-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"TcpFlags`":-1,`"Protocol`":[6],`"CaptureSingleDirectionTrafficOnly`":true}]}"
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
### <span data-ttu-id="91383-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="91383-113">Example 3</span></span>
<span data-ttu-id="91383-114">Csomagkapcsolt rögzítési példa az összes belső és külső csomag rögzítésére</span><span class="sxs-lookup"><span data-stu-id="91383-114">Packet Capture example for capture all inner and outer packets</span></span>
```powershell
$a = "{`"TracingFlags`": 11,`"MaxPacketBufferSize`": 120,`"MaxFileSize`": 500,`"Filters`" :[{`"CaptureSingleDirectionTrafficOnly`": false}]}"
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

## <span data-ttu-id="91383-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="91383-115">PARAMETERS</span></span>

### <span data-ttu-id="91383-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91383-116">-AsJob</span></span>
<span data-ttu-id="91383-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="91383-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91383-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="91383-118">-Confirm</span></span>
<span data-ttu-id="91383-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="91383-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91383-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91383-120">-DefaultProfile</span></span>
<span data-ttu-id="91383-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="91383-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91383-122">-FilterData</span><span class="sxs-lookup"><span data-stu-id="91383-122">-FilterData</span></span>
<span data-ttu-id="91383-123">Szűrési lehetőségek a virtuális hálózati átjáró kapcsolaton keresztüli csomagok rögzítésének megkezdéséhez.</span><span class="sxs-lookup"><span data-stu-id="91383-123">Filter options for start packet capture on virtual network gateway connection.</span></span>

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

### <span data-ttu-id="91383-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91383-124">-InputObject</span></span>
<span data-ttu-id="91383-125">A virtuális hálózati átjáró kapcsolat objektuma, ahol a csomag elindítható.</span><span class="sxs-lookup"><span data-stu-id="91383-125">The virtual network gateway connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="91383-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="91383-126">-Name</span></span>
<span data-ttu-id="91383-127">A virtuális hálózati átjáró kapcsolatának neve, amelybe a csomagot el kell indítani.</span><span class="sxs-lookup"><span data-stu-id="91383-127">The virtual network gateway connection name where packet capture to be started.</span></span>

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

### <span data-ttu-id="91383-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91383-128">-ResourceGroupName</span></span>
<span data-ttu-id="91383-129">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="91383-129">The resource group name.</span></span>

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

### <span data-ttu-id="91383-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91383-130">-ResourceId</span></span>
<span data-ttu-id="91383-131">Az Azure Resource ID a VirtualNetworkGatewayConnection, ahol a csomagot el szeretné indítani.</span><span class="sxs-lookup"><span data-stu-id="91383-131">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="91383-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91383-132">-WhatIf</span></span>
<span data-ttu-id="91383-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="91383-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91383-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="91383-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91383-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91383-135">CommonParameters</span></span>
<span data-ttu-id="91383-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="91383-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91383-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="91383-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91383-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="91383-138">INPUTS</span></span>

### <span data-ttu-id="91383-139">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="91383-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="91383-140">System. String</span><span class="sxs-lookup"><span data-stu-id="91383-140">System.String</span></span>

## <span data-ttu-id="91383-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91383-141">OUTPUTS</span></span>

### <span data-ttu-id="91383-142">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="91383-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="91383-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="91383-143">NOTES</span></span>

## <span data-ttu-id="91383-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91383-144">RELATED LINKS</span></span>
[<span data-ttu-id="91383-145">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="91383-145">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>](./Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md)