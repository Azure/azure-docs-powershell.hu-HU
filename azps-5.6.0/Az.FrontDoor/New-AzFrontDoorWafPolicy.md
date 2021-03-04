---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 5c39a86b29ce27ea57d51e7e3bfb048560ef1ee6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928033"
---
# <span data-ttu-id="d0ebe-101">New-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="d0ebe-101">New-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="d0ebe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0ebe-102">SYNOPSIS</span></span>
<span data-ttu-id="d0ebe-103">WaF-házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="d0ebe-103">Create WAF policy</span></span>

## <span data-ttu-id="d0ebe-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d0ebe-104">SYNTAX</span></span>

```
New-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>] [-RequestBodyCheck <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0ebe-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d0ebe-105">DESCRIPTION</span></span>
<span data-ttu-id="d0ebe-106">A **New-AzFrontDoorWafPolicy** parancsmag új Azure WAF-házirendet hoz létre a megadott erőforráscsoportban az aktuális előfizetés alatt</span><span class="sxs-lookup"><span data-stu-id="d0ebe-106">The **New-AzFrontDoorWafPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="d0ebe-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d0ebe-107">EXAMPLES</span></span>

### <span data-ttu-id="d0ebe-108">1. példa: WaF-házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="d0ebe-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="d0ebe-109">WaF-házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="d0ebe-109">Create WAF policy</span></span>

## <span data-ttu-id="d0ebe-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0ebe-110">PARAMETERS</span></span>

### <span data-ttu-id="d0ebe-111">-CustomBlockResponseBlock</span><span class="sxs-lookup"><span data-stu-id="d0ebe-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="d0ebe-112">Egyéni válasz törzse</span><span class="sxs-lookup"><span data-stu-id="d0ebe-112">Custom Response Body</span></span>

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

### <span data-ttu-id="d0ebe-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="d0ebe-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="d0ebe-114">Egyéni válaszállapot-kód</span><span class="sxs-lookup"><span data-stu-id="d0ebe-114">Custom Response Status Code</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0ebe-115">-Customrule</span><span class="sxs-lookup"><span data-stu-id="d0ebe-115">-Customrule</span></span>
<span data-ttu-id="d0ebe-116">Egyéni szabályok a házirenden belül</span><span class="sxs-lookup"><span data-stu-id="d0ebe-116">Custom rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0ebe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0ebe-117">-DefaultProfile</span></span>
<span data-ttu-id="d0ebe-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d0ebe-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0ebe-119">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="d0ebe-119">-EnabledState</span></span>
<span data-ttu-id="d0ebe-120">Hogy a házirend engedélyezett vagy letiltott állapotban van-e.</span><span class="sxs-lookup"><span data-stu-id="d0ebe-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="d0ebe-121">Lehetséges értékek: "Letiltva", "Engedélyezve"</span><span class="sxs-lookup"><span data-stu-id="d0ebe-121">Possible values include: 'Disabled', 'Enabled'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0ebe-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="d0ebe-122">-ManagedRule</span></span>
<span data-ttu-id="d0ebe-123">Felügyelt szabályok a házirenden belül</span><span class="sxs-lookup"><span data-stu-id="d0ebe-123">Managed rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0ebe-124">-Mód</span><span class="sxs-lookup"><span data-stu-id="d0ebe-124">-Mode</span></span>
<span data-ttu-id="d0ebe-125">Ez a cikk azt ismerteti, hogy észlelési vagy megelőzési módban van-e házirendszinten.</span><span class="sxs-lookup"><span data-stu-id="d0ebe-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="d0ebe-126">Lehetséges értékek: "Megelőzés", "Észlelés"</span><span class="sxs-lookup"><span data-stu-id="d0ebe-126">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="d0ebe-127">-Name</span><span class="sxs-lookup"><span data-stu-id="d0ebe-127">-Name</span></span>
<span data-ttu-id="d0ebe-128">WebApplicationFireWallPolicy neve.</span><span class="sxs-lookup"><span data-stu-id="d0ebe-128">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="d0ebe-129">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="d0ebe-129">-RedirectUrl</span></span>
<span data-ttu-id="d0ebe-130">Url-cím átirányítása</span><span class="sxs-lookup"><span data-stu-id="d0ebe-130">Redirect URL</span></span>

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

### <span data-ttu-id="d0ebe-131">-RequestCheck</span><span class="sxs-lookup"><span data-stu-id="d0ebe-131">-RequestBodyCheck</span></span>
<span data-ttu-id="d0ebe-132">Azt határozza meg, hogy a felügyelt szabályoknak meg kell-e vizsgálniuk a törzset.</span><span class="sxs-lookup"><span data-stu-id="d0ebe-132">Defines if the body should be inspected by managed rules.</span></span> <span data-ttu-id="d0ebe-133">Lehetséges értékek: "Engedélyezve", "Letiltva"</span><span class="sxs-lookup"><span data-stu-id="d0ebe-133">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="d0ebe-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0ebe-134">-ResourceGroupName</span></span>
<span data-ttu-id="d0ebe-135">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="d0ebe-135">The resource group name</span></span>

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

### <span data-ttu-id="d0ebe-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0ebe-136">-Confirm</span></span>
<span data-ttu-id="d0ebe-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d0ebe-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0ebe-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0ebe-138">-WhatIf</span></span>
<span data-ttu-id="d0ebe-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d0ebe-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0ebe-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d0ebe-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0ebe-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0ebe-141">CommonParameters</span></span>
<span data-ttu-id="d0ebe-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0ebe-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0ebe-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0ebe-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0ebe-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d0ebe-144">INPUTS</span></span>

### <span data-ttu-id="d0ebe-145">Nincs</span><span class="sxs-lookup"><span data-stu-id="d0ebe-145">None</span></span>

## <span data-ttu-id="d0ebe-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0ebe-146">OUTPUTS</span></span>

### <span data-ttu-id="d0ebe-147">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="d0ebe-147">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="d0ebe-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d0ebe-148">NOTES</span></span>

## <span data-ttu-id="d0ebe-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0ebe-149">RELATED LINKS</span></span>

<span data-ttu-id="d0ebe-150">[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="d0ebe-150">[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
