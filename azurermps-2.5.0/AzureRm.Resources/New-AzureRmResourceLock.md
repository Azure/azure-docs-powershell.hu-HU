---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcelock
schema: 2.0.0
ms.openlocfilehash: 8556f71263aefe721225906aa1480c4f0bc19f7c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850250"
---
# <span data-ttu-id="372a4-101">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="372a4-101">New-AzureRmResourceLock</span></span>

## <span data-ttu-id="372a4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="372a4-102">SYNOPSIS</span></span>
<span data-ttu-id="372a4-103">Erőforrás-zárolást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="372a4-103">Creates a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="372a4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="372a4-104">SYNTAX</span></span>

### <span data-ttu-id="372a4-105">BySpecifiedScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="372a4-105">BySpecifiedScope (Default)</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="372a4-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="372a4-106">ByResourceGroup</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="372a4-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="372a4-107">ByResourceGroupLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="372a4-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="372a4-108">BySubscription</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="372a4-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="372a4-109">BySubscriptionLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="372a4-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="372a4-110">ByTenantLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="372a4-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="372a4-111">ByLockId</span></span>
```
New-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="372a4-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="372a4-112">DESCRIPTION</span></span>
<span data-ttu-id="372a4-113">A **New-AzureRmResourceLock** parancsmag létrehoz egy erőforrás-zárolást.</span><span class="sxs-lookup"><span data-stu-id="372a4-113">The **New-AzureRmResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="372a4-114">Példák</span><span class="sxs-lookup"><span data-stu-id="372a4-114">EXAMPLES</span></span>

### <span data-ttu-id="372a4-115">Példa 1: erőforrás-zárolás létrehozása webhelyre</span><span class="sxs-lookup"><span data-stu-id="372a4-115">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="372a4-116">Ez a parancs egy erőforrás-zárolást hoz létre egy webhelyen.</span><span class="sxs-lookup"><span data-stu-id="372a4-116">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="372a4-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="372a4-117">PARAMETERS</span></span>

### <span data-ttu-id="372a4-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="372a4-118">-ApiVersion</span></span>
<span data-ttu-id="372a4-119">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="372a4-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="372a4-120">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="372a4-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="372a4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="372a4-121">-DefaultProfile</span></span>
<span data-ttu-id="372a4-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="372a4-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="372a4-123">-Force</span><span class="sxs-lookup"><span data-stu-id="372a4-123">-Force</span></span>
<span data-ttu-id="372a4-124">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="372a4-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="372a4-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="372a4-125">-InformationAction</span></span>
<span data-ttu-id="372a4-126">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="372a4-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="372a4-127">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="372a4-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="372a4-128">Folytassa</span><span class="sxs-lookup"><span data-stu-id="372a4-128">Continue</span></span>
- <span data-ttu-id="372a4-129">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="372a4-129">Ignore</span></span>
- <span data-ttu-id="372a4-130">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="372a4-130">Inquire</span></span>
- <span data-ttu-id="372a4-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="372a4-131">SilentlyContinue</span></span>
- <span data-ttu-id="372a4-132">állj</span><span class="sxs-lookup"><span data-stu-id="372a4-132">Stop</span></span>
- <span data-ttu-id="372a4-133">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="372a4-133">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="372a4-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="372a4-134">-InformationVariable</span></span>
<span data-ttu-id="372a4-135">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="372a4-135">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="372a4-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="372a4-136">-LockId</span></span>
<span data-ttu-id="372a4-137">A zárolás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="372a4-137">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="372a4-138">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="372a4-138">-LockLevel</span></span>
<span data-ttu-id="372a4-139">A zárolás szintjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="372a4-139">Specifies the level for the lock.</span></span>
<span data-ttu-id="372a4-140">Jelenleg az érvényes értékek CanNotDelete, ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="372a4-140">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel
Parameter Sets: (All)
Aliases: Level

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="372a4-141">-LockName</span><span class="sxs-lookup"><span data-stu-id="372a4-141">-LockName</span></span>
<span data-ttu-id="372a4-142">A zárolás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="372a4-142">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="372a4-143">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="372a4-143">-LockNotes</span></span>
<span data-ttu-id="372a4-144">A zároláshoz kapcsolódó jegyzeteket adja meg.</span><span class="sxs-lookup"><span data-stu-id="372a4-144">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="372a4-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="372a4-145">-Pre</span></span>
<span data-ttu-id="372a4-146">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="372a4-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="372a4-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="372a4-147">-ResourceGroupName</span></span>
<span data-ttu-id="372a4-148">Annak az erőforráscsoport a nevét adja meg, amelyhez a zárolás érvényes, vagy amely azt az erőforráscsoportot tartalmazza, amelyre a zárolás érvényes.</span><span class="sxs-lookup"><span data-stu-id="372a4-148">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="372a4-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="372a4-149">-ResourceName</span></span>
<span data-ttu-id="372a4-150">Annak az erőforrásnak a nevét adja meg, amelynek a zárolását alkalmazni kívánja.</span><span class="sxs-lookup"><span data-stu-id="372a4-150">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="372a4-151">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="372a4-151">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="372a4-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="372a4-152">-ResourceType</span></span>
<span data-ttu-id="372a4-153">Annak az erőforrásnak az erőforrás típusát adja meg, amelyre vonatkozóan a zárolás érvényes.</span><span class="sxs-lookup"><span data-stu-id="372a4-153">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="372a4-154">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="372a4-154">-Scope</span></span>
<span data-ttu-id="372a4-155">Azt a hatókört adja meg, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="372a4-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="372a4-156">Ha például meg szeretne adni egy adatbázist, használja a következő formátumot: `/subscriptions/` előfizetés-azonosító `/resourceGroups/` erőforráscsoport neve `/providers/Microsoft.Sql/servers/` kiszolgálónév `/databases/` -adatbázis neve az erőforráscsoport megadásához, használja a következő formátumot: `/subscriptions/` előfizetés azonosítója `/resourceGroups/` Erőforrás-csoport neve</span><span class="sxs-lookup"><span data-stu-id="372a4-156">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="372a4-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="372a4-157">-TenantLevel</span></span>
<span data-ttu-id="372a4-158">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="372a4-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="372a4-159">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="372a4-159">-Confirm</span></span>
<span data-ttu-id="372a4-160">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="372a4-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="372a4-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="372a4-161">-WhatIf</span></span>
<span data-ttu-id="372a4-162">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="372a4-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="372a4-163">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="372a4-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="372a4-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="372a4-164">CommonParameters</span></span>
<span data-ttu-id="372a4-165">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="372a4-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="372a4-166">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="372a4-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="372a4-167">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="372a4-167">INPUTS</span></span>

## <span data-ttu-id="372a4-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="372a4-168">OUTPUTS</span></span>

## <span data-ttu-id="372a4-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="372a4-169">NOTES</span></span>

## <span data-ttu-id="372a4-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="372a4-170">RELATED LINKS</span></span>

[<span data-ttu-id="372a4-171">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="372a4-171">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="372a4-172">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="372a4-172">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="372a4-173">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="372a4-173">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


