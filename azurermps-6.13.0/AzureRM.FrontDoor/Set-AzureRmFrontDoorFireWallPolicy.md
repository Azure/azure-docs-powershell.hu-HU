---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/set-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: a02510cc72b9e674f9d4fded1355ae5b2cadc807
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93671968"
---
# <span data-ttu-id="1edcd-101">Set-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="1edcd-101">Set-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="1edcd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1edcd-102">SYNOPSIS</span></span>
<span data-ttu-id="1edcd-103">a WAF házirend frissítése</span><span class="sxs-lookup"><span data-stu-id="1edcd-103">update WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1edcd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1edcd-104">SYNTAX</span></span>

### <span data-ttu-id="1edcd-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1edcd-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1edcd-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1edcd-106">ByObjectParameterSet</span></span>
```
Set-AzureRmFrontDoorFireWallPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1edcd-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1edcd-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmFrontDoorFireWallPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1edcd-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1edcd-108">DESCRIPTION</span></span>
<span data-ttu-id="1edcd-109">A **set-AzureRmFrontDoor** parancsmag egy meglévő WAF-házirendet frissít.</span><span class="sxs-lookup"><span data-stu-id="1edcd-109">The **Set-AzureRmFrontDoor** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="1edcd-110">Ha a bemeneti paraméterek nem érhetők el, akkor a meglévő WAF-házirendből származó régi paramétereket fogja használni.</span><span class="sxs-lookup"><span data-stu-id="1edcd-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="1edcd-111">Példák</span><span class="sxs-lookup"><span data-stu-id="1edcd-111">EXAMPLES</span></span>

### <span data-ttu-id="1edcd-112">Példa 1: meglévő WAF-házirend frissítése</span><span class="sxs-lookup"><span data-stu-id="1edcd-112">Example 1: update an existing WAF policy</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -Name $name -ResourceGroupName $resourceGroup -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $node

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="1edcd-113">meglévő WAF-házirend frissítése</span><span class="sxs-lookup"><span data-stu-id="1edcd-113">update an existing WAF policy</span></span>

### <span data-ttu-id="1edcd-114">2. példa: meglévő WAF-házirend frissítése</span><span class="sxs-lookup"><span data-stu-id="1edcd-114">Example 2: update an existing WAF policy</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -InputObject $policy1 -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="1edcd-115">meglévő WAF-házirend frissítése</span><span class="sxs-lookup"><span data-stu-id="1edcd-115">update an existing WAF policy</span></span>

### <span data-ttu-id="1edcd-116">3. példa: meglévő WAF-házirend frissítése</span><span class="sxs-lookup"><span data-stu-id="1edcd-116">Example 3: update an existing WAF policy</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -ResourceId $resourcdId -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="1edcd-117">meglévő WAF-házirend frissítése</span><span class="sxs-lookup"><span data-stu-id="1edcd-117">update an existing WAF policy</span></span>

### <span data-ttu-id="1edcd-118">4. példa: az összes WAF-házirend frissítése a $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="1edcd-118">Example 4: update all WAF policies in $resourceGroup</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoorFireWallPolicy -ResourceGroupName $resourceGroup | Set-AzureRmFrontDoorFireWallPolicy -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode
```

<span data-ttu-id="1edcd-119">az összes WAF-házirend frissítése a $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="1edcd-119">update all WAF policies in $resourceGroup</span></span>

## <span data-ttu-id="1edcd-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1edcd-120">PARAMETERS</span></span>

### <span data-ttu-id="1edcd-121">-Customrule</span><span class="sxs-lookup"><span data-stu-id="1edcd-121">-Customrule</span></span>
<span data-ttu-id="1edcd-122">A házirenden belüli egyéni szabályok</span><span class="sxs-lookup"><span data-stu-id="1edcd-122">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="1edcd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1edcd-123">-DefaultProfile</span></span>
<span data-ttu-id="1edcd-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1edcd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1edcd-125">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="1edcd-125">-EnabledState</span></span>
<span data-ttu-id="1edcd-126">A házirend engedélyezett állapotú vagy letiltott állapotú-e.</span><span class="sxs-lookup"><span data-stu-id="1edcd-126">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="1edcd-127">A lehetséges értékek a következők: "disabled", "engedélyezve"</span><span class="sxs-lookup"><span data-stu-id="1edcd-127">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="1edcd-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1edcd-128">-InputObject</span></span>
<span data-ttu-id="1edcd-129">A frissítendő FireWallPolicy objektum.</span><span class="sxs-lookup"><span data-stu-id="1edcd-129">The FireWallPolicy object to update.</span></span>

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

### <span data-ttu-id="1edcd-130">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="1edcd-130">-ManagedRule</span></span>
<span data-ttu-id="1edcd-131">Felügyelt szabályok a házirenden belül</span><span class="sxs-lookup"><span data-stu-id="1edcd-131">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="1edcd-132">Üzemmód</span><span class="sxs-lookup"><span data-stu-id="1edcd-132">-Mode</span></span>
<span data-ttu-id="1edcd-133">Ez a cikk azt mutatja be, hogy az észlelési üzemmódban vagy a megelőzési módban van-e házirend szintű beállítás.</span><span class="sxs-lookup"><span data-stu-id="1edcd-133">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="1edcd-134">A lehetséges értékek a következők: "megelőzés", "észlelés"</span><span class="sxs-lookup"><span data-stu-id="1edcd-134">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="1edcd-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1edcd-135">-Name</span></span>
<span data-ttu-id="1edcd-136">A frissítendő FireWallPolicy neve.</span><span class="sxs-lookup"><span data-stu-id="1edcd-136">The name of the FireWallPolicy to update.</span></span>

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

### <span data-ttu-id="1edcd-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1edcd-137">-ResourceGroupName</span></span>
<span data-ttu-id="1edcd-138">Az az erőforráscsoport, amelyhez a FireWallPolicy tartozik.</span><span class="sxs-lookup"><span data-stu-id="1edcd-138">The resource group to which the FireWallPolicy belongs.</span></span>

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

### <span data-ttu-id="1edcd-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1edcd-139">-ResourceId</span></span>
<span data-ttu-id="1edcd-140">A frissítendő FireWallPolicy erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="1edcd-140">Resource Id of the FireWallPolicy to update</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1edcd-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1edcd-141">-Confirm</span></span>
<span data-ttu-id="1edcd-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1edcd-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1edcd-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1edcd-143">-WhatIf</span></span>
<span data-ttu-id="1edcd-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1edcd-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1edcd-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1edcd-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1edcd-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1edcd-146">CommonParameters</span></span>
<span data-ttu-id="1edcd-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1edcd-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1edcd-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1edcd-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1edcd-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1edcd-149">INPUTS</span></span>

### <span data-ttu-id="1edcd-150">Microsoft. Azure. Command. FrontDoor. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="1edcd-150">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="1edcd-151">System. String</span><span class="sxs-lookup"><span data-stu-id="1edcd-151">System.String</span></span>

## <span data-ttu-id="1edcd-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1edcd-152">OUTPUTS</span></span>

### <span data-ttu-id="1edcd-153">Microsoft. Azure. Command. FrontDoor. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="1edcd-153">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="1edcd-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1edcd-154">NOTES</span></span>

## <span data-ttu-id="1edcd-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1edcd-155">RELATED LINKS</span></span>

<span data-ttu-id="1edcd-156">[Új – AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md) 
 [Új – AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md) 
 [Új – AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="1edcd-156">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)
[New-AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)
[New-AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span></span>
