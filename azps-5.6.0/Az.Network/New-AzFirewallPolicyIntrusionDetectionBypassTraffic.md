---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicyintrusiondetectionbypasstraffic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionBypassTraffic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionBypassTraffic.md
ms.openlocfilehash: dd15a93fc2df022a0b016f9dae4845da13240534
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933465"
---
# <span data-ttu-id="f435b-101">New-AzFirewallPolicyIntrusionDetectionBypassTraffic</span><span class="sxs-lookup"><span data-stu-id="f435b-101">New-AzFirewallPolicyIntrusionDetectionBypassTraffic</span></span>

## <span data-ttu-id="f435b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f435b-102">SYNOPSIS</span></span>
<span data-ttu-id="f435b-103">Új Azure firewall policy intrusion Detection Bypass Traffic Setting (Adatforgalom megkerülése beállítás) létrehozása</span><span class="sxs-lookup"><span data-stu-id="f435b-103">Creates a new Azure Firewall Policy Intrusion Detection Bypass Traffic Setting</span></span>

## <span data-ttu-id="f435b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f435b-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name <String> [-Description <String>] -Protocol <String>
 [-SourceAddress <String[]>] [-DestinationAddress <String[]>] [-SourceIpGroup <String[]>]
 [-DestinationIpGroup <String[]>] -DestinationPort <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f435b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f435b-105">DESCRIPTION</span></span>
<span data-ttu-id="f435b-106">A **New-AzFirewallPolicyIntrusionDetectionBypassTraffic** parancsmag létrehoz egy Azure tűzfalházi házirend-behúzás észlelését a forgalomobjektum megkerülése során.</span><span class="sxs-lookup"><span data-stu-id="f435b-106">The **New-AzFirewallPolicyIntrusionDetectionBypassTraffic** cmdlet creates an Azure Firewall Policy Intrusion Detection Bypass Traffic Object.</span></span>

## <span data-ttu-id="f435b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f435b-107">EXAMPLES</span></span>

### <span data-ttu-id="f435b-108">1. példa: 1.</span><span class="sxs-lookup"><span data-stu-id="f435b-108">Example 1: 1.</span></span> <span data-ttu-id="f435b-109">Adatforgalom megkerülése adott port- és forráscímekkel</span><span class="sxs-lookup"><span data-stu-id="f435b-109">Create bypass traffic with specific port and source address</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress "*"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Deny" -BypassTraffic $bypass
```

<span data-ttu-id="f435b-110">Ez a példa behúzás észlelését hozza létre a forgalom megkerülése beállítással</span><span class="sxs-lookup"><span data-stu-id="f435b-110">This example creates intrusion detection with bypass traffic setting</span></span>

## <span data-ttu-id="f435b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f435b-111">PARAMETERS</span></span>

### <span data-ttu-id="f435b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f435b-112">-DefaultProfile</span></span>
<span data-ttu-id="f435b-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f435b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f435b-114">-Leírás</span><span class="sxs-lookup"><span data-stu-id="f435b-114">-Description</span></span>
<span data-ttu-id="f435b-115">Figyelmen kívül kell mellőzni a beállítás leírását.</span><span class="sxs-lookup"><span data-stu-id="f435b-115">Bypass setting description.</span></span>

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

### <span data-ttu-id="f435b-116">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="f435b-116">-DestinationAddress</span></span>
<span data-ttu-id="f435b-117">A cél IP-címek vagy -tartományok listája.</span><span class="sxs-lookup"><span data-stu-id="f435b-117">List of destination IP addresses or ranges.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f435b-118">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="f435b-118">-DestinationIpGroup</span></span>
<span data-ttu-id="f435b-119">A cél IpGroups listája.</span><span class="sxs-lookup"><span data-stu-id="f435b-119">List of destination IpGroups.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f435b-120">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="f435b-120">-DestinationPort</span></span>
<span data-ttu-id="f435b-121">A célportok vagy tartományok listája.</span><span class="sxs-lookup"><span data-stu-id="f435b-121">List of destination ports or ranges.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f435b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f435b-122">-Name</span></span>
<span data-ttu-id="f435b-123">A beállítás nevének megkerülése</span><span class="sxs-lookup"><span data-stu-id="f435b-123">Bypass setting name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f435b-124">-Protocol</span><span class="sxs-lookup"><span data-stu-id="f435b-124">-Protocol</span></span>
<span data-ttu-id="f435b-125">Protokollbeállítás megkerülése</span><span class="sxs-lookup"><span data-stu-id="f435b-125">Bypass setting protocol.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: TCP, UDP, ICMP, ANY

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f435b-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="f435b-126">-SourceAddress</span></span>
<span data-ttu-id="f435b-127">Forrás IP-címek vagy -tartományok listája.</span><span class="sxs-lookup"><span data-stu-id="f435b-127">List of source IP addresses or ranges.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f435b-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="f435b-128">-SourceIpGroup</span></span>
<span data-ttu-id="f435b-129">A forrás IpGroups listája.</span><span class="sxs-lookup"><span data-stu-id="f435b-129">List of source IpGroups.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f435b-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f435b-130">-Confirm</span></span>
<span data-ttu-id="f435b-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f435b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f435b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f435b-132">-WhatIf</span></span>
<span data-ttu-id="f435b-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f435b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f435b-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f435b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f435b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f435b-135">CommonParameters</span></span>
<span data-ttu-id="f435b-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f435b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f435b-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f435b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f435b-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f435b-138">INPUTS</span></span>

### <span data-ttu-id="f435b-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="f435b-139">None</span></span>

## <span data-ttu-id="f435b-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f435b-140">OUTPUTS</span></span>

### <span data-ttu-id="f435b-141">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting</span><span class="sxs-lookup"><span data-stu-id="f435b-141">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting</span></span>

## <span data-ttu-id="f435b-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f435b-142">NOTES</span></span>

## <span data-ttu-id="f435b-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f435b-143">RELATED LINKS</span></span>
