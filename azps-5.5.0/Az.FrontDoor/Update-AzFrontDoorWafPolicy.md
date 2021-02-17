---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/update-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
ms.openlocfilehash: a3358681fd501602833f0168a6920dc2c3ec7864
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209447"
---
# <span data-ttu-id="d69f4-101">Update-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="d69f4-101">Update-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="d69f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d69f4-102">SYNOPSIS</span></span>
<span data-ttu-id="d69f4-103">WaF-házirend frissítése</span><span class="sxs-lookup"><span data-stu-id="d69f4-103">Update WAF policy</span></span>

## <span data-ttu-id="d69f4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d69f4-104">SYNTAX</span></span>

### <span data-ttu-id="d69f4-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d69f4-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>] [-RequestBodyCheck <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d69f4-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d69f4-106">ByObjectParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>] [-RequestBodyCheck <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d69f4-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d69f4-107">ByResourceIdParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>] [-RequestBodyCheck <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d69f4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d69f4-108">DESCRIPTION</span></span>
<span data-ttu-id="d69f4-109">Az **Update-AzFrontDoorWafPolicy** parancsmag frissíti a meglévő WAF-házirendeket.</span><span class="sxs-lookup"><span data-stu-id="d69f4-109">The **Update-AzFrontDoorWafPolicy** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="d69f4-110">Ha nem ad meg bemeneti paramétereket, a meglévő waf-házirend régi paraméterei lesznek használatosak.</span><span class="sxs-lookup"><span data-stu-id="d69f4-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="d69f4-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d69f4-111">EXAMPLES</span></span>

### <span data-ttu-id="d69f4-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="d69f4-112">Example 1</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -CustomBlockResponseStatusCode 403

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="d69f4-113">Meglévő waf-házirend egyéni állapotkód frissítése.</span><span class="sxs-lookup"><span data-stu-id="d69f4-113">Update an existing WAF policy custom status code.</span></span>

### <span data-ttu-id="d69f4-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="d69f4-114">Example 2</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Detection            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="d69f4-115">Meglévő WaF-házirendmód frissítése</span><span class="sxs-lookup"><span data-stu-id="d69f4-115">Update an existing WAF policy mode.</span></span>

### <span data-ttu-id="d69f4-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="d69f4-116">Example 3</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection -EnabledState Disabled

Name          PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----          ---------- ------------------ ----------------------------- -----------
{policyName}  Detection           Disabled                           403 https://www.bing.com/
```

<span data-ttu-id="d69f4-117">Meglévő waf-házirend állapotának és módjának frissítése.</span><span class="sxs-lookup"><span data-stu-id="d69f4-117">Update an existing WAF policy enabled state and mode.</span></span>

### <span data-ttu-id="d69f4-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="d69f4-118">Example 4</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Update-AzFrontDoorWafPolicy -Mode Detection -EnabledState Disabled
```

<span data-ttu-id="d69f4-119">Az összes waf-házirend frissítése a $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d69f4-119">Update all WAF policies in $resourceGroupName</span></span>

## <span data-ttu-id="d69f4-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d69f4-120">PARAMETERS</span></span>

### <span data-ttu-id="d69f4-121">-CustomBlockResponseBlock</span><span class="sxs-lookup"><span data-stu-id="d69f4-121">-CustomBlockResponseBody</span></span>
<span data-ttu-id="d69f4-122">Egyéni válasz törzse</span><span class="sxs-lookup"><span data-stu-id="d69f4-122">Custom Response Body</span></span>

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

