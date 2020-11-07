---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
ms.openlocfilehash: 6aad78a873b1eb24f1534c9b8c0b38d1567ee2ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670344"
---
# <span data-ttu-id="1f92c-101">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="1f92c-101">New-AzFirewallApplicationRule</span></span>

## <span data-ttu-id="1f92c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1f92c-102">SYNOPSIS</span></span>
<span data-ttu-id="1f92c-103">Tűzfal-alkalmazási szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1f92c-103">Creates a Firewall Application Rule.</span></span>

## <span data-ttu-id="1f92c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1f92c-104">SYNTAX</span></span>

### <span data-ttu-id="1f92c-105">TargetFqdn (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1f92c-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f92c-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="1f92c-106">FqdnTag</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f92c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1f92c-107">DESCRIPTION</span></span>
<span data-ttu-id="1f92c-108">A **New-AzFirewallApplicationRule** parancsmag létrehoz egy szabályt az Azure tűzfalhoz.</span><span class="sxs-lookup"><span data-stu-id="1f92c-108">The **New-AzFirewallApplicationRule** cmdlet creates an application rule for Azure Firewall.</span></span>

## <span data-ttu-id="1f92c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1f92c-109">EXAMPLES</span></span>

### <span data-ttu-id="1f92c-110">1: szabály létrehozása az összes HTTPS-forgalom engedélyezéséhez a 10.0.0.0-ból</span><span class="sxs-lookup"><span data-stu-id="1f92c-110">1:  Create a rule to allow all HTTPS traffic from 10.0.0.0</span></span>
```
New-AzFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

<span data-ttu-id="1f92c-111">Ez a példa létrehoz egy szabályt, amely lehetővé teszi az 443-on lévő összes HTTPS-forgalom használatát a 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="1f92c-111">This example creates a rule which will allow all HTTPS traffic on port 443 from 10.0.0.0.</span></span>

### <span data-ttu-id="1f92c-112">2: szabály létrehozása a 10.0.0.0/24 alhálózat WindowsUpdate engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="1f92c-112">2:  Create a rule to allow WindowsUpdate for 10.0.0.0/24 subnet</span></span>
```
New-AzFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

<span data-ttu-id="1f92c-113">Ez a példa létrehoz egy szabályt, amely lehetővé teszi a Windows-frissítések 10.0.0.0/24 tartományhoz való forgalmát.</span><span class="sxs-lookup"><span data-stu-id="1f92c-113">This example creates a rule which will allow traffic for Windows Updates for 10.0.0.0/24 domain.</span></span>

## <span data-ttu-id="1f92c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1f92c-114">PARAMETERS</span></span>

### <span data-ttu-id="1f92c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f92c-115">-DefaultProfile</span></span>
<span data-ttu-id="1f92c-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1f92c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f92c-117">-Leírás</span><span class="sxs-lookup"><span data-stu-id="1f92c-117">-Description</span></span>
<span data-ttu-id="1f92c-118">A szabály választható leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f92c-118">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="1f92c-119">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="1f92c-119">-FqdnTag</span></span>
<span data-ttu-id="1f92c-120">A szabályhoz tartozó FQDN-címkék listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f92c-120">Specifies a list of FQDN Tags for this rule.</span></span> <span data-ttu-id="1f92c-121">A rendelkezésre álló címkéket a [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) parancsmag használatával lehet beolvasni.</span><span class="sxs-lookup"><span data-stu-id="1f92c-121">The available tags can be retrieved using [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) cmdlet.</span></span>

```yaml
Type: System.String[]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f92c-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1f92c-122">-Name</span></span>
<span data-ttu-id="1f92c-123">Az alkalmazási szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f92c-123">Specifies the name of this application rule.</span></span> <span data-ttu-id="1f92c-124">A névnek egyedinek kell lennie egy szabály-gyűjteményen belül.</span><span class="sxs-lookup"><span data-stu-id="1f92c-124">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="1f92c-125">-Protocol</span><span class="sxs-lookup"><span data-stu-id="1f92c-125">-Protocol</span></span>
<span data-ttu-id="1f92c-126">Adja meg, hogy milyen típusú forgalmat szeretne szűrni a szabály.</span><span class="sxs-lookup"><span data-stu-id="1f92c-126">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="1f92c-127">A formátum <protocol type> : <port> .</span><span class="sxs-lookup"><span data-stu-id="1f92c-127">The format is <protocol type>:<port>.</span></span> <span data-ttu-id="1f92c-128">Például "http: 80" vagy "https: 443".</span><span class="sxs-lookup"><span data-stu-id="1f92c-128">For example, "http:80" or "https:443".</span></span>
<span data-ttu-id="1f92c-129">A protokoll a TargetFqdn használatakor kötelező, de a FqdnTag nem használható.</span><span class="sxs-lookup"><span data-stu-id="1f92c-129">Protocol is mandatory when TargetFqdn is used, but it cannot be used with FqdnTag.</span></span> <span data-ttu-id="1f92c-130">A támogatott protokollok a HTTP és a HTTPS.</span><span class="sxs-lookup"><span data-stu-id="1f92c-130">The supported protocols are HTTP and HTTPS.</span></span>

```yaml
Type: System.String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f92c-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="1f92c-131">-SourceAddress</span></span>
<span data-ttu-id="1f92c-132">A szabály forrásául szolgáló cím</span><span class="sxs-lookup"><span data-stu-id="1f92c-132">The source addresses of the rule</span></span>

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

### <span data-ttu-id="1f92c-133">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="1f92c-133">-TargetFqdn</span></span>
<span data-ttu-id="1f92c-134">A szabály által szűrt tartománynevek listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f92c-134">Specifies a list of domain names filtered by this rule.</span></span>
<span data-ttu-id="1f92c-135">A formázásával karakter (' *) csak a lista teljes tartománynevének első karaktere. Használatakor a formázásával tetszőleges számú karaktert helyettesít. (például a "* MSN.com" a MSN.com és annak összes altartományával egyezik)</span><span class="sxs-lookup"><span data-stu-id="1f92c-135">The asterik character, ' *', is accepted only as the first character of an FQDN in the list. When used, the asterik matches any number of characters. (e.g. '* msn.com' will match msn.com and all its subdomains)</span></span>

```yaml
Type: System.String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f92c-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1f92c-136">-Confirm</span></span>
<span data-ttu-id="1f92c-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1f92c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f92c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f92c-138">-WhatIf</span></span>
<span data-ttu-id="1f92c-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1f92c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f92c-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1f92c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f92c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f92c-141">CommonParameters</span></span>
<span data-ttu-id="1f92c-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1f92c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f92c-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f92c-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f92c-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f92c-144">INPUTS</span></span>

### <span data-ttu-id="1f92c-145">Nincs</span><span class="sxs-lookup"><span data-stu-id="1f92c-145">None</span></span>

## <span data-ttu-id="1f92c-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f92c-146">OUTPUTS</span></span>

### <span data-ttu-id="1f92c-147">Microsoft. Azure. commands. Network. models. PSAzureFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="1f92c-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule</span></span>

## <span data-ttu-id="1f92c-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1f92c-148">NOTES</span></span>

## <span data-ttu-id="1f92c-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f92c-149">RELATED LINKS</span></span>

[<span data-ttu-id="1f92c-150">Új – AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1f92c-150">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="1f92c-151">Új – AzFirewall</span><span class="sxs-lookup"><span data-stu-id="1f92c-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="1f92c-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="1f92c-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="1f92c-153">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="1f92c-153">Get-AzFirewallFqdnTag</span></span>](./Get-AzFirewallFqdnTag.md)
