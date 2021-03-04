---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/powershell/module/az.appconfiguration/update-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
ms.openlocfilehash: b8297580f088678f1fdd61b8bff670adb03d2bcf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925266"
---
# <span data-ttu-id="95833-101">Update-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="95833-101">Update-AzAppConfigurationStore</span></span>

## <span data-ttu-id="95833-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95833-102">SYNOPSIS</span></span>
<span data-ttu-id="95833-103">A megadott paraméterekkel frissíti a konfigurációs tárolót.</span><span class="sxs-lookup"><span data-stu-id="95833-103">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="95833-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="95833-104">SYNTAX</span></span>

### <span data-ttu-id="95833-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="95833-105">UpdateExpanded (Default)</span></span>
```
Update-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyIdentifier <String>] [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="95833-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="95833-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-EncryptionKeyIdentifier <String>]
 [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="95833-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="95833-107">DESCRIPTION</span></span>
<span data-ttu-id="95833-108">A megadott paraméterekkel frissíti a konfigurációs tárolót.</span><span class="sxs-lookup"><span data-stu-id="95833-108">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="95833-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="95833-109">EXAMPLES</span></span>

### <span data-ttu-id="95833-110">1. példa: Az appkonfigurációs tároló adattitkosításának engedélyezése rendszer által hozzárendelt felügyelt identitás alapján</span><span class="sxs-lookup"><span data-stu-id="95833-110">Example 1: Enable data encryption of the app configuration store by system-assigned managed identity</span></span>
```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName kv-Name -Name key-Name -Destination 'Software'
PS C:\> $systemAssignedAppStore = New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location $env.location -Sku 'standard' -IdentityType "SystemAssigned"
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName kv-Name -ObjectId $systemAssignedAppStore.IdentityPrincipalId -PermissionsToKeys get,unwrapKey,wrapKey -PassThru
PS C:\> Update-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -EncryptionKeyIdentifier $key.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="95833-111">Ez a parancs lehetővé teszi az Azure Key Vaultban tárolt kulcs adattitkosítását egy rendszer által hozzárendelt felügyelt identitás használatával.</span><span class="sxs-lookup"><span data-stu-id="95833-111">This command enables data encryption by a key stored in Azure Key Vault using a system-assigned managed identity.</span></span>
<span data-ttu-id="95833-112">A tárolónak engedélyeznie kell a szoftveres törlést és a végleges törlés elleni védelmet, és a felügyelt identitásnak rendelkeznie kell a következő kulcsengedélyekkel: get, wrapKey, unwrapKey.</span><span class="sxs-lookup"><span data-stu-id="95833-112">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="95833-113">2. példa: Az appkonfigurációs tároló adattitkosításának engedélyezése felhasználó által hozzárendelt felügyelt identitás alapján</span><span class="sxs-lookup"><span data-stu-id="95833-113">Example 2: Enable data encryption of the app configuration store by user-assigned managed identity</span></span>
```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName kv-Name -Name key-Name -Destination 'Software'
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location $env.location -Sku 'standard' -IdentityType "UserAssigned" -UserAssignedIdentity $assignedIdentity.Id
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName kv-Name -ObjectId $assignedIdentity.PrincipalId -PermissionsToKeys get,unwrapKey,wrapKey -PassThru
PS C:\> Update-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test11 -EncryptionKeyIdentifier $key.Id -KeyVaultIdentityClientId $assignedIdentity.ClientId

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="95833-114">Ez a parancs lehetővé teszi az Azure Key Vaultban tárolt kulcs adattitkosítását egy felhasználó által hozzárendelt felügyelt identitás használatával.</span><span class="sxs-lookup"><span data-stu-id="95833-114">This command enables data encryption by a key stored in Azure Key Vault using a user-assigned managed identity.</span></span>
<span data-ttu-id="95833-115">A felhasználó által hozzárendelt identitásnak a következővel kell lennie `-UserAssignedIdentity` beállítva: .</span><span class="sxs-lookup"><span data-stu-id="95833-115">The user-assigned identity must have been set with `-UserAssignedIdentity`.</span></span>
<span data-ttu-id="95833-116">A tárolónak engedélyeznie kell a szoftveres törlést és a végleges törlés elleni védelmet, és a felügyelt identitásnak rendelkeznie kell a következő kulcsengedélyekkel: get, wrapKey, unwrapKey.</span><span class="sxs-lookup"><span data-stu-id="95833-116">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="95833-117">3. példa: Az appkonfigurációs áruház titkosításának letiltása.</span><span class="sxs-lookup"><span data-stu-id="95833-117">Example 3: Disable encryption of an app configuration store.</span></span>
```powershell
PS C:\> $appConf = Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -EncryptionKeyIdentifier $null

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="95833-118">Ez a parancs letiltja az alkalmazáskonfigurációs áruház titkosítását.</span><span class="sxs-lookup"><span data-stu-id="95833-118">This command disables encryption of an app configuration store.</span></span>

### <span data-ttu-id="95833-119">3. példa: Egy alkalmazáskonfigurációs áruház termékváltozatának és címkéjának frissítése folyamat szerint.</span><span class="sxs-lookup"><span data-stu-id="95833-119">Example 3: Update sku and tag of an app configuration store by pipeline.</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -Sku 'standard' -Tag @{'key'='update'}

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="95833-120">Ez a parancs folyamat szerint frissíti az appkonfigurációs áruház termékváltozatát és címkéit.</span><span class="sxs-lookup"><span data-stu-id="95833-120">This command updates sku and tag of an app configuration store by pipeline.</span></span>

