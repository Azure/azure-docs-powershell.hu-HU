---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
ms.openlocfilehash: 6e7c2d90b912364bee8e1b97fc7e56fd64916666
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937385"
---
# <span data-ttu-id="97e39-101">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="97e39-101">Remove-AzResourceLock</span></span>

## <span data-ttu-id="97e39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97e39-102">SYNOPSIS</span></span>
<span data-ttu-id="97e39-103">Eltávolítja az erőforrászárolást.</span><span class="sxs-lookup"><span data-stu-id="97e39-103">Removes a resource lock.</span></span>

## <span data-ttu-id="97e39-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="97e39-104">SYNTAX</span></span>

### <span data-ttu-id="97e39-105">ByLockId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="97e39-105">ByLockId (Default)</span></span>
```
Remove-AzResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97e39-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="97e39-106">ByResourceGroup</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97e39-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="97e39-107">ByResourceGroupLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97e39-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="97e39-108">BySpecifiedScope</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97e39-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="97e39-109">BySubscription</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97e39-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="97e39-110">BySubscriptionLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="97e39-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="97e39-111">DESCRIPTION</span></span>
<span data-ttu-id="97e39-112">A **Remove-AzResourceLock** parancsmag eltávolítja az Azure-erőforrászárat.</span><span class="sxs-lookup"><span data-stu-id="97e39-112">The **Remove-AzResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="97e39-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="97e39-113">EXAMPLES</span></span>

### <span data-ttu-id="97e39-114">1. példa: Zárolás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="97e39-114">Example 1: Remove a lock</span></span>
```powershell
PS C:\>Remove-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="97e39-115">Ez a parancs eltávolítja a ContosoSiteLock nevű zárolást.</span><span class="sxs-lookup"><span data-stu-id="97e39-115">This command removes the lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="97e39-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="97e39-116">Example 2</span></span>

<span data-ttu-id="97e39-117">Eltávolítja az erőforrászárolást.</span><span class="sxs-lookup"><span data-stu-id="97e39-117">Removes a resource lock.</span></span> <span data-ttu-id="97e39-118">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="97e39-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
Remove-AzResourceLock -LockName 'ContosoSiteLock' -ResourceGroupName myresourcegroup -ResourceName '/subscriptions/00000000-0000-0000-0000-00000000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test' -ResourceType 'Microsoft.ClassicCompute/storageAccounts'
```

## <span data-ttu-id="97e39-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97e39-119">PARAMETERS</span></span>

### <span data-ttu-id="97e39-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="97e39-120">-ApiVersion</span></span>
<span data-ttu-id="97e39-121">Az erőforrás-szolgáltató API-jának használnia kell verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="97e39-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="97e39-122">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="97e39-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="97e39-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97e39-123">-DefaultProfile</span></span>
<span data-ttu-id="97e39-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="97e39-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97e39-125">-Force</span><span class="sxs-lookup"><span data-stu-id="97e39-125">-Force</span></span>
<span data-ttu-id="97e39-126">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="97e39-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="97e39-127">-LockId</span><span class="sxs-lookup"><span data-stu-id="97e39-127">-LockId</span></span>
<span data-ttu-id="97e39-128">A parancsmag által eltávolított zárolás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="97e39-128">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="97e39-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="97e39-129">-LockName</span></span>
<span data-ttu-id="97e39-130">A parancsmag által eltávolított lakat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="97e39-130">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97e39-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="97e39-131">-Pre</span></span>
<span data-ttu-id="97e39-132">Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.</span><span class="sxs-lookup"><span data-stu-id="97e39-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="97e39-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97e39-133">-ResourceGroupName</span></span>
<span data-ttu-id="97e39-134">Annak az erőforráscsoportnak a nevét adja meg, amelyre a zárolás érvényes.</span><span class="sxs-lookup"><span data-stu-id="97e39-134">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="97e39-135">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="97e39-135">-ResourceName</span></span>
<span data-ttu-id="97e39-136">Annak az erőforrásnak a nevét adja meg, amelyre a zárolás érvényes.</span><span class="sxs-lookup"><span data-stu-id="97e39-136">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="97e39-137">Adatbázis megadásához például használja a következő `/` formátumot: Kiszolgálói adatbázis</span><span class="sxs-lookup"><span data-stu-id="97e39-137">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="97e39-138">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="97e39-138">-ResourceType</span></span>
<span data-ttu-id="97e39-139">Annak az erőforrásnak az erőforrástípusát adja meg, amelyre a zárolás érvényes.</span><span class="sxs-lookup"><span data-stu-id="97e39-139">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="97e39-140">-Scope</span><span class="sxs-lookup"><span data-stu-id="97e39-140">-Scope</span></span>
<span data-ttu-id="97e39-141">A zárolás hatókörét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="97e39-141">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="97e39-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="97e39-142">-Confirm</span></span>
<span data-ttu-id="97e39-143">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="97e39-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97e39-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97e39-144">-WhatIf</span></span>
<span data-ttu-id="97e39-145">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="97e39-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97e39-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="97e39-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97e39-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97e39-147">CommonParameters</span></span>
<span data-ttu-id="97e39-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97e39-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97e39-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97e39-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97e39-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="97e39-150">INPUTS</span></span>

### <span data-ttu-id="97e39-151">System.String</span><span class="sxs-lookup"><span data-stu-id="97e39-151">System.String</span></span>

## <span data-ttu-id="97e39-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97e39-152">OUTPUTS</span></span>

### <span data-ttu-id="97e39-153">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="97e39-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="97e39-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="97e39-154">NOTES</span></span>

## <span data-ttu-id="97e39-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97e39-155">RELATED LINKS</span></span>

[<span data-ttu-id="97e39-156">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="97e39-156">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="97e39-157">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="97e39-157">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="97e39-158">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="97e39-158">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


