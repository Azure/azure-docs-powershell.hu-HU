---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
ms.openlocfilehash: f3034d7197a26e8dd2ba803f478b6a71c8d50e8c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672842"
---
# <span data-ttu-id="8a300-101">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="8a300-101">Remove-AzureRmResourceLock</span></span>

## <span data-ttu-id="8a300-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8a300-102">SYNOPSIS</span></span>
<span data-ttu-id="8a300-103">Erőforrás-zárolás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="8a300-103">Removes a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a300-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8a300-104">SYNTAX</span></span>

### <span data-ttu-id="8a300-105">ByLockId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8a300-105">ByLockId (Default)</span></span>
```
Remove-AzureRmResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a300-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8a300-106">ByResourceGroup</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a300-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="8a300-107">ByResourceGroupLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a300-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="8a300-108">BySpecifiedScope</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a300-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="8a300-109">BySubscription</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a300-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="8a300-110">BySubscriptionLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a300-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="8a300-111">ByTenantLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8a300-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="8a300-112">DESCRIPTION</span></span>
<span data-ttu-id="8a300-113">A **Remove-AzureRmResourceLock** parancsmag eltávolítja az Azure-erőforrás zárolását.</span><span class="sxs-lookup"><span data-stu-id="8a300-113">The **Remove-AzureRmResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="8a300-114">Példák</span><span class="sxs-lookup"><span data-stu-id="8a300-114">EXAMPLES</span></span>

### <span data-ttu-id="8a300-115">1. példa: zárolás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8a300-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="8a300-116">Ez a parancs eltávolítja a ContosoSiteLock nevű zárolást.</span><span class="sxs-lookup"><span data-stu-id="8a300-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="8a300-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8a300-117">PARAMETERS</span></span>

### <span data-ttu-id="8a300-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8a300-118">-ApiVersion</span></span>
<span data-ttu-id="8a300-119">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8a300-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8a300-120">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="8a300-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8a300-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a300-121">-DefaultProfile</span></span>
<span data-ttu-id="8a300-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8a300-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a300-123">-Force</span><span class="sxs-lookup"><span data-stu-id="8a300-123">-Force</span></span>
<span data-ttu-id="8a300-124">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="8a300-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8a300-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8a300-125">-InformationAction</span></span>
<span data-ttu-id="8a300-126">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="8a300-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8a300-127">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8a300-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8a300-128">Folytassa</span><span class="sxs-lookup"><span data-stu-id="8a300-128">Continue</span></span>
- <span data-ttu-id="8a300-129">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="8a300-129">Ignore</span></span>
- <span data-ttu-id="8a300-130">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="8a300-130">Inquire</span></span>
- <span data-ttu-id="8a300-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8a300-131">SilentlyContinue</span></span>
- <span data-ttu-id="8a300-132">állj</span><span class="sxs-lookup"><span data-stu-id="8a300-132">Stop</span></span>
- <span data-ttu-id="8a300-133">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="8a300-133">Suspend</span></span>

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

### <span data-ttu-id="8a300-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8a300-134">-InformationVariable</span></span>
<span data-ttu-id="8a300-135">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="8a300-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8a300-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="8a300-136">-LockId</span></span>
<span data-ttu-id="8a300-137">A parancsmag által eltávolított zárolás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8a300-137">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8a300-138">-LockName</span><span class="sxs-lookup"><span data-stu-id="8a300-138">-LockName</span></span>
<span data-ttu-id="8a300-139">Annak a zárolásnak a neve, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="8a300-139">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a300-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="8a300-140">-Pre</span></span>
<span data-ttu-id="8a300-141">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="8a300-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8a300-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a300-142">-ResourceGroupName</span></span>
<span data-ttu-id="8a300-143">Annak az erőforráscsoport-csoportnak a neve, amelyhez a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="8a300-143">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="8a300-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8a300-144">-ResourceName</span></span>
<span data-ttu-id="8a300-145">Annak az erőforrásnak a nevét adja meg, amelynek a zárolását alkalmazni kívánja.</span><span class="sxs-lookup"><span data-stu-id="8a300-145">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="8a300-146">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot:</span><span class="sxs-lookup"><span data-stu-id="8a300-146">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="8a300-147">Kiszolgálói `/` adatbázis</span><span class="sxs-lookup"><span data-stu-id="8a300-147">Server`/`Database</span></span>

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

### <span data-ttu-id="8a300-148">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="8a300-148">-ResourceType</span></span>
<span data-ttu-id="8a300-149">Annak az erőforrásnak az erőforrás típusát adja meg, amelyre vonatkozóan a zárolás érvényes.</span><span class="sxs-lookup"><span data-stu-id="8a300-149">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="8a300-150">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="8a300-150">-Scope</span></span>
<span data-ttu-id="8a300-151">Azt a hatókört adja meg, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="8a300-151">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="8a300-152">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="8a300-152">-TenantLevel</span></span>
<span data-ttu-id="8a300-153">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="8a300-153">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="8a300-154">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8a300-154">-Confirm</span></span>
<span data-ttu-id="8a300-155">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8a300-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a300-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a300-156">-WhatIf</span></span>
<span data-ttu-id="8a300-157">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8a300-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a300-158">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8a300-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a300-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a300-159">CommonParameters</span></span>
<span data-ttu-id="8a300-160">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8a300-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a300-161">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a300-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a300-162">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a300-162">INPUTS</span></span>

### <span data-ttu-id="8a300-163">Nincs</span><span class="sxs-lookup"><span data-stu-id="8a300-163">None</span></span>
<span data-ttu-id="8a300-164">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="8a300-164">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8a300-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a300-165">OUTPUTS</span></span>

### <span data-ttu-id="8a300-166">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="8a300-166">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8a300-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8a300-167">NOTES</span></span>

## <span data-ttu-id="8a300-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8a300-168">RELATED LINKS</span></span>

[<span data-ttu-id="8a300-169">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="8a300-169">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="8a300-170">Új – AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="8a300-170">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="8a300-171">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="8a300-171">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


