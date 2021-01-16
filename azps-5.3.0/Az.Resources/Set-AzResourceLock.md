---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
ms.openlocfilehash: c532633de593294c6b5dbe0e09b9615a1d5355a3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480198"
---
# <span data-ttu-id="f1758-101">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f1758-101">Set-AzResourceLock</span></span>

## <span data-ttu-id="f1758-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1758-102">SYNOPSIS</span></span>
<span data-ttu-id="f1758-103">Módosítja az erőforrás zárolását.</span><span class="sxs-lookup"><span data-stu-id="f1758-103">Modifies a resource lock.</span></span>

## <span data-ttu-id="f1758-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f1758-104">SYNTAX</span></span>

### <span data-ttu-id="f1758-105">BySpecifiedScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f1758-105">BySpecifiedScope (Default)</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f1758-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f1758-106">ByResourceGroup</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1758-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="f1758-107">ByResourceGroupLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1758-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="f1758-108">BySubscription</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f1758-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="f1758-109">BySubscriptionLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1758-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="f1758-110">ByLockId</span></span>
```
Set-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1758-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f1758-111">DESCRIPTION</span></span>
<span data-ttu-id="f1758-112">A **Set-AzResourceLock** parancsmag módosítja az erőforrás zárolását.</span><span class="sxs-lookup"><span data-stu-id="f1758-112">The **Set-AzResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="f1758-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f1758-113">EXAMPLES</span></span>

### <span data-ttu-id="f1758-114">1. példa: Jegyzetek frissítése a zároláshoz</span><span class="sxs-lookup"><span data-stu-id="f1758-114">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="f1758-115">Ez a parancs frissíti a ContosoSiteLock nevű lakat megjegyzését.</span><span class="sxs-lookup"><span data-stu-id="f1758-115">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="f1758-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1758-116">PARAMETERS</span></span>

### <span data-ttu-id="f1758-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f1758-117">-ApiVersion</span></span>
<span data-ttu-id="f1758-118">Az erőforrás-szolgáltató API-jának használnia kell verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1758-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f1758-119">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="f1758-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f1758-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1758-120">-DefaultProfile</span></span>
<span data-ttu-id="f1758-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f1758-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1758-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f1758-122">-Force</span></span>
<span data-ttu-id="f1758-123">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="f1758-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f1758-124">-LockId</span><span class="sxs-lookup"><span data-stu-id="f1758-124">-LockId</span></span>
<span data-ttu-id="f1758-125">A parancsmag által módosított zárolás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f1758-125">Specifies the ID of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f1758-126">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="f1758-126">-LockLevel</span></span>
<span data-ttu-id="f1758-127">A zárolás szintjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1758-127">Specifies the level for the lock.</span></span>
<span data-ttu-id="f1758-128">Jelenleg az egyetlen érvényes érték a CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="f1758-128">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="f1758-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="f1758-129">-LockName</span></span>
<span data-ttu-id="f1758-130">A parancsmag által módosított lakat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1758-130">Specifies the name of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f1758-131">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="f1758-131">-LockNotes</span></span>
<span data-ttu-id="f1758-132">A zárolás megjegyzéseit adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1758-132">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="f1758-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="f1758-133">-Pre</span></span>
<span data-ttu-id="f1758-134">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="f1758-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f1758-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1758-135">-ResourceGroupName</span></span>
<span data-ttu-id="f1758-136">Annak az erőforráscsoportnak a nevét adja meg, amelyre a zárolás érvényes.</span><span class="sxs-lookup"><span data-stu-id="f1758-136">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="f1758-137">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f1758-137">-ResourceName</span></span>
<span data-ttu-id="f1758-138">Annak az erőforrásnak a nevét adja meg, amelyre a zárolás érvényes.</span><span class="sxs-lookup"><span data-stu-id="f1758-138">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="f1758-139">Adatbázis megadásához például használja a következő `/` formátumot: Kiszolgálói adatbázis</span><span class="sxs-lookup"><span data-stu-id="f1758-139">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="f1758-140">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="f1758-140">-ResourceType</span></span>
<span data-ttu-id="f1758-141">Azt az erőforrástípust adja meg, amelyre a zárolás érvényes.</span><span class="sxs-lookup"><span data-stu-id="f1758-141">Specifies the resource type for which the lock applies.</span></span>

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

### <span data-ttu-id="f1758-142">-Scope</span><span class="sxs-lookup"><span data-stu-id="f1758-142">-Scope</span></span>
<span data-ttu-id="f1758-143">A zárolás hatókörét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="f1758-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="f1758-144">Adatbázis megadásához például használja a következő formátumot: Előfizetés-azonosító erőforráscsoport neve kiszolgáló neve adatbázis neve Erőforráscsoport megadásához használja a következő `/subscriptions/` `/resourceGroups/` `/providers/Microsoft.Sql/servers/` formátumot: `/databases/` `/subscriptions/` előfizetés-azonosító `/resourceGroups/` erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="f1758-144">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="f1758-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1758-145">-Confirm</span></span>
<span data-ttu-id="f1758-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f1758-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1758-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1758-147">-WhatIf</span></span>
<span data-ttu-id="f1758-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f1758-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1758-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f1758-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1758-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1758-150">CommonParameters</span></span>
<span data-ttu-id="f1758-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1758-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1758-152">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1758-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1758-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f1758-153">INPUTS</span></span>

### <span data-ttu-id="f1758-154">System.String</span><span class="sxs-lookup"><span data-stu-id="f1758-154">System.String</span></span>

### <span data-ttu-id="f1758-155">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span><span class="sxs-lookup"><span data-stu-id="f1758-155">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="f1758-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1758-156">OUTPUTS</span></span>

### <span data-ttu-id="f1758-157">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="f1758-157">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f1758-158">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f1758-158">NOTES</span></span>

## <span data-ttu-id="f1758-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1758-159">RELATED LINKS</span></span>

[<span data-ttu-id="f1758-160">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f1758-160">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="f1758-161">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f1758-161">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="f1758-162">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f1758-162">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)


