---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvpnconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
ms.openlocfilehash: 720b81b858799e2930ed3d2cdd45e25220697e6a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202404"
---
# <span data-ttu-id="f1e76-101">Start-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f1e76-101">Start-AzVpnConnectionPacketCapture</span></span>

## <span data-ttu-id="f1e76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1e76-102">SYNOPSIS</span></span>
<span data-ttu-id="f1e76-103">Elindítja a csomagrögzítési műveletet Vpn-kapcsolaton.</span><span class="sxs-lookup"><span data-stu-id="f1e76-103">Starts Packet Capture Operation on a Vpn Connection.</span></span>

## <span data-ttu-id="f1e76-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f1e76-104">SYNTAX</span></span>

### <span data-ttu-id="f1e76-105">ByVpnConnectionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f1e76-105">ByVpnConnectionName (Default)</span></span>
```
Start-AzVpnConnectionPacketCapture -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-FilterData <String>] -LinkConnectionName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1e76-106">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="f1e76-106">ByVpnConnectionObject</span></span>
```
Start-AzVpnConnectionPacketCapture -InputObject <PSVpnConnection> [-FilterData <String>]
 -LinkConnectionName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f1e76-107">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="f1e76-107">ByVpnConnectionResourceId</span></span>
```
Start-AzVpnConnectionPacketCapture -ResourceId <String> [-FilterData <String>] -LinkConnectionName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1e76-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f1e76-108">DESCRIPTION</span></span>
<span data-ttu-id="f1e76-109">Elindítja a csomagrögzítési műveletet Vpn-kapcsolaton.</span><span class="sxs-lookup"><span data-stu-id="f1e76-109">Starts Packet Capture Operation on a Vpn Connection.</span></span>

## <span data-ttu-id="f1e76-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f1e76-110">EXAMPLES</span></span>

### <span data-ttu-id="f1e76-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="f1e76-111">Example 1</span></span>
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

### <span data-ttu-id="f1e76-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="f1e76-112">Example 2</span></span>
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

## <span data-ttu-id="f1e76-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1e76-113">PARAMETERS</span></span>

### <span data-ttu-id="f1e76-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1e76-114">-AsJob</span></span>
<span data-ttu-id="f1e76-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f1e76-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1e76-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1e76-116">-DefaultProfile</span></span>
<span data-ttu-id="f1e76-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f1e76-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1e76-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="f1e76-118">-FilterData</span></span>
<span data-ttu-id="f1e76-119">A csomagrögzítés indítási beállításai Vpn-kapcsolaton.</span><span class="sxs-lookup"><span data-stu-id="f1e76-119">Filter options for start packet capture on Vpn connection.</span></span>

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

### <span data-ttu-id="f1e76-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1e76-120">-InputObject</span></span>
<span data-ttu-id="f1e76-121">A Vpn-kapcsolatobjektum, amelyben a csomagrögzítést el kell kezdeni.</span><span class="sxs-lookup"><span data-stu-id="f1e76-121">The Vpn connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="f1e76-122">-LinkConnectionName</span><span class="sxs-lookup"><span data-stu-id="f1e76-122">-LinkConnectionName</span></span>
<span data-ttu-id="f1e76-123">A SiteLinkConnection nevei.</span><span class="sxs-lookup"><span data-stu-id="f1e76-123">The names of the SiteLinkConnection.</span></span>

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

### <span data-ttu-id="f1e76-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f1e76-124">-Name</span></span>
<span data-ttu-id="f1e76-125">A Vpn-kapcsolat neve, ahol a csomagrögzítést el kell kezdeni.</span><span class="sxs-lookup"><span data-stu-id="f1e76-125">The Vpn connection name where packet capture to be started.</span></span>

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

### <span data-ttu-id="f1e76-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="f1e76-126">-ParentResourceName</span></span>
<span data-ttu-id="f1e76-127">A szülő Vpngateway neve.</span><span class="sxs-lookup"><span data-stu-id="f1e76-127">The name of the Parent Vpngateway.</span></span>

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

### <span data-ttu-id="f1e76-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1e76-128">-ResourceGroupName</span></span>
<span data-ttu-id="f1e76-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f1e76-129">The resource group name.</span></span>

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

### <span data-ttu-id="f1e76-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1e76-130">-ResourceId</span></span>
<span data-ttu-id="f1e76-131">A VpnConnection Azure-erőforrásazonosítója, ahol a csomagrögzítést el kell kezdeni.</span><span class="sxs-lookup"><span data-stu-id="f1e76-131">The Azure resource ID of the VpnConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="f1e76-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1e76-132">-Confirm</span></span>
<span data-ttu-id="f1e76-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f1e76-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1e76-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1e76-134">-WhatIf</span></span>
<span data-ttu-id="f1e76-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f1e76-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1e76-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f1e76-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1e76-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1e76-137">CommonParameters</span></span>
<span data-ttu-id="f1e76-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1e76-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1e76-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1e76-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1e76-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f1e76-140">INPUTS</span></span>

### <span data-ttu-id="f1e76-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="f1e76-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

### <span data-ttu-id="f1e76-142">System.String</span><span class="sxs-lookup"><span data-stu-id="f1e76-142">System.String</span></span>

## <span data-ttu-id="f1e76-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1e76-143">OUTPUTS</span></span>

### <span data-ttu-id="f1e76-144">Microsoft.Azure.Commands.Network.Models.PSVpnConnectionPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="f1e76-144">Microsoft.Azure.Commands.Network.Models.PSVpnConnectionPacketCaptureResult</span></span>

## <span data-ttu-id="f1e76-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f1e76-145">NOTES</span></span>

## <span data-ttu-id="f1e76-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1e76-146">RELATED LINKS</span></span>

[<span data-ttu-id="f1e76-147">Stop-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f1e76-147">Stop-AzVpnConnectionPacketCapture</span></span>](./Stop-AzVpnConnectionPacketCapture.md)