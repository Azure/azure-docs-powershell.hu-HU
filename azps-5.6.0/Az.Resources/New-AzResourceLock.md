---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
ms.openlocfilehash: 630ea593304523572403fce0db3d6118be66403f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927794"
---
# <span data-ttu-id="c40e8-101">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="c40e8-101">New-AzResourceLock</span></span>

## <span data-ttu-id="c40e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c40e8-102">SYNOPSIS</span></span>
<span data-ttu-id="c40e8-103">Erőforrászárolást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c40e8-103">Creates a resource lock.</span></span>

## <span data-ttu-id="c40e8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c40e8-104">SYNTAX</span></span>

### <span data-ttu-id="c40e8-105">BySpecifiedScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c40e8-105">BySpecifiedScope (Default)</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c40e8-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c40e8-106">ByResourceGroup</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c40e8-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="c40e8-107">ByResourceGroupLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c40e8-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="c40e8-108">BySubscription</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c40e8-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="c40e8-109">BySubscriptionLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c40e8-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="c40e8-110">ByLockId</span></span>
```
New-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c40e8-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c40e8-111">DESCRIPTION</span></span>
<span data-ttu-id="c40e8-112">A **New-AzResourceLock** parancsmag erőforrás-zárolást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c40e8-112">The **New-AzResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="c40e8-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c40e8-113">EXAMPLES</span></span>

### <span data-ttu-id="c40e8-114">1. példa: Erőforrás zárolásának létrehozása egy webhelyen</span><span class="sxs-lookup"><span data-stu-id="c40e8-114">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="c40e8-115">Ez a parancs erőforrás-zárolást hoz létre egy webhelyen.</span><span class="sxs-lookup"><span data-stu-id="c40e8-115">This command creates a resource lock on a website.</span></span>

### <span data-ttu-id="c40e8-116">2. példa: Erőforrászárolás létrehozása adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="c40e8-116">Example 2: Create a resource lock on a database</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "Lock note" -LockName "db-lock" -ResourceName "server1/ContosoDB"  -ResourceGroupName "RG1" -ResourceType "Microsoft.Sql/servers/databases"
```

<span data-ttu-id="c40e8-117">Ez a parancs erőforrás-zárolást hoz létre egy Azure-adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="c40e8-117">This command creates a resource lock on a Azure database.</span></span>

## <span data-ttu-id="c40e8-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c40e8-118">PARAMETERS</span></span>

### <span data-ttu-id="c40e8-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c40e8-119">-ApiVersion</span></span>
<span data-ttu-id="c40e8-120">Az erőforrás-szolgáltató API-jának használnia kell verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c40e8-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c40e8-121">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="c40e8-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c40e8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c40e8-122">-DefaultProfile</span></span>
<span data-ttu-id="c40e8-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c40e8-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c40e8-124">-Force</span><span class="sxs-lookup"><span data-stu-id="c40e8-124">-Force</span></span>
<span data-ttu-id="c40e8-125">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="c40e8-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c40e8-126">-LockId</span><span class="sxs-lookup"><span data-stu-id="c40e8-126">-LockId</span></span>
<span data-ttu-id="c40e8-127">A zárolás azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c40e8-127">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="c40e8-128">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="c40e8-128">-LockLevel</span></span>
<span data-ttu-id="c40e8-129">A zárolás szintjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c40e8-129">Specifies the level for the lock.</span></span>
<span data-ttu-id="c40e8-130">Jelenleg érvényes értékek: CanNotDelete, ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="c40e8-130">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

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

### <span data-ttu-id="c40e8-131">-LockName</span><span class="sxs-lookup"><span data-stu-id="c40e8-131">-LockName</span></span>
<span data-ttu-id="c40e8-132">A zárolás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c40e8-132">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="c40e8-133">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="c40e8-133">-LockNotes</span></span>
<span data-ttu-id="c40e8-134">A zárolás megjegyzéseit adja meg.</span><span class="sxs-lookup"><span data-stu-id="c40e8-134">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="c40e8-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="c40e8-135">-Pre</span></span>
<span data-ttu-id="c40e8-136">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="c40e8-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c40e8-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c40e8-137">-ResourceGroupName</span></span>
<span data-ttu-id="c40e8-138">Annak az erőforráscsoportnak a nevét adja meg, amelyre a zárolás vonatkozik, vagy amely azt az erőforráscsoportot tartalmazza, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="c40e8-138">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="c40e8-139">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c40e8-139">-ResourceName</span></span>
<span data-ttu-id="c40e8-140">Annak az erőforrásnak a nevét adja meg, amelyre a zárolás érvényes.</span><span class="sxs-lookup"><span data-stu-id="c40e8-140">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="c40e8-141">Adatbázis megadásához például használja az alábbi formátumot: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="c40e8-141">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="c40e8-142">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c40e8-142">-ResourceType</span></span>
<span data-ttu-id="c40e8-143">Annak az erőforrásnak az erőforrástípusát adja meg, amelyre a zárolás érvényes.</span><span class="sxs-lookup"><span data-stu-id="c40e8-143">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="c40e8-144">-Scope</span><span class="sxs-lookup"><span data-stu-id="c40e8-144">-Scope</span></span>
<span data-ttu-id="c40e8-145">A zárolás hatókörét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="c40e8-145">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="c40e8-146">Adatbázis megadásához például használja a következő formátumot: Előfizetés-azonosító erőforráscsoport neve kiszolgáló neve adatbázis neve Erőforráscsoport megadásához használja a következő `/subscriptions/` `/resourceGroups/` `/providers/Microsoft.Sql/servers/` formátumot: `/databases/` `/subscriptions/` előfizetés-azonosító `/resourceGroups/` erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c40e8-146">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="c40e8-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c40e8-147">-Confirm</span></span>
<span data-ttu-id="c40e8-148">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c40e8-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c40e8-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c40e8-149">-WhatIf</span></span>
<span data-ttu-id="c40e8-150">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c40e8-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c40e8-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c40e8-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c40e8-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c40e8-152">CommonParameters</span></span>
<span data-ttu-id="c40e8-153">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c40e8-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c40e8-154">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c40e8-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c40e8-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c40e8-155">INPUTS</span></span>

### <span data-ttu-id="c40e8-156">System.String</span><span class="sxs-lookup"><span data-stu-id="c40e8-156">System.String</span></span>

### <span data-ttu-id="c40e8-157">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span><span class="sxs-lookup"><span data-stu-id="c40e8-157">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="c40e8-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c40e8-158">OUTPUTS</span></span>

### <span data-ttu-id="c40e8-159">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="c40e8-159">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c40e8-160">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c40e8-160">NOTES</span></span>

## <span data-ttu-id="c40e8-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c40e8-161">RELATED LINKS</span></span>

[<span data-ttu-id="c40e8-162">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="c40e8-162">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="c40e8-163">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="c40e8-163">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="c40e8-164">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="c40e8-164">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


