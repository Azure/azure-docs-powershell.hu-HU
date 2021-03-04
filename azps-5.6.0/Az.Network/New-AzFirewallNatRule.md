---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
ms.openlocfilehash: 2bbac9bebd79f1ca51a7defd4c57589764b2c34e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935617"
---
# <span data-ttu-id="5dd9e-101">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="5dd9e-101">New-AzFirewallNatRule</span></span>

## <span data-ttu-id="5dd9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5dd9e-102">SYNOPSIS</span></span>
<span data-ttu-id="5dd9e-103">Tűzfal NAT-szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="5dd9e-103">Creates a Firewall NAT Rule.</span></span>

## <span data-ttu-id="5dd9e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5dd9e-104">SYNTAX</span></span>

```
New-AzFirewallNatRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]>
 [-TranslatedAddress <String>] [-TranslatedFqdn <String>] -TranslatedPort <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5dd9e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5dd9e-105">DESCRIPTION</span></span>
<span data-ttu-id="5dd9e-106">A **New-AzFirewallNatRule** parancsmag nat-szabályt hoz létre az Azure tűzfalhoz.</span><span class="sxs-lookup"><span data-stu-id="5dd9e-106">The **New-AzFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="5dd9e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5dd9e-107">EXAMPLES</span></span>

### <span data-ttu-id="5dd9e-108">1. példa: Szabály létrehozása a 10.0.0.0/24-es tcp-forgalomRA a 10.1.2.3:80-as célhelyen a 10.4.5.6:8080-as célhelyen</span><span class="sxs-lookup"><span data-stu-id="5dd9e-108">Example 1: Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```powershell
New-AzFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="5dd9e-109">Ez a példa létrehoz egy szabályt, amely a 10.0.0.0/24-es kódú, 10.1.2.3:80–10.4.5.6:8080-as célhelyen származó ÖSSZES FORGALOM.</span><span class="sxs-lookup"><span data-stu-id="5dd9e-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="5dd9e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5dd9e-110">PARAMETERS</span></span>

### <span data-ttu-id="5dd9e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dd9e-111">-DefaultProfile</span></span>
<span data-ttu-id="5dd9e-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5dd9e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5dd9e-113">-Leírás</span><span class="sxs-lookup"><span data-stu-id="5dd9e-113">-Description</span></span>
<span data-ttu-id="5dd9e-114">A szabály opcionális leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="5dd9e-114">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="5dd9e-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="5dd9e-115">-DestinationAddress</span></span>
<span data-ttu-id="5dd9e-116">A szabály célcíme</span><span class="sxs-lookup"><span data-stu-id="5dd9e-116">The destination addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dd9e-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="5dd9e-117">-DestinationPort</span></span>
<span data-ttu-id="5dd9e-118">A szabály célportjai</span><span class="sxs-lookup"><span data-stu-id="5dd9e-118">The destination ports of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dd9e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5dd9e-119">-Name</span></span>
<span data-ttu-id="5dd9e-120">A NAT-szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5dd9e-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="5dd9e-121">A névnek egyedinek kell lennie egy szabálygyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="5dd9e-121">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="5dd9e-122">-Protocol</span><span class="sxs-lookup"><span data-stu-id="5dd9e-122">-Protocol</span></span>
<span data-ttu-id="5dd9e-123">Meghatározza, hogy milyen típusú adatforgalom szűrhető ezzel a s szabálysal.</span><span class="sxs-lookup"><span data-stu-id="5dd9e-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="5dd9e-124">A támogatott protokollok a TCP és az UDP.</span><span class="sxs-lookup"><span data-stu-id="5dd9e-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="5dd9e-125">Az "Any" speciális érték engedélyezett, ami azt jelenti, hogy a TCP-nek és az UDP-nek egyaránt megfelel, más protokollok azonban nem.</span><span class="sxs-lookup"><span data-stu-id="5dd9e-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dd9e-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="5dd9e-126">-SourceAddress</span></span>
<span data-ttu-id="5dd9e-127">A szabály forráscíme</span><span class="sxs-lookup"><span data-stu-id="5dd9e-127">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dd9e-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="5dd9e-128">-SourceIpGroup</span></span>
<span data-ttu-id="5dd9e-129">A szabály forrás IP-csoportja</span><span class="sxs-lookup"><span data-stu-id="5dd9e-129">The source ipgroup of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dd9e-130">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="5dd9e-130">-TranslatedAddress</span></span>
<span data-ttu-id="5dd9e-131">A címfordítás kívánt eredményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5dd9e-131">Specifies the desired result of the address translation</span></span>

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

### <span data-ttu-id="5dd9e-132">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="5dd9e-132">-TranslatedFqdn</span></span>
<span data-ttu-id="5dd9e-133">A NAT-szabály lefordított teljes tartománya</span><span class="sxs-lookup"><span data-stu-id="5dd9e-133">The translated FQDN for this NAT rule</span></span>

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

### <span data-ttu-id="5dd9e-134">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="5dd9e-134">-TranslatedPort</span></span>
<span data-ttu-id="5dd9e-135">A portfordítás kívánt eredményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5dd9e-135">Specifies the desired result of the port translation</span></span>

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

### <span data-ttu-id="5dd9e-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5dd9e-136">-Confirm</span></span>
<span data-ttu-id="5dd9e-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5dd9e-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dd9e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5dd9e-138">-WhatIf</span></span>
<span data-ttu-id="5dd9e-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5dd9e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5dd9e-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5dd9e-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dd9e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dd9e-141">CommonParameters</span></span>
<span data-ttu-id="5dd9e-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dd9e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dd9e-143">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dd9e-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dd9e-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5dd9e-144">INPUTS</span></span>

### <span data-ttu-id="5dd9e-145">Nincs</span><span class="sxs-lookup"><span data-stu-id="5dd9e-145">None</span></span>

## <span data-ttu-id="5dd9e-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5dd9e-146">OUTPUTS</span></span>

### <span data-ttu-id="5dd9e-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="5dd9e-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="5dd9e-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5dd9e-148">NOTES</span></span>

## <span data-ttu-id="5dd9e-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5dd9e-149">RELATED LINKS</span></span>

[<span data-ttu-id="5dd9e-150">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="5dd9e-150">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="5dd9e-151">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="5dd9e-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="5dd9e-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="5dd9e-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
