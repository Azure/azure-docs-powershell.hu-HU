---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
ms.openlocfilehash: a0d796d49114cc11fcc50aef85a3ab502593dc35
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838908"
---
# <span data-ttu-id="d8484-101">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="d8484-101">New-AzResourceLock</span></span>

## <span data-ttu-id="d8484-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d8484-102">SYNOPSIS</span></span>
<span data-ttu-id="d8484-103">Erőforrás-zárolást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d8484-103">Creates a resource lock.</span></span>

## <span data-ttu-id="d8484-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d8484-104">SYNTAX</span></span>

### <span data-ttu-id="d8484-105">BySpecifiedScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d8484-105">BySpecifiedScope (Default)</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8484-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d8484-106">ByResourceGroup</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8484-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="d8484-107">ByResourceGroupLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8484-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="d8484-108">BySubscription</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8484-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="d8484-109">BySubscriptionLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8484-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="d8484-110">ByTenantLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8484-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="d8484-111">ByLockId</span></span>
```
New-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d8484-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="d8484-112">DESCRIPTION</span></span>
<span data-ttu-id="d8484-113">A **New-AzResourceLock** parancsmag létrehoz egy erőforrás-zárolást.</span><span class="sxs-lookup"><span data-stu-id="d8484-113">The **New-AzResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="d8484-114">Példák</span><span class="sxs-lookup"><span data-stu-id="d8484-114">EXAMPLES</span></span>

### <span data-ttu-id="d8484-115">Példa 1: erőforrás-zárolás létrehozása webhelyre</span><span class="sxs-lookup"><span data-stu-id="d8484-115">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="d8484-116">Ez a parancs egy erőforrás-zárolást hoz létre egy webhelyen.</span><span class="sxs-lookup"><span data-stu-id="d8484-116">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="d8484-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d8484-117">PARAMETERS</span></span>

### <span data-ttu-id="d8484-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d8484-118">-ApiVersion</span></span>
<span data-ttu-id="d8484-119">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d8484-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="d8484-120">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="d8484-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="d8484-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8484-121">-DefaultProfile</span></span>
<span data-ttu-id="d8484-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d8484-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8484-123">-Force</span><span class="sxs-lookup"><span data-stu-id="d8484-123">-Force</span></span>
<span data-ttu-id="d8484-124">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="d8484-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d8484-125">-LockId</span><span class="sxs-lookup"><span data-stu-id="d8484-125">-LockId</span></span>
<span data-ttu-id="d8484-126">A zárolás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d8484-126">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="d8484-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="d8484-127">-LockLevel</span></span>
<span data-ttu-id="d8484-128">A zárolás szintjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d8484-128">Specifies the level for the lock.</span></span>
<span data-ttu-id="d8484-129">Jelenleg az érvényes értékek CanNotDelete, ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="d8484-129">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

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

### <span data-ttu-id="d8484-130">-LockName</span><span class="sxs-lookup"><span data-stu-id="d8484-130">-LockName</span></span>
<span data-ttu-id="d8484-131">A zárolás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d8484-131">Specifies the name of the lock.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope, ByResourceGroup, ByResourceGroupLevel, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8484-132">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="d8484-132">-LockNotes</span></span>
<span data-ttu-id="d8484-133">A zároláshoz kapcsolódó jegyzeteket adja meg.</span><span class="sxs-lookup"><span data-stu-id="d8484-133">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="d8484-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="d8484-134">-Pre</span></span>
<span data-ttu-id="d8484-135">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="d8484-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d8484-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8484-136">-ResourceGroupName</span></span>
<span data-ttu-id="d8484-137">Annak az erőforráscsoport a nevét adja meg, amelyhez a zárolás érvényes, vagy amely azt az erőforráscsoportot tartalmazza, amelyre a zárolás érvényes.</span><span class="sxs-lookup"><span data-stu-id="d8484-137">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="d8484-138">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d8484-138">-ResourceName</span></span>
<span data-ttu-id="d8484-139">Annak az erőforrásnak a nevét adja meg, amelynek a zárolását alkalmazni kívánja.</span><span class="sxs-lookup"><span data-stu-id="d8484-139">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="d8484-140">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="d8484-140">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8484-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="d8484-141">-ResourceType</span></span>
<span data-ttu-id="d8484-142">Annak az erőforrásnak az erőforrás típusát adja meg, amelyre vonatkozóan a zárolás érvényes.</span><span class="sxs-lookup"><span data-stu-id="d8484-142">Specifies the resource type of the resource for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8484-143">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="d8484-143">-Scope</span></span>
<span data-ttu-id="d8484-144">Azt a hatókört adja meg, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="d8484-144">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="d8484-145">Ha például meg szeretne adni egy adatbázist, használja a következő formátumot: `/subscriptions/` előfizetés-azonosító `/resourceGroups/` erőforráscsoport neve `/providers/Microsoft.Sql/servers/` kiszolgálónév `/databases/` -adatbázis neve az erőforráscsoport megadásához, használja a következő formátumot: `/subscriptions/` előfizetés azonosítója `/resourceGroups/` Erőforrás-csoport neve</span><span class="sxs-lookup"><span data-stu-id="d8484-145">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="d8484-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="d8484-146">-TenantLevel</span></span>
<span data-ttu-id="d8484-147">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="d8484-147">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8484-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d8484-148">-Confirm</span></span>
<span data-ttu-id="d8484-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d8484-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8484-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8484-150">-WhatIf</span></span>
<span data-ttu-id="d8484-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d8484-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8484-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d8484-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8484-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8484-153">CommonParameters</span></span>
<span data-ttu-id="d8484-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d8484-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8484-155">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8484-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8484-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8484-156">INPUTS</span></span>

### <span data-ttu-id="d8484-157">System. String</span><span class="sxs-lookup"><span data-stu-id="d8484-157">System.String</span></span>

### <span data-ttu-id="d8484-158">Microsoft. Azure. Command. ResourceManager. parancsmagok. jogalanyok. locks. LockLevel</span><span class="sxs-lookup"><span data-stu-id="d8484-158">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="d8484-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8484-159">OUTPUTS</span></span>

### <span data-ttu-id="d8484-160">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="d8484-160">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d8484-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d8484-161">NOTES</span></span>

## <span data-ttu-id="d8484-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8484-162">RELATED LINKS</span></span>

[<span data-ttu-id="d8484-163">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="d8484-163">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="d8484-164">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="d8484-164">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="d8484-165">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="d8484-165">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


