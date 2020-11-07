---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzResourceLock.md
ms.openlocfilehash: fdf9f91570fc598806427b6812f52e397fb19322
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843181"
---
# <span data-ttu-id="35d71-101">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="35d71-101">Set-AzResourceLock</span></span>

## <span data-ttu-id="35d71-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="35d71-102">SYNOPSIS</span></span>
<span data-ttu-id="35d71-103">Módosítja az erőforrás-zárolást.</span><span class="sxs-lookup"><span data-stu-id="35d71-103">Modifies a resource lock.</span></span>

## <span data-ttu-id="35d71-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="35d71-104">SYNTAX</span></span>

### <span data-ttu-id="35d71-105">BySpecifiedScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="35d71-105">BySpecifiedScope (Default)</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35d71-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="35d71-106">ByResourceGroup</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35d71-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="35d71-107">ByResourceGroupLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35d71-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="35d71-108">BySubscription</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35d71-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="35d71-109">BySubscriptionLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35d71-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="35d71-110">ByTenantLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35d71-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="35d71-111">ByLockId</span></span>
```
Set-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="35d71-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="35d71-112">DESCRIPTION</span></span>
<span data-ttu-id="35d71-113">A **set-AzResourceLock** parancsmag módosítja az erőforrás-zárolást.</span><span class="sxs-lookup"><span data-stu-id="35d71-113">The **Set-AzResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="35d71-114">Példák</span><span class="sxs-lookup"><span data-stu-id="35d71-114">EXAMPLES</span></span>

### <span data-ttu-id="35d71-115">Példa 1: a zárolási megjegyzések frissítése</span><span class="sxs-lookup"><span data-stu-id="35d71-115">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="35d71-116">A parancs frissíti a ContosoSiteLock nevű zárolás megjegyzését.</span><span class="sxs-lookup"><span data-stu-id="35d71-116">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="35d71-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="35d71-117">PARAMETERS</span></span>

### <span data-ttu-id="35d71-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="35d71-118">-ApiVersion</span></span>
<span data-ttu-id="35d71-119">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="35d71-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="35d71-120">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="35d71-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="35d71-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35d71-121">-DefaultProfile</span></span>
<span data-ttu-id="35d71-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="35d71-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35d71-123">-Force</span><span class="sxs-lookup"><span data-stu-id="35d71-123">-Force</span></span>
<span data-ttu-id="35d71-124">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="35d71-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="35d71-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="35d71-125">-InformationAction</span></span>
<span data-ttu-id="35d71-126">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="35d71-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="35d71-127">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="35d71-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="35d71-128">Folytassa</span><span class="sxs-lookup"><span data-stu-id="35d71-128">Continue</span></span>
- <span data-ttu-id="35d71-129">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="35d71-129">Ignore</span></span>
- <span data-ttu-id="35d71-130">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="35d71-130">Inquire</span></span>
- <span data-ttu-id="35d71-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="35d71-131">SilentlyContinue</span></span>
- <span data-ttu-id="35d71-132">állj</span><span class="sxs-lookup"><span data-stu-id="35d71-132">Stop</span></span>
- <span data-ttu-id="35d71-133">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="35d71-133">Suspend</span></span>

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

### <span data-ttu-id="35d71-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="35d71-134">-InformationVariable</span></span>
<span data-ttu-id="35d71-135">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="35d71-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="35d71-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="35d71-136">-LockId</span></span>
<span data-ttu-id="35d71-137">A parancsmag által módosított zárolás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="35d71-137">Specifies the ID of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="35d71-138">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="35d71-138">-LockLevel</span></span>
<span data-ttu-id="35d71-139">A zárolás szintjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="35d71-139">Specifies the level for the lock.</span></span>
<span data-ttu-id="35d71-140">Jelenleg az egyetlen érvényes érték a CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="35d71-140">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="35d71-141">-LockName</span><span class="sxs-lookup"><span data-stu-id="35d71-141">-LockName</span></span>
<span data-ttu-id="35d71-142">A parancsmag által módosított zárolás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="35d71-142">Specifies the name of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="35d71-143">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="35d71-143">-LockNotes</span></span>
<span data-ttu-id="35d71-144">A zároláshoz kapcsolódó jegyzeteket adja meg.</span><span class="sxs-lookup"><span data-stu-id="35d71-144">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="35d71-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="35d71-145">-Pre</span></span>
<span data-ttu-id="35d71-146">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="35d71-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="35d71-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35d71-147">-ResourceGroupName</span></span>
<span data-ttu-id="35d71-148">Annak az erőforráscsoport-csoportnak a neve, amelyhez a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="35d71-148">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="35d71-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="35d71-149">-ResourceName</span></span>
<span data-ttu-id="35d71-150">Annak az erőforrásnak a nevét adja meg, amelynek a zárolását alkalmazni kívánja.</span><span class="sxs-lookup"><span data-stu-id="35d71-150">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="35d71-151">Ha például egy adatbázist szeretne megadni, használja a következő formátumot: kiszolgálói `/` adatbázis</span><span class="sxs-lookup"><span data-stu-id="35d71-151">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="35d71-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="35d71-152">-ResourceType</span></span>
<span data-ttu-id="35d71-153">Annak az erőforrásnak a típusa, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="35d71-153">Specifies the resource type for which the lock applies.</span></span>

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

### <span data-ttu-id="35d71-154">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="35d71-154">-Scope</span></span>
<span data-ttu-id="35d71-155">Azt a hatókört adja meg, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="35d71-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="35d71-156">Ha például meg szeretne adni egy adatbázist, használja a következő formátumot: `/subscriptions/` előfizetés-azonosító `/resourceGroups/` erőforráscsoport neve `/providers/Microsoft.Sql/servers/` kiszolgálónév `/databases/` -adatbázis neve az erőforráscsoport megadásához, használja a következő formátumot: `/subscriptions/` előfizetés azonosítója `/resourceGroups/` Erőforrás-csoport neve</span><span class="sxs-lookup"><span data-stu-id="35d71-156">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="35d71-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="35d71-157">-TenantLevel</span></span>
<span data-ttu-id="35d71-158">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="35d71-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="35d71-159">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="35d71-159">-Confirm</span></span>
<span data-ttu-id="35d71-160">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="35d71-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35d71-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35d71-161">-WhatIf</span></span>
<span data-ttu-id="35d71-162">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="35d71-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35d71-163">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="35d71-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35d71-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35d71-164">CommonParameters</span></span>
<span data-ttu-id="35d71-165">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="35d71-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35d71-166">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35d71-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35d71-167">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="35d71-167">INPUTS</span></span>

## <span data-ttu-id="35d71-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="35d71-168">OUTPUTS</span></span>

## <span data-ttu-id="35d71-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="35d71-169">NOTES</span></span>

## <span data-ttu-id="35d71-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="35d71-170">RELATED LINKS</span></span>

[<span data-ttu-id="35d71-171">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="35d71-171">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="35d71-172">Új – AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="35d71-172">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="35d71-173">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="35d71-173">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)


