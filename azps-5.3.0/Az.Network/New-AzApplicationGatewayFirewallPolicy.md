---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 03e03de70f61672d1246ffeb8469efe0c04b3ea4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379468"
---
# <span data-ttu-id="3c0a2-101">New-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="3c0a2-101">New-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="3c0a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c0a2-102">SYNOPSIS</span></span>
<span data-ttu-id="3c0a2-103">Alkalmazásátjáró tűzfal házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3c0a2-103">Creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="3c0a2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3c0a2-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c0a2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3c0a2-105">DESCRIPTION</span></span>
<span data-ttu-id="3c0a2-106">A **New-AzApplicationGatewayFirewallPolicy parancsmag** létrehoz egy alkalmazás-átjáró tűzfal házirendet.</span><span class="sxs-lookup"><span data-stu-id="3c0a2-106">The **New-AzApplicationGatewayFirewallPolicy** cmdlet creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="3c0a2-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3c0a2-107">EXAMPLES</span></span>

### <span data-ttu-id="3c0a2-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="3c0a2-108">Example 1</span></span>
```powershell
PS C:\> $firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name wafResource1 -ResourceGroupName "rg1"  -Location  "westus" -CustomRule $customRule
```

<span data-ttu-id="3c0a2-109">Ez a parancs létrehoz egy "wafResource1" nevű új Azure-alkalmazás átjáró tűzfal házirendet az "rg1" erőforráscsoportban a "westus" helyen, a $customRule változóban definiált egyéni szabályokkal</span><span class="sxs-lookup"><span data-stu-id="3c0a2-109">This command creates a new Azure application gateway firewall policy named "wafResource1" in resource group "rg1" in location "westus" with custom rules defined in the $customRule variable</span></span>

## <span data-ttu-id="3c0a2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c0a2-110">PARAMETERS</span></span>

### <span data-ttu-id="3c0a2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c0a2-111">-AsJob</span></span>
<span data-ttu-id="3c0a2-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3c0a2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c0a2-113">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="3c0a2-113">-CustomRule</span></span>
<span data-ttu-id="3c0a2-114">The list of CustomRules</span><span class="sxs-lookup"><span data-stu-id="3c0a2-114">The list of CustomRules</span></span>

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

### <span data-ttu-id="3c0a2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c0a2-115">-DefaultProfile</span></span>
<span data-ttu-id="3c0a2-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3c0a2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c0a2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3c0a2-117">-Force</span></span>
<span data-ttu-id="3c0a2-118">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="3c0a2-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="3c0a2-119">-Location</span><span class="sxs-lookup"><span data-stu-id="3c0a2-119">-Location</span></span>
<span data-ttu-id="3c0a2-120">helyére.</span><span class="sxs-lookup"><span data-stu-id="3c0a2-120">location.</span></span>

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

### <span data-ttu-id="3c0a2-121">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="3c0a2-121">-ManagedRule</span></span>
<span data-ttu-id="3c0a2-122">Felügyelt szabály beállítása</span><span class="sxs-lookup"><span data-stu-id="3c0a2-122">Managed Rule Setting</span></span>

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

### <span data-ttu-id="3c0a2-123">-Name</span><span class="sxs-lookup"><span data-stu-id="3c0a2-123">-Name</span></span>
<span data-ttu-id="3c0a2-124">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="3c0a2-124">The resource name.</span></span>

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

### <span data-ttu-id="3c0a2-125">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="3c0a2-125">-PolicySetting</span></span>
<span data-ttu-id="3c0a2-126">A webalkalmazás tűzfalának házirendbeállítása</span><span class="sxs-lookup"><span data-stu-id="3c0a2-126">Policy Settings for Web Application Firewall</span></span>

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

### <span data-ttu-id="3c0a2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c0a2-127">-ResourceGroupName</span></span>
<span data-ttu-id="3c0a2-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3c0a2-128">The resource group name.</span></span>

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

### <span data-ttu-id="3c0a2-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="3c0a2-129">-Tag</span></span>
<span data-ttu-id="3c0a2-130">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="3c0a2-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="3c0a2-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c0a2-131">-Confirm</span></span>
<span data-ttu-id="3c0a2-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3c0a2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c0a2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c0a2-133">-WhatIf</span></span>
<span data-ttu-id="3c0a2-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3c0a2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c0a2-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3c0a2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c0a2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c0a2-136">CommonParameters</span></span>
<span data-ttu-id="3c0a2-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c0a2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c0a2-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c0a2-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c0a2-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3c0a2-139">INPUTS</span></span>

### <span data-ttu-id="3c0a2-140">System.String</span><span class="sxs-lookup"><span data-stu-id="3c0a2-140">System.String</span></span>

### <span data-ttu-id="3c0a2-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span><span class="sxs-lookup"><span data-stu-id="3c0a2-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span></span>

### <span data-ttu-id="3c0a2-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="3c0a2-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

### <span data-ttu-id="3c0a2-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="3c0a2-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

### <span data-ttu-id="3c0a2-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3c0a2-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3c0a2-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c0a2-145">OUTPUTS</span></span>

### <span data-ttu-id="3c0a2-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="3c0a2-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="3c0a2-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3c0a2-147">NOTES</span></span>

## <span data-ttu-id="3c0a2-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c0a2-148">RELATED LINKS</span></span>
