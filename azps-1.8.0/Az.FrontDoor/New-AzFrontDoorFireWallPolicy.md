---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFireWallPolicy.md
ms.openlocfilehash: 67caf6c97c493ad1d19b95ef00c896cb96a47582
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836165"
---
# <span data-ttu-id="8d308-101">New-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="8d308-101">New-AzFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="8d308-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8d308-102">SYNOPSIS</span></span>
<span data-ttu-id="8d308-103">WAF-házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="8d308-103">Create WAF policy</span></span>

## <span data-ttu-id="8d308-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8d308-104">SYNTAX</span></span>

```
New-AzFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d308-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8d308-105">DESCRIPTION</span></span>
<span data-ttu-id="8d308-106">A **New-AzFrontDoorFireWallPolicy** parancsmag új Azure WAF-házirendet hoz létre az aktuális előfizetés csoportban a megadott erőforrás csoportban.</span><span class="sxs-lookup"><span data-stu-id="8d308-106">The **New-AzFrontDoorFireWallPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="8d308-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8d308-107">EXAMPLES</span></span>

### <span data-ttu-id="8d308-108">1. példa: WAF-házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="8d308-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="8d308-109">WAF-házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="8d308-109">Create WAF policy</span></span>

## <span data-ttu-id="8d308-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8d308-110">PARAMETERS</span></span>

### <span data-ttu-id="8d308-111">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="8d308-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="8d308-112">Egyéni válasz törzse</span><span class="sxs-lookup"><span data-stu-id="8d308-112">Custom Response Body</span></span>

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

### <span data-ttu-id="8d308-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="8d308-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="8d308-114">Egyéni válasz állapotkód</span><span class="sxs-lookup"><span data-stu-id="8d308-114">Custom Response Status Code</span></span>

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

### <span data-ttu-id="8d308-115">-Customrule</span><span class="sxs-lookup"><span data-stu-id="8d308-115">-Customrule</span></span>
<span data-ttu-id="8d308-116">A házirenden belüli egyéni szabályok</span><span class="sxs-lookup"><span data-stu-id="8d308-116">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="8d308-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d308-117">-DefaultProfile</span></span>
<span data-ttu-id="8d308-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d308-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d308-119">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="8d308-119">-EnabledState</span></span>
<span data-ttu-id="8d308-120">A házirend engedélyezett állapotú vagy letiltott állapotú-e.</span><span class="sxs-lookup"><span data-stu-id="8d308-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="8d308-121">A lehetséges értékek a következők: "disabled", "engedélyezve"</span><span class="sxs-lookup"><span data-stu-id="8d308-121">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="8d308-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="8d308-122">-ManagedRule</span></span>
<span data-ttu-id="8d308-123">Felügyelt szabályok a házirenden belül</span><span class="sxs-lookup"><span data-stu-id="8d308-123">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="8d308-124">Üzemmód</span><span class="sxs-lookup"><span data-stu-id="8d308-124">-Mode</span></span>
<span data-ttu-id="8d308-125">Ez a cikk azt mutatja be, hogy az észlelési üzemmódban vagy a megelőzési módban van-e házirend szintű beállítás.</span><span class="sxs-lookup"><span data-stu-id="8d308-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="8d308-126">A lehetséges értékek a következők: "megelőzés", "észlelés"</span><span class="sxs-lookup"><span data-stu-id="8d308-126">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="8d308-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8d308-127">-Name</span></span>
<span data-ttu-id="8d308-128">WebApplicationFireWallPolicy neve</span><span class="sxs-lookup"><span data-stu-id="8d308-128">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="8d308-129">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="8d308-129">-RedirectUrl</span></span>
<span data-ttu-id="8d308-130">Átirányítás URL-címe</span><span class="sxs-lookup"><span data-stu-id="8d308-130">Redirect URL</span></span>

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

### <span data-ttu-id="8d308-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d308-131">-ResourceGroupName</span></span>
<span data-ttu-id="8d308-132">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="8d308-132">The resource group name</span></span>

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

### <span data-ttu-id="8d308-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8d308-133">-Confirm</span></span>
<span data-ttu-id="8d308-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8d308-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d308-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d308-135">-WhatIf</span></span>
<span data-ttu-id="8d308-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8d308-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d308-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8d308-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d308-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d308-138">CommonParameters</span></span>
<span data-ttu-id="8d308-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8d308-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d308-140">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8d308-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d308-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d308-141">INPUTS</span></span>

### <span data-ttu-id="8d308-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="8d308-142">None</span></span>

## <span data-ttu-id="8d308-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d308-143">OUTPUTS</span></span>

### <span data-ttu-id="8d308-144">Microsoft. Azure. Command. FrontDoor. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="8d308-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="8d308-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8d308-145">NOTES</span></span>

## <span data-ttu-id="8d308-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d308-146">RELATED LINKS</span></span>

<span data-ttu-id="8d308-147">[Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md) 
 [Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md) 
 [Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md) 
 [Új – AzFrontDoorManagedRuleObject](./New-AzFrontDoorManagedRuleObject.md) 
 [Új – AzFrontDoorCustomRuleObject](./New-AzFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="8d308-147">[Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)
[Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md)
[Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md)
[New-AzFrontDoorManagedRuleObject](./New-AzFrontDoorManagedRuleObject.md)
[New-AzFrontDoorCustomRuleObject](./New-AzFrontDoorManagedRuleObject.md)</span></span>
