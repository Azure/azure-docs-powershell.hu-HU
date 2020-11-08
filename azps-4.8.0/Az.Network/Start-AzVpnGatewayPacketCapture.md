---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Start-AzVpnGatewayPacketCapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
ms.openlocfilehash: 931c01b925416a7b1357d1eac15806035eef46d4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94172856"
---
# <span data-ttu-id="c3a07-101">Start-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c3a07-101">Start-AzVpnGatewayPacketCapture</span></span>

## <span data-ttu-id="c3a07-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c3a07-102">SYNOPSIS</span></span>
<span data-ttu-id="c3a07-103">A csomag-rögzítési művelet elindítása VPN-átjárón</span><span class="sxs-lookup"><span data-stu-id="c3a07-103">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="c3a07-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c3a07-104">SYNTAX</span></span>

### <span data-ttu-id="c3a07-105">ByVpnGatewayName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c3a07-105">ByVpnGatewayName (Default)</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3a07-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="c3a07-106">ByVpnGatewayObject</span></span>
```
Start-AzVpnGatewayPacketCapture -InputObject <PSVpnGateway> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3a07-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="c3a07-107">ByVpnGatewayResourceId</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3a07-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c3a07-108">DESCRIPTION</span></span>
<span data-ttu-id="c3a07-109">A csomag-rögzítési művelet elindítása VPN-átjárón</span><span class="sxs-lookup"><span data-stu-id="c3a07-109">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="c3a07-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c3a07-110">EXAMPLES</span></span>

### <span data-ttu-id="c3a07-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c3a07-111">Example 1</span></span>
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

### <span data-ttu-id="c3a07-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="c3a07-112">Example 2</span></span>
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

## <span data-ttu-id="c3a07-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c3a07-113">PARAMETERS</span></span>

### <span data-ttu-id="c3a07-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3a07-114">-AsJob</span></span>
<span data-ttu-id="c3a07-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c3a07-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c3a07-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3a07-116">-DefaultProfile</span></span>
<span data-ttu-id="c3a07-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c3a07-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3a07-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="c3a07-118">-FilterData</span></span>
<span data-ttu-id="c3a07-119">Szűrési lehetőségek a csomagok rögzítésének megkezdése VPN-átjárón.</span><span class="sxs-lookup"><span data-stu-id="c3a07-119">Filter options for start packet capture on Vpn Gateway.</span></span>

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

### <span data-ttu-id="c3a07-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3a07-120">-InputObject</span></span>
<span data-ttu-id="c3a07-121">A VPN-átjáró objektum, amelybe a csomag elindul.</span><span class="sxs-lookup"><span data-stu-id="c3a07-121">The Vpn Gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="c3a07-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c3a07-122">-Name</span></span>
<span data-ttu-id="c3a07-123">Annak a VPN-átjárónak a neve, amelybe a csomagot el kell indítani.</span><span class="sxs-lookup"><span data-stu-id="c3a07-123">The Vpn Gateway name where packet capture is to be started.</span></span>

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

### <span data-ttu-id="c3a07-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3a07-124">-ResourceGroupName</span></span>
<span data-ttu-id="c3a07-125">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="c3a07-125">The resource group name.</span></span>

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

### <span data-ttu-id="c3a07-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3a07-126">-ResourceId</span></span>
<span data-ttu-id="c3a07-127">Az Azure Resource ID a VpnGateway, ahol a csomagot el szeretné indítani.</span><span class="sxs-lookup"><span data-stu-id="c3a07-127">The Azure resource ID of the VpnGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="c3a07-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c3a07-128">-Confirm</span></span>
<span data-ttu-id="c3a07-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c3a07-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3a07-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3a07-130">-WhatIf</span></span>
<span data-ttu-id="c3a07-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c3a07-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3a07-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c3a07-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3a07-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3a07-133">CommonParameters</span></span>
<span data-ttu-id="c3a07-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c3a07-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3a07-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c3a07-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3a07-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3a07-136">INPUTS</span></span>

### <span data-ttu-id="c3a07-137">Microsoft. Azure. commands. Network. models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c3a07-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="c3a07-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c3a07-138">System.String</span></span>

## <span data-ttu-id="c3a07-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3a07-139">OUTPUTS</span></span>

### <span data-ttu-id="c3a07-140">Microsoft. Azure. commands. Network. models. PSVpnGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="c3a07-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="c3a07-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c3a07-141">NOTES</span></span>

## <span data-ttu-id="c3a07-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3a07-142">RELATED LINKS</span></span>

[<span data-ttu-id="c3a07-143">Stop-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c3a07-143">Stop-AzVpnGatewayPacketCapture</span></span>](./Stop-AzVpnGatewayPacketCapture.md)