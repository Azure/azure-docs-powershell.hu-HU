---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
ms.openlocfilehash: c363279c0cbb6dc20b0ddcc7bae32266a848fb3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504751"
---
# <span data-ttu-id="a190d-101">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="a190d-101">New-AzureRmResourceLock</span></span>

## <span data-ttu-id="a190d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a190d-102">SYNOPSIS</span></span>
<span data-ttu-id="a190d-103">Erőforrás-zárolást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a190d-103">Creates a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a190d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a190d-104">SYNTAX</span></span>

### <span data-ttu-id="a190d-105">A megadott hatókör zárolása.</span><span class="sxs-lookup"><span data-stu-id="a190d-105">A lock at the specified scope.</span></span> <span data-ttu-id="a190d-106">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="a190d-106">(Default)</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a190d-107">Az erőforráscsoport hatókörének zárolása.</span><span class="sxs-lookup"><span data-stu-id="a190d-107">A lock at the resource group scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a190d-108">Zárolás az erőforrás-csoport erőforrás-hatókörében.</span><span class="sxs-lookup"><span data-stu-id="a190d-108">A lock at the resource group resource scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a190d-109">Zárolás az előfizetéses hatókörben.</span><span class="sxs-lookup"><span data-stu-id="a190d-109">A lock at the subscription scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a190d-110">Zárolás az előfizetés erőforrás-tartományában.</span><span class="sxs-lookup"><span data-stu-id="a190d-110">A lock at the subscription resource scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a190d-111">A bérlői erőforrás hatókörének zárolása.</span><span class="sxs-lookup"><span data-stu-id="a190d-111">A lock at the tenant resource scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a190d-112">Zárolás, azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="a190d-112">A lock, by Id.</span></span>
```
New-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a190d-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="a190d-113">DESCRIPTION</span></span>
<span data-ttu-id="a190d-114">A **New-AzureRmResourceLock** parancsmag létrehoz egy erőforrás-zárolást.</span><span class="sxs-lookup"><span data-stu-id="a190d-114">The **New-AzureRmResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="a190d-115">Példák</span><span class="sxs-lookup"><span data-stu-id="a190d-115">EXAMPLES</span></span>

### <span data-ttu-id="a190d-116">Példa 1: erőforrás-zárolás létrehozása webhelyre</span><span class="sxs-lookup"><span data-stu-id="a190d-116">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="a190d-117">Ez a parancs egy erőforrás-zárolást hoz létre egy webhelyen.</span><span class="sxs-lookup"><span data-stu-id="a190d-117">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="a190d-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a190d-118">PARAMETERS</span></span>

### <span data-ttu-id="a190d-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a190d-119">-ApiVersion</span></span>
<span data-ttu-id="a190d-120">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a190d-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a190d-121">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="a190d-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a190d-122">-Force</span><span class="sxs-lookup"><span data-stu-id="a190d-122">-Force</span></span>
<span data-ttu-id="a190d-123">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="a190d-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a190d-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a190d-124">-InformationAction</span></span>
<span data-ttu-id="a190d-125">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="a190d-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a190d-126">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a190d-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a190d-127">Folytassa</span><span class="sxs-lookup"><span data-stu-id="a190d-127">Continue</span></span>
- <span data-ttu-id="a190d-128">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="a190d-128">Ignore</span></span>
- <span data-ttu-id="a190d-129">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="a190d-129">Inquire</span></span>
- <span data-ttu-id="a190d-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a190d-130">SilentlyContinue</span></span>
- <span data-ttu-id="a190d-131">állj</span><span class="sxs-lookup"><span data-stu-id="a190d-131">Stop</span></span>
- <span data-ttu-id="a190d-132">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="a190d-132">Suspend</span></span>

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

### <span data-ttu-id="a190d-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a190d-133">-InformationVariable</span></span>
<span data-ttu-id="a190d-134">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="a190d-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a190d-135">-LockId</span><span class="sxs-lookup"><span data-stu-id="a190d-135">-LockId</span></span>
<span data-ttu-id="a190d-136">A zárolás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a190d-136">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="a190d-137">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="a190d-137">-LockLevel</span></span>
<span data-ttu-id="a190d-138">A zárolás szintjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a190d-138">Specifies the level for the lock.</span></span>
<span data-ttu-id="a190d-139">Jelenleg az egyetlen érvényes érték a CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="a190d-139">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="a190d-140">-LockName</span><span class="sxs-lookup"><span data-stu-id="a190d-140">-LockName</span></span>
<span data-ttu-id="a190d-141">A zárolás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a190d-141">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="a190d-142">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="a190d-142">-LockNotes</span></span>
<span data-ttu-id="a190d-143">A zároláshoz kapcsolódó jegyzeteket adja meg.</span><span class="sxs-lookup"><span data-stu-id="a190d-143">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="a190d-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="a190d-144">-Pre</span></span>
<span data-ttu-id="a190d-145">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="a190d-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a190d-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a190d-146">-ResourceGroupName</span></span>
<span data-ttu-id="a190d-147">Annak az erőforráscsoport a nevét adja meg, amelyhez a zárolás érvényes, vagy amely azt az erőforráscsoportot tartalmazza, amelyre a zárolás érvényes.</span><span class="sxs-lookup"><span data-stu-id="a190d-147">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="a190d-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a190d-148">-ResourceName</span></span>
<span data-ttu-id="a190d-149">Annak az erőforrásnak a nevét adja meg, amelynek a zárolását alkalmazni kívánja.</span><span class="sxs-lookup"><span data-stu-id="a190d-149">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="a190d-150">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot:</span><span class="sxs-lookup"><span data-stu-id="a190d-150">For instance, to specify a database, use the following format:</span></span> 

`ContosoServer/ContosoDatabase`

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

### <span data-ttu-id="a190d-151">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a190d-151">-ResourceType</span></span>
<span data-ttu-id="a190d-152">Annak az erőforrásnak az erőforrás típusát adja meg, amelyre vonatkozóan a zárolás érvényes.</span><span class="sxs-lookup"><span data-stu-id="a190d-152">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="a190d-153">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="a190d-153">-Scope</span></span>
<span data-ttu-id="a190d-154">Azt a hatókört adja meg, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="a190d-154">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="a190d-155">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot:</span><span class="sxs-lookup"><span data-stu-id="a190d-155">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="a190d-156">`/subscriptions/`előfizetés-azonosító erőforrás-kiszolgálócsoport neve- `/resourceGroups/` `/providers/Microsoft.Sql/servers/` `/databases/` adatbázis neve</span><span class="sxs-lookup"><span data-stu-id="a190d-156">`/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name</span></span>

