---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyintrusiondetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetection.md
ms.openlocfilehash: bc3c71c8900be049dce7b00b698068e96ccc8519
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151715"
---
# <span data-ttu-id="5bb6a-101">New-AzFirewallPolicyIntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="5bb6a-101">New-AzFirewallPolicyIntrusionDetection</span></span>

## <span data-ttu-id="5bb6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bb6a-102">SYNOPSIS</span></span>
<span data-ttu-id="5bb6a-103">Új Azure tűzfal házirend-behatolásészlelés létrehozása a tűzfal házirendhez való társításhoz</span><span class="sxs-lookup"><span data-stu-id="5bb6a-103">Creates a new Azure Firewall Policy Intrusion Detection to associate with Firewall Policy</span></span>

## <span data-ttu-id="5bb6a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5bb6a-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetection -Mode <String>
 [-SignatureOverride <PSAzureFirewallPolicyIntrusionDetectionSignatureOverride[]>]
 [-BypassTraffic <PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bb6a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5bb6a-105">DESCRIPTION</span></span>
<span data-ttu-id="5bb6a-106">A **New-AzFirewallPolicyIntrusionDetection parancsmag** létrehoz egy Azure tűzfalházitér-házirend intrusion észlelési objektumot.</span><span class="sxs-lookup"><span data-stu-id="5bb6a-106">The **New-AzFirewallPolicyIntrusionDetection** cmdlet creates an Azure Firewall Policy Intrusion Detection Object.</span></span>

## <span data-ttu-id="5bb6a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5bb6a-107">EXAMPLES</span></span>

### <span data-ttu-id="5bb6a-108">1. példa: 1.</span><span class="sxs-lookup"><span data-stu-id="5bb6a-108">Example 1: 1.</span></span> <span data-ttu-id="5bb6a-109">Intrusion detection with mode</span><span class="sxs-lookup"><span data-stu-id="5bb6a-109">Create intrusion detection with mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert"
```

<span data-ttu-id="5bb6a-110">Ez a példa behúzás észlelését hozza létre riasztási (észlelési) módban</span><span class="sxs-lookup"><span data-stu-id="5bb6a-110">This example creates intrusion detection with Alert (detection) mode</span></span>

### <span data-ttu-id="5bb6a-111">2. példa: 2.</span><span class="sxs-lookup"><span data-stu-id="5bb6a-111">Example 2: 2.</span></span> <span data-ttu-id="5bb6a-112">Beszúrás észlelése aláírás-felülbírálásokkal</span><span class="sxs-lookup"><span data-stu-id="5bb6a-112">Create intrusion detection with signature overrides</span></span>
```powershell
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride
```

<span data-ttu-id="5bb6a-113">Ez a példa speciális aláírás-felülbírálással hoz létre behatolásészlelést</span><span class="sxs-lookup"><span data-stu-id="5bb6a-113">This example creates intrusion detection with specific signature override</span></span>

### <span data-ttu-id="5bb6a-114">3. példa: 3.</span><span class="sxs-lookup"><span data-stu-id="5bb6a-114">Example 3: 3.</span></span> <span data-ttu-id="5bb6a-115">Tűzfal házirend létrehozása a forgalom megkerülése beállítással konfigurált intrusion észleléssel</span><span class="sxs-lookup"><span data-stu-id="5bb6a-115">Create firewall policy with intrusion detection configured with bypass traffic setting</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress "10.0.0.0"
PS C:\> $intrusionDetection = New-AzFirewallPolicyIntrusionDetection -Mode "Deny" -BypassTraffic $bypass
PS C:\> New-AzFirewallPolicy -Name fp1 -Location "westus2" -ResourceGroup TestRg -SkuTier "Premium" -IntrusionDetection $intrusionDetection
```

<span data-ttu-id="5bb6a-116">Ez a példa behúzás észlelését hozza létre a forgalom megkerülése beállítással</span><span class="sxs-lookup"><span data-stu-id="5bb6a-116">This example creates intrusion detection with bypass traffic setting</span></span>

## <span data-ttu-id="5bb6a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bb6a-117">PARAMETERS</span></span>

### <span data-ttu-id="5bb6a-118">-BypassTraffic</span><span class="sxs-lookup"><span data-stu-id="5bb6a-118">-BypassTraffic</span></span>
<span data-ttu-id="5bb6a-119">A megkerülni való forgalomra vonatkozó szabályok listája.</span><span class="sxs-lookup"><span data-stu-id="5bb6a-119">List of rules for traffic to bypass.</span></span>

```yaml
Type: PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb6a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bb6a-120">-DefaultProfile</span></span>
<span data-ttu-id="5bb6a-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5bb6a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bb6a-122">-Mód</span><span class="sxs-lookup"><span data-stu-id="5bb6a-122">-Mode</span></span>
<span data-ttu-id="5bb6a-123">Intrusion Detection general state.</span><span class="sxs-lookup"><span data-stu-id="5bb6a-123">Intrusion Detection general state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Off, Alert, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb6a-124">-SignatureOverride</span><span class="sxs-lookup"><span data-stu-id="5bb6a-124">-SignatureOverride</span></span>
<span data-ttu-id="5bb6a-125">Az aláírások egyes államai.</span><span class="sxs-lookup"><span data-stu-id="5bb6a-125">List of specific signatures states.</span></span>

```yaml
Type: PSAzureFirewallPolicyIntrusionDetectionSignatureOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb6a-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5bb6a-126">-Confirm</span></span>
<span data-ttu-id="5bb6a-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5bb6a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bb6a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bb6a-128">-WhatIf</span></span>
<span data-ttu-id="5bb6a-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5bb6a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bb6a-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5bb6a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bb6a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bb6a-131">CommonParameters</span></span>
<span data-ttu-id="5bb6a-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bb6a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bb6a-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5bb6a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bb6a-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5bb6a-134">INPUTS</span></span>

### <span data-ttu-id="5bb6a-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="5bb6a-135">None</span></span>

## <span data-ttu-id="5bb6a-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5bb6a-136">OUTPUTS</span></span>

### <span data-ttu-id="5bb6a-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="5bb6a-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetection</span></span>

## <span data-ttu-id="5bb6a-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5bb6a-138">NOTES</span></span>

## <span data-ttu-id="5bb6a-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5bb6a-139">RELATED LINKS</span></span>
