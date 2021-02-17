---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
ms.openlocfilehash: d5c3a560f0afcfb28224cf4681af78d6bd5249ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156915"
---
# <span data-ttu-id="9a600-101">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="9a600-101">New-AzFirewallApplicationRule</span></span>

## <span data-ttu-id="9a600-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a600-102">SYNOPSIS</span></span>
<span data-ttu-id="9a600-103">Tűzfalalkalmazási szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9a600-103">Creates a Firewall Application Rule.</span></span>

## <span data-ttu-id="9a600-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9a600-104">SYNTAX</span></span>

### <span data-ttu-id="9a600-105">TargetFqdn (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9a600-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -TargetFqdn <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a600-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="9a600-106">FqdnTag</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a600-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9a600-107">DESCRIPTION</span></span>
<span data-ttu-id="9a600-108">A **New-AzFirewallApplicationRule** parancsmag létrehoz egy alkalmazásszabályt az Azure tűzfalhoz.</span><span class="sxs-lookup"><span data-stu-id="9a600-108">The **New-AzFirewallApplicationRule** cmdlet creates an application rule for Azure Firewall.</span></span>

## <span data-ttu-id="9a600-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9a600-109">EXAMPLES</span></span>

### <span data-ttu-id="9a600-110">1. példa: Szabály létrehozása a 10.0.0.0-s összes HTTPS-adatforgalom engedélyezése érdekében</span><span class="sxs-lookup"><span data-stu-id="9a600-110">Example 1: Create a rule to allow all HTTPS traffic from 10.0.0.0</span></span>
```powershell
New-AzFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

<span data-ttu-id="9a600-111">Ez a példa létrehoz egy szabályt, amely engedélyezi a 443-as port összes HTTPS-adatforgalmát a 10.0.0.0-s portról.</span><span class="sxs-lookup"><span data-stu-id="9a600-111">This example creates a rule which will allow all HTTPS traffic on port 443 from 10.0.0.0.</span></span>

### <span data-ttu-id="9a600-112">2. példa: Szabály létrehozása a WindowsUpdate 10.0.0.0/24 alhálózathoz való engedélyezése érdekében</span><span class="sxs-lookup"><span data-stu-id="9a600-112">Example 2: Create a rule to allow WindowsUpdate for 10.0.0.0/24 subnet</span></span>
```powershell
New-AzFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

<span data-ttu-id="9a600-113">Ez a példa létrehoz egy szabályt, amely engedélyezi a Windows-frissítések forgalmát a 10.0.0.0/24 tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="9a600-113">This example creates a rule which will allow traffic for Windows Updates for 10.0.0.0/24 domain.</span></span>

## <span data-ttu-id="9a600-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a600-114">PARAMETERS</span></span>

### <span data-ttu-id="9a600-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a600-115">-DefaultProfile</span></span>
<span data-ttu-id="9a600-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9a600-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a600-117">-Leírás</span><span class="sxs-lookup"><span data-stu-id="9a600-117">-Description</span></span>
<span data-ttu-id="9a600-118">A szabály opcionális leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="9a600-118">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="9a600-119">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="9a600-119">-FqdnTag</span></span>
<span data-ttu-id="9a600-120">Megadja a szabály teljes tartománycímkéinek listáját.</span><span class="sxs-lookup"><span data-stu-id="9a600-120">Specifies a list of FQDN Tags for this rule.</span></span> <span data-ttu-id="9a600-121">A rendelkezésre álló címkék a [Get-AzFirewallFqdnTag parancsmag](./Get-AzFirewallFqdnTag.md) használatával szerezhetők be.</span><span class="sxs-lookup"><span data-stu-id="9a600-121">The available tags can be retrieved using [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) cmdlet.</span></span>

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

