---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRule.md
ms.openlocfilehash: 8a59f09184c7042b12abbd549398ca4690ace235
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680326"
---
# <span data-ttu-id="0a3c8-101">New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="0a3c8-101">New-AzureRmFirewallApplicationRule</span></span>

## <span data-ttu-id="0a3c8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0a3c8-102">SYNOPSIS</span></span>
<span data-ttu-id="0a3c8-103">Tűzfal-alkalmazási szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0a3c8-103">Creates a Firewall Application Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a3c8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0a3c8-104">SYNTAX</span></span>

### <span data-ttu-id="0a3c8-105">TargetFqdn (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0a3c8-105">TargetFqdn (Default)</span></span>
```
New-AzureRmFirewallApplicationRule -Name <String> [-Description <String>]
 [-SourceAddress <System.Collections.Generic.List`1[System.String]>]
 -TargetFqdn <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a3c8-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="0a3c8-106">FqdnTag</span></span>
```
New-AzureRmFirewallApplicationRule -Name <String> [-Description <String>]
 [-SourceAddress <System.Collections.Generic.List`1[System.String]>]
 -FqdnTag <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a3c8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0a3c8-107">DESCRIPTION</span></span>
<span data-ttu-id="0a3c8-108">A **New-AzureRmFirewallApplicationRule** parancsmag létrehoz egy szabályt az Azure tűzfalhoz.</span><span class="sxs-lookup"><span data-stu-id="0a3c8-108">The **New-AzureRmFirewallApplicationRule** cmdlet creates an application rule for Azure Firewall.</span></span>

## <span data-ttu-id="0a3c8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0a3c8-109">EXAMPLES</span></span>

### <span data-ttu-id="0a3c8-110">1: szabály létrehozása az összes HTTPS-forgalom engedélyezéséhez a 10.0.0.0-ból</span><span class="sxs-lookup"><span data-stu-id="0a3c8-110">1:  Create a rule to allow all HTTPS traffic from 10.0.0.0</span></span>
```
New-AzureRmFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

<span data-ttu-id="0a3c8-111">Ez a példa létrehoz egy szabályt, amely lehetővé teszi az 443-on lévő összes HTTPS-forgalom használatát a 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="0a3c8-111">This example creates a rule which will allow all HTTPS traffic on port 443 from 10.0.0.0.</span></span>

### <span data-ttu-id="0a3c8-112">2: szabály létrehozása a 10.0.0.0/24 alhálózat WindowsUpdate engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="0a3c8-112">2:  Create a rule to allow WindowsUpdate for 10.0.0.0/24 subnet</span></span>
```
New-AzureRmFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

<span data-ttu-id="0a3c8-113">Ez a példa létrehoz egy szabályt, amely lehetővé teszi a Windows-frissítések 10.0.0.0/24 tartományhoz való forgalmát.</span><span class="sxs-lookup"><span data-stu-id="0a3c8-113">This example creates a rule which will allow traffic for Windows Updates for 10.0.0.0/24 domain.</span></span>

## <span data-ttu-id="0a3c8-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0a3c8-114">PARAMETERS</span></span>

