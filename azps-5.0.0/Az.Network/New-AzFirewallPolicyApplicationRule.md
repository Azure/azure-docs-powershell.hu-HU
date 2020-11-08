---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
ms.openlocfilehash: aaf6e2006797a99d37bf5ece341863c34038a3dc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188118"
---
# <span data-ttu-id="44e40-101">New-AzFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="44e40-101">New-AzFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="44e40-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="44e40-102">SYNOPSIS</span></span>
<span data-ttu-id="44e40-103">Új Azure tűzfal-házirend alkalmazási szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="44e40-103">Create a new Azure Firewall Policy Application Rule</span></span>

## <span data-ttu-id="44e40-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="44e40-104">SYNTAX</span></span>

### <span data-ttu-id="44e40-105">TargetFqdn (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="44e40-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -TargetFqdn <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44e40-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="44e40-106">FqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44e40-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="44e40-107">DESCRIPTION</span></span>
<span data-ttu-id="44e40-108">A **New-AzFirewallPolicyApplicationRule** parancsmag egy alkalmazási szabályt hoz létre az Azure tűzfal házirendjéhez.</span><span class="sxs-lookup"><span data-stu-id="44e40-108">The **New-AzFirewallPolicyApplicationRule** cmdlet creates an Application Rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="44e40-109">Példák</span><span class="sxs-lookup"><span data-stu-id="44e40-109">EXAMPLES</span></span>

### <span data-ttu-id="44e40-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="44e40-110">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -TargetFqdn "*.ro", "*.com"
```

<span data-ttu-id="44e40-111">Ebben a példában egy alkalmazási szabályt hoz létre a forráscím, a protokoll és a cél FQDN-jei között.</span><span class="sxs-lookup"><span data-stu-id="44e40-111">This example creates an application rule with the source address, protocol and the target fqdns.</span></span>

### <span data-ttu-id="44e40-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="44e40-112">Example 2</span></span>

<span data-ttu-id="44e40-113">Új Azure Firewall Policy Application Rule létrehozása</span><span class="sxs-lookup"><span data-stu-id="44e40-113">Create a new Azure Firewall Policy Application Rule.</span></span> <span data-ttu-id="44e40-114">autogenerated</span><span class="sxs-lookup"><span data-stu-id="44e40-114">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzFirewallPolicyApplicationRule -Description 'Allow web service' -Name AR1 -Protocol 'http:80' -SourceAddress '192.168.0.0/16' -TargetFqdn '*.ro'
```

## <span data-ttu-id="44e40-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="44e40-115">PARAMETERS</span></span>

### <span data-ttu-id="44e40-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44e40-116">-DefaultProfile</span></span>
<span data-ttu-id="44e40-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="44e40-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44e40-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="44e40-118">-Description</span></span>
<span data-ttu-id="44e40-119">A szabály leírása</span><span class="sxs-lookup"><span data-stu-id="44e40-119">The description of the rule</span></span>

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

### <span data-ttu-id="44e40-120">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="44e40-120">-FqdnTag</span></span>
<span data-ttu-id="44e40-121">A szabály FQDN-címkéi</span><span class="sxs-lookup"><span data-stu-id="44e40-121">The FQDN Tags of the rule</span></span>

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

### <span data-ttu-id="44e40-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="44e40-122">-Name</span></span>
<span data-ttu-id="44e40-123">A kérelmezési szabály neve</span><span class="sxs-lookup"><span data-stu-id="44e40-123">The name of the Application Rule</span></span>

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

### <span data-ttu-id="44e40-124">-Protocol</span><span class="sxs-lookup"><span data-stu-id="44e40-124">-Protocol</span></span>
<span data-ttu-id="44e40-125">A szabály protokolljai</span><span class="sxs-lookup"><span data-stu-id="44e40-125">The protocols of the rule</span></span>

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

### <span data-ttu-id="44e40-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="44e40-126">-SourceAddress</span></span>
<span data-ttu-id="44e40-127">A szabály forrásául szolgáló cím</span><span class="sxs-lookup"><span data-stu-id="44e40-127">The source addresses of the rule</span></span>

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

### <span data-ttu-id="44e40-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="44e40-128">-SourceIpGroup</span></span>
<span data-ttu-id="44e40-129">A szabály forrás ipgroups</span><span class="sxs-lookup"><span data-stu-id="44e40-129">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="44e40-130">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="44e40-130">-TargetFqdn</span></span>
<span data-ttu-id="44e40-131">A szabály cél FQDN-jei</span><span class="sxs-lookup"><span data-stu-id="44e40-131">The target FQDNs of the rule</span></span>

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

### <span data-ttu-id="44e40-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="44e40-132">-Confirm</span></span>
<span data-ttu-id="44e40-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="44e40-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44e40-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44e40-134">-WhatIf</span></span>
<span data-ttu-id="44e40-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="44e40-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44e40-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="44e40-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44e40-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44e40-137">CommonParameters</span></span>
<span data-ttu-id="44e40-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="44e40-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44e40-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="44e40-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44e40-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="44e40-140">INPUTS</span></span>

### <span data-ttu-id="44e40-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="44e40-141">None</span></span>

## <span data-ttu-id="44e40-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="44e40-142">OUTPUTS</span></span>

### <span data-ttu-id="44e40-143">Microsoft. Azure. commands. Network. models. PSAzureFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="44e40-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="44e40-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="44e40-144">NOTES</span></span>

## <span data-ttu-id="44e40-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="44e40-145">RELATED LINKS</span></span>