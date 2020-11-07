---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcelock
schema: 2.0.0
ms.openlocfilehash: fdf60c029f260d30aae8983165cbfb4d20203824
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849482"
---
# <span data-ttu-id="0ade3-101">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="0ade3-101">Remove-AzureRmResourceLock</span></span>

## <span data-ttu-id="0ade3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0ade3-102">SYNOPSIS</span></span>
<span data-ttu-id="0ade3-103">Erőforrás-zárolás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="0ade3-103">Removes a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ade3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0ade3-104">SYNTAX</span></span>

### <span data-ttu-id="0ade3-105">ByLockId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0ade3-105">ByLockId (Default)</span></span>
```
Remove-AzureRmResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ade3-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0ade3-106">ByResourceGroup</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ade3-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="0ade3-107">ByResourceGroupLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0ade3-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="0ade3-108">BySpecifiedScope</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ade3-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="0ade3-109">BySubscription</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ade3-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="0ade3-110">BySubscriptionLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0ade3-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="0ade3-111">ByTenantLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0ade3-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="0ade3-112">DESCRIPTION</span></span>
<span data-ttu-id="0ade3-113">A **Remove-AzureRmResourceLock** parancsmag eltávolítja az Azure-erőforrás zárolását.</span><span class="sxs-lookup"><span data-stu-id="0ade3-113">The **Remove-AzureRmResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="0ade3-114">Példák</span><span class="sxs-lookup"><span data-stu-id="0ade3-114">EXAMPLES</span></span>

### <span data-ttu-id="0ade3-115">1. példa: zárolás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0ade3-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="0ade3-116">Ez a parancs eltávolítja a ContosoSiteLock nevű zárolást.</span><span class="sxs-lookup"><span data-stu-id="0ade3-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="0ade3-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0ade3-117">PARAMETERS</span></span>

### <span data-ttu-id="0ade3-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0ade3-118">-ApiVersion</span></span>
<span data-ttu-id="0ade3-119">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ade3-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="0ade3-120">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="0ade3-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0ade3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ade3-121">-DefaultProfile</span></span>
<span data-ttu-id="0ade3-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0ade3-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ade3-123">-Force</span><span class="sxs-lookup"><span data-stu-id="0ade3-123">-Force</span></span>
<span data-ttu-id="0ade3-124">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="0ade3-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0ade3-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0ade3-125">-InformationAction</span></span>
<span data-ttu-id="0ade3-126">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="0ade3-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="0ade3-127">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0ade3-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0ade3-128">Folytassa</span><span class="sxs-lookup"><span data-stu-id="0ade3-128">Continue</span></span>
- <span data-ttu-id="0ade3-129">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="0ade3-129">Ignore</span></span>
- <span data-ttu-id="0ade3-130">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="0ade3-130">Inquire</span></span>
- <span data-ttu-id="0ade3-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0ade3-131">SilentlyContinue</span></span>
- <span data-ttu-id="0ade3-132">állj</span><span class="sxs-lookup"><span data-stu-id="0ade3-132">Stop</span></span>
- <span data-ttu-id="0ade3-133">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="0ade3-133">Suspend</span></span>

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

### <span data-ttu-id="0ade3-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0ade3-134">-InformationVariable</span></span>
<span data-ttu-id="0ade3-135">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="0ade3-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0ade3-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="0ade3-136">-LockId</span></span>
<span data-ttu-id="0ade3-137">A parancsmag által eltávolított zárolás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ade3-137">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0ade3-138">-LockName</span><span class="sxs-lookup"><span data-stu-id="0ade3-138">-LockName</span></span>
<span data-ttu-id="0ade3-139">Annak a zárolásnak a neve, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="0ade3-139">Specifies the name of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0ade3-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="0ade3-140">-Pre</span></span>
<span data-ttu-id="0ade3-141">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="0ade3-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0ade3-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ade3-142">-ResourceGroupName</span></span>
<span data-ttu-id="0ade3-143">Annak az erőforráscsoport-csoportnak a neve, amelyhez a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="0ade3-143">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="0ade3-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0ade3-144">-ResourceName</span></span>
<span data-ttu-id="0ade3-145">Annak az erőforrásnak a nevét adja meg, amelynek a zárolását alkalmazni kívánja.</span><span class="sxs-lookup"><span data-stu-id="0ade3-145">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="0ade3-146">Ha például egy adatbázist szeretne megadni, használja a következő formátumot: kiszolgálói `/` adatbázis</span><span class="sxs-lookup"><span data-stu-id="0ade3-146">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="0ade3-147">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0ade3-147">-ResourceType</span></span>
<span data-ttu-id="0ade3-148">Annak az erőforrásnak az erőforrás típusát adja meg, amelyre vonatkozóan a zárolás érvényes.</span><span class="sxs-lookup"><span data-stu-id="0ade3-148">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="0ade3-149">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="0ade3-149">-Scope</span></span>
<span data-ttu-id="0ade3-150">Azt a hatókört adja meg, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="0ade3-150">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="0ade3-151">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="0ade3-151">-TenantLevel</span></span>
<span data-ttu-id="0ade3-152">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="0ade3-152">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="0ade3-153">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0ade3-153">-Confirm</span></span>
<span data-ttu-id="0ade3-154">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0ade3-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ade3-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ade3-155">-WhatIf</span></span>
<span data-ttu-id="0ade3-156">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0ade3-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ade3-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0ade3-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ade3-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ade3-158">CommonParameters</span></span>
<span data-ttu-id="0ade3-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0ade3-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ade3-160">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ade3-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ade3-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ade3-161">INPUTS</span></span>

## <span data-ttu-id="0ade3-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ade3-162">OUTPUTS</span></span>

## <span data-ttu-id="0ade3-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0ade3-163">NOTES</span></span>

## <span data-ttu-id="0ade3-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ade3-164">RELATED LINKS</span></span>

[<span data-ttu-id="0ade3-165">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="0ade3-165">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="0ade3-166">Új – AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="0ade3-166">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="0ade3-167">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="0ade3-167">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


