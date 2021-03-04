---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/start-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
ms.openlocfilehash: 4f17777d366884f2b71c16c289e50dbf8425d729
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918561"
---
# <span data-ttu-id="2a949-101">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2a949-101">Start-AzVirtualnetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="2a949-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a949-102">SYNOPSIS</span></span>
<span data-ttu-id="2a949-103">Elindítja a csomagrögzítési műveletet egy virtuális hálózati átjárón.</span><span class="sxs-lookup"><span data-stu-id="2a949-103">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="2a949-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2a949-104">SYNTAX</span></span>

### <span data-ttu-id="2a949-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2a949-105">ByName (Default)</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a949-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2a949-106">ByInputObject</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a949-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2a949-107">ByResourceId</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a949-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2a949-108">DESCRIPTION</span></span>
<span data-ttu-id="2a949-109">Elindítja a csomagrögzítési műveletet egy virtuális hálózati átjárón.</span><span class="sxs-lookup"><span data-stu-id="2a949-109">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="2a949-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2a949-110">EXAMPLES</span></span>

### <span data-ttu-id="2a949-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="2a949-111">Example 1</span></span>
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
### <span data-ttu-id="2a949-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="2a949-112">Example 2</span></span>
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
### <span data-ttu-id="2a949-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="2a949-113">Example 3</span></span>
<span data-ttu-id="2a949-114">Packet Capture example for capture all inner and outer packets</span><span class="sxs-lookup"><span data-stu-id="2a949-114">Packet Capture example for capture all inner and outer packets</span></span>
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

## <span data-ttu-id="2a949-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a949-115">PARAMETERS</span></span>

### <span data-ttu-id="2a949-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a949-116">-AsJob</span></span>
<span data-ttu-id="2a949-117">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2a949-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2a949-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a949-118">-Confirm</span></span>
<span data-ttu-id="2a949-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2a949-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a949-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a949-120">-DefaultProfile</span></span>
<span data-ttu-id="2a949-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2a949-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a949-122">-FilterData</span><span class="sxs-lookup"><span data-stu-id="2a949-122">-FilterData</span></span>
<span data-ttu-id="2a949-123">Filter options for start packet capture on virtual network gateway.</span><span class="sxs-lookup"><span data-stu-id="2a949-123">Filter options for start packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="2a949-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a949-124">-InputObject</span></span>
<span data-ttu-id="2a949-125">A virtuális hálózati átjáró objektum, amelyben a csomagrögzítést el kell kezdeni.</span><span class="sxs-lookup"><span data-stu-id="2a949-125">The virtual network gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="2a949-126">-Name</span><span class="sxs-lookup"><span data-stu-id="2a949-126">-Name</span></span>
<span data-ttu-id="2a949-127">A virtuális hálózati átjáró neve, ahol a csomagrögzítést el kell kezdeni.</span><span class="sxs-lookup"><span data-stu-id="2a949-127">The virtual network gateway name where packet capture is to be started.</span></span>

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

### <span data-ttu-id="2a949-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a949-128">-ResourceGroupName</span></span>
<span data-ttu-id="2a949-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2a949-129">The resource group name.</span></span>

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

### <span data-ttu-id="2a949-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a949-130">-ResourceId</span></span>
<span data-ttu-id="2a949-131">A VirtualNetworkGateway Azure-erőforrásazonosítója, ahol a csomagrögzítést el kell kezdeni.</span><span class="sxs-lookup"><span data-stu-id="2a949-131">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="2a949-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a949-132">-WhatIf</span></span>
<span data-ttu-id="2a949-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2a949-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a949-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2a949-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a949-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a949-135">CommonParameters</span></span>
<span data-ttu-id="2a949-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a949-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a949-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a949-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a949-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2a949-138">INPUTS</span></span>

### <span data-ttu-id="2a949-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2a949-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="2a949-140">System.String</span><span class="sxs-lookup"><span data-stu-id="2a949-140">System.String</span></span>

## <span data-ttu-id="2a949-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a949-141">OUTPUTS</span></span>

### <span data-ttu-id="2a949-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="2a949-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="2a949-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2a949-143">NOTES</span></span>

## <span data-ttu-id="2a949-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2a949-144">RELATED LINKS</span></span>
[<span data-ttu-id="2a949-145">Stop-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2a949-145">Stop-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)