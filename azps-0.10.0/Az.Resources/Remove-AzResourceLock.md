---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzResourceLock.md
ms.openlocfilehash: 6b9a0b792b1a8a5572ce26561202284f3103d764
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843234"
---
# <span data-ttu-id="396a6-101">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="396a6-101">Remove-AzResourceLock</span></span>

## <span data-ttu-id="396a6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="396a6-102">SYNOPSIS</span></span>
<span data-ttu-id="396a6-103">Erőforrás-zárolás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="396a6-103">Removes a resource lock.</span></span>

## <span data-ttu-id="396a6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="396a6-104">SYNTAX</span></span>

### <span data-ttu-id="396a6-105">ByLockId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="396a6-105">ByLockId (Default)</span></span>
```
Remove-AzResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="396a6-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="396a6-106">ByResourceGroup</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="396a6-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="396a6-107">ByResourceGroupLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="396a6-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="396a6-108">BySpecifiedScope</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="396a6-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="396a6-109">BySubscription</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="396a6-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="396a6-110">BySubscriptionLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="396a6-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="396a6-111">ByTenantLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="396a6-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="396a6-112">DESCRIPTION</span></span>
<span data-ttu-id="396a6-113">A **Remove-AzResourceLock** parancsmag eltávolítja az Azure-erőforrás zárolását.</span><span class="sxs-lookup"><span data-stu-id="396a6-113">The **Remove-AzResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="396a6-114">Példák</span><span class="sxs-lookup"><span data-stu-id="396a6-114">EXAMPLES</span></span>

### <span data-ttu-id="396a6-115">1. példa: zárolás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="396a6-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="396a6-116">Ez a parancs eltávolítja a ContosoSiteLock nevű zárolást.</span><span class="sxs-lookup"><span data-stu-id="396a6-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="396a6-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="396a6-117">PARAMETERS</span></span>

### <span data-ttu-id="396a6-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="396a6-118">-ApiVersion</span></span>
<span data-ttu-id="396a6-119">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="396a6-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="396a6-120">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="396a6-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="396a6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="396a6-121">-DefaultProfile</span></span>
<span data-ttu-id="396a6-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="396a6-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="396a6-123">-Force</span><span class="sxs-lookup"><span data-stu-id="396a6-123">-Force</span></span>
<span data-ttu-id="396a6-124">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="396a6-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="396a6-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="396a6-125">-InformationAction</span></span>
<span data-ttu-id="396a6-126">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="396a6-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="396a6-127">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="396a6-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="396a6-128">Folytassa</span><span class="sxs-lookup"><span data-stu-id="396a6-128">Continue</span></span>
- <span data-ttu-id="396a6-129">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="396a6-129">Ignore</span></span>
- <span data-ttu-id="396a6-130">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="396a6-130">Inquire</span></span>
- <span data-ttu-id="396a6-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="396a6-131">SilentlyContinue</span></span>
- <span data-ttu-id="396a6-132">állj</span><span class="sxs-lookup"><span data-stu-id="396a6-132">Stop</span></span>
- <span data-ttu-id="396a6-133">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="396a6-133">Suspend</span></span>

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

### <span data-ttu-id="396a6-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="396a6-134">-InformationVariable</span></span>
<span data-ttu-id="396a6-135">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="396a6-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="396a6-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="396a6-136">-LockId</span></span>
<span data-ttu-id="396a6-137">A parancsmag által eltávolított zárolás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="396a6-137">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="396a6-138">-LockName</span><span class="sxs-lookup"><span data-stu-id="396a6-138">-LockName</span></span>
<span data-ttu-id="396a6-139">Annak a zárolásnak a neve, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="396a6-139">Specifies the name of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="396a6-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="396a6-140">-Pre</span></span>
<span data-ttu-id="396a6-141">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="396a6-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="396a6-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="396a6-142">-ResourceGroupName</span></span>
<span data-ttu-id="396a6-143">Annak az erőforráscsoport-csoportnak a neve, amelyhez a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="396a6-143">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="396a6-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="396a6-144">-ResourceName</span></span>
<span data-ttu-id="396a6-145">Annak az erőforrásnak a nevét adja meg, amelynek a zárolását alkalmazni kívánja.</span><span class="sxs-lookup"><span data-stu-id="396a6-145">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="396a6-146">Ha például egy adatbázist szeretne megadni, használja a következő formátumot: kiszolgálói `/` adatbázis</span><span class="sxs-lookup"><span data-stu-id="396a6-146">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="396a6-147">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="396a6-147">-ResourceType</span></span>
<span data-ttu-id="396a6-148">Annak az erőforrásnak az erőforrás típusát adja meg, amelyre vonatkozóan a zárolás érvényes.</span><span class="sxs-lookup"><span data-stu-id="396a6-148">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="396a6-149">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="396a6-149">-Scope</span></span>
<span data-ttu-id="396a6-150">Azt a hatókört adja meg, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="396a6-150">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="396a6-151">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="396a6-151">-TenantLevel</span></span>
<span data-ttu-id="396a6-152">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="396a6-152">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="396a6-153">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="396a6-153">-Confirm</span></span>
<span data-ttu-id="396a6-154">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="396a6-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="396a6-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="396a6-155">-WhatIf</span></span>
<span data-ttu-id="396a6-156">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="396a6-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="396a6-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="396a6-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="396a6-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="396a6-158">CommonParameters</span></span>
<span data-ttu-id="396a6-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="396a6-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="396a6-160">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="396a6-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="396a6-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="396a6-161">INPUTS</span></span>

## <span data-ttu-id="396a6-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="396a6-162">OUTPUTS</span></span>

## <span data-ttu-id="396a6-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="396a6-163">NOTES</span></span>

## <span data-ttu-id="396a6-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="396a6-164">RELATED LINKS</span></span>

[<span data-ttu-id="396a6-165">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="396a6-165">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="396a6-166">Új – AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="396a6-166">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="396a6-167">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="396a6-167">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


