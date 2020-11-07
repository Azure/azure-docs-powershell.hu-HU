---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/update-azfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorFireWallPolicy.md
ms.openlocfilehash: 3e0502d3503bdbf95fb81c779829b73e896b150f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836105"
---
# <span data-ttu-id="e8df4-101">Update-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="e8df4-101">Update-AzFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="e8df4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e8df4-102">SYNOPSIS</span></span>
<span data-ttu-id="e8df4-103">A WAF házirend frissítése</span><span class="sxs-lookup"><span data-stu-id="e8df4-103">Update WAF policy</span></span>

## <span data-ttu-id="e8df4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e8df4-104">SYNTAX</span></span>

### <span data-ttu-id="e8df4-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e8df4-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8df4-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8df4-106">ByObjectParameterSet</span></span>
```
Update-AzFrontDoorFireWallPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8df4-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8df4-107">ByResourceIdParameterSet</span></span>
```
Update-AzFrontDoorFireWallPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8df4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e8df4-108">DESCRIPTION</span></span>
<span data-ttu-id="e8df4-109">Az **Update-AzFrontDoorFireWallPolicy** parancsmag egy meglévő WAF-házirendet frissít.</span><span class="sxs-lookup"><span data-stu-id="e8df4-109">The **Update-AzFrontDoorFireWallPolicy** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="e8df4-110">Ha a bemeneti paraméterek nem érhetők el, akkor a meglévő WAF-házirendből származó régi paramétereket fogja használni.</span><span class="sxs-lookup"><span data-stu-id="e8df4-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="e8df4-111">Példák</span><span class="sxs-lookup"><span data-stu-id="e8df4-111">EXAMPLES</span></span>

### <span data-ttu-id="e8df4-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e8df4-112">Example 1</span></span>
```powershell
PS C:\> Update-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName -CustomBlockResponseStatusCode 403

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="e8df4-113">A meglévő WAF-házirendek egyéni állapotkód frissítése</span><span class="sxs-lookup"><span data-stu-id="e8df4-113">Update an existing WAF policy custom status code.</span></span>

### <span data-ttu-id="e8df4-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="e8df4-114">Example 2</span></span>
```powershell
PS C:\> Update-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Detection            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="e8df4-115">Meglévő WAF-házirendi mód frissítése</span><span class="sxs-lookup"><span data-stu-id="e8df4-115">Update an existing WAF policy mode.</span></span>

### <span data-ttu-id="e8df4-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="e8df4-116">Example 3</span></span>
```powershell
PS C:\> Update-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection -EnabledState Disabled

Name          PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----          ---------- ------------------ ----------------------------- -----------
{policyName}  Detection           Disabled                           403 https://www.bing.com/
```

<span data-ttu-id="e8df4-117">Meglévő WAF-házirend állapotának és üzemmódjának frissítése</span><span class="sxs-lookup"><span data-stu-id="e8df4-117">Update an existing WAF policy enabled state and mode.</span></span>

### <span data-ttu-id="e8df4-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="e8df4-118">Example 4</span></span>
```powershell
PS C:\> Get-AzFrontDoorFireWallPolicy -ResourceGroupName $resourceGroupName | Update-AzFrontDoorFireWallPolicy -Mode Detection -EnabledState Disabled
```

<span data-ttu-id="e8df4-119">Az összes WAF-házirend frissítése a $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8df4-119">Update all WAF policies in $resourceGroupName</span></span>

## <span data-ttu-id="e8df4-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e8df4-120">PARAMETERS</span></span>

### <span data-ttu-id="e8df4-121">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="e8df4-121">-CustomBlockResponseBody</span></span>
<span data-ttu-id="e8df4-122">Egyéni válasz törzse</span><span class="sxs-lookup"><span data-stu-id="e8df4-122">Custom Response Body</span></span>

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

### <span data-ttu-id="e8df4-123">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="e8df4-123">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="e8df4-124">Egyéni válasz állapotkód</span><span class="sxs-lookup"><span data-stu-id="e8df4-124">Custom Response Status Code</span></span>

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

