---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
ms.openlocfilehash: f1220db034a2cdcc81ffbd7a146fee8e2c7201be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838870"
---
# <span data-ttu-id="c1c66-101">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="c1c66-101">Set-AzResourceLock</span></span>

## <span data-ttu-id="c1c66-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c1c66-102">SYNOPSIS</span></span>
<span data-ttu-id="c1c66-103">Módosítja az erőforrás-zárolást.</span><span class="sxs-lookup"><span data-stu-id="c1c66-103">Modifies a resource lock.</span></span>

## <span data-ttu-id="c1c66-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c1c66-104">SYNTAX</span></span>

### <span data-ttu-id="c1c66-105">BySpecifiedScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c1c66-105">BySpecifiedScope (Default)</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1c66-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c1c66-106">ByResourceGroup</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1c66-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="c1c66-107">ByResourceGroupLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1c66-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="c1c66-108">BySubscription</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1c66-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="c1c66-109">BySubscriptionLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1c66-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="c1c66-110">ByTenantLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1c66-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="c1c66-111">ByLockId</span></span>
```
Set-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1c66-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="c1c66-112">DESCRIPTION</span></span>
<span data-ttu-id="c1c66-113">A **set-AzResourceLock** parancsmag módosítja az erőforrás-zárolást.</span><span class="sxs-lookup"><span data-stu-id="c1c66-113">The **Set-AzResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="c1c66-114">Példák</span><span class="sxs-lookup"><span data-stu-id="c1c66-114">EXAMPLES</span></span>

### <span data-ttu-id="c1c66-115">Példa 1: a zárolási megjegyzések frissítése</span><span class="sxs-lookup"><span data-stu-id="c1c66-115">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="c1c66-116">A parancs frissíti a ContosoSiteLock nevű zárolás megjegyzését.</span><span class="sxs-lookup"><span data-stu-id="c1c66-116">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="c1c66-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c1c66-117">PARAMETERS</span></span>

### <span data-ttu-id="c1c66-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c1c66-118">-ApiVersion</span></span>
<span data-ttu-id="c1c66-119">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c1c66-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c1c66-120">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="c1c66-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c1c66-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1c66-121">-DefaultProfile</span></span>
<span data-ttu-id="c1c66-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c1c66-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1c66-123">-Force</span><span class="sxs-lookup"><span data-stu-id="c1c66-123">-Force</span></span>
<span data-ttu-id="c1c66-124">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="c1c66-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c1c66-125">-LockId</span><span class="sxs-lookup"><span data-stu-id="c1c66-125">-LockId</span></span>
<span data-ttu-id="c1c66-126">A parancsmag által módosított zárolás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c1c66-126">Specifies the ID of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c1c66-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="c1c66-127">-LockLevel</span></span>
<span data-ttu-id="c1c66-128">A zárolás szintjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c1c66-128">Specifies the level for the lock.</span></span>
<span data-ttu-id="c1c66-129">Jelenleg az egyetlen érvényes érték a CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="c1c66-129">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="c1c66-130">-LockName</span><span class="sxs-lookup"><span data-stu-id="c1c66-130">-LockName</span></span>
<span data-ttu-id="c1c66-131">A parancsmag által módosított zárolás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c1c66-131">Specifies the name of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c1c66-132">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="c1c66-132">-LockNotes</span></span>
<span data-ttu-id="c1c66-133">A zároláshoz kapcsolódó jegyzeteket adja meg.</span><span class="sxs-lookup"><span data-stu-id="c1c66-133">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="c1c66-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="c1c66-134">-Pre</span></span>
<span data-ttu-id="c1c66-135">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="c1c66-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c1c66-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1c66-136">-ResourceGroupName</span></span>
<span data-ttu-id="c1c66-137">Annak az erőforráscsoport-csoportnak a neve, amelyhez a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="c1c66-137">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="c1c66-138">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c1c66-138">-ResourceName</span></span>
<span data-ttu-id="c1c66-139">Annak az erőforrásnak a nevét adja meg, amelynek a zárolását alkalmazni kívánja.</span><span class="sxs-lookup"><span data-stu-id="c1c66-139">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="c1c66-140">Ha például egy adatbázist szeretne megadni, használja a következő formátumot: kiszolgálói `/` adatbázis</span><span class="sxs-lookup"><span data-stu-id="c1c66-140">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="c1c66-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c1c66-141">-ResourceType</span></span>
<span data-ttu-id="c1c66-142">Annak az erőforrásnak a típusa, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="c1c66-142">Specifies the resource type for which the lock applies.</span></span>

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

### <span data-ttu-id="c1c66-143">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="c1c66-143">-Scope</span></span>
<span data-ttu-id="c1c66-144">Azt a hatókört adja meg, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="c1c66-144">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="c1c66-145">Ha például meg szeretne adni egy adatbázist, használja a következő formátumot: `/subscriptions/` előfizetés-azonosító `/resourceGroups/` erőforráscsoport neve `/providers/Microsoft.Sql/servers/` kiszolgálónév `/databases/` -adatbázis neve az erőforráscsoport megadásához, használja a következő formátumot: `/subscriptions/` előfizetés azonosítója `/resourceGroups/` Erőforrás-csoport neve</span><span class="sxs-lookup"><span data-stu-id="c1c66-145">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="c1c66-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="c1c66-146">-TenantLevel</span></span>
<span data-ttu-id="c1c66-147">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="c1c66-147">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="c1c66-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c1c66-148">-Confirm</span></span>
<span data-ttu-id="c1c66-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c1c66-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1c66-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1c66-150">-WhatIf</span></span>
<span data-ttu-id="c1c66-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c1c66-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1c66-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c1c66-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1c66-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1c66-153">CommonParameters</span></span>
<span data-ttu-id="c1c66-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c1c66-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1c66-155">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1c66-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1c66-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1c66-156">INPUTS</span></span>

### <span data-ttu-id="c1c66-157">System. String</span><span class="sxs-lookup"><span data-stu-id="c1c66-157">System.String</span></span>

### <span data-ttu-id="c1c66-158">Microsoft. Azure. Command. ResourceManager. parancsmagok. jogalanyok. locks. LockLevel</span><span class="sxs-lookup"><span data-stu-id="c1c66-158">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="c1c66-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1c66-159">OUTPUTS</span></span>

### <span data-ttu-id="c1c66-160">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c1c66-160">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c1c66-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c1c66-161">NOTES</span></span>

## <span data-ttu-id="c1c66-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1c66-162">RELATED LINKS</span></span>

[<span data-ttu-id="c1c66-163">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="c1c66-163">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="c1c66-164">Új – AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="c1c66-164">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="c1c66-165">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="c1c66-165">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)