## <span data-ttu-id="95833-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95833-121">PARAMETERS</span></span>

### <span data-ttu-id="95833-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95833-122">-AsJob</span></span>
<span data-ttu-id="95833-123">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="95833-123">Run the command as a job</span></span>

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

### <span data-ttu-id="95833-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95833-124">-DefaultProfile</span></span>
<span data-ttu-id="95833-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="95833-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95833-126">-EncryptionKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="95833-126">-EncryptionKeyIdentifier</span></span>
<span data-ttu-id="95833-127">Az adatok titkosításához használt kulcstárkulcs URI-ja.</span><span class="sxs-lookup"><span data-stu-id="95833-127">The URI of the key vault key used to encrypt data.</span></span>

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

### <span data-ttu-id="95833-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="95833-128">-IdentityType</span></span>
<span data-ttu-id="95833-129">A használt felügyelt identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="95833-129">The type of managed identity used.</span></span>
<span data-ttu-id="95833-130">A "SystemAssignedAndUserAssigned" típus magában foglal egy implicit módon létrehozott identitást és egy felhasználóhoz rendelt identitások készletét.</span><span class="sxs-lookup"><span data-stu-id="95833-130">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="95833-131">A "Nincs" típus eltávolítja az identitásokat.</span><span class="sxs-lookup"><span data-stu-id="95833-131">The type 'None' will remove any identities.</span></span>

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

### <span data-ttu-id="95833-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95833-132">-InputObject</span></span>
<span data-ttu-id="95833-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="95833-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95833-134">-KeyVaultIdentityClientId</span><span class="sxs-lookup"><span data-stu-id="95833-134">-KeyVaultIdentityClientId</span></span>
<span data-ttu-id="95833-135">A kulcstár eléréséhez használt identitás ügyfél-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="95833-135">The client id of the identity which will be used to access key vault.</span></span>

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

### <span data-ttu-id="95833-136">-Name</span><span class="sxs-lookup"><span data-stu-id="95833-136">-Name</span></span>
<span data-ttu-id="95833-137">A konfigurációs tároló neve.</span><span class="sxs-lookup"><span data-stu-id="95833-137">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95833-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="95833-138">-NoWait</span></span>
<span data-ttu-id="95833-139">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="95833-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="95833-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95833-140">-ResourceGroupName</span></span>
<span data-ttu-id="95833-141">Annak az erőforráscsoportnak a neve, amelyhez a tároló beállításjegyzék tartozik.</span><span class="sxs-lookup"><span data-stu-id="95833-141">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95833-142">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="95833-142">-Sku</span></span>
<span data-ttu-id="95833-143">A konfigurációs tároló termékváltozatának neve.</span><span class="sxs-lookup"><span data-stu-id="95833-143">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="95833-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="95833-144">-SubscriptionId</span></span>
<span data-ttu-id="95833-145">A Microsoft Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="95833-145">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95833-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="95833-146">-Tag</span></span>
<span data-ttu-id="95833-147">A ARM erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="95833-147">The ARM resource tags.</span></span>

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

### <span data-ttu-id="95833-148">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="95833-148">-UserAssignedIdentity</span></span>
<span data-ttu-id="95833-149">Az erőforráshoz társított, felhasználóhoz rendelt identitások listája.</span><span class="sxs-lookup"><span data-stu-id="95833-149">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="95833-150">A felhasználó által hozzárendelt identitásszótárkulcsok ARM következő űrlapon található erőforrás-azonosítók lesznek: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span><span class="sxs-lookup"><span data-stu-id="95833-150">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="95833-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95833-151">-Confirm</span></span>
<span data-ttu-id="95833-152">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="95833-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95833-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95833-153">-WhatIf</span></span>
<span data-ttu-id="95833-154">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="95833-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95833-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="95833-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95833-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95833-156">CommonParameters</span></span>
<span data-ttu-id="95833-157">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95833-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95833-158">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95833-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95833-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="95833-159">INPUTS</span></span>

### <span data-ttu-id="95833-160">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="95833-160">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="95833-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="95833-161">OUTPUTS</span></span>

### <span data-ttu-id="95833-162">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="95833-162">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="95833-163">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="95833-163">NOTES</span></span>

<span data-ttu-id="95833-164">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="95833-164">ALIASES</span></span>

<span data-ttu-id="95833-165">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="95833-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="95833-166">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="95833-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="95833-167">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="95833-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="95833-168">INPUTOBJECT: <IAppConfigurationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="95833-168">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="95833-169">`[ConfigStoreName <String>]`: A konfigurációs tároló neve.</span><span class="sxs-lookup"><span data-stu-id="95833-169">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="95833-170">`[GroupName <String>]`: A privát csatolású erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="95833-170">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="95833-171">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="95833-171">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="95833-172">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span><span class="sxs-lookup"><span data-stu-id="95833-172">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="95833-173">`[ResourceGroupName <String>]`: Annak az erőforráscsoportnak a neve, amelyhez a tároló beállításjegyzék tartozik.</span><span class="sxs-lookup"><span data-stu-id="95833-173">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="95833-174">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="95833-174">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="95833-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="95833-175">RELATED LINKS</span></span>



<span data-ttu-id="95833-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0) 
 [New-AzUserAssignedIdentity](https://docs.microsoft.com/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span><span class="sxs-lookup"><span data-stu-id="95833-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0)
[New-AzUserAssignedIdentity](https://docs.microsoft.com/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span></span>

