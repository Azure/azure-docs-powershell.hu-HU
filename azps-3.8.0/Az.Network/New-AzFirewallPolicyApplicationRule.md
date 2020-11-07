---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
ms.openlocfilehash: 1b9fd10e11cb283f880979e7e4a5d703521c9a87
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93844989"
---
# <span data-ttu-id="498ac-101">New-AzFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="498ac-101">New-AzFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="498ac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="498ac-102">SYNOPSIS</span></span>
<span data-ttu-id="498ac-103">Új Azure tűzfal-házirend alkalmazási szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="498ac-103">Create a new Azure Firewall Policy Application Rule</span></span>

## <span data-ttu-id="498ac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="498ac-104">SYNTAX</span></span>

### <span data-ttu-id="498ac-105">TargetFqdn (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="498ac-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="498ac-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="498ac-106">FqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="498ac-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="498ac-107">DESCRIPTION</span></span>
<span data-ttu-id="498ac-108">A **New-AzFirewallPolicyApplicationRule** parancsmag egy alkalmazási szabályt hoz létre az Azure tűzfal házirendjéhez.</span><span class="sxs-lookup"><span data-stu-id="498ac-108">The **New-AzFirewallPolicyApplicationRule** cmdlet creates an Application Rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="498ac-109">Példák</span><span class="sxs-lookup"><span data-stu-id="498ac-109">EXAMPLES</span></span>

### <span data-ttu-id="498ac-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="498ac-110">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -TargetFqdn "*.ro", "*.com"
```

<span data-ttu-id="498ac-111">Ebben a példában egy alkalmazási szabályt hoz létre a forráscím, a protokoll és a cél FQDN-jei között.</span><span class="sxs-lookup"><span data-stu-id="498ac-111">This example creates an application rule with the source address, protocol and the target fqdns.</span></span>

## <span data-ttu-id="498ac-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="498ac-112">PARAMETERS</span></span>

### <span data-ttu-id="498ac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="498ac-113">-DefaultProfile</span></span>
<span data-ttu-id="498ac-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="498ac-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="498ac-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="498ac-115">-Description</span></span>
<span data-ttu-id="498ac-116">A szabály leírása</span><span class="sxs-lookup"><span data-stu-id="498ac-116">The description of the rule</span></span>

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

### <span data-ttu-id="498ac-117">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="498ac-117">-FqdnTag</span></span>
<span data-ttu-id="498ac-118">A szabály FQDN-címkéi</span><span class="sxs-lookup"><span data-stu-id="498ac-118">The FQDN Tags of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="498ac-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="498ac-119">-Name</span></span>
<span data-ttu-id="498ac-120">A kérelmezési szabály neve</span><span class="sxs-lookup"><span data-stu-id="498ac-120">The name of the Application Rule</span></span>

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

### <span data-ttu-id="498ac-121">-Protocol</span><span class="sxs-lookup"><span data-stu-id="498ac-121">-Protocol</span></span>
<span data-ttu-id="498ac-122">A szabály protokolljai</span><span class="sxs-lookup"><span data-stu-id="498ac-122">The protocols of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="498ac-123">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="498ac-123">-SourceAddress</span></span>
<span data-ttu-id="498ac-124">A szabály forrásául szolgáló cím</span><span class="sxs-lookup"><span data-stu-id="498ac-124">The source addresses of the rule</span></span>

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

### <span data-ttu-id="498ac-125">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="498ac-125">-TargetFqdn</span></span>
<span data-ttu-id="498ac-126">A szabály cél FQDN-jei</span><span class="sxs-lookup"><span data-stu-id="498ac-126">The target FQDNs of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="498ac-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="498ac-127">-Confirm</span></span>
<span data-ttu-id="498ac-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="498ac-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="498ac-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="498ac-129">-WhatIf</span></span>
<span data-ttu-id="498ac-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="498ac-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="498ac-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="498ac-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="498ac-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="498ac-132">CommonParameters</span></span>
<span data-ttu-id="498ac-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="498ac-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="498ac-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="498ac-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="498ac-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="498ac-135">INPUTS</span></span>

### <span data-ttu-id="498ac-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="498ac-136">None</span></span>

## <span data-ttu-id="498ac-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="498ac-137">OUTPUTS</span></span>

### <span data-ttu-id="498ac-138">Microsoft. Azure. commands. Network. models. PSAzureFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="498ac-138">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="498ac-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="498ac-139">NOTES</span></span>

## <span data-ttu-id="498ac-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="498ac-140">RELATED LINKS</span></span>
