---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvpnconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
ms.openlocfilehash: 720b81b858799e2930ed3d2cdd45e25220697e6a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303521"
---
# <span data-ttu-id="46156-101">Start-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="46156-101">Start-AzVpnConnectionPacketCapture</span></span>

## <span data-ttu-id="46156-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="46156-102">SYNOPSIS</span></span>
<span data-ttu-id="46156-103">A csomag-rögzítési művelet elindítása VPN-kapcsolaton.</span><span class="sxs-lookup"><span data-stu-id="46156-103">Starts Packet Capture Operation on a Vpn Connection.</span></span>

## <span data-ttu-id="46156-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="46156-104">SYNTAX</span></span>

### <span data-ttu-id="46156-105">ByVpnConnectionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="46156-105">ByVpnConnectionName (Default)</span></span>
```
Start-AzVpnConnectionPacketCapture -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-FilterData <String>] -LinkConnectionName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46156-106">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="46156-106">ByVpnConnectionObject</span></span>
```
Start-AzVpnConnectionPacketCapture -InputObject <PSVpnConnection> [-FilterData <String>]
 -LinkConnectionName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="46156-107">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="46156-107">ByVpnConnectionResourceId</span></span>
```
Start-AzVpnConnectionPacketCapture -ResourceId <String> [-FilterData <String>] -LinkConnectionName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46156-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="46156-108">DESCRIPTION</span></span>
<span data-ttu-id="46156-109">A csomag-rögzítési művelet elindítása VPN-kapcsolaton.</span><span class="sxs-lookup"><span data-stu-id="46156-109">Starts Packet Capture Operation on a Vpn Connection.</span></span>

## <span data-ttu-id="46156-110">Példák</span><span class="sxs-lookup"><span data-stu-id="46156-110">EXAMPLES</span></span>

### <span data-ttu-id="46156-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="46156-111">Example 1</span></span>
```powershell
Start-AzVpnConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -ParentResourceName "VpnGw1" -LinkConnectionName "PktCaptureTestSite2Site1CnLink1"
Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
LinkConnectionName: PktCaptureTestSite2Site1CnLink1
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

### <span data-ttu-id="46156-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="46156-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"IpSubnetValueAsAny`":true,`"TcpFlags`":-1,`"PortValueAsAny`":true,`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVpnConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -ParentResourceName "VpnGw1" -LinkConnectionName "PktCaptureTestSite2Site1CnLink1,PktCaptureTestSite2Site1CnLink1" -FilterData $a 
Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
LinkConnectionName: PktCaptureTestSite2Site1CnLink1,PktCaptureTestSite2Site1CnLink1
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

## <span data-ttu-id="46156-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="46156-113">PARAMETERS</span></span>

### <span data-ttu-id="46156-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46156-114">-AsJob</span></span>
<span data-ttu-id="46156-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="46156-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46156-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46156-116">-DefaultProfile</span></span>
<span data-ttu-id="46156-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="46156-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46156-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="46156-118">-FilterData</span></span>
<span data-ttu-id="46156-119">A csomagok rögzítésének megkezdésére szolgáló szűrési beállítások a VPN-kapcsolaton.</span><span class="sxs-lookup"><span data-stu-id="46156-119">Filter options for start packet capture on Vpn connection.</span></span>

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

### <span data-ttu-id="46156-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46156-120">-InputObject</span></span>
<span data-ttu-id="46156-121">A VPN-kapcsolat objektum, amelybe a csomagot el kell indítani.</span><span class="sxs-lookup"><span data-stu-id="46156-121">The Vpn connection object where packet capture to be started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46156-122">-LinkConnectionName</span><span class="sxs-lookup"><span data-stu-id="46156-122">-LinkConnectionName</span></span>
<span data-ttu-id="46156-123">A SiteLinkConnection nevei.</span><span class="sxs-lookup"><span data-stu-id="46156-123">The names of the SiteLinkConnection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46156-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="46156-124">-Name</span></span>
<span data-ttu-id="46156-125">Annak a virtuális magánhálózati kapcsolatnak a neve, amelybe a csomagot el kell indítani.</span><span class="sxs-lookup"><span data-stu-id="46156-125">The Vpn connection name where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46156-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="46156-126">-ParentResourceName</span></span>
<span data-ttu-id="46156-127">A szülő Vpngateway neve.</span><span class="sxs-lookup"><span data-stu-id="46156-127">The name of the Parent Vpngateway.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46156-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46156-128">-ResourceGroupName</span></span>
<span data-ttu-id="46156-129">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="46156-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46156-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46156-130">-ResourceId</span></span>
<span data-ttu-id="46156-131">Az Azure Resource ID a VpnConnection, ahol a csomagot el szeretné indítani.</span><span class="sxs-lookup"><span data-stu-id="46156-131">The Azure resource ID of the VpnConnection where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46156-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="46156-132">-Confirm</span></span>
<span data-ttu-id="46156-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="46156-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46156-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46156-134">-WhatIf</span></span>
<span data-ttu-id="46156-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="46156-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46156-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="46156-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46156-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46156-137">CommonParameters</span></span>
<span data-ttu-id="46156-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="46156-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46156-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="46156-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46156-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="46156-140">INPUTS</span></span>

### <span data-ttu-id="46156-141">Microsoft. Azure. commands. Network. models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="46156-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

### <span data-ttu-id="46156-142">System. String</span><span class="sxs-lookup"><span data-stu-id="46156-142">System.String</span></span>

## <span data-ttu-id="46156-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="46156-143">OUTPUTS</span></span>

### <span data-ttu-id="46156-144">Microsoft. Azure. commands. Network. models. PSVpnConnectionPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="46156-144">Microsoft.Azure.Commands.Network.Models.PSVpnConnectionPacketCaptureResult</span></span>

## <span data-ttu-id="46156-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="46156-145">NOTES</span></span>

## <span data-ttu-id="46156-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="46156-146">RELATED LINKS</span></span>

[<span data-ttu-id="46156-147">Stop-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="46156-147">Stop-AzVpnConnectionPacketCapture</span></span>](./Stop-AzVpnConnectionPacketCapture.md)