### <span data-ttu-id="d69f4-123">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="d69f4-123">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="d69f4-124">Egyéni válaszállapot-kód</span><span class="sxs-lookup"><span data-stu-id="d69f4-124">Custom Response Status Code</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d69f4-125">-Customrule</span><span class="sxs-lookup"><span data-stu-id="d69f4-125">-Customrule</span></span>
<span data-ttu-id="d69f4-126">Egyéni szabályok a házirenden belül</span><span class="sxs-lookup"><span data-stu-id="d69f4-126">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="d69f4-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d69f4-127">-DefaultProfile</span></span>
<span data-ttu-id="d69f4-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d69f4-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d69f4-129">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="d69f4-129">-EnabledState</span></span>
<span data-ttu-id="d69f4-130">Hogy a házirend engedélyezett vagy letiltott állapotban van-e.</span><span class="sxs-lookup"><span data-stu-id="d69f4-130">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="d69f4-131">Lehetséges értékek: "Letiltva", "Engedélyezve"</span><span class="sxs-lookup"><span data-stu-id="d69f4-131">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="d69f4-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d69f4-132">-InputObject</span></span>
<span data-ttu-id="d69f4-133">Frissítenünk kell a FireWallPolicy objektumot.</span><span class="sxs-lookup"><span data-stu-id="d69f4-133">The FireWallPolicy object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d69f4-134">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="d69f4-134">-ManagedRule</span></span>
<span data-ttu-id="d69f4-135">Felügyelt szabályok a házirenden belül</span><span class="sxs-lookup"><span data-stu-id="d69f4-135">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="d69f4-136">-Mód</span><span class="sxs-lookup"><span data-stu-id="d69f4-136">-Mode</span></span>
<span data-ttu-id="d69f4-137">Ez a cikk azt ismerteti, hogy észlelési vagy megelőzési módban van-e házirendszinten.</span><span class="sxs-lookup"><span data-stu-id="d69f4-137">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="d69f4-138">Lehetséges értékek: "Megelőzés", "Észlelés"</span><span class="sxs-lookup"><span data-stu-id="d69f4-138">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="d69f4-139">-Name</span><span class="sxs-lookup"><span data-stu-id="d69f4-139">-Name</span></span>
<span data-ttu-id="d69f4-140">A frissítenie kell a FireWallPolicy neve.</span><span class="sxs-lookup"><span data-stu-id="d69f4-140">The name of the FireWallPolicy to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d69f4-141">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="d69f4-141">-RedirectUrl</span></span>
<span data-ttu-id="d69f4-142">Url-cím átirányítása</span><span class="sxs-lookup"><span data-stu-id="d69f4-142">Redirect URL</span></span>

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

### <span data-ttu-id="d69f4-143">-RequestCheck</span><span class="sxs-lookup"><span data-stu-id="d69f4-143">-RequestBodyCheck</span></span>
<span data-ttu-id="d69f4-144">Azt határozza meg, hogy a felügyelt szabályoknak meg kell-e vizsgálniuk a törzset.</span><span class="sxs-lookup"><span data-stu-id="d69f4-144">Defines if the body should be inspected by managed rules.</span></span> <span data-ttu-id="d69f4-145">Lehetséges értékek: "Engedélyezve", "Letiltva"</span><span class="sxs-lookup"><span data-stu-id="d69f4-145">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="d69f4-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d69f4-146">-ResourceGroupName</span></span>
<span data-ttu-id="d69f4-147">Az az erőforráscsoport, amelyhez a FireWallPolicy tartozik.</span><span class="sxs-lookup"><span data-stu-id="d69f4-147">The resource group to which the FireWallPolicy belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d69f4-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d69f4-148">-ResourceId</span></span>
<span data-ttu-id="d69f4-149">Frissítenünk kell a FireWallPolicy erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="d69f4-149">Resource Id of the FireWallPolicy to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d69f4-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d69f4-150">-Confirm</span></span>
<span data-ttu-id="d69f4-151">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d69f4-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d69f4-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d69f4-152">-WhatIf</span></span>
<span data-ttu-id="d69f4-153">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d69f4-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d69f4-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d69f4-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d69f4-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d69f4-155">CommonParameters</span></span>
<span data-ttu-id="d69f4-156">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d69f4-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d69f4-157">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d69f4-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d69f4-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d69f4-158">INPUTS</span></span>

### <span data-ttu-id="d69f4-159">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="d69f4-159">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="d69f4-160">System.String</span><span class="sxs-lookup"><span data-stu-id="d69f4-160">System.String</span></span>

## <span data-ttu-id="d69f4-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d69f4-161">OUTPUTS</span></span>

### <span data-ttu-id="d69f4-162">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="d69f4-162">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="d69f4-163">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d69f4-163">NOTES</span></span>

## <span data-ttu-id="d69f4-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d69f4-164">RELATED LINKS</span></span>

<span data-ttu-id="d69f4-165">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="d69f4-165">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
