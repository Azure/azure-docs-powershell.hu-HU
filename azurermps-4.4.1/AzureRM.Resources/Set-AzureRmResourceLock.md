---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
ms.openlocfilehash: 73d82366cc0120e057d0c083e7f6da0b3cdebb76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679333"
---
# <span data-ttu-id="880cb-101">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="880cb-101">Set-AzureRmResourceLock</span></span>

## <span data-ttu-id="880cb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="880cb-102">SYNOPSIS</span></span>
<span data-ttu-id="880cb-103">Módosítja az erőforrás-zárolást.</span><span class="sxs-lookup"><span data-stu-id="880cb-103">Modifies a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="880cb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="880cb-104">SYNTAX</span></span>

### <span data-ttu-id="880cb-105">A megadott hatókör zárolása.</span><span class="sxs-lookup"><span data-stu-id="880cb-105">A lock at the specified scope.</span></span> <span data-ttu-id="880cb-106">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="880cb-106">(Default)</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="880cb-107">Az erőforráscsoport hatókörének zárolása.</span><span class="sxs-lookup"><span data-stu-id="880cb-107">A lock at the resource group scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="880cb-108">Zárolás az erőforrás-csoport erőforrás-hatókörében.</span><span class="sxs-lookup"><span data-stu-id="880cb-108">A lock at the resource group resource scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="880cb-109">Zárolás az előfizetéses hatókörben.</span><span class="sxs-lookup"><span data-stu-id="880cb-109">A lock at the subscription scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="880cb-110">Zárolás az előfizetés erőforrás-tartományában.</span><span class="sxs-lookup"><span data-stu-id="880cb-110">A lock at the subscription resource scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="880cb-111">A bérlői erőforrás hatókörének zárolása.</span><span class="sxs-lookup"><span data-stu-id="880cb-111">A lock at the tenant resource scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="880cb-112">Zárolás, azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="880cb-112">A lock, by Id.</span></span>
```
Set-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="880cb-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="880cb-113">DESCRIPTION</span></span>
<span data-ttu-id="880cb-114">A **set-AzureRmResourceLock** parancsmag módosítja az erőforrás-zárolást.</span><span class="sxs-lookup"><span data-stu-id="880cb-114">The **Set-AzureRmResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="880cb-115">Példák</span><span class="sxs-lookup"><span data-stu-id="880cb-115">EXAMPLES</span></span>

### <span data-ttu-id="880cb-116">Példa 1: a zárolási megjegyzések frissítése</span><span class="sxs-lookup"><span data-stu-id="880cb-116">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="880cb-117">A parancs frissíti a ContosoSiteLock nevű zárolás megjegyzését.</span><span class="sxs-lookup"><span data-stu-id="880cb-117">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="880cb-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="880cb-118">PARAMETERS</span></span>

### <span data-ttu-id="880cb-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="880cb-119">-ApiVersion</span></span>
<span data-ttu-id="880cb-120">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="880cb-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="880cb-121">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="880cb-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="880cb-122">-Force</span><span class="sxs-lookup"><span data-stu-id="880cb-122">-Force</span></span>
<span data-ttu-id="880cb-123">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="880cb-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="880cb-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="880cb-124">-InformationAction</span></span>
<span data-ttu-id="880cb-125">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="880cb-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="880cb-126">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="880cb-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="880cb-127">Folytassa</span><span class="sxs-lookup"><span data-stu-id="880cb-127">Continue</span></span>
- <span data-ttu-id="880cb-128">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="880cb-128">Ignore</span></span>
- <span data-ttu-id="880cb-129">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="880cb-129">Inquire</span></span>
- <span data-ttu-id="880cb-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="880cb-130">SilentlyContinue</span></span>
- <span data-ttu-id="880cb-131">állj</span><span class="sxs-lookup"><span data-stu-id="880cb-131">Stop</span></span>
- <span data-ttu-id="880cb-132">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="880cb-132">Suspend</span></span>

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

### <span data-ttu-id="880cb-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="880cb-133">-InformationVariable</span></span>
<span data-ttu-id="880cb-134">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="880cb-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="880cb-135">-LockId</span><span class="sxs-lookup"><span data-stu-id="880cb-135">-LockId</span></span>
<span data-ttu-id="880cb-136">A parancsmag által módosított zárolás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="880cb-136">Specifies the ID of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock, by Id.
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="880cb-137">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="880cb-137">-LockLevel</span></span>
<span data-ttu-id="880cb-138">A zárolás szintjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="880cb-138">Specifies the level for the lock.</span></span>
<span data-ttu-id="880cb-139">Jelenleg az egyetlen érvényes érték a CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="880cb-139">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="880cb-140">-LockName</span><span class="sxs-lookup"><span data-stu-id="880cb-140">-LockName</span></span>
<span data-ttu-id="880cb-141">A parancsmag által módosított zárolás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="880cb-141">Specifies the name of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the specified scope., A lock at the resource group scope., A lock at the resource group resource scope., A lock at the subscription scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="880cb-142">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="880cb-142">-LockNotes</span></span>
<span data-ttu-id="880cb-143">A zároláshoz kapcsolódó jegyzeteket adja meg.</span><span class="sxs-lookup"><span data-stu-id="880cb-143">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="880cb-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="880cb-144">-Pre</span></span>
<span data-ttu-id="880cb-145">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="880cb-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="880cb-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="880cb-146">-ResourceGroupName</span></span>
<span data-ttu-id="880cb-147">Annak az erőforráscsoport-csoportnak a neve, amelyhez a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="880cb-147">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="880cb-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="880cb-148">-ResourceName</span></span>
<span data-ttu-id="880cb-149">Annak az erőforrásnak a nevét adja meg, amelynek a zárolását alkalmazni kívánja.</span><span class="sxs-lookup"><span data-stu-id="880cb-149">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="880cb-150">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot:</span><span class="sxs-lookup"><span data-stu-id="880cb-150">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="880cb-151">Kiszolgálói `/` adatbázis</span><span class="sxs-lookup"><span data-stu-id="880cb-151">Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="880cb-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="880cb-152">-ResourceType</span></span>
<span data-ttu-id="880cb-153">Annak az erőforrásnak a típusa, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="880cb-153">Specifies the resource type for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="880cb-154">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="880cb-154">-Scope</span></span>
<span data-ttu-id="880cb-155">Azt a hatókört adja meg, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="880cb-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="880cb-156">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot:</span><span class="sxs-lookup"><span data-stu-id="880cb-156">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="880cb-157">`/subscriptions/`előfizetés-azonosító erőforrás-kiszolgálócsoport neve- `/resourceGroups/` `/providers/Microsoft.Sql/servers/` `/databases/` adatbázis neve</span><span class="sxs-lookup"><span data-stu-id="880cb-157">`/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name</span></span>