<span data-ttu-id="a190d-157">Erőforráscsoport megadásához használja a következő formátumot:</span><span class="sxs-lookup"><span data-stu-id="a190d-157">To specify a resource group, use the following format:</span></span> 

<span data-ttu-id="a190d-158">`/subscriptions/`előfizetés-azonosító `/resourceGroups/` Erőforrás-csoport neve</span><span class="sxs-lookup"><span data-stu-id="a190d-158">`/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="a190d-159">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="a190d-159">-TenantLevel</span></span>
<span data-ttu-id="a190d-160">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="a190d-160">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="a190d-161">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a190d-161">-Confirm</span></span>
<span data-ttu-id="a190d-162">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a190d-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a190d-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a190d-163">-WhatIf</span></span>
<span data-ttu-id="a190d-164">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a190d-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a190d-165">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a190d-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a190d-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a190d-166">-DefaultProfile</span></span>
<span data-ttu-id="a190d-167">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a190d-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a190d-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a190d-168">CommonParameters</span></span>
<span data-ttu-id="a190d-169">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a190d-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a190d-170">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a190d-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a190d-171">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a190d-171">INPUTS</span></span>

## <span data-ttu-id="a190d-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a190d-172">OUTPUTS</span></span>

### <span data-ttu-id="a190d-173">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a190d-173">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a190d-174">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a190d-174">NOTES</span></span>

## <span data-ttu-id="a190d-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a190d-175">RELATED LINKS</span></span>

[<span data-ttu-id="a190d-176">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="a190d-176">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="a190d-177">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="a190d-177">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="a190d-178">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="a190d-178">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


