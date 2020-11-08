---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: da83c8cd863d8d3cfa62d47c7a4126d15c4dd670
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014818"
---
# <span data-ttu-id="55eb1-101">New-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="55eb1-101">New-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="55eb1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="55eb1-102">SYNOPSIS</span></span>
<span data-ttu-id="55eb1-103">Egy alkalmazás-átjáró tűzfal-házirendjét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="55eb1-103">Creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="55eb1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="55eb1-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55eb1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="55eb1-105">DESCRIPTION</span></span>
<span data-ttu-id="55eb1-106">A **New-AzApplicationGatewayFirewallPolicy** parancsmag egy alkalmazás-átjáró tűzfal-házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="55eb1-106">The **New-AzApplicationGatewayFirewallPolicy** cmdlet creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="55eb1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="55eb1-107">EXAMPLES</span></span>

### <span data-ttu-id="55eb1-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="55eb1-108">Example 1</span></span>
```powershell
PS C:\> $firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name wafResource1 -ResourceGroupName "rg1"  -Location  "westus" -CustomRules $customRule
```

<span data-ttu-id="55eb1-109">Ezzel a paranccsal létrehoz egy új Azure Application gateway-tűzfal-házirendet "wafResource1" nevű erőforráscsoport "rg1" nevű erőforráscsoport "westus" nevű "" nevű "" nevű új, a $customRule változóban meghatározott egyéni szabályokkal.</span><span class="sxs-lookup"><span data-stu-id="55eb1-109">This command creates a new Azure application gateway firewall policy named "wafResource1" in resource group "rg1" in location "westus" with custom rules defined in the $customRule variable</span></span>

## <span data-ttu-id="55eb1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="55eb1-110">PARAMETERS</span></span>

### <span data-ttu-id="55eb1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55eb1-111">-AsJob</span></span>
<span data-ttu-id="55eb1-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="55eb1-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55eb1-113">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="55eb1-113">-CustomRule</span></span>
<span data-ttu-id="55eb1-114">A CustomRules listája</span><span class="sxs-lookup"><span data-stu-id="55eb1-114">The list of CustomRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55eb1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55eb1-115">-DefaultProfile</span></span>
<span data-ttu-id="55eb1-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="55eb1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55eb1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="55eb1-117">-Force</span></span>
<span data-ttu-id="55eb1-118">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="55eb1-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="55eb1-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="55eb1-119">-Location</span></span>
<span data-ttu-id="55eb1-120">helyre.</span><span class="sxs-lookup"><span data-stu-id="55eb1-120">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55eb1-121">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="55eb1-121">-ManagedRule</span></span>
<span data-ttu-id="55eb1-122">Felügyelt szabály beállítása</span><span class="sxs-lookup"><span data-stu-id="55eb1-122">Managed Rule Setting</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55eb1-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="55eb1-123">-Name</span></span>
<span data-ttu-id="55eb1-124">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="55eb1-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55eb1-125">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="55eb1-125">-PolicySetting</span></span>
<span data-ttu-id="55eb1-126">A webalkalmazás-tűzfal házirend-beállításai</span><span class="sxs-lookup"><span data-stu-id="55eb1-126">Policy Settings for Web Application Firewall</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55eb1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55eb1-127">-ResourceGroupName</span></span>
<span data-ttu-id="55eb1-128">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="55eb1-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55eb1-129">-Címke</span><span class="sxs-lookup"><span data-stu-id="55eb1-129">-Tag</span></span>
<span data-ttu-id="55eb1-130">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="55eb1-130">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55eb1-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="55eb1-131">-Confirm</span></span>
<span data-ttu-id="55eb1-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="55eb1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55eb1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55eb1-133">-WhatIf</span></span>
<span data-ttu-id="55eb1-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="55eb1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55eb1-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="55eb1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55eb1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55eb1-136">CommonParameters</span></span>
<span data-ttu-id="55eb1-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="55eb1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55eb1-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="55eb1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55eb1-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="55eb1-139">INPUTS</span></span>

### <span data-ttu-id="55eb1-140">System. String</span><span class="sxs-lookup"><span data-stu-id="55eb1-140">System.String</span></span>

### <span data-ttu-id="55eb1-141">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFirewallCustomRule []</span><span class="sxs-lookup"><span data-stu-id="55eb1-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span></span>

### <span data-ttu-id="55eb1-142">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="55eb1-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

### <span data-ttu-id="55eb1-143">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="55eb1-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

### <span data-ttu-id="55eb1-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="55eb1-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="55eb1-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="55eb1-145">OUTPUTS</span></span>

### <span data-ttu-id="55eb1-146">Microsoft. Azure. commands. Network. models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="55eb1-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="55eb1-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="55eb1-147">NOTES</span></span>

## <span data-ttu-id="55eb1-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="55eb1-148">RELATED LINKS</span></span>