### <span data-ttu-id="9a600-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9a600-122">-Name</span></span>
<span data-ttu-id="9a600-123">Az alkalmazásszabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9a600-123">Specifies the name of this application rule.</span></span> <span data-ttu-id="9a600-124">A névnek egyedinek kell lennie egy szabálygyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="9a600-124">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="9a600-125">-Protocol</span><span class="sxs-lookup"><span data-stu-id="9a600-125">-Protocol</span></span>
<span data-ttu-id="9a600-126">Meghatározza, hogy milyen típusú adatforgalom szűrhető ezzel a s szabálysal.</span><span class="sxs-lookup"><span data-stu-id="9a600-126">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="9a600-127">A formátum: <protocol type> <port> .</span><span class="sxs-lookup"><span data-stu-id="9a600-127">The format is <protocol type>:<port>.</span></span> <span data-ttu-id="9a600-128">Például: "http:80" vagy "https:443".</span><span class="sxs-lookup"><span data-stu-id="9a600-128">For example, "http:80" or "https:443".</span></span>
<span data-ttu-id="9a600-129">A Protokoll kötelező a TargetFqdn használatakor, de nem használható a teljes tartománynévvel.</span><span class="sxs-lookup"><span data-stu-id="9a600-129">Protocol is mandatory when TargetFqdn is used, but it cannot be used with FqdnTag.</span></span> <span data-ttu-id="9a600-130">A támogatott protokollok a HTTP és a HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9a600-130">The supported protocols are HTTP and HTTPS.</span></span>

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

### <span data-ttu-id="9a600-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="9a600-131">-SourceAddress</span></span>
<span data-ttu-id="9a600-132">A szabály forráscíme</span><span class="sxs-lookup"><span data-stu-id="9a600-132">The source addresses of the rule</span></span>

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

### <span data-ttu-id="9a600-133">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="9a600-133">-SourceIpGroup</span></span>
<span data-ttu-id="9a600-134">A szabály forrás IP-csoportja</span><span class="sxs-lookup"><span data-stu-id="9a600-134">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="9a600-135">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="9a600-135">-TargetFqdn</span></span>
<span data-ttu-id="9a600-136">A szabály által szűrt tartománynevek listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9a600-136">Specifies a list of domain names filtered by this rule.</span></span>
<span data-ttu-id="9a600-137">A csillag karaktert (' ' ) csak a teljes tartomány teljes tartományának első karaktereként *fogadja el a listában. Ha használja, a csillag bármilyen számú karakterrel egyezik meg. (például a '* msn.com' meg fog egyezni msn.com altartományokkal)</span><span class="sxs-lookup"><span data-stu-id="9a600-137">The asterisk character, '*', is accepted only as the first character of an FQDN in the list. When used, the asterisk matches any number of characters. (e.g. '* msn.com' will match msn.com and all its subdomains)</span></span>

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

### <span data-ttu-id="9a600-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a600-138">-Confirm</span></span>
<span data-ttu-id="9a600-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9a600-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a600-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a600-140">-WhatIf</span></span>
<span data-ttu-id="9a600-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9a600-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a600-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9a600-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a600-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a600-143">CommonParameters</span></span>
<span data-ttu-id="9a600-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a600-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a600-145">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a600-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a600-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a600-146">INPUTS</span></span>

### <span data-ttu-id="9a600-147">Nincs</span><span class="sxs-lookup"><span data-stu-id="9a600-147">None</span></span>

## <span data-ttu-id="9a600-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a600-148">OUTPUTS</span></span>

### <span data-ttu-id="9a600-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="9a600-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule</span></span>

## <span data-ttu-id="9a600-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9a600-150">NOTES</span></span>

## <span data-ttu-id="9a600-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a600-151">RELATED LINKS</span></span>

[<span data-ttu-id="9a600-152">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="9a600-152">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="9a600-153">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="9a600-153">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="9a600-154">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="9a600-154">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="9a600-155">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="9a600-155">Get-AzFirewallFqdnTag</span></span>](./Get-AzFirewallFqdnTag.md)