### <span data-ttu-id="0a3c8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a3c8-115">-DefaultProfile</span></span>
<span data-ttu-id="0a3c8-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0a3c8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a3c8-117">-Leírás</span><span class="sxs-lookup"><span data-stu-id="0a3c8-117">-Description</span></span>
<span data-ttu-id="0a3c8-118">A szabály választható leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a3c8-118">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="0a3c8-119">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="0a3c8-119">-FqdnTag</span></span>
<span data-ttu-id="0a3c8-120">A szabályhoz tartozó FQDN-címkék listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a3c8-120">Specifies a list of FQDN Tags for this rule.</span></span> <span data-ttu-id="0a3c8-121">A rendelkezésre álló címkéket a [Get-AzureRmFirewallFqdnTag](./Get-AzureRmFirewallFqdnTag.md) parancsmag használatával lehet beolvasni.</span><span class="sxs-lookup"><span data-stu-id="0a3c8-121">The available tags can be retrieved using [Get-AzureRmFirewallFqdnTag](./Get-AzureRmFirewallFqdnTag.md) cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a3c8-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0a3c8-122">-Name</span></span>
<span data-ttu-id="0a3c8-123">Az alkalmazási szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a3c8-123">Specifies the name of this application rule.</span></span> <span data-ttu-id="0a3c8-124">A névnek egyedinek kell lennie egy szabály-gyűjteményen belül.</span><span class="sxs-lookup"><span data-stu-id="0a3c8-124">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="0a3c8-125">-Protocol</span><span class="sxs-lookup"><span data-stu-id="0a3c8-125">-Protocol</span></span>
<span data-ttu-id="0a3c8-126">Adja meg, hogy milyen típusú forgalmat szeretne szűrni a szabály.</span><span class="sxs-lookup"><span data-stu-id="0a3c8-126">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="0a3c8-127">A formátum <protocol type> : <port> .</span><span class="sxs-lookup"><span data-stu-id="0a3c8-127">The format is <protocol type>:<port>.</span></span> <span data-ttu-id="0a3c8-128">Például "http: 80" vagy "https: 443".</span><span class="sxs-lookup"><span data-stu-id="0a3c8-128">For example, "http:80" or "https:443".</span></span>
<span data-ttu-id="0a3c8-129">A protokoll a TargetFqdn használatakor kötelező, de a FqdnTag nem használható.</span><span class="sxs-lookup"><span data-stu-id="0a3c8-129">Protocol is mandatory when TargetFqdn is used, but it cannot be used with FqdnTag.</span></span> <span data-ttu-id="0a3c8-130">A támogatott protokollok a HTTP és a HTTPS.</span><span class="sxs-lookup"><span data-stu-id="0a3c8-130">The supported protocols are HTTP and HTTPS.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a3c8-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="0a3c8-131">-SourceAddress</span></span>
<span data-ttu-id="0a3c8-132">A szabály forrásául szolgáló cím</span><span class="sxs-lookup"><span data-stu-id="0a3c8-132">The source addresses of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a3c8-133">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="0a3c8-133">-TargetFqdn</span></span>
<span data-ttu-id="0a3c8-134">A szabály által szűrt tartománynevek listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a3c8-134">Specifies a list of domain names filtered by this rule.</span></span>
<span data-ttu-id="0a3c8-135">A formázásával karakter (' *) csak a lista teljes tartománynevének első karaktere. Használatakor a formázásával tetszőleges számú karaktert helyettesít. (például a "* MSN.com" a MSN.com és annak összes altartományával egyezik)</span><span class="sxs-lookup"><span data-stu-id="0a3c8-135">The asterik character, ' *', is accepted only as the first character of an FQDN in the list. When used, the asterik matches any number of characters. (e.g. '* msn.com' will match msn.com and all its subdomains)</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a3c8-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0a3c8-136">-Confirm</span></span>
<span data-ttu-id="0a3c8-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0a3c8-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a3c8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a3c8-138">-WhatIf</span></span>
<span data-ttu-id="0a3c8-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0a3c8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a3c8-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0a3c8-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a3c8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a3c8-141">CommonParameters</span></span>
<span data-ttu-id="0a3c8-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0a3c8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a3c8-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a3c8-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a3c8-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a3c8-144">INPUTS</span></span>

### <span data-ttu-id="0a3c8-145">Nincs</span><span class="sxs-lookup"><span data-stu-id="0a3c8-145">None</span></span>
<span data-ttu-id="0a3c8-146">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="0a3c8-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0a3c8-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a3c8-147">OUTPUTS</span></span>

### <span data-ttu-id="0a3c8-148">Microsoft. Azure. commands. Network. models. PSFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="0a3c8-148">Microsoft.Azure.Commands.Network.Models.PSFirewallApplicationRule</span></span>

## <span data-ttu-id="0a3c8-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0a3c8-149">NOTES</span></span>

## <span data-ttu-id="0a3c8-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a3c8-150">RELATED LINKS</span></span>

[<span data-ttu-id="0a3c8-151">Új – AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="0a3c8-151">New-AzureRmFirewallApplicationRuleCollection</span></span>](./New-AzureRmFirewallApplicationRuleCollection.md)

[<span data-ttu-id="0a3c8-152">Új – AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="0a3c8-152">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="0a3c8-153">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="0a3c8-153">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="0a3c8-154">Get-AzureRmFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="0a3c8-154">Get-AzureRmFirewallFqdnTag</span></span>](./Get-AzureRmFirewallFqdnTag.md)
