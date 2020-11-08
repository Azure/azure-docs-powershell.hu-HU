---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/update-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
ms.openlocfilehash: cafb705ec5f2882eb239931b22ccfba610721100
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185436"
---
# <span data-ttu-id="8c765-101">Update-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="8c765-101">Update-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="8c765-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8c765-102">SYNOPSIS</span></span>
<span data-ttu-id="8c765-103">A WAF házirend frissítése</span><span class="sxs-lookup"><span data-stu-id="8c765-103">Update WAF policy</span></span>

## <span data-ttu-id="8c765-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8c765-104">SYNTAX</span></span>

### <span data-ttu-id="8c765-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8c765-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c765-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c765-106">ByObjectParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c765-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c765-107">ByResourceIdParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c765-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8c765-108">DESCRIPTION</span></span>
<span data-ttu-id="8c765-109">Az **Update-AzFrontDoorWafPolicy** parancsmag egy meglévő WAF-házirendet frissít.</span><span class="sxs-lookup"><span data-stu-id="8c765-109">The **Update-AzFrontDoorWafPolicy** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="8c765-110">Ha a bemeneti paraméterek nem érhetők el, akkor a meglévő WAF-házirendből származó régi paramétereket fogja használni.</span><span class="sxs-lookup"><span data-stu-id="8c765-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="8c765-111">Példák</span><span class="sxs-lookup"><span data-stu-id="8c765-111">EXAMPLES</span></span>

### <span data-ttu-id="8c765-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8c765-112">Example 1</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -CustomBlockResponseStatusCode 403

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="8c765-113">A meglévő WAF-házirendek egyéni állapotkód frissítése</span><span class="sxs-lookup"><span data-stu-id="8c765-113">Update an existing WAF policy custom status code.</span></span>

### <span data-ttu-id="8c765-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="8c765-114">Example 2</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Detection            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="8c765-115">Meglévő WAF-házirendi mód frissítése</span><span class="sxs-lookup"><span data-stu-id="8c765-115">Update an existing WAF policy mode.</span></span>

### <span data-ttu-id="8c765-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="8c765-116">Example 3</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection -EnabledState Disabled

Name          PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----          ---------- ------------------ ----------------------------- -----------
{policyName}  Detection           Disabled                           403 https://www.bing.com/
```

<span data-ttu-id="8c765-117">Meglévő WAF-házirend állapotának és üzemmódjának frissítése</span><span class="sxs-lookup"><span data-stu-id="8c765-117">Update an existing WAF policy enabled state and mode.</span></span>

### <span data-ttu-id="8c765-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="8c765-118">Example 4</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Update-AzFrontDoorWafPolicy -Mode Detection -EnabledState Disabled
```

<span data-ttu-id="8c765-119">Az összes WAF-házirend frissítése a $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c765-119">Update all WAF policies in $resourceGroupName</span></span>

## <span data-ttu-id="8c765-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8c765-120">PARAMETERS</span></span>

### <span data-ttu-id="8c765-121">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="8c765-121">-CustomBlockResponseBody</span></span>
<span data-ttu-id="8c765-122">Egyéni válasz törzse</span><span class="sxs-lookup"><span data-stu-id="8c765-122">Custom Response Body</span></span>

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

### <span data-ttu-id="8c765-123">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="8c765-123">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="8c765-124">Egyéni válasz állapotkód</span><span class="sxs-lookup"><span data-stu-id="8c765-124">Custom Response Status Code</span></span>

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

### <span data-ttu-id="8c765-125">-Customrule</span><span class="sxs-lookup"><span data-stu-id="8c765-125">-Customrule</span></span>
<span data-ttu-id="8c765-126">A házirenden belüli egyéni szabályok</span><span class="sxs-lookup"><span data-stu-id="8c765-126">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="8c765-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c765-127">-DefaultProfile</span></span>
<span data-ttu-id="8c765-128">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8c765-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c765-129">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="8c765-129">-EnabledState</span></span>
<span data-ttu-id="8c765-130">A házirend engedélyezett állapotú vagy letiltott állapotú-e.</span><span class="sxs-lookup"><span data-stu-id="8c765-130">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="8c765-131">A lehetséges értékek a következők: "disabled", "engedélyezve"</span><span class="sxs-lookup"><span data-stu-id="8c765-131">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="8c765-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c765-132">-InputObject</span></span>
<span data-ttu-id="8c765-133">A frissítendő FireWallPolicy objektum.</span><span class="sxs-lookup"><span data-stu-id="8c765-133">The FireWallPolicy object to update.</span></span>

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

### <span data-ttu-id="8c765-134">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="8c765-134">-ManagedRule</span></span>
<span data-ttu-id="8c765-135">Felügyelt szabályok a házirenden belül</span><span class="sxs-lookup"><span data-stu-id="8c765-135">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="8c765-136">Üzemmód</span><span class="sxs-lookup"><span data-stu-id="8c765-136">-Mode</span></span>
<span data-ttu-id="8c765-137">Ez a cikk azt mutatja be, hogy az észlelési üzemmódban vagy a megelőzési módban van-e házirend szintű beállítás.</span><span class="sxs-lookup"><span data-stu-id="8c765-137">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="8c765-138">A lehetséges értékek a következők: "megelőzés", "észlelés"</span><span class="sxs-lookup"><span data-stu-id="8c765-138">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="8c765-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8c765-139">-Name</span></span>
<span data-ttu-id="8c765-140">A frissítendő FireWallPolicy neve.</span><span class="sxs-lookup"><span data-stu-id="8c765-140">The name of the FireWallPolicy to update.</span></span>

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

### <span data-ttu-id="8c765-141">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="8c765-141">-RedirectUrl</span></span>
<span data-ttu-id="8c765-142">Átirányítás URL-címe</span><span class="sxs-lookup"><span data-stu-id="8c765-142">Redirect URL</span></span>

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

### <span data-ttu-id="8c765-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c765-143">-ResourceGroupName</span></span>
<span data-ttu-id="8c765-144">Az az erőforráscsoport, amelyhez a FireWallPolicy tartozik.</span><span class="sxs-lookup"><span data-stu-id="8c765-144">The resource group to which the FireWallPolicy belongs.</span></span>

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

### <span data-ttu-id="8c765-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c765-145">-ResourceId</span></span>
<span data-ttu-id="8c765-146">A frissítendő FireWallPolicy erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="8c765-146">Resource Id of the FireWallPolicy to update</span></span>

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

### <span data-ttu-id="8c765-147">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8c765-147">-Confirm</span></span>
<span data-ttu-id="8c765-148">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8c765-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c765-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c765-149">-WhatIf</span></span>
<span data-ttu-id="8c765-150">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8c765-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c765-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8c765-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c765-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c765-152">CommonParameters</span></span>
<span data-ttu-id="8c765-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8c765-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c765-154">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8c765-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c765-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c765-155">INPUTS</span></span>

### <span data-ttu-id="8c765-156">Microsoft. Azure. Command. FrontDoor. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="8c765-156">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="8c765-157">System. String</span><span class="sxs-lookup"><span data-stu-id="8c765-157">System.String</span></span>

## <span data-ttu-id="8c765-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c765-158">OUTPUTS</span></span>

### <span data-ttu-id="8c765-159">Microsoft. Azure. Command. FrontDoor. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="8c765-159">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="8c765-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8c765-160">NOTES</span></span>

## <span data-ttu-id="8c765-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c765-161">RELATED LINKS</span></span>

<span data-ttu-id="8c765-162">[Új – AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [Új – AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [Új – AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="8c765-162">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
