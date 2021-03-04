---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
ms.openlocfilehash: a633718402f7c06e583030c379544ff45a216fb1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926441"
---
# <span data-ttu-id="c0170-101">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="c0170-101">Set-AzResourceLock</span></span>

## <span data-ttu-id="c0170-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0170-102">SYNOPSIS</span></span>
<span data-ttu-id="c0170-103">Módosítja az erőforrás zárolását.</span><span class="sxs-lookup"><span data-stu-id="c0170-103">Modifies a resource lock.</span></span>

## <span data-ttu-id="c0170-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c0170-104">SYNTAX</span></span>

### <span data-ttu-id="c0170-105">BySpecifiedScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c0170-105">BySpecifiedScope (Default)</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c0170-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c0170-106">ByResourceGroup</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0170-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="c0170-107">ByResourceGroupLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0170-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="c0170-108">BySubscription</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c0170-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="c0170-109">BySubscriptionLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0170-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="c0170-110">ByLockId</span></span>
```
Set-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0170-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c0170-111">DESCRIPTION</span></span>
<span data-ttu-id="c0170-112">A **Set-AzResourceLock** parancsmag módosítja az erőforrás zárolását.</span><span class="sxs-lookup"><span data-stu-id="c0170-112">The **Set-AzResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="c0170-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c0170-113">EXAMPLES</span></span>

### <span data-ttu-id="c0170-114">1. példa: Jegyzetek frissítése a zároláshoz</span><span class="sxs-lookup"><span data-stu-id="c0170-114">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="c0170-115">Ez a parancs frissíti a ContosoSiteLock nevű lakat megjegyzését.</span><span class="sxs-lookup"><span data-stu-id="c0170-115">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="c0170-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0170-116">PARAMETERS</span></span>

### <span data-ttu-id="c0170-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c0170-117">-ApiVersion</span></span>
<span data-ttu-id="c0170-118">Az erőforrás-szolgáltató API-jának használnia kell verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0170-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c0170-119">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="c0170-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c0170-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0170-120">-DefaultProfile</span></span>
<span data-ttu-id="c0170-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c0170-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0170-122">-Force</span><span class="sxs-lookup"><span data-stu-id="c0170-122">-Force</span></span>
<span data-ttu-id="c0170-123">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="c0170-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c0170-124">-LockId</span><span class="sxs-lookup"><span data-stu-id="c0170-124">-LockId</span></span>
<span data-ttu-id="c0170-125">A parancsmag által módosított zárolás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c0170-125">Specifies the ID of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c0170-126">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="c0170-126">-LockLevel</span></span>
<span data-ttu-id="c0170-127">A zárolás szintjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0170-127">Specifies the level for the lock.</span></span>
<span data-ttu-id="c0170-128">Jelenleg az egyetlen érvényes érték a CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="c0170-128">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="c0170-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="c0170-129">-LockName</span></span>
<span data-ttu-id="c0170-130">A parancsmag által módosított lakat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0170-130">Specifies the name of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c0170-131">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="c0170-131">-LockNotes</span></span>
<span data-ttu-id="c0170-132">A zárolás megjegyzéseit adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0170-132">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="c0170-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="c0170-133">-Pre</span></span>
<span data-ttu-id="c0170-134">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="c0170-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c0170-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0170-135">-ResourceGroupName</span></span>
<span data-ttu-id="c0170-136">Annak az erőforráscsoportnak a nevét adja meg, amelyre a zárolás érvényes.</span><span class="sxs-lookup"><span data-stu-id="c0170-136">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="c0170-137">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c0170-137">-ResourceName</span></span>
<span data-ttu-id="c0170-138">Annak az erőforrásnak a nevét adja meg, amelyre a zárolás érvényes.</span><span class="sxs-lookup"><span data-stu-id="c0170-138">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="c0170-139">Adatbázis megadásához például használja a következő `/` formátumot: Kiszolgálói adatbázis</span><span class="sxs-lookup"><span data-stu-id="c0170-139">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="c0170-140">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c0170-140">-ResourceType</span></span>
<span data-ttu-id="c0170-141">Azt az erőforrástípust adja meg, amelyre a zárolás érvényes.</span><span class="sxs-lookup"><span data-stu-id="c0170-141">Specifies the resource type for which the lock applies.</span></span>

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

### <span data-ttu-id="c0170-142">-Scope</span><span class="sxs-lookup"><span data-stu-id="c0170-142">-Scope</span></span>
<span data-ttu-id="c0170-143">A zárolás hatókörét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="c0170-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="c0170-144">Adatbázis megadásához például használja a következő formátumot: Előfizetés-azonosító erőforráscsoport neve kiszolgáló neve adatbázis neve Erőforráscsoport megadásához használja a következő `/subscriptions/` `/resourceGroups/` `/providers/Microsoft.Sql/servers/` formátumot: `/databases/` `/subscriptions/` előfizetés-azonosító `/resourceGroups/` erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c0170-144">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="c0170-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0170-145">-Confirm</span></span>
<span data-ttu-id="c0170-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c0170-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0170-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0170-147">-WhatIf</span></span>
<span data-ttu-id="c0170-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c0170-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0170-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c0170-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0170-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0170-150">CommonParameters</span></span>
<span data-ttu-id="c0170-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0170-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0170-152">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0170-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0170-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c0170-153">INPUTS</span></span>

### <span data-ttu-id="c0170-154">System.String</span><span class="sxs-lookup"><span data-stu-id="c0170-154">System.String</span></span>

### <span data-ttu-id="c0170-155">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span><span class="sxs-lookup"><span data-stu-id="c0170-155">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="c0170-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0170-156">OUTPUTS</span></span>

### <span data-ttu-id="c0170-157">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="c0170-157">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c0170-158">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c0170-158">NOTES</span></span>

## <span data-ttu-id="c0170-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0170-159">RELATED LINKS</span></span>

[<span data-ttu-id="c0170-160">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="c0170-160">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="c0170-161">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="c0170-161">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="c0170-162">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="c0170-162">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)


