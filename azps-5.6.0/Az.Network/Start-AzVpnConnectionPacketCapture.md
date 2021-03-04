---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/start-azvpnconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
ms.openlocfilehash: 0b920adf2f0357db7e9babf7b8e4b4e603255fab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918554"
---
# <span data-ttu-id="dd68c-101">Start-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dd68c-101">Start-AzVpnConnectionPacketCapture</span></span>

## <span data-ttu-id="dd68c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd68c-102">SYNOPSIS</span></span>
<span data-ttu-id="dd68c-103">Elindítja a csomagrögzítési műveletet Vpn-kapcsolaton.</span><span class="sxs-lookup"><span data-stu-id="dd68c-103">Starts Packet Capture Operation on a Vpn Connection.</span></span>

## <span data-ttu-id="dd68c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dd68c-104">SYNTAX</span></span>

### <span data-ttu-id="dd68c-105">ByVpnConnectionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dd68c-105">ByVpnConnectionName (Default)</span></span>
```
Start-AzVpnConnectionPacketCapture -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-FilterData <String>] -LinkConnectionName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd68c-106">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="dd68c-106">ByVpnConnectionObject</span></span>
```
Start-AzVpnConnectionPacketCapture -InputObject <PSVpnConnection> [-FilterData <String>]
 -LinkConnectionName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd68c-107">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="dd68c-107">ByVpnConnectionResourceId</span></span>
```
Start-AzVpnConnectionPacketCapture -ResourceId <String> [-FilterData <String>] -LinkConnectionName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd68c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dd68c-108">DESCRIPTION</span></span>
<span data-ttu-id="dd68c-109">Elindítja a csomagrögzítési műveletet Vpn-kapcsolaton.</span><span class="sxs-lookup"><span data-stu-id="dd68c-109">Starts Packet Capture Operation on a Vpn Connection.</span></span>

## <span data-ttu-id="dd68c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dd68c-110">EXAMPLES</span></span>

### <span data-ttu-id="dd68c-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="dd68c-111">Example 1</span></span>
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

### <span data-ttu-id="dd68c-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="dd68c-112">Example 2</span></span>
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

## <span data-ttu-id="dd68c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd68c-113">PARAMETERS</span></span>

### <span data-ttu-id="dd68c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd68c-114">-AsJob</span></span>
<span data-ttu-id="dd68c-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="dd68c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd68c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd68c-116">-DefaultProfile</span></span>
<span data-ttu-id="dd68c-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dd68c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd68c-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="dd68c-118">-FilterData</span></span>
<span data-ttu-id="dd68c-119">Filter options for start packet capture on Vpn connection.</span><span class="sxs-lookup"><span data-stu-id="dd68c-119">Filter options for start packet capture on Vpn connection.</span></span>

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

### <span data-ttu-id="dd68c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd68c-120">-InputObject</span></span>
<span data-ttu-id="dd68c-121">A Vpn-kapcsolatobjektum, amelyben a csomagrögzítést el kell kezdeni.</span><span class="sxs-lookup"><span data-stu-id="dd68c-121">The Vpn connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="dd68c-122">-LinkConnectionName</span><span class="sxs-lookup"><span data-stu-id="dd68c-122">-LinkConnectionName</span></span>
<span data-ttu-id="dd68c-123">A SiteLinkConnection nevei.</span><span class="sxs-lookup"><span data-stu-id="dd68c-123">The names of the SiteLinkConnection.</span></span>

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

### <span data-ttu-id="dd68c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="dd68c-124">-Name</span></span>
<span data-ttu-id="dd68c-125">A Vpn-kapcsolat neve, ahol a csomagrögzítést el kell kezdeni.</span><span class="sxs-lookup"><span data-stu-id="dd68c-125">The Vpn connection name where packet capture to be started.</span></span>

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

### <span data-ttu-id="dd68c-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="dd68c-126">-ParentResourceName</span></span>
<span data-ttu-id="dd68c-127">A szülő Vpngateway neve.</span><span class="sxs-lookup"><span data-stu-id="dd68c-127">The name of the Parent Vpngateway.</span></span>

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

### <span data-ttu-id="dd68c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd68c-128">-ResourceGroupName</span></span>
<span data-ttu-id="dd68c-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="dd68c-129">The resource group name.</span></span>

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

### <span data-ttu-id="dd68c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd68c-130">-ResourceId</span></span>
<span data-ttu-id="dd68c-131">A VpnConnection Azure-erőforrásazonosítója, ahol a csomagrögzítést el kell kezdeni.</span><span class="sxs-lookup"><span data-stu-id="dd68c-131">The Azure resource ID of the VpnConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="dd68c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd68c-132">-Confirm</span></span>
<span data-ttu-id="dd68c-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="dd68c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd68c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd68c-134">-WhatIf</span></span>
<span data-ttu-id="dd68c-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="dd68c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd68c-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dd68c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd68c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd68c-137">CommonParameters</span></span>
<span data-ttu-id="dd68c-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd68c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd68c-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd68c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd68c-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dd68c-140">INPUTS</span></span>

### <span data-ttu-id="dd68c-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="dd68c-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

### <span data-ttu-id="dd68c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="dd68c-142">System.String</span></span>

## <span data-ttu-id="dd68c-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd68c-143">OUTPUTS</span></span>

### <span data-ttu-id="dd68c-144">Microsoft.Azure.Commands.Network.Models.PSVpnConnectionPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="dd68c-144">Microsoft.Azure.Commands.Network.Models.PSVpnConnectionPacketCaptureResult</span></span>

## <span data-ttu-id="dd68c-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dd68c-145">NOTES</span></span>

## <span data-ttu-id="dd68c-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd68c-146">RELATED LINKS</span></span>

[<span data-ttu-id="dd68c-147">Stop-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dd68c-147">Stop-AzVpnConnectionPacketCapture</span></span>](./Stop-AzVpnConnectionPacketCapture.md)