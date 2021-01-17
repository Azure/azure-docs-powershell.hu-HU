---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 441e47b4ef2a796fcdf5ee802cba83f0fce7e352
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332238"
---
# <span data-ttu-id="f30bb-101">New-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="f30bb-101">New-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="f30bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f30bb-102">SYNOPSIS</span></span>
<span data-ttu-id="f30bb-103">WaF-házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="f30bb-103">Create WAF policy</span></span>

## <span data-ttu-id="f30bb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f30bb-104">SYNTAX</span></span>

```
New-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f30bb-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f30bb-105">DESCRIPTION</span></span>
<span data-ttu-id="f30bb-106">A **New-AzFrontDoorWafPolicy** parancsmag új Azure WAF-házirendet hoz létre a megadott erőforráscsoportban az aktuális előfizetés alatt</span><span class="sxs-lookup"><span data-stu-id="f30bb-106">The **New-AzFrontDoorWafPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="f30bb-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f30bb-107">EXAMPLES</span></span>

### <span data-ttu-id="f30bb-108">1. példa: WaF-házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="f30bb-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="f30bb-109">WaF-házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="f30bb-109">Create WAF policy</span></span>

## <span data-ttu-id="f30bb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f30bb-110">PARAMETERS</span></span>

### <span data-ttu-id="f30bb-111">-CustomBlockResponseBlock</span><span class="sxs-lookup"><span data-stu-id="f30bb-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="f30bb-112">Egyéni válasz törzse</span><span class="sxs-lookup"><span data-stu-id="f30bb-112">Custom Response Body</span></span>

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

### <span data-ttu-id="f30bb-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="f30bb-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="f30bb-114">Egyéni válaszállapot-kód</span><span class="sxs-lookup"><span data-stu-id="f30bb-114">Custom Response Status Code</span></span>

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

### <span data-ttu-id="f30bb-115">-Customrule</span><span class="sxs-lookup"><span data-stu-id="f30bb-115">-Customrule</span></span>
<span data-ttu-id="f30bb-116">Egyéni szabályok a házirenden belül</span><span class="sxs-lookup"><span data-stu-id="f30bb-116">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="f30bb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f30bb-117">-DefaultProfile</span></span>
<span data-ttu-id="f30bb-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f30bb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f30bb-119">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="f30bb-119">-EnabledState</span></span>
<span data-ttu-id="f30bb-120">Hogy a házirend engedélyezett vagy letiltott állapotban van-e.</span><span class="sxs-lookup"><span data-stu-id="f30bb-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="f30bb-121">Lehetséges értékek: "Letiltva", "Engedélyezve"</span><span class="sxs-lookup"><span data-stu-id="f30bb-121">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="f30bb-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="f30bb-122">-ManagedRule</span></span>
<span data-ttu-id="f30bb-123">Felügyelt szabályok a házirenden belül</span><span class="sxs-lookup"><span data-stu-id="f30bb-123">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="f30bb-124">-Mód</span><span class="sxs-lookup"><span data-stu-id="f30bb-124">-Mode</span></span>
<span data-ttu-id="f30bb-125">Ez a cikk azt ismerteti, hogy észlelési vagy megelőzési módban van-e házirendszinten.</span><span class="sxs-lookup"><span data-stu-id="f30bb-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="f30bb-126">Lehetséges értékek: "Megelőzés", "Észlelés"</span><span class="sxs-lookup"><span data-stu-id="f30bb-126">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="f30bb-127">-Name</span><span class="sxs-lookup"><span data-stu-id="f30bb-127">-Name</span></span>
<span data-ttu-id="f30bb-128">WebApplicationFireWallPolicy neve.</span><span class="sxs-lookup"><span data-stu-id="f30bb-128">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="f30bb-129">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="f30bb-129">-RedirectUrl</span></span>
<span data-ttu-id="f30bb-130">Url-cím átirányítása</span><span class="sxs-lookup"><span data-stu-id="f30bb-130">Redirect URL</span></span>

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

### <span data-ttu-id="f30bb-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f30bb-131">-ResourceGroupName</span></span>
<span data-ttu-id="f30bb-132">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="f30bb-132">The resource group name</span></span>

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

### <span data-ttu-id="f30bb-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f30bb-133">-Confirm</span></span>
<span data-ttu-id="f30bb-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f30bb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f30bb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f30bb-135">-WhatIf</span></span>
<span data-ttu-id="f30bb-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f30bb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f30bb-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f30bb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f30bb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f30bb-138">CommonParameters</span></span>
<span data-ttu-id="f30bb-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f30bb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f30bb-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f30bb-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f30bb-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f30bb-141">INPUTS</span></span>

### <span data-ttu-id="f30bb-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="f30bb-142">None</span></span>

## <span data-ttu-id="f30bb-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f30bb-143">OUTPUTS</span></span>

### <span data-ttu-id="f30bb-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="f30bb-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="f30bb-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f30bb-145">NOTES</span></span>

## <span data-ttu-id="f30bb-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f30bb-146">RELATED LINKS</span></span>

<span data-ttu-id="f30bb-147">[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="f30bb-147">[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
