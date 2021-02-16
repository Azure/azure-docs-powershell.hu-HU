---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
ms.openlocfilehash: b0010134ac6b819afc3e8621b11d5530a08008a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160539"
---
# <span data-ttu-id="9f673-101">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9f673-101">Start-AzVirtualnetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="9f673-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f673-102">SYNOPSIS</span></span>
<span data-ttu-id="9f673-103">Elindítja a csomagrögzítési műveletet egy virtuális hálózati átjárón.</span><span class="sxs-lookup"><span data-stu-id="9f673-103">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="9f673-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9f673-104">SYNTAX</span></span>

### <span data-ttu-id="9f673-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9f673-105">ByName (Default)</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f673-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9f673-106">ByInputObject</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f673-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9f673-107">ByResourceId</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f673-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9f673-108">DESCRIPTION</span></span>
<span data-ttu-id="9f673-109">Elindítja a csomagrögzítési műveletet egy virtuális hálózati átjárón.</span><span class="sxs-lookup"><span data-stu-id="9f673-109">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="9f673-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9f673-110">EXAMPLES</span></span>

### <span data-ttu-id="9f673-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="9f673-111">Example 1</span></span>
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
### <span data-ttu-id="9f673-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="9f673-112">Example 2</span></span>
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
### <span data-ttu-id="9f673-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="9f673-113">Example 3</span></span>
<span data-ttu-id="9f673-114">Packet Capture example for capture all inner and outer packets</span><span class="sxs-lookup"><span data-stu-id="9f673-114">Packet Capture example for capture all inner and outer packets</span></span>
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

## <span data-ttu-id="9f673-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f673-115">PARAMETERS</span></span>

### <span data-ttu-id="9f673-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f673-116">-AsJob</span></span>
<span data-ttu-id="9f673-117">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9f673-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9f673-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f673-118">-Confirm</span></span>
<span data-ttu-id="9f673-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9f673-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f673-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f673-120">-DefaultProfile</span></span>
<span data-ttu-id="9f673-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9f673-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f673-122">-FilterData</span><span class="sxs-lookup"><span data-stu-id="9f673-122">-FilterData</span></span>
<span data-ttu-id="9f673-123">A csomagrögzítés indítási beállításai a virtuális hálózati átjárón.</span><span class="sxs-lookup"><span data-stu-id="9f673-123">Filter options for start packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="9f673-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f673-124">-InputObject</span></span>
<span data-ttu-id="9f673-125">Az a virtuális hálózati átjáróobjektum, amelyben a csomagrögzítést el kell kezdeni.</span><span class="sxs-lookup"><span data-stu-id="9f673-125">The virtual network gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="9f673-126">-Name</span><span class="sxs-lookup"><span data-stu-id="9f673-126">-Name</span></span>
<span data-ttu-id="9f673-127">A virtuális hálózati átjáró neve, ahol a csomagrögzítést el kell kezdeni.</span><span class="sxs-lookup"><span data-stu-id="9f673-127">The virtual network gateway name where packet capture is to be started.</span></span>

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

### <span data-ttu-id="9f673-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f673-128">-ResourceGroupName</span></span>
<span data-ttu-id="9f673-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9f673-129">The resource group name.</span></span>

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

### <span data-ttu-id="9f673-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f673-130">-ResourceId</span></span>
<span data-ttu-id="9f673-131">A VirtualNetworkGateway Azure-erőforrásazonosítója, ahol a csomagrögzítést el kell kezdeni.</span><span class="sxs-lookup"><span data-stu-id="9f673-131">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="9f673-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f673-132">-WhatIf</span></span>
<span data-ttu-id="9f673-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9f673-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f673-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9f673-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f673-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f673-135">CommonParameters</span></span>
<span data-ttu-id="9f673-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f673-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f673-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f673-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f673-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f673-138">INPUTS</span></span>

### <span data-ttu-id="9f673-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9f673-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="9f673-140">System.String</span><span class="sxs-lookup"><span data-stu-id="9f673-140">System.String</span></span>

## <span data-ttu-id="9f673-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f673-141">OUTPUTS</span></span>

### <span data-ttu-id="9f673-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="9f673-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="9f673-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9f673-143">NOTES</span></span>

## <span data-ttu-id="9f673-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f673-144">RELATED LINKS</span></span>
[<span data-ttu-id="9f673-145">Stop-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9f673-145">Stop-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)