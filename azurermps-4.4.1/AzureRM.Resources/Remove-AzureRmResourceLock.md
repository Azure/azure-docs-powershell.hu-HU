---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
ms.openlocfilehash: c45d78b815586e54c9f39cfd536fed5a26c2eb19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500711"
---
# <span data-ttu-id="99eb2-101">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="99eb2-101">Remove-AzureRmResourceLock</span></span>

## <span data-ttu-id="99eb2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="99eb2-102">SYNOPSIS</span></span>
<span data-ttu-id="99eb2-103">Erőforrás-zárolás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="99eb2-103">Removes a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99eb2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="99eb2-104">SYNTAX</span></span>

### <span data-ttu-id="99eb2-105">Zárolás, azonosító szerint. (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="99eb2-105">A lock, by Id. (Default)</span></span>
```
Remove-AzureRmResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99eb2-106">Az erőforráscsoport hatókörének zárolása.</span><span class="sxs-lookup"><span data-stu-id="99eb2-106">A lock at the resource group scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99eb2-107">Zárolás az erőforrás-csoport erőforrás-hatókörében.</span><span class="sxs-lookup"><span data-stu-id="99eb2-107">A lock at the resource group resource scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99eb2-108">A megadott hatókör zárolása.</span><span class="sxs-lookup"><span data-stu-id="99eb2-108">A lock at the specified scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99eb2-109">Zárolás az előfizetéses hatókörben.</span><span class="sxs-lookup"><span data-stu-id="99eb2-109">A lock at the subscription scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99eb2-110">Zárolás az előfizetés erőforrás-tartományában.</span><span class="sxs-lookup"><span data-stu-id="99eb2-110">A lock at the subscription resource scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99eb2-111">A bérlői erőforrás hatókörének zárolása.</span><span class="sxs-lookup"><span data-stu-id="99eb2-111">A lock at the tenant resource scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="99eb2-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="99eb2-112">DESCRIPTION</span></span>
<span data-ttu-id="99eb2-113">A **Remove-AzureRmResourceLock** parancsmag eltávolítja az Azure-erőforrás zárolását.</span><span class="sxs-lookup"><span data-stu-id="99eb2-113">The **Remove-AzureRmResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="99eb2-114">Példák</span><span class="sxs-lookup"><span data-stu-id="99eb2-114">EXAMPLES</span></span>

### <span data-ttu-id="99eb2-115">1. példa: zárolás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="99eb2-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="99eb2-116">Ez a parancs eltávolítja a ContosoSiteLock nevű zárolást.</span><span class="sxs-lookup"><span data-stu-id="99eb2-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="99eb2-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="99eb2-117">PARAMETERS</span></span>

### <span data-ttu-id="99eb2-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="99eb2-118">-ApiVersion</span></span>
<span data-ttu-id="99eb2-119">Az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="99eb2-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="99eb2-120">Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.</span><span class="sxs-lookup"><span data-stu-id="99eb2-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="99eb2-121">-Force</span><span class="sxs-lookup"><span data-stu-id="99eb2-121">-Force</span></span>
<span data-ttu-id="99eb2-122">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="99eb2-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="99eb2-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="99eb2-123">-InformationAction</span></span>
<span data-ttu-id="99eb2-124">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="99eb2-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="99eb2-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="99eb2-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="99eb2-126">Folytassa</span><span class="sxs-lookup"><span data-stu-id="99eb2-126">Continue</span></span>
- <span data-ttu-id="99eb2-127">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="99eb2-127">Ignore</span></span>
- <span data-ttu-id="99eb2-128">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="99eb2-128">Inquire</span></span>
- <span data-ttu-id="99eb2-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="99eb2-129">SilentlyContinue</span></span>
- <span data-ttu-id="99eb2-130">állj</span><span class="sxs-lookup"><span data-stu-id="99eb2-130">Stop</span></span>
- <span data-ttu-id="99eb2-131">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="99eb2-131">Suspend</span></span>

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

### <span data-ttu-id="99eb2-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="99eb2-132">-InformationVariable</span></span>
<span data-ttu-id="99eb2-133">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="99eb2-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="99eb2-134">-LockId</span><span class="sxs-lookup"><span data-stu-id="99eb2-134">-LockId</span></span>
<span data-ttu-id="99eb2-135">A parancsmag által eltávolított zárolás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="99eb2-135">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="99eb2-136">-LockName</span><span class="sxs-lookup"><span data-stu-id="99eb2-136">-LockName</span></span>
<span data-ttu-id="99eb2-137">Annak a zárolásnak a neve, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="99eb2-137">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope., A lock at the specified scope., A lock at the subscription scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99eb2-138">-Pre</span><span class="sxs-lookup"><span data-stu-id="99eb2-138">-Pre</span></span>
<span data-ttu-id="99eb2-139">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="99eb2-139">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="99eb2-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99eb2-140">-ResourceGroupName</span></span>
<span data-ttu-id="99eb2-141">Annak az erőforráscsoport-csoportnak a neve, amelyhez a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="99eb2-141">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="99eb2-142">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="99eb2-142">-ResourceName</span></span>
<span data-ttu-id="99eb2-143">Annak az erőforrásnak a nevét adja meg, amelynek a zárolását alkalmazni kívánja.</span><span class="sxs-lookup"><span data-stu-id="99eb2-143">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="99eb2-144">Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot:</span><span class="sxs-lookup"><span data-stu-id="99eb2-144">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="99eb2-145">Kiszolgálói `/` adatbázis</span><span class="sxs-lookup"><span data-stu-id="99eb2-145">Server`/`Database</span></span>

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

### <span data-ttu-id="99eb2-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="99eb2-146">-ResourceType</span></span>
<span data-ttu-id="99eb2-147">Annak az erőforrásnak az erőforrás típusát adja meg, amelyre vonatkozóan a zárolás érvényes.</span><span class="sxs-lookup"><span data-stu-id="99eb2-147">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="99eb2-148">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="99eb2-148">-Scope</span></span>
<span data-ttu-id="99eb2-149">Azt a hatókört adja meg, amelyre a zárolás vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="99eb2-149">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="99eb2-150">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="99eb2-150">-TenantLevel</span></span>
<span data-ttu-id="99eb2-151">Jelzi, hogy ez a parancsmag a bérlői szinten működik.</span><span class="sxs-lookup"><span data-stu-id="99eb2-151">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="99eb2-152">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="99eb2-152">-Confirm</span></span>
<span data-ttu-id="99eb2-153">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="99eb2-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99eb2-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99eb2-154">-WhatIf</span></span>
<span data-ttu-id="99eb2-155">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="99eb2-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99eb2-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="99eb2-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99eb2-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99eb2-157">-DefaultProfile</span></span>
<span data-ttu-id="99eb2-158">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99eb2-158">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99eb2-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99eb2-159">CommonParameters</span></span>
<span data-ttu-id="99eb2-160">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="99eb2-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99eb2-161">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99eb2-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99eb2-162">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="99eb2-162">INPUTS</span></span>

## <span data-ttu-id="99eb2-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99eb2-163">OUTPUTS</span></span>

### <span data-ttu-id="99eb2-164">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="99eb2-164">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="99eb2-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="99eb2-165">NOTES</span></span>

## <span data-ttu-id="99eb2-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99eb2-166">RELATED LINKS</span></span>

[<span data-ttu-id="99eb2-167">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="99eb2-167">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="99eb2-168">Új – AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="99eb2-168">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="99eb2-169">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="99eb2-169">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


