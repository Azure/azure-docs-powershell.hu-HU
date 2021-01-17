---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
ms.openlocfilehash: 20f3985553a3fc7a993480bdf154a7f8e6776bf6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381484"
---
# <span data-ttu-id="19c44-101">New-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="19c44-101">New-AzAppConfigurationStore</span></span>

## <span data-ttu-id="19c44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19c44-102">SYNOPSIS</span></span>
<span data-ttu-id="19c44-103">Létrehoz egy konfigurációs tárolót a megadott paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="19c44-103">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="19c44-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="19c44-104">SYNTAX</span></span>

```
New-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> -Location <String> -Sku <String>
 [-SubscriptionId <String>] [-IdentityType <IdentityType>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="19c44-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="19c44-105">DESCRIPTION</span></span>
<span data-ttu-id="19c44-106">Létrehoz egy konfigurációs tárolót a megadott paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="19c44-106">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="19c44-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="19c44-107">EXAMPLES</span></span>

### <span data-ttu-id="19c44-108">1. példa: Alkalmazáskonfigurációs áruház létrehozása</span><span class="sxs-lookup"><span data-stu-id="19c44-108">Example 1: Create an app configuration store</span></span>
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku free

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="19c44-109">Ez a parancs létrehoz egy alkalmazáskonfigurációs áruházat.</span><span class="sxs-lookup"><span data-stu-id="19c44-109">This command creates an app configuration store.</span></span>

### <span data-ttu-id="19c44-110">2. példa: Appkonfiguráció létrehozása a "UserAssigned" IdentityType-val</span><span class="sxs-lookup"><span data-stu-id="19c44-110">Example 2: Create an app configuration with the IdentityType set to "UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="19c44-111">Ez a parancs létrehoz egy appkonfigurációt, és hozzárendel hozzá egy felhasználó által hozzárendelt felügyelt identitást.</span><span class="sxs-lookup"><span data-stu-id="19c44-111">This command creates an app configuration and assign a user-assigned managed identity to it.</span></span>
<span data-ttu-id="19c44-112">A cmk (cusomer managed key) engedélyezéséhez kövesse az alábbi `Update-AzAppConfigurationStore` lépéseket.</span><span class="sxs-lookup"><span data-stu-id="19c44-112">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="19c44-113">3. példa: Alkalmazáskonfiguráció létrehozása a "SystemAssigned" IdentityType-val</span><span class="sxs-lookup"><span data-stu-id="19c44-113">Example 3: Create an app configuration with the IdentityType set to "SystemAssigned"</span></span> 
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned"

Location Name             Type
-------- ----             ----
eastus   appconfig-test11 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="19c44-114">Ez a parancs létrehoz egy appkonfigurációt, és engedélyezi az erőforráshoz társított, rendszerhez rendelt felügyelt identitást.</span><span class="sxs-lookup"><span data-stu-id="19c44-114">This command creates an app configuration and enables the system-assigned managed identity associated with the resource.</span></span>
<span data-ttu-id="19c44-115">A cmk (cusomer managed key) engedélyezéséhez kövesse az alábbi `Update-AzAppConfigurationStore` lépéseket.</span><span class="sxs-lookup"><span data-stu-id="19c44-115">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="19c44-116">4. példa: Appkonfiguráció létrehozása úgy, hogy az IdentityType beállítása "SystemAssigned, UserAssigned"</span><span class="sxs-lookup"><span data-stu-id="19c44-116">Example 4: Create an app configuration with the IdentityType set to "SystemAssigned, UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned, UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="19c44-117">Engedélyezheti a rendszer által hozzárendelt felügyelt identitást, és egyidejűleg adhat felhasználói identitásokat is.</span><span class="sxs-lookup"><span data-stu-id="19c44-117">You can enable system-assigned managed identity and give user-assigned identities at the same time.</span></span>
<span data-ttu-id="19c44-118">A cmk (cusomer managed key) engedélyezéséhez kövesse az alábbi `Update-AzAppConfigurationStore` lépéseket.</span><span class="sxs-lookup"><span data-stu-id="19c44-118">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

## <span data-ttu-id="19c44-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19c44-119">PARAMETERS</span></span>

### <span data-ttu-id="19c44-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19c44-120">-AsJob</span></span>
<span data-ttu-id="19c44-121">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="19c44-121">Run the command as a job</span></span>

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

### <span data-ttu-id="19c44-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19c44-122">-DefaultProfile</span></span>
<span data-ttu-id="19c44-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19c44-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c44-124">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="19c44-124">-IdentityType</span></span>
<span data-ttu-id="19c44-125">A használt felügyelt identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="19c44-125">The type of managed identity used.</span></span>
<span data-ttu-id="19c44-126">A "SystemAssignedAndUserAssigned" típus magában foglal egy implicit módon létrehozott identitást és egy felhasználóhoz rendelt identitások készletét.</span><span class="sxs-lookup"><span data-stu-id="19c44-126">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="19c44-127">A "Nincs" típus eltávolítja az identitásokat.</span><span class="sxs-lookup"><span data-stu-id="19c44-127">The type 'None' will remove any identities.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Support.IdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c44-128">-Location</span><span class="sxs-lookup"><span data-stu-id="19c44-128">-Location</span></span>
<span data-ttu-id="19c44-129">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="19c44-129">The location of the resource.</span></span>
<span data-ttu-id="19c44-130">Ez az erőforrás létrehozása után nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="19c44-130">This cannot be changed after the resource is created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c44-131">-Name</span><span class="sxs-lookup"><span data-stu-id="19c44-131">-Name</span></span>
<span data-ttu-id="19c44-132">A konfigurációs tároló neve.</span><span class="sxs-lookup"><span data-stu-id="19c44-132">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c44-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="19c44-133">-NoWait</span></span>
<span data-ttu-id="19c44-134">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="19c44-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="19c44-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19c44-135">-ResourceGroupName</span></span>
<span data-ttu-id="19c44-136">Annak az erőforráscsoportnak a neve, amelyhez a tároló beállításjegyzék tartozik.</span><span class="sxs-lookup"><span data-stu-id="19c44-136">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c44-137">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="19c44-137">-Sku</span></span>
<span data-ttu-id="19c44-138">A konfigurációs tároló termékváltozatának neve.</span><span class="sxs-lookup"><span data-stu-id="19c44-138">The SKU name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c44-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="19c44-139">-SubscriptionId</span></span>
<span data-ttu-id="19c44-140">A Microsoft Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="19c44-140">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c44-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="19c44-141">-Tag</span></span>
<span data-ttu-id="19c44-142">Az erőforrás címkéi.</span><span class="sxs-lookup"><span data-stu-id="19c44-142">The tags of the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c44-143">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="19c44-143">-UserAssignedIdentity</span></span>
<span data-ttu-id="19c44-144">Az erőforráshoz társított, felhasználóhoz rendelt identitások listája.</span><span class="sxs-lookup"><span data-stu-id="19c44-144">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="19c44-145">A felhasználó által hozzárendelt identitásszótárkulcsok ARM következő űrlapon található erőforrás-azonosítók lesznek: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span><span class="sxs-lookup"><span data-stu-id="19c44-145">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c44-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19c44-146">-Confirm</span></span>
<span data-ttu-id="19c44-147">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="19c44-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c44-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19c44-148">-WhatIf</span></span>
<span data-ttu-id="19c44-149">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="19c44-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19c44-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="19c44-150">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c44-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19c44-151">CommonParameters</span></span>
<span data-ttu-id="19c44-152">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19c44-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19c44-153">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19c44-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19c44-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19c44-154">INPUTS</span></span>

## <span data-ttu-id="19c44-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19c44-155">OUTPUTS</span></span>

### <span data-ttu-id="19c44-156">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="19c44-156">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="19c44-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="19c44-157">NOTES</span></span>

<span data-ttu-id="19c44-158">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="19c44-158">ALIASES</span></span>

## <span data-ttu-id="19c44-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19c44-159">RELATED LINKS</span></span>



[<span data-ttu-id="19c44-160">New-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="19c44-160">New-AzUserAssignedIdentity</span></span>](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)

