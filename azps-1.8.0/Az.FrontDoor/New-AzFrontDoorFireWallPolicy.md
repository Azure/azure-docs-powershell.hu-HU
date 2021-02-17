---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFireWallPolicy.md
ms.openlocfilehash: 9b1339d138087207b84a7f515c66bd9964420dcd
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401487"
---
# <span data-ttu-id="5e4b0-101">New-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="5e4b0-101">New-AzFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="5e4b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e4b0-102">SYNOPSIS</span></span>
<span data-ttu-id="5e4b0-103">WaF-házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="5e4b0-103">Create WAF policy</span></span>

## <span data-ttu-id="5e4b0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5e4b0-104">SYNTAX</span></span>

```
New-AzFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e4b0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5e4b0-105">DESCRIPTION</span></span>
<span data-ttu-id="5e4b0-106">A **New-AzFrontDoorFireWallPolicy** parancsmag létrehoz egy új Azure WAF-házirendet a megadott erőforráscsoportban az aktuális előfizetés alatt</span><span class="sxs-lookup"><span data-stu-id="5e4b0-106">The **New-AzFrontDoorFireWallPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="5e4b0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5e4b0-107">EXAMPLES</span></span>

### <span data-ttu-id="5e4b0-108">1. példa: WaF-házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="5e4b0-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="5e4b0-109">WaF-házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="5e4b0-109">Create WAF policy</span></span>

## <span data-ttu-id="5e4b0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e4b0-110">PARAMETERS</span></span>

### <span data-ttu-id="5e4b0-111">-CustomBlockResponseBlock</span><span class="sxs-lookup"><span data-stu-id="5e4b0-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="5e4b0-112">Egyéni válasz törzse</span><span class="sxs-lookup"><span data-stu-id="5e4b0-112">Custom Response Body</span></span>

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

### <span data-ttu-id="5e4b0-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="5e4b0-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="5e4b0-114">Egyéni válaszállapot-kód</span><span class="sxs-lookup"><span data-stu-id="5e4b0-114">Custom Response Status Code</span></span>

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

### <span data-ttu-id="5e4b0-115">-Customrule</span><span class="sxs-lookup"><span data-stu-id="5e4b0-115">-Customrule</span></span>
<span data-ttu-id="5e4b0-116">Egyéni szabályok a házirenden belül</span><span class="sxs-lookup"><span data-stu-id="5e4b0-116">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="5e4b0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e4b0-117">-DefaultProfile</span></span>
<span data-ttu-id="5e4b0-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5e4b0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e4b0-119">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="5e4b0-119">-EnabledState</span></span>
<span data-ttu-id="5e4b0-120">Hogy a házirend engedélyezett vagy letiltott állapotban van-e.</span><span class="sxs-lookup"><span data-stu-id="5e4b0-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="5e4b0-121">Lehetséges értékek: "Letiltva", "Engedélyezve"</span><span class="sxs-lookup"><span data-stu-id="5e4b0-121">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="5e4b0-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="5e4b0-122">-ManagedRule</span></span>
<span data-ttu-id="5e4b0-123">Felügyelt szabályok a házirenden belül</span><span class="sxs-lookup"><span data-stu-id="5e4b0-123">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="5e4b0-124">-Mód</span><span class="sxs-lookup"><span data-stu-id="5e4b0-124">-Mode</span></span>
<span data-ttu-id="5e4b0-125">Ez a cikk azt ismerteti, hogy észlelési vagy megelőzési módban van-e házirendszinten.</span><span class="sxs-lookup"><span data-stu-id="5e4b0-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="5e4b0-126">Lehetséges értékek: "Megelőzés", "Észlelés"</span><span class="sxs-lookup"><span data-stu-id="5e4b0-126">Possible values include:'Prevention', 'Detection'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMode
Parameter Sets: (All)
Aliases:
Accepted values: Prevention, Detection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e4b0-127">-Name</span><span class="sxs-lookup"><span data-stu-id="5e4b0-127">-Name</span></span>
<span data-ttu-id="5e4b0-128">WebApplicationFireWallPolicy neve.</span><span class="sxs-lookup"><span data-stu-id="5e4b0-128">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="5e4b0-129">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="5e4b0-129">-RedirectUrl</span></span>
<span data-ttu-id="5e4b0-130">Url-cím átirányítása</span><span class="sxs-lookup"><span data-stu-id="5e4b0-130">Redirect URL</span></span>

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

### <span data-ttu-id="5e4b0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e4b0-131">-ResourceGroupName</span></span>
<span data-ttu-id="5e4b0-132">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="5e4b0-132">The resource group name</span></span>

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

### <span data-ttu-id="5e4b0-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e4b0-133">-Confirm</span></span>
<span data-ttu-id="5e4b0-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5e4b0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e4b0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e4b0-135">-WhatIf</span></span>
<span data-ttu-id="5e4b0-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5e4b0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e4b0-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5e4b0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e4b0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e4b0-138">CommonParameters</span></span>
<span data-ttu-id="5e4b0-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e4b0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e4b0-140">További információt a [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e4b0-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e4b0-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5e4b0-141">INPUTS</span></span>

### <span data-ttu-id="5e4b0-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="5e4b0-142">None</span></span>

## <span data-ttu-id="5e4b0-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e4b0-143">OUTPUTS</span></span>

### <span data-ttu-id="5e4b0-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="5e4b0-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="5e4b0-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5e4b0-145">NOTES</span></span>

## <span data-ttu-id="5e4b0-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e4b0-146">RELATED LINKS</span></span>

<span data-ttu-id="5e4b0-147">[Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md) 
 [Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md) 
 [Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md) 
 [New-AzFrontDoorManagedRuleObject](./New-AzFrontDoorManagedRuleObject.md) 
 [New-AzFrontDoorCustomRuleObject](./New-AzFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="5e4b0-147">[Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md)
[Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md)
[Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md)
[New-AzFrontDoorManagedRuleObject](./New-AzFrontDoorManagedRuleObject.md)
[New-AzFrontDoorCustomRuleObject](./New-AzFrontDoorManagedRuleObject.md)</span></span>
