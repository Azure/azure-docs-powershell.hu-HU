---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Start-AzVpnGatewayPacketCapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
ms.openlocfilehash: 931c01b925416a7b1357d1eac15806035eef46d4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365034"
---
# <span data-ttu-id="95028-101">Start-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="95028-101">Start-AzVpnGatewayPacketCapture</span></span>

## <span data-ttu-id="95028-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95028-102">SYNOPSIS</span></span>
<span data-ttu-id="95028-103">Csomagrögzítési műveletet kezd Vpn-átjárón.</span><span class="sxs-lookup"><span data-stu-id="95028-103">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="95028-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="95028-104">SYNTAX</span></span>

### <span data-ttu-id="95028-105">ByVpnGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="95028-105">ByVpnGatewayName (Default)</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95028-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="95028-106">ByVpnGatewayObject</span></span>
```
Start-AzVpnGatewayPacketCapture -InputObject <PSVpnGateway> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95028-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="95028-107">ByVpnGatewayResourceId</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95028-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="95028-108">DESCRIPTION</span></span>
<span data-ttu-id="95028-109">Csomagrögzítési műveletet kezd Vpn-átjárón.</span><span class="sxs-lookup"><span data-stu-id="95028-109">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="95028-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="95028-110">EXAMPLES</span></span>

### <span data-ttu-id="95028-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="95028-111">Example 1</span></span>
```powershell
Start-AzVpnGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG"
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

### <span data-ttu-id="95028-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="95028-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"TcpFlags`":-1,`"Protocol`":[6],`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVpnGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG" -FilterData $a
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

## <span data-ttu-id="95028-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95028-113">PARAMETERS</span></span>

### <span data-ttu-id="95028-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95028-114">-AsJob</span></span>
<span data-ttu-id="95028-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="95028-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95028-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95028-116">-DefaultProfile</span></span>
<span data-ttu-id="95028-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="95028-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95028-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="95028-118">-FilterData</span></span>
<span data-ttu-id="95028-119">A Csomagrögzítés indítási beállításai Vpn-átjárón.</span><span class="sxs-lookup"><span data-stu-id="95028-119">Filter options for start packet capture on Vpn Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95028-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95028-120">-InputObject</span></span>
<span data-ttu-id="95028-121">A Vpn Gateway-objektum, amelyben a csomagrögzítést el kell kezdeni.</span><span class="sxs-lookup"><span data-stu-id="95028-121">The Vpn Gateway object where packet capture to be started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95028-122">-Name</span><span class="sxs-lookup"><span data-stu-id="95028-122">-Name</span></span>
<span data-ttu-id="95028-123">A Vpn-átjáró neve, ahol a csomagrögzítést el kell kezdeni.</span><span class="sxs-lookup"><span data-stu-id="95028-123">The Vpn Gateway name where packet capture is to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95028-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95028-124">-ResourceGroupName</span></span>
<span data-ttu-id="95028-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="95028-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95028-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95028-126">-ResourceId</span></span>
<span data-ttu-id="95028-127">Annak a VpnGatewaynek az Azure-erőforrás-azonosítója, ahol a csomagrögzítést el kell kezdeni.</span><span class="sxs-lookup"><span data-stu-id="95028-127">The Azure resource ID of the VpnGateway where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95028-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95028-128">-Confirm</span></span>
<span data-ttu-id="95028-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="95028-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95028-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95028-130">-WhatIf</span></span>
<span data-ttu-id="95028-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="95028-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95028-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="95028-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95028-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95028-133">CommonParameters</span></span>
<span data-ttu-id="95028-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95028-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95028-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95028-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95028-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="95028-136">INPUTS</span></span>

### <span data-ttu-id="95028-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="95028-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="95028-138">System.String</span><span class="sxs-lookup"><span data-stu-id="95028-138">System.String</span></span>

## <span data-ttu-id="95028-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="95028-139">OUTPUTS</span></span>

### <span data-ttu-id="95028-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="95028-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="95028-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="95028-141">NOTES</span></span>

## <span data-ttu-id="95028-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="95028-142">RELATED LINKS</span></span>

[<span data-ttu-id="95028-143">Stop-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="95028-143">Stop-AzVpnGatewayPacketCapture</span></span>](./Stop-AzVpnGatewayPacketCapture.md)