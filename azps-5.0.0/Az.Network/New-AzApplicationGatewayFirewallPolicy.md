---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 03e03de70f61672d1246ffeb8469efe0c04b3ea4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194285"
---
# <span data-ttu-id="f6d93-101">New-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f6d93-101">New-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="f6d93-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f6d93-102">SYNOPSIS</span></span>
<span data-ttu-id="f6d93-103">Egy alkalmazás-átjáró tűzfal-házirendjét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="f6d93-103">Creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="f6d93-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f6d93-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6d93-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f6d93-105">DESCRIPTION</span></span>
<span data-ttu-id="f6d93-106">A **New-AzApplicationGatewayFirewallPolicy** parancsmag egy alkalmazás-átjáró tűzfal-házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f6d93-106">The **New-AzApplicationGatewayFirewallPolicy** cmdlet creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="f6d93-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f6d93-107">EXAMPLES</span></span>

### <span data-ttu-id="f6d93-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f6d93-108">Example 1</span></span>
```powershell
PS C:\> $firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name wafResource1 -ResourceGroupName "rg1"  -Location  "westus" -CustomRule $customRule
```

<span data-ttu-id="f6d93-109">Ezzel a paranccsal létrehoz egy új Azure Application gateway-tűzfal-házirendet "wafResource1" nevű erőforráscsoport "rg1" nevű erőforráscsoport "westus" nevű "" nevű "" nevű új, a $customRule változóban meghatározott egyéni szabályokkal.</span><span class="sxs-lookup"><span data-stu-id="f6d93-109">This command creates a new Azure application gateway firewall policy named "wafResource1" in resource group "rg1" in location "westus" with custom rules defined in the $customRule variable</span></span>

## <span data-ttu-id="f6d93-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f6d93-110">PARAMETERS</span></span>

### <span data-ttu-id="f6d93-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6d93-111">-AsJob</span></span>
<span data-ttu-id="f6d93-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f6d93-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f6d93-113">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="f6d93-113">-CustomRule</span></span>
<span data-ttu-id="f6d93-114">A CustomRules listája</span><span class="sxs-lookup"><span data-stu-id="f6d93-114">The list of CustomRules</span></span>

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

### <span data-ttu-id="f6d93-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6d93-115">-DefaultProfile</span></span>
<span data-ttu-id="f6d93-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f6d93-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6d93-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f6d93-117">-Force</span></span>
<span data-ttu-id="f6d93-118">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f6d93-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f6d93-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="f6d93-119">-Location</span></span>
<span data-ttu-id="f6d93-120">helyre.</span><span class="sxs-lookup"><span data-stu-id="f6d93-120">location.</span></span>

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

### <span data-ttu-id="f6d93-121">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="f6d93-121">-ManagedRule</span></span>
<span data-ttu-id="f6d93-122">Felügyelt szabály beállítása</span><span class="sxs-lookup"><span data-stu-id="f6d93-122">Managed Rule Setting</span></span>

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

### <span data-ttu-id="f6d93-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f6d93-123">-Name</span></span>
<span data-ttu-id="f6d93-124">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="f6d93-124">The resource name.</span></span>

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

### <span data-ttu-id="f6d93-125">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="f6d93-125">-PolicySetting</span></span>
<span data-ttu-id="f6d93-126">A webalkalmazás-tűzfal házirend-beállításai</span><span class="sxs-lookup"><span data-stu-id="f6d93-126">Policy Settings for Web Application Firewall</span></span>

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

### <span data-ttu-id="f6d93-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6d93-127">-ResourceGroupName</span></span>
<span data-ttu-id="f6d93-128">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f6d93-128">The resource group name.</span></span>

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

### <span data-ttu-id="f6d93-129">-Címke</span><span class="sxs-lookup"><span data-stu-id="f6d93-129">-Tag</span></span>
<span data-ttu-id="f6d93-130">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="f6d93-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f6d93-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f6d93-131">-Confirm</span></span>
<span data-ttu-id="f6d93-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f6d93-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6d93-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6d93-133">-WhatIf</span></span>
<span data-ttu-id="f6d93-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f6d93-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6d93-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f6d93-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6d93-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6d93-136">CommonParameters</span></span>
<span data-ttu-id="f6d93-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f6d93-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6d93-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f6d93-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6d93-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6d93-139">INPUTS</span></span>

### <span data-ttu-id="f6d93-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f6d93-140">System.String</span></span>

### <span data-ttu-id="f6d93-141">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFirewallCustomRule []</span><span class="sxs-lookup"><span data-stu-id="f6d93-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span></span>

### <span data-ttu-id="f6d93-142">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="f6d93-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

### <span data-ttu-id="f6d93-143">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="f6d93-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

### <span data-ttu-id="f6d93-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f6d93-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f6d93-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6d93-145">OUTPUTS</span></span>

### <span data-ttu-id="f6d93-146">Microsoft. Azure. commands. Network. models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f6d93-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="f6d93-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f6d93-147">NOTES</span></span>

## <span data-ttu-id="f6d93-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6d93-148">RELATED LINKS</span></span>