### <span data-ttu-id="e8df4-125">-Customrule</span><span class="sxs-lookup"><span data-stu-id="e8df4-125">-Customrule</span></span>
<span data-ttu-id="e8df4-126">A házirenden belüli egyéni szabályok</span><span class="sxs-lookup"><span data-stu-id="e8df4-126">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="e8df4-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8df4-127">-DefaultProfile</span></span>
<span data-ttu-id="e8df4-128">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e8df4-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8df4-129">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="e8df4-129">-EnabledState</span></span>
<span data-ttu-id="e8df4-130">A házirend engedélyezett állapotú vagy letiltott állapotú-e.</span><span class="sxs-lookup"><span data-stu-id="e8df4-130">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="e8df4-131">A lehetséges értékek a következők: "disabled", "engedélyezve"</span><span class="sxs-lookup"><span data-stu-id="e8df4-131">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="e8df4-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8df4-132">-InputObject</span></span>
<span data-ttu-id="e8df4-133">A frissítendő FireWallPolicy objektum.</span><span class="sxs-lookup"><span data-stu-id="e8df4-133">The FireWallPolicy object to update.</span></span>

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

### <span data-ttu-id="e8df4-134">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="e8df4-134">-ManagedRule</span></span>
<span data-ttu-id="e8df4-135">Felügyelt szabályok a házirenden belül</span><span class="sxs-lookup"><span data-stu-id="e8df4-135">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="e8df4-136">Üzemmód</span><span class="sxs-lookup"><span data-stu-id="e8df4-136">-Mode</span></span>
<span data-ttu-id="e8df4-137">Ez a cikk azt mutatja be, hogy az észlelési üzemmódban vagy a megelőzési módban van-e házirend szintű beállítás.</span><span class="sxs-lookup"><span data-stu-id="e8df4-137">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="e8df4-138">A lehetséges értékek a következők: "megelőzés", "észlelés"</span><span class="sxs-lookup"><span data-stu-id="e8df4-138">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="e8df4-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e8df4-139">-Name</span></span>
<span data-ttu-id="e8df4-140">A frissítendő FireWallPolicy neve.</span><span class="sxs-lookup"><span data-stu-id="e8df4-140">The name of the FireWallPolicy to update.</span></span>

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

### <span data-ttu-id="e8df4-141">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="e8df4-141">-RedirectUrl</span></span>
<span data-ttu-id="e8df4-142">Átirányítás URL-címe</span><span class="sxs-lookup"><span data-stu-id="e8df4-142">Redirect URL</span></span>

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

### <span data-ttu-id="e8df4-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8df4-143">-ResourceGroupName</span></span>
<span data-ttu-id="e8df4-144">Az az erőforráscsoport, amelyhez a FireWallPolicy tartozik.</span><span class="sxs-lookup"><span data-stu-id="e8df4-144">The resource group to which the FireWallPolicy belongs.</span></span>

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

### <span data-ttu-id="e8df4-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8df4-145">-ResourceId</span></span>
<span data-ttu-id="e8df4-146">A frissítendő FireWallPolicy erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="e8df4-146">Resource Id of the FireWallPolicy to update</span></span>

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

### <span data-ttu-id="e8df4-147">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e8df4-147">-Confirm</span></span>
<span data-ttu-id="e8df4-148">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e8df4-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8df4-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8df4-149">-WhatIf</span></span>
<span data-ttu-id="e8df4-150">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e8df4-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8df4-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e8df4-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8df4-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8df4-152">CommonParameters</span></span>
<span data-ttu-id="e8df4-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e8df4-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8df4-154">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e8df4-154">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8df4-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8df4-155">INPUTS</span></span>

### <span data-ttu-id="e8df4-156">Microsoft. Azure. Command. FrontDoor. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="e8df4-156">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="e8df4-157">System. String</span><span class="sxs-lookup"><span data-stu-id="e8df4-157">System.String</span></span>

## <span data-ttu-id="e8df4-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8df4-158">OUTPUTS</span></span>

### <span data-ttu-id="e8df4-159">Microsoft. Azure. Command. FrontDoor. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="e8df4-159">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="e8df4-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e8df4-160">NOTES</span></span>

## <span data-ttu-id="e8df4-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8df4-161">RELATED LINKS</span></span>

<span data-ttu-id="e8df4-162">[Új – AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md) 
 [Új – AzFrontDoorManagedRuleObject](./New-AzFrontDoorManagedRuleObject.md) 
 [Új – AzFrontDoorCustomRuleObject](./New-AzFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="e8df4-162">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md)
[New-AzFrontDoorManagedRuleObject](./New-AzFrontDoorManagedRuleObject.md)
[New-AzFrontDoorCustomRuleObject](./New-AzFrontDoorManagedRuleObject.md)</span></span>
