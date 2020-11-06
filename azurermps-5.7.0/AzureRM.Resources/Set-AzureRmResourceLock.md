---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
ms.openlocfilehash: 12d1a696bd37cd6844a54f32f60bf70eaba6a0b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502455"
---
# <span data-ttu-id="2d493-101">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="2d493-101">Set-AzureRmResourceLock</span></span>

## <span data-ttu-id="2d493-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2d493-102">SYNOPSIS</span></span>
<span data-ttu-id="2d493-103">Módosítja az erőforrás-zárolást.</span><span class="sxs-lookup"><span data-stu-id="2d493-103">Modifies a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d493-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2d493-104">SYNTAX</span></span>

### <span data-ttu-id="2d493-105">BySpecifiedScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2d493-105">BySpecifiedScope (Default)</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d493-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2d493-106">ByResourceGroup</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d493-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="2d493-107">ByResourceGroupLevel</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d493-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="2d493-108">BySubscription</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d493-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="2d493-109">BySubscriptionLevel</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d493-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="2d493-110">ByTenantLevel</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d493-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="2d493-111">ByLockId</span></span>
```
Set-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2d493-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="2d493-112">DESCRIPTION</span></span>
<span data-ttu-id="2d493-113">A **set-AzureRmResourceLock** parancsmag módosítja az erőforrás-zárolást.</span><span class="sxs-lookup"><span data-stu-id="2d493-113">The **Set-AzureRmResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="2d493-114">Példák</span><span class="sxs-lookup"><span data-stu-id="2d493-114">EXAMPLES</span></span>

### <span data-ttu-id="2d493-115">Példa 1: a zárolási megjegyzések frissítése</span><span class="sxs-lookup"><span data-stu-id="2d493-115">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="2d493-116">A parancs frissíti a ContosoSiteLock nevű zárolás megjegyzését.</span><span class="sxs-lookup"><span data-stu-id="2d493-116">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="2d493-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2d493-117">PARAMETERS</span></span>

### <span data-ttu-id="2d493-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2d493-118">-ApiVersion</span></span>
<span data-ttu-id="2d493-119">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d493-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="2d493-120">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="2d493-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d493-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d493-121">-DefaultProfile</span></span>
<span data-ttu-id="2d493-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2d493-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d493-123">-Force</span><span class="sxs-lookup"><span data-stu-id="2d493-123">-Force</span></span>
<span data-ttu-id="2d493-124">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="2d493-124">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d493-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2d493-125">-InformationAction</span></span>
<span data-ttu-id="2d493-126">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="2d493-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2d493-127">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="2d493-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2d493-128">Folytassa</span><span class="sxs-lookup"><span data-stu-id="2d493-128">Continue</span></span>
- <span data-ttu-id="2d493-129">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="2d493-129">Ignore</span></span>
- <span data-ttu-id="2d493-130">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="2d493-130">Inquire</span></span>
- <span data-ttu-id="2d493-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2d493-131">SilentlyContinue</span></span>
- <span data-ttu-id="2d493-132">állj</span><span class="sxs-lookup"><span data-stu-id="2d493-132">Stop</span></span>
- <span data-ttu-id="2d493-133">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="2d493-133">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d493-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2d493-134">-InformationVariable</span></span>
<span data-ttu-id="2d493-135">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="2d493-135">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d493-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="2d493-136">-LockId</span></span>
<span data-ttu-id="2d493-137">A parancsmag által módosított zárolás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d493-137">Specifies the ID of the lock that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d493-138">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="2d493-138">-LockLevel</span></span>
<span data-ttu-id="2d493-139">A zárolás szintjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d493-139">Specifies the level for the lock.</span></span>
<span data-ttu-id="2d493-140">Jelenleg az egyetlen érvényes érték a CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="2d493-140">Currently, the only valid value is CanNotDelete.</span></span>

```yaml
Type: LockLevel
Parameter Sets: (All)
Aliases: Level

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d493-141">-LockName</span><span class="sxs-lookup"><span data-stu-id="2d493-141">-LockName</span></span>
<span data-ttu-id="2d493-142">A parancsmag által módosított zárolás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d493-142">Specifies the name of the lock that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: BySpecifiedScope, ByResourceGroup, ByResourceGroupLevel, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d493-143">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="2d493-143">-LockNotes</span></span>
<span data-ttu-id="2d493-144">A zároláshoz kapcsolódó jegyzeteket adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d493-144">Specifies the notes for the lock.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Notes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d493-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="2d493-145">-Pre</span></span>
<span data-ttu-id="2d493-146">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="2d493-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d493-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d493-147">-ResourceGroupName</span></span>
<span data-ttu-id="2d493-148">Annak az erőforráscsoport-csoportnak a neve, amelyhez a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="2d493-148">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d493-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="2d493-149">-ResourceName</span></span>
<span data-ttu-id="2d493-150">Annak az erőforrásnak a nevét adja meg, amelynek a zárolását alkalmazni kívánja.</span><span class="sxs-lookup"><span data-stu-id="2d493-150">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="2d493-151">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot:</span><span class="sxs-lookup"><span data-stu-id="2d493-151">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="2d493-152">Kiszolgálói `/` adatbázis</span><span class="sxs-lookup"><span data-stu-id="2d493-152">Server`/`Database</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d493-153">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="2d493-153">-ResourceType</span></span>
<span data-ttu-id="2d493-154">Annak az erőforrásnak a típusa, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="2d493-154">Specifies the resource type for which the lock applies.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d493-155">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="2d493-155">-Scope</span></span>
<span data-ttu-id="2d493-156">Azt a hatókört adja meg, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="2d493-156">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="2d493-157">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot:</span><span class="sxs-lookup"><span data-stu-id="2d493-157">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="2d493-158">`/subscriptions/`előfizetés-azonosító erőforrás-kiszolgálócsoport neve- `/resourceGroups/` `/providers/Microsoft.Sql/servers/` `/databases/` adatbázis neve</span><span class="sxs-lookup"><span data-stu-id="2d493-158">`/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name</span></span>

<span data-ttu-id="2d493-159">Erőforráscsoport megadásához használja a következő formátumot:</span><span class="sxs-lookup"><span data-stu-id="2d493-159">To specify a resource group, use the following format:</span></span> 

<span data-ttu-id="2d493-160">`/subscriptions/`előfizetés-azonosító `/resourceGroups/` Erőforrás-csoport neve</span><span class="sxs-lookup"><span data-stu-id="2d493-160">`/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

```yaml
Type: String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d493-161">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="2d493-161">-TenantLevel</span></span>
<span data-ttu-id="2d493-162">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="2d493-162">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d493-163">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2d493-163">-Confirm</span></span>
<span data-ttu-id="2d493-164">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2d493-164">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d493-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d493-165">-WhatIf</span></span>
<span data-ttu-id="2d493-166">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2d493-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d493-167">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2d493-167">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d493-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d493-168">CommonParameters</span></span>
<span data-ttu-id="2d493-169">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2d493-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d493-170">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d493-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d493-171">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d493-171">INPUTS</span></span>

### <span data-ttu-id="2d493-172">Nincs</span><span class="sxs-lookup"><span data-stu-id="2d493-172">None</span></span>
<span data-ttu-id="2d493-173">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="2d493-173">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2d493-174">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d493-174">OUTPUTS</span></span>

### <span data-ttu-id="2d493-175">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="2d493-175">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="2d493-176">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2d493-176">NOTES</span></span>

## <span data-ttu-id="2d493-177">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d493-177">RELATED LINKS</span></span>

[<span data-ttu-id="2d493-178">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="2d493-178">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="2d493-179">Új – AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="2d493-179">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="2d493-180">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="2d493-180">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)


