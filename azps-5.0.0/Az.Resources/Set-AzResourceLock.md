---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
ms.openlocfilehash: c532633de593294c6b5dbe0e09b9615a1d5355a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300950"
---
# <span data-ttu-id="4826b-101">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="4826b-101">Set-AzResourceLock</span></span>

## <span data-ttu-id="4826b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4826b-102">SYNOPSIS</span></span>
<span data-ttu-id="4826b-103">Módosítja az erőforrás-zárolást.</span><span class="sxs-lookup"><span data-stu-id="4826b-103">Modifies a resource lock.</span></span>

## <span data-ttu-id="4826b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4826b-104">SYNTAX</span></span>

### <span data-ttu-id="4826b-105">BySpecifiedScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4826b-105">BySpecifiedScope (Default)</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4826b-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4826b-106">ByResourceGroup</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4826b-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="4826b-107">ByResourceGroupLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4826b-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="4826b-108">BySubscription</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4826b-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="4826b-109">BySubscriptionLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4826b-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="4826b-110">ByLockId</span></span>
```
Set-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4826b-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="4826b-111">DESCRIPTION</span></span>
<span data-ttu-id="4826b-112">A **set-AzResourceLock** parancsmag módosítja az erőforrás-zárolást.</span><span class="sxs-lookup"><span data-stu-id="4826b-112">The **Set-AzResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="4826b-113">Példák</span><span class="sxs-lookup"><span data-stu-id="4826b-113">EXAMPLES</span></span>

### <span data-ttu-id="4826b-114">Példa 1: a zárolási megjegyzések frissítése</span><span class="sxs-lookup"><span data-stu-id="4826b-114">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="4826b-115">A parancs frissíti a ContosoSiteLock nevű zárolás megjegyzését.</span><span class="sxs-lookup"><span data-stu-id="4826b-115">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="4826b-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4826b-116">PARAMETERS</span></span>

### <span data-ttu-id="4826b-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4826b-117">-ApiVersion</span></span>
<span data-ttu-id="4826b-118">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4826b-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="4826b-119">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="4826b-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="4826b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4826b-120">-DefaultProfile</span></span>
<span data-ttu-id="4826b-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4826b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4826b-122">-Force</span><span class="sxs-lookup"><span data-stu-id="4826b-122">-Force</span></span>
<span data-ttu-id="4826b-123">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="4826b-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4826b-124">-LockId</span><span class="sxs-lookup"><span data-stu-id="4826b-124">-LockId</span></span>
<span data-ttu-id="4826b-125">A parancsmag által módosított zárolás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4826b-125">Specifies the ID of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4826b-126">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="4826b-126">-LockLevel</span></span>
<span data-ttu-id="4826b-127">A zárolás szintjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4826b-127">Specifies the level for the lock.</span></span>
<span data-ttu-id="4826b-128">Jelenleg az egyetlen érvényes érték a CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="4826b-128">Currently, the only valid value is CanNotDelete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: CanNotDelete, ReadOnly

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4826b-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="4826b-129">-LockName</span></span>
<span data-ttu-id="4826b-130">A parancsmag által módosított zárolás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4826b-130">Specifies the name of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope, ByResourceGroup, ByResourceGroupLevel, BySubscription, BySubscriptionLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4826b-131">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="4826b-131">-LockNotes</span></span>
<span data-ttu-id="4826b-132">A zároláshoz kapcsolódó jegyzeteket adja meg.</span><span class="sxs-lookup"><span data-stu-id="4826b-132">Specifies the notes for the lock.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Notes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4826b-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="4826b-133">-Pre</span></span>
<span data-ttu-id="4826b-134">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="4826b-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4826b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4826b-135">-ResourceGroupName</span></span>
<span data-ttu-id="4826b-136">Annak az erőforráscsoport-csoportnak a neve, amelyhez a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="4826b-136">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4826b-137">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="4826b-137">-ResourceName</span></span>
<span data-ttu-id="4826b-138">Annak az erőforrásnak a nevét adja meg, amelynek a zárolását alkalmazni kívánja.</span><span class="sxs-lookup"><span data-stu-id="4826b-138">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="4826b-139">Ha például egy adatbázist szeretne megadni, használja a következő formátumot: kiszolgálói `/` adatbázis</span><span class="sxs-lookup"><span data-stu-id="4826b-139">For instance, to specify a database, use the following format: Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4826b-140">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="4826b-140">-ResourceType</span></span>
<span data-ttu-id="4826b-141">Annak az erőforrásnak a típusa, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="4826b-141">Specifies the resource type for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4826b-142">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="4826b-142">-Scope</span></span>
<span data-ttu-id="4826b-143">Azt a hatókört adja meg, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="4826b-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="4826b-144">Ha például meg szeretne adni egy adatbázist, használja a következő formátumot: `/subscriptions/` előfizetés-azonosító `/resourceGroups/` erőforráscsoport neve `/providers/Microsoft.Sql/servers/` kiszolgálónév `/databases/` -adatbázis neve az erőforráscsoport megadásához, használja a következő formátumot: `/subscriptions/` előfizetés azonosítója `/resourceGroups/` Erőforrás-csoport neve</span><span class="sxs-lookup"><span data-stu-id="4826b-144">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4826b-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4826b-145">-Confirm</span></span>
<span data-ttu-id="4826b-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4826b-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4826b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4826b-147">-WhatIf</span></span>
<span data-ttu-id="4826b-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4826b-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4826b-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4826b-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4826b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4826b-150">CommonParameters</span></span>
<span data-ttu-id="4826b-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4826b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4826b-152">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4826b-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4826b-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4826b-153">INPUTS</span></span>

### <span data-ttu-id="4826b-154">System. String</span><span class="sxs-lookup"><span data-stu-id="4826b-154">System.String</span></span>

### <span data-ttu-id="4826b-155">Microsoft. Azure. Command. ResourceManager. parancsmagok. jogalanyok. locks. LockLevel</span><span class="sxs-lookup"><span data-stu-id="4826b-155">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="4826b-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4826b-156">OUTPUTS</span></span>

### <span data-ttu-id="4826b-157">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="4826b-157">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4826b-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4826b-158">NOTES</span></span>

## <span data-ttu-id="4826b-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4826b-159">RELATED LINKS</span></span>

[<span data-ttu-id="4826b-160">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="4826b-160">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="4826b-161">Új – AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="4826b-161">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="4826b-162">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="4826b-162">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)


