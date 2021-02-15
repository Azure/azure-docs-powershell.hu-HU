---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
ms.openlocfilehash: c3cf6ce07ab746806181af917f656d27c6ffbbaa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151739"
---
# <span data-ttu-id="f883b-101">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f883b-101">New-AzFirewallNetworkRule</span></span>

## <span data-ttu-id="f883b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f883b-102">SYNOPSIS</span></span>
<span data-ttu-id="f883b-103">Tűzfalhálózati szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f883b-103">Creates a Firewall Network Rule.</span></span>

## <span data-ttu-id="f883b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f883b-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] [-DestinationAddress <String[]>] [-DestinationIpGroup <String[]>]
 [-DestinationFqdn <String[]>] -DestinationPort <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f883b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f883b-105">DESCRIPTION</span></span>
<span data-ttu-id="f883b-106">A **New-AzFirewallNetworkRule** parancsmag létrehoz egy hálózati szabályt az Azure tűzfalhoz.</span><span class="sxs-lookup"><span data-stu-id="f883b-106">The **New-AzFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="f883b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f883b-107">EXAMPLES</span></span>

### <span data-ttu-id="f883b-108">1. példa: Szabály létrehozása az összes TCP-forgalomhoz</span><span class="sxs-lookup"><span data-stu-id="f883b-108">Example 1: Create a rule for all TCP traffic</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="f883b-109">Ez a példa létrehoz egy szabályt az összes TCP-forgalomra.</span><span class="sxs-lookup"><span data-stu-id="f883b-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="f883b-110">Egy felhasználó kényszeríti, hogy a forgalom engedélyezett vagy megtagadható legyen-e egy szabályhoz a hozzá társított szabálygyűjtemény alapján.</span><span class="sxs-lookup"><span data-stu-id="f883b-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="f883b-111">2. példa: Szabály létrehozása az összes TCP-forgalomhoz 10.0.0.0-tól 60.1.5.0:4040-ig</span><span class="sxs-lookup"><span data-stu-id="f883b-111">Example 2: Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="f883b-112">Ebben a példában a 10.0.0.0-tól a 60.1.5.0:4040-ig minden TCP-forgalomra létrehoz egy szabályt.</span><span class="sxs-lookup"><span data-stu-id="f883b-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="f883b-113">Egy felhasználó kényszeríti, hogy a forgalom engedélyezett vagy megtagadható legyen-e egy szabályhoz a hozzá társított szabálygyűjtemény alapján.</span><span class="sxs-lookup"><span data-stu-id="f883b-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="f883b-114">3. példa: Szabály létrehozása bármely forrásból a 10.0.0.0/16-os számú TCP- és ICMP-forgalomra</span><span class="sxs-lookup"><span data-stu-id="f883b-114">Example 3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="f883b-115">Ebben a példában a 10.0.0.0/16-os számú forrásból származó összes TCP-forgalomra létrehoz egy szabályt.</span><span class="sxs-lookup"><span data-stu-id="f883b-115">This example creates a rule for all TCP traffic from any source to 10.0.0.0/16.</span></span> <span data-ttu-id="f883b-116">A felhasználó kényszeríti, hogy a forgalom engedélyezett vagy megtagadható legyen-e egy szabályhoz a hozzá társított szabálygyűjtemény alapján.</span><span class="sxs-lookup"><span data-stu-id="f883b-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="f883b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f883b-117">PARAMETERS</span></span>

### <span data-ttu-id="f883b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f883b-118">-DefaultProfile</span></span>
<span data-ttu-id="f883b-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f883b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f883b-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="f883b-120">-Description</span></span>
<span data-ttu-id="f883b-121">A szabály opcionális leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="f883b-121">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="f883b-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="f883b-122">-DestinationAddress</span></span>
<span data-ttu-id="f883b-123">A szabály célcíme</span><span class="sxs-lookup"><span data-stu-id="f883b-123">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="f883b-124">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="f883b-124">-DestinationFqdn</span></span>
<span data-ttu-id="f883b-125">A szabály cél teljes tartományának tartománya</span><span class="sxs-lookup"><span data-stu-id="f883b-125">The destination FQDN of the rule</span></span>

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

### <span data-ttu-id="f883b-126">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="f883b-126">-DestinationIpGroup</span></span>
<span data-ttu-id="f883b-127">A szabály cél ip-csoportja</span><span class="sxs-lookup"><span data-stu-id="f883b-127">The destination ipgroup of the rule</span></span>

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

### <span data-ttu-id="f883b-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="f883b-128">-DestinationPort</span></span>
<span data-ttu-id="f883b-129">A szabály célportjai</span><span class="sxs-lookup"><span data-stu-id="f883b-129">The destination ports of the rule</span></span>

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

### <span data-ttu-id="f883b-130">-Name</span><span class="sxs-lookup"><span data-stu-id="f883b-130">-Name</span></span>
<span data-ttu-id="f883b-131">A hálózati szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f883b-131">Specifies the name of this network rule.</span></span> <span data-ttu-id="f883b-132">A névnek egyedinek kell lennie egy szabálygyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="f883b-132">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="f883b-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="f883b-133">-Protocol</span></span>
<span data-ttu-id="f883b-134">Meghatározza, hogy milyen típusú adatforgalom legyen szűrve ezzel a s szabálysal.</span><span class="sxs-lookup"><span data-stu-id="f883b-134">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="f883b-135">Lehetséges értékek: TCP, UDP, ICMP és Any.</span><span class="sxs-lookup"><span data-stu-id="f883b-135">Possible values are TCP, UDP, ICMP and Any.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP, ICMP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f883b-136">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="f883b-136">-SourceAddress</span></span>
<span data-ttu-id="f883b-137">A szabály forráscíme</span><span class="sxs-lookup"><span data-stu-id="f883b-137">The source addresses of the rule</span></span>

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

### <span data-ttu-id="f883b-138">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="f883b-138">-SourceIpGroup</span></span>
<span data-ttu-id="f883b-139">A szabály forrás IP-csoportja</span><span class="sxs-lookup"><span data-stu-id="f883b-139">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="f883b-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f883b-140">-Confirm</span></span>
<span data-ttu-id="f883b-141">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f883b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f883b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f883b-142">-WhatIf</span></span>
<span data-ttu-id="f883b-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f883b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f883b-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f883b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f883b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f883b-145">CommonParameters</span></span>
<span data-ttu-id="f883b-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f883b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f883b-147">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f883b-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f883b-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f883b-148">INPUTS</span></span>

### <span data-ttu-id="f883b-149">Nincs</span><span class="sxs-lookup"><span data-stu-id="f883b-149">None</span></span>

## <span data-ttu-id="f883b-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f883b-150">OUTPUTS</span></span>

### <span data-ttu-id="f883b-151">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f883b-151">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="f883b-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f883b-152">NOTES</span></span>

## <span data-ttu-id="f883b-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f883b-153">RELATED LINKS</span></span>

[<span data-ttu-id="f883b-154">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f883b-154">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)

[<span data-ttu-id="f883b-155">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f883b-155">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="f883b-156">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f883b-156">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
