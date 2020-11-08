---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
ms.openlocfilehash: 7f21704783a9992cc0d1b0fdf3da50cb21656b0e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180967"
---
# <span data-ttu-id="abc0b-101">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="abc0b-101">New-AzResourceLock</span></span>

## <span data-ttu-id="abc0b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="abc0b-102">SYNOPSIS</span></span>
<span data-ttu-id="abc0b-103">Erőforrás-zárolást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="abc0b-103">Creates a resource lock.</span></span>

## <span data-ttu-id="abc0b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="abc0b-104">SYNTAX</span></span>

### <span data-ttu-id="abc0b-105">BySpecifiedScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="abc0b-105">BySpecifiedScope (Default)</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="abc0b-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="abc0b-106">ByResourceGroup</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abc0b-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="abc0b-107">ByResourceGroupLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abc0b-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="abc0b-108">BySubscription</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="abc0b-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="abc0b-109">BySubscriptionLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abc0b-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="abc0b-110">ByLockId</span></span>
```
New-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="abc0b-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="abc0b-111">DESCRIPTION</span></span>
<span data-ttu-id="abc0b-112">A **New-AzResourceLock** parancsmag létrehoz egy erőforrás-zárolást.</span><span class="sxs-lookup"><span data-stu-id="abc0b-112">The **New-AzResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="abc0b-113">Példák</span><span class="sxs-lookup"><span data-stu-id="abc0b-113">EXAMPLES</span></span>

### <span data-ttu-id="abc0b-114">Példa 1: erőforrás-zárolás létrehozása webhelyre</span><span class="sxs-lookup"><span data-stu-id="abc0b-114">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="abc0b-115">Ez a parancs egy erőforrás-zárolást hoz létre egy webhelyen.</span><span class="sxs-lookup"><span data-stu-id="abc0b-115">This command creates a resource lock on a website.</span></span>

### <span data-ttu-id="abc0b-116">2. példa: erőforrás-zárolás létrehozása adatbázison</span><span class="sxs-lookup"><span data-stu-id="abc0b-116">Example 2: Create a resource lock on a database</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "Lock note" -LockName "db-lock" -ResourceName "server1/ContosoDB"  -ResourceGroupName "RG1" -ResourceType "Microsoft.Sql/servers/databases"
```

<span data-ttu-id="abc0b-117">A parancs az Azure-adatbázisokban létrehoz egy erőforrás-zárolást.</span><span class="sxs-lookup"><span data-stu-id="abc0b-117">This command creates a resource lock on a Azure database.</span></span>

## <span data-ttu-id="abc0b-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="abc0b-118">PARAMETERS</span></span>

### <span data-ttu-id="abc0b-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="abc0b-119">-ApiVersion</span></span>
<span data-ttu-id="abc0b-120">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="abc0b-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="abc0b-121">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="abc0b-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="abc0b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abc0b-122">-DefaultProfile</span></span>
<span data-ttu-id="abc0b-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="abc0b-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="abc0b-124">-Force</span><span class="sxs-lookup"><span data-stu-id="abc0b-124">-Force</span></span>
<span data-ttu-id="abc0b-125">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="abc0b-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="abc0b-126">-LockId</span><span class="sxs-lookup"><span data-stu-id="abc0b-126">-LockId</span></span>
<span data-ttu-id="abc0b-127">A zárolás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="abc0b-127">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="abc0b-128">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="abc0b-128">-LockLevel</span></span>
<span data-ttu-id="abc0b-129">A zárolás szintjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="abc0b-129">Specifies the level for the lock.</span></span>
<span data-ttu-id="abc0b-130">Jelenleg az érvényes értékek CanNotDelete, ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="abc0b-130">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

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

### <span data-ttu-id="abc0b-131">-LockName</span><span class="sxs-lookup"><span data-stu-id="abc0b-131">-LockName</span></span>
<span data-ttu-id="abc0b-132">A zárolás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="abc0b-132">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="abc0b-133">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="abc0b-133">-LockNotes</span></span>
<span data-ttu-id="abc0b-134">A zároláshoz kapcsolódó jegyzeteket adja meg.</span><span class="sxs-lookup"><span data-stu-id="abc0b-134">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="abc0b-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="abc0b-135">-Pre</span></span>
<span data-ttu-id="abc0b-136">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="abc0b-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="abc0b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abc0b-137">-ResourceGroupName</span></span>
<span data-ttu-id="abc0b-138">Annak az erőforráscsoport a nevét adja meg, amelyhez a zárolás érvényes, vagy amely azt az erőforráscsoportot tartalmazza, amelyre a zárolás érvényes.</span><span class="sxs-lookup"><span data-stu-id="abc0b-138">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="abc0b-139">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="abc0b-139">-ResourceName</span></span>
<span data-ttu-id="abc0b-140">Annak az erőforrásnak a nevét adja meg, amelynek a zárolását alkalmazni kívánja.</span><span class="sxs-lookup"><span data-stu-id="abc0b-140">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="abc0b-141">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="abc0b-141">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="abc0b-142">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="abc0b-142">-ResourceType</span></span>
<span data-ttu-id="abc0b-143">Annak az erőforrásnak az erőforrás típusát adja meg, amelyre vonatkozóan a zárolás érvényes.</span><span class="sxs-lookup"><span data-stu-id="abc0b-143">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="abc0b-144">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="abc0b-144">-Scope</span></span>
<span data-ttu-id="abc0b-145">Azt a hatókört adja meg, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="abc0b-145">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="abc0b-146">Ha például meg szeretne adni egy adatbázist, használja a következő formátumot: `/subscriptions/` előfizetés-azonosító `/resourceGroups/` erőforráscsoport neve `/providers/Microsoft.Sql/servers/` kiszolgálónév `/databases/` -adatbázis neve az erőforráscsoport megadásához, használja a következő formátumot: `/subscriptions/` előfizetés azonosítója `/resourceGroups/` Erőforrás-csoport neve</span><span class="sxs-lookup"><span data-stu-id="abc0b-146">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="abc0b-147">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="abc0b-147">-Confirm</span></span>
<span data-ttu-id="abc0b-148">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="abc0b-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abc0b-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abc0b-149">-WhatIf</span></span>
<span data-ttu-id="abc0b-150">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="abc0b-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abc0b-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="abc0b-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abc0b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abc0b-152">CommonParameters</span></span>
<span data-ttu-id="abc0b-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="abc0b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abc0b-154">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="abc0b-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abc0b-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="abc0b-155">INPUTS</span></span>

### <span data-ttu-id="abc0b-156">System. String</span><span class="sxs-lookup"><span data-stu-id="abc0b-156">System.String</span></span>

### <span data-ttu-id="abc0b-157">Microsoft. Azure. Command. ResourceManager. parancsmagok. jogalanyok. locks. LockLevel</span><span class="sxs-lookup"><span data-stu-id="abc0b-157">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="abc0b-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="abc0b-158">OUTPUTS</span></span>

### <span data-ttu-id="abc0b-159">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="abc0b-159">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="abc0b-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="abc0b-160">NOTES</span></span>

## <span data-ttu-id="abc0b-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="abc0b-161">RELATED LINKS</span></span>

[<span data-ttu-id="abc0b-162">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="abc0b-162">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="abc0b-163">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="abc0b-163">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="abc0b-164">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="abc0b-164">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


