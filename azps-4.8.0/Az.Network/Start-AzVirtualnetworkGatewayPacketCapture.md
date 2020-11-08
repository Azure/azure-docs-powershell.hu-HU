---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
ms.openlocfilehash: b0010134ac6b819afc3e8621b11d5530a08008a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94172858"
---
# <span data-ttu-id="a369b-101">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a369b-101">Start-AzVirtualnetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="a369b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a369b-102">SYNOPSIS</span></span>
<span data-ttu-id="a369b-103">Egy virtuális hálózati átjárón elindítja a csomag rögzítési műveletét.</span><span class="sxs-lookup"><span data-stu-id="a369b-103">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="a369b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a369b-104">SYNTAX</span></span>

### <span data-ttu-id="a369b-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a369b-105">ByName (Default)</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a369b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a369b-106">ByInputObject</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a369b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a369b-107">ByResourceId</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a369b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a369b-108">DESCRIPTION</span></span>
<span data-ttu-id="a369b-109">Egy virtuális hálózati átjárón elindítja a csomag rögzítési műveletét.</span><span class="sxs-lookup"><span data-stu-id="a369b-109">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="a369b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a369b-110">EXAMPLES</span></span>

### <span data-ttu-id="a369b-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a369b-111">Example 1</span></span>
```powershell
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG"

Code              : Succeeded
EndTime           : 10/1/2019 12:57:27 AM
StartTime         : 10/1/2019 12:57:16 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2VNG
Etag              :
Id                :
```
### <span data-ttu-id="a369b-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="a369b-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"TcpFlags`":-1,`"Protocol`":[6],`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG" -FilterData $a

Code              : Succeeded
EndTime           : 10/1/2019 12:57:27 AM
StartTime         : 10/1/2019 12:57:16 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2VNG
Etag              :
Id                :
```
### <span data-ttu-id="a369b-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="a369b-113">Example 3</span></span>
<span data-ttu-id="a369b-114">Csomagkapcsolt rögzítési példa az összes belső és külső csomag rögzítésére</span><span class="sxs-lookup"><span data-stu-id="a369b-114">Packet Capture example for capture all inner and outer packets</span></span>
```powershell
$a = "{`"TracingFlags`": 11,`"MaxPacketBufferSize`": 120,`"MaxFileSize`": 500,`"Filters`" :[{`"CaptureSingleDirectionTrafficOnly`": false}]}"
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG" -FilterData $a

Code              : Succeeded
EndTime           : 10/1/2019 12:57:27 AM
StartTime         : 10/1/2019 12:57:16 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2VNG
Etag              :
Id                :
```

## <span data-ttu-id="a369b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a369b-115">PARAMETERS</span></span>

### <span data-ttu-id="a369b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a369b-116">-AsJob</span></span>
<span data-ttu-id="a369b-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a369b-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a369b-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a369b-118">-Confirm</span></span>
<span data-ttu-id="a369b-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a369b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a369b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a369b-120">-DefaultProfile</span></span>
<span data-ttu-id="a369b-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a369b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a369b-122">-FilterData</span><span class="sxs-lookup"><span data-stu-id="a369b-122">-FilterData</span></span>
<span data-ttu-id="a369b-123">Szűrési lehetőségek a virtuális hálózati átjáró indítási csomagjának rögzítésére.</span><span class="sxs-lookup"><span data-stu-id="a369b-123">Filter options for start packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="a369b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a369b-124">-InputObject</span></span>
<span data-ttu-id="a369b-125">A virtuális hálózati átjáró objektum, amelyen a csomag elindítható.</span><span class="sxs-lookup"><span data-stu-id="a369b-125">The virtual network gateway object where packet capture to be started.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: ByInputObject
Aliases: VirtualNetworkGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a369b-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a369b-126">-Name</span></span>
<span data-ttu-id="a369b-127">A virtuális hálózat átjárójának neve, ahová a csomagot el kell indítani.</span><span class="sxs-lookup"><span data-stu-id="a369b-127">The virtual network gateway name where packet capture is to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, VirtualNetworkGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a369b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a369b-128">-ResourceGroupName</span></span>
<span data-ttu-id="a369b-129">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="a369b-129">The resource group name.</span></span>

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

### <span data-ttu-id="a369b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a369b-130">-ResourceId</span></span>
<span data-ttu-id="a369b-131">Az Azure Resource ID a VirtualNetworkGateway, ahol a csomagot el szeretné indítani.</span><span class="sxs-lookup"><span data-stu-id="a369b-131">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="a369b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a369b-132">-WhatIf</span></span>
<span data-ttu-id="a369b-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a369b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a369b-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a369b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a369b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a369b-135">CommonParameters</span></span>
<span data-ttu-id="a369b-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a369b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a369b-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a369b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a369b-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a369b-138">INPUTS</span></span>

### <span data-ttu-id="a369b-139">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a369b-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="a369b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a369b-140">System.String</span></span>

## <span data-ttu-id="a369b-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a369b-141">OUTPUTS</span></span>

### <span data-ttu-id="a369b-142">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="a369b-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="a369b-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a369b-143">NOTES</span></span>

## <span data-ttu-id="a369b-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a369b-144">RELATED LINKS</span></span>
[<span data-ttu-id="a369b-145">Stop-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a369b-145">Stop-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)