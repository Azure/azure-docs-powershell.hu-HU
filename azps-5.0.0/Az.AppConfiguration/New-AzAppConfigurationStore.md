---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
ms.openlocfilehash: 20f3985553a3fc7a993480bdf154a7f8e6776bf6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186449"
---
# <span data-ttu-id="0f297-101">New-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="0f297-101">New-AzAppConfigurationStore</span></span>

## <span data-ttu-id="0f297-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0f297-102">SYNOPSIS</span></span>
<span data-ttu-id="0f297-103">A megadott paramétereket tartalmazó konfigurációs tárolót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0f297-103">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="0f297-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0f297-104">SYNTAX</span></span>

```
New-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> -Location <String> -Sku <String>
 [-SubscriptionId <String>] [-IdentityType <IdentityType>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="0f297-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0f297-105">DESCRIPTION</span></span>
<span data-ttu-id="0f297-106">A megadott paramétereket tartalmazó konfigurációs tárolót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0f297-106">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="0f297-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0f297-107">EXAMPLES</span></span>

### <span data-ttu-id="0f297-108">1. példa: alkalmazás-konfigurációs tároló létrehozása</span><span class="sxs-lookup"><span data-stu-id="0f297-108">Example 1: Create an app configuration store</span></span>
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku free

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="0f297-109">Ezzel a paranccsal létrehozhatja az App Configuration Store áruházát.</span><span class="sxs-lookup"><span data-stu-id="0f297-109">This command creates an app configuration store.</span></span>

### <span data-ttu-id="0f297-110">2. példa: app-konfiguráció létrehozása a IdentityType "UserAssigned" beállítással</span><span class="sxs-lookup"><span data-stu-id="0f297-110">Example 2: Create an app configuration with the IdentityType set to "UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="0f297-111">Ez a parancs létrehoz egy app-konfigurációt, és hozzárendelt egy felhasználó által hozzárendelt felügyelt identitást.</span><span class="sxs-lookup"><span data-stu-id="0f297-111">This command creates an app configuration and assign a user-assigned managed identity to it.</span></span>
<span data-ttu-id="0f297-112">Az `Update-AzAppConfigurationStore` alábbi lépésekből megtudhatja, hogy miként engedélyezheti a CMK (cusomer felügyelt kulcsát).</span><span class="sxs-lookup"><span data-stu-id="0f297-112">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="0f297-113">3. példa: app-konfiguráció létrehozása a IdentityType "SystemAssigned" értékre</span><span class="sxs-lookup"><span data-stu-id="0f297-113">Example 3: Create an app configuration with the IdentityType set to "SystemAssigned"</span></span> 
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned"

Location Name             Type
-------- ----             ----
eastus   appconfig-test11 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="0f297-114">Ez a parancs egy app-konfigurációt hoz létre, és lehetővé teszi az erőforráshoz társított rendszerhez rendelt felügyelt identitást.</span><span class="sxs-lookup"><span data-stu-id="0f297-114">This command creates an app configuration and enables the system-assigned managed identity associated with the resource.</span></span>
<span data-ttu-id="0f297-115">Az `Update-AzAppConfigurationStore` alábbi lépésekből megtudhatja, hogy miként engedélyezheti a CMK (cusomer felügyelt kulcsát).</span><span class="sxs-lookup"><span data-stu-id="0f297-115">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="0f297-116">Példa 4: app-konfiguráció létrehozása a IdentityType "SystemAssigned, UserAssigned" értékre</span><span class="sxs-lookup"><span data-stu-id="0f297-116">Example 4: Create an app configuration with the IdentityType set to "SystemAssigned, UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned, UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="0f297-117">Engedélyezheti a rendszer által hozzárendelt felügyelt identitást, és egy időben felhasználó által kiosztott identitást adhat.</span><span class="sxs-lookup"><span data-stu-id="0f297-117">You can enable system-assigned managed identity and give user-assigned identities at the same time.</span></span>
<span data-ttu-id="0f297-118">Az `Update-AzAppConfigurationStore` alábbi lépésekből megtudhatja, hogy miként engedélyezheti a CMK (cusomer felügyelt kulcsát).</span><span class="sxs-lookup"><span data-stu-id="0f297-118">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

## <span data-ttu-id="0f297-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0f297-119">PARAMETERS</span></span>

### <span data-ttu-id="0f297-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f297-120">-AsJob</span></span>
<span data-ttu-id="0f297-121">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="0f297-121">Run the command as a job</span></span>

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

### <span data-ttu-id="0f297-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f297-122">-DefaultProfile</span></span>
<span data-ttu-id="0f297-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0f297-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f297-124">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="0f297-124">-IdentityType</span></span>
<span data-ttu-id="0f297-125">A használt felügyelt identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="0f297-125">The type of managed identity used.</span></span>
<span data-ttu-id="0f297-126">Az "SystemAssignedAndUserAssigned" típus egy implicit módon létrehozott identitást és egy felhasználó által kiosztott identitást tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="0f297-126">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="0f297-127">A "nincs" típust eltávolítja a program az azonosítók közül.</span><span class="sxs-lookup"><span data-stu-id="0f297-127">The type 'None' will remove any identities.</span></span>

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

### <span data-ttu-id="0f297-128">-Hely</span><span class="sxs-lookup"><span data-stu-id="0f297-128">-Location</span></span>
<span data-ttu-id="0f297-129">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="0f297-129">The location of the resource.</span></span>
<span data-ttu-id="0f297-130">Ez a beállítás nem módosítható az erőforrás létrehozása után.</span><span class="sxs-lookup"><span data-stu-id="0f297-130">This cannot be changed after the resource is created.</span></span>

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

### <span data-ttu-id="0f297-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0f297-131">-Name</span></span>
<span data-ttu-id="0f297-132">A konfigurációs tároló neve.</span><span class="sxs-lookup"><span data-stu-id="0f297-132">The name of the configuration store.</span></span>

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

### <span data-ttu-id="0f297-133">-Várva</span><span class="sxs-lookup"><span data-stu-id="0f297-133">-NoWait</span></span>
<span data-ttu-id="0f297-134">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="0f297-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0f297-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f297-135">-ResourceGroupName</span></span>
<span data-ttu-id="0f297-136">Annak az erőforráscsoportnek a neve, amelyhez a tároló beállításjegyzéke tartozik.</span><span class="sxs-lookup"><span data-stu-id="0f297-136">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="0f297-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="0f297-137">-Sku</span></span>
<span data-ttu-id="0f297-138">A konfigurációs tároló SKU-neve.</span><span class="sxs-lookup"><span data-stu-id="0f297-138">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="0f297-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0f297-139">-SubscriptionId</span></span>
<span data-ttu-id="0f297-140">A Microsoft Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0f297-140">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="0f297-141">-Címke</span><span class="sxs-lookup"><span data-stu-id="0f297-141">-Tag</span></span>
<span data-ttu-id="0f297-142">Az erőforrás címkéi.</span><span class="sxs-lookup"><span data-stu-id="0f297-142">The tags of the resource.</span></span>

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

### <span data-ttu-id="0f297-143">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="0f297-143">-UserAssignedIdentity</span></span>
<span data-ttu-id="0f297-144">Az erőforráshoz társított felhasználó által hozzárendelt identitások listája.</span><span class="sxs-lookup"><span data-stu-id="0f297-144">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="0f297-145">A felhasználó által kiosztott identitás szótárai az űrlapon az "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}" típusú erőforrás-azonosítók lesznek.</span><span class="sxs-lookup"><span data-stu-id="0f297-145">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="0f297-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0f297-146">-Confirm</span></span>
<span data-ttu-id="0f297-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0f297-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f297-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f297-148">-WhatIf</span></span>
<span data-ttu-id="0f297-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0f297-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f297-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0f297-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f297-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f297-151">CommonParameters</span></span>
<span data-ttu-id="0f297-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0f297-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f297-153">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0f297-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f297-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f297-154">INPUTS</span></span>

## <span data-ttu-id="0f297-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f297-155">OUTPUTS</span></span>

### <span data-ttu-id="0f297-156">Microsoft. Azure. PowerShell. parancsmagok. AppConfiguration. modellek. Api20200601. IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="0f297-156">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="0f297-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0f297-157">NOTES</span></span>

<span data-ttu-id="0f297-158">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="0f297-158">ALIASES</span></span>

## <span data-ttu-id="0f297-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f297-159">RELATED LINKS</span></span>



[<span data-ttu-id="0f297-160">Új – AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="0f297-160">New-AzUserAssignedIdentity</span></span>](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)