<span data-ttu-id="880cb-158">Erőforráscsoport megadásához használja a következő formátumot:</span><span class="sxs-lookup"><span data-stu-id="880cb-158">To specify a resource group, use the following format:</span></span> 

<span data-ttu-id="880cb-159">`/subscriptions/`előfizetés-azonosító `/resourceGroups/` Erőforrás-csoport neve</span><span class="sxs-lookup"><span data-stu-id="880cb-159">`/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the specified scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="880cb-160">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="880cb-160">-TenantLevel</span></span>
<span data-ttu-id="880cb-161">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="880cb-161">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="880cb-162">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="880cb-162">-Confirm</span></span>
<span data-ttu-id="880cb-163">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="880cb-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="880cb-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="880cb-164">-WhatIf</span></span>
<span data-ttu-id="880cb-165">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="880cb-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="880cb-166">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="880cb-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="880cb-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="880cb-167">-DefaultProfile</span></span>
<span data-ttu-id="880cb-168">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="880cb-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="880cb-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="880cb-169">CommonParameters</span></span>
<span data-ttu-id="880cb-170">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="880cb-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="880cb-171">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="880cb-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="880cb-172">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="880cb-172">INPUTS</span></span>

## <span data-ttu-id="880cb-173">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="880cb-173">OUTPUTS</span></span>

### <span data-ttu-id="880cb-174">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="880cb-174">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="880cb-175">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="880cb-175">NOTES</span></span>

## <span data-ttu-id="880cb-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="880cb-176">RELATED LINKS</span></span>

[<span data-ttu-id="880cb-177">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="880cb-177">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="880cb-178">Új – AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="880cb-178">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="880cb-179">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="880cb-179">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)


