---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
ms.openlocfilehash: 32a3dbb458c4848a5578309593b205b4ced5be03
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838111"
---
# <span data-ttu-id="619e8-101">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="619e8-101">Remove-AzResourceLock</span></span>

## <span data-ttu-id="619e8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="619e8-102">SYNOPSIS</span></span>
<span data-ttu-id="619e8-103">Erőforrás-zárolás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="619e8-103">Removes a resource lock.</span></span>

## <span data-ttu-id="619e8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="619e8-104">SYNTAX</span></span>

### <span data-ttu-id="619e8-105">ByLockId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="619e8-105">ByLockId (Default)</span></span>
```
Remove-AzResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="619e8-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="619e8-106">ByResourceGroup</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="619e8-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="619e8-107">ByResourceGroupLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="619e8-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="619e8-108">BySpecifiedScope</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="619e8-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="619e8-109">BySubscription</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="619e8-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="619e8-110">BySubscriptionLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="619e8-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="619e8-111">ByTenantLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="619e8-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="619e8-112">DESCRIPTION</span></span>
<span data-ttu-id="619e8-113">A **Remove-AzResourceLock** parancsmag eltávolítja az Azure-erőforrás zárolását.</span><span class="sxs-lookup"><span data-stu-id="619e8-113">The **Remove-AzResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="619e8-114">Példák</span><span class="sxs-lookup"><span data-stu-id="619e8-114">EXAMPLES</span></span>

### <span data-ttu-id="619e8-115">1. példa: zárolás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="619e8-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="619e8-116">Ez a parancs eltávolítja a ContosoSiteLock nevű zárolást.</span><span class="sxs-lookup"><span data-stu-id="619e8-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="619e8-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="619e8-117">PARAMETERS</span></span>

### <span data-ttu-id="619e8-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="619e8-118">-ApiVersion</span></span>
<span data-ttu-id="619e8-119">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="619e8-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="619e8-120">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="619e8-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="619e8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="619e8-121">-DefaultProfile</span></span>
<span data-ttu-id="619e8-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="619e8-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="619e8-123">-Force</span><span class="sxs-lookup"><span data-stu-id="619e8-123">-Force</span></span>
<span data-ttu-id="619e8-124">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="619e8-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="619e8-125">-LockId</span><span class="sxs-lookup"><span data-stu-id="619e8-125">-LockId</span></span>
<span data-ttu-id="619e8-126">A parancsmag által eltávolított zárolás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="619e8-126">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="619e8-127">-LockName</span><span class="sxs-lookup"><span data-stu-id="619e8-127">-LockName</span></span>
<span data-ttu-id="619e8-128">Annak a zárolásnak a neve, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="619e8-128">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="619e8-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="619e8-129">-Pre</span></span>
<span data-ttu-id="619e8-130">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="619e8-130">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="619e8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="619e8-131">-ResourceGroupName</span></span>
<span data-ttu-id="619e8-132">Annak az erőforráscsoport-csoportnak a neve, amelyhez a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="619e8-132">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="619e8-133">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="619e8-133">-ResourceName</span></span>
<span data-ttu-id="619e8-134">Annak az erőforrásnak a nevét adja meg, amelynek a zárolását alkalmazni kívánja.</span><span class="sxs-lookup"><span data-stu-id="619e8-134">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="619e8-135">Ha például egy adatbázist szeretne megadni, használja a következő formátumot: kiszolgálói `/` adatbázis</span><span class="sxs-lookup"><span data-stu-id="619e8-135">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="619e8-136">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="619e8-136">-ResourceType</span></span>
<span data-ttu-id="619e8-137">Annak az erőforrásnak az erőforrás típusát adja meg, amelyre vonatkozóan a zárolás érvényes.</span><span class="sxs-lookup"><span data-stu-id="619e8-137">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="619e8-138">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="619e8-138">-Scope</span></span>
<span data-ttu-id="619e8-139">Azt a hatókört adja meg, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="619e8-139">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="619e8-140">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="619e8-140">-TenantLevel</span></span>
<span data-ttu-id="619e8-141">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="619e8-141">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="619e8-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="619e8-142">-Confirm</span></span>
<span data-ttu-id="619e8-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="619e8-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="619e8-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="619e8-144">-WhatIf</span></span>
<span data-ttu-id="619e8-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="619e8-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="619e8-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="619e8-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="619e8-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="619e8-147">CommonParameters</span></span>
<span data-ttu-id="619e8-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="619e8-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="619e8-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="619e8-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="619e8-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="619e8-150">INPUTS</span></span>

### <span data-ttu-id="619e8-151">System. String</span><span class="sxs-lookup"><span data-stu-id="619e8-151">System.String</span></span>

## <span data-ttu-id="619e8-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="619e8-152">OUTPUTS</span></span>

### <span data-ttu-id="619e8-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="619e8-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="619e8-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="619e8-154">NOTES</span></span>

## <span data-ttu-id="619e8-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="619e8-155">RELATED LINKS</span></span>

[<span data-ttu-id="619e8-156">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="619e8-156">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="619e8-157">Új – AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="619e8-157">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="619e8-158">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="619e8-158">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


