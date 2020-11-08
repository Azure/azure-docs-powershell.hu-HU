---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/update-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
ms.openlocfilehash: 944241dc7434646272c7149d81b380996e71db8f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186441"
---
# <span data-ttu-id="3670c-101">Update-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="3670c-101">Update-AzAppConfigurationStore</span></span>

## <span data-ttu-id="3670c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3670c-102">SYNOPSIS</span></span>
<span data-ttu-id="3670c-103">A megadott paraméterekkel frissíti a konfigurációs tárolót.</span><span class="sxs-lookup"><span data-stu-id="3670c-103">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="3670c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3670c-104">SYNTAX</span></span>

### <span data-ttu-id="3670c-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3670c-105">UpdateExpanded (Default)</span></span>
```
Update-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyIdentifier <String>] [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3670c-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3670c-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-EncryptionKeyIdentifier <String>]
 [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="3670c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3670c-107">DESCRIPTION</span></span>
<span data-ttu-id="3670c-108">A megadott paraméterekkel frissíti a konfigurációs tárolót.</span><span class="sxs-lookup"><span data-stu-id="3670c-108">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="3670c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3670c-109">EXAMPLES</span></span>

### <span data-ttu-id="3670c-110">1. példa: az App conifguration-tárolójának adattitkosításának engedélyezése rendszerszintű felügyelt identitással</span><span class="sxs-lookup"><span data-stu-id="3670c-110">Example 1: Enable data encryption of the app conifguration store by system-assigned managed identity</span></span>
```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName kv-Name -Name key-Name -Destination 'Software'
PS C:\> $systemAssignedAppStore = New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location $env.location -Sku 'standard' -IdentityType "SystemAssigned"
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName kv-Name -ObjectId $systemAssignedAppStore.IdentityPrincipalId -PermissionsToKeys get,unwrapKey,wrapKey -PassThru
PS C:\> Update-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -EncryptionKeyIdentifier $key.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="3670c-111">Ez a parancs az Azure Key Vault-ban tárolt kulccsal titkosítja az adattitkosítást egy rendszer által hozzárendelt felügyelt identitással.</span><span class="sxs-lookup"><span data-stu-id="3670c-111">This command enables data encryption by a key stored in Azure Key Vault using a system-assigned managed identity.</span></span>
<span data-ttu-id="3670c-112">A boltozatnak engedélyezve kell lennie a Soft-delete és a Purge-védelem beállításnak, és a felügyelt identitásnak meg kell felelnie a következő fontos engedélyeknek: Get, wrapKey, unwrapKey.</span><span class="sxs-lookup"><span data-stu-id="3670c-112">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="3670c-113">2. példa: az App conifguration-tárolójának adattitkosításának engedélyezése felhasználó által hozzárendelt felügyelt identitással</span><span class="sxs-lookup"><span data-stu-id="3670c-113">Example 2: Enable data encryption of the app conifguration store by user-assigned managed identity</span></span>
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

<span data-ttu-id="3670c-114">Ezzel a paranccsal az Azure Key Vault-ban tárolt kulccsal titkosíthatja az adattitkosítást egy felhasználó által hozzárendelt felügyelt identitás használatával.</span><span class="sxs-lookup"><span data-stu-id="3670c-114">This command enables data encryption by a key stored in Azure Key Vault using a user-assigned managed identity.</span></span>
<span data-ttu-id="3670c-115">A felhasználó által hozzárendelt identitást be kell állítani `-UserAssignedIdentity` .</span><span class="sxs-lookup"><span data-stu-id="3670c-115">The user-assigned identity must have been set with `-UserAssignedIdentity`.</span></span>
<span data-ttu-id="3670c-116">A boltozatnak engedélyezve kell lennie a Soft-delete és a Purge-védelem beállításnak, és a felügyelt identitásnak meg kell felelnie a következő fontos engedélyeknek: Get, wrapKey, unwrapKey.</span><span class="sxs-lookup"><span data-stu-id="3670c-116">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="3670c-117">3. példa: az App conifguration-tárolójának titkosításának letiltása.</span><span class="sxs-lookup"><span data-stu-id="3670c-117">Example 3: Disable encryption of an app conifguration store.</span></span>
```powershell
PS C:\> $appConf = Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -EncryptionKeyIdentifier $null

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="3670c-118">Ez a parancs letiltja az App conifguration-tárolójának titkosítását.</span><span class="sxs-lookup"><span data-stu-id="3670c-118">This command disables encryption of an app conifguration store.</span></span>

### <span data-ttu-id="3670c-119">3. példa: az conifguration-tároló (SKU) és a címkéje a csővezeték alapján.</span><span class="sxs-lookup"><span data-stu-id="3670c-119">Example 3: Update sku and tag of an app conifguration store by pipeline.</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -Sku 'standard' -Tag @{'key'='update'}

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="3670c-120">Ez a parancs a conifguration-tárolóban lévő app-tárolók SKU-és címkéjét frissíti.</span><span class="sxs-lookup"><span data-stu-id="3670c-120">This command updates sku and tag of an app conifguration store by pipeline.</span></span>

## <span data-ttu-id="3670c-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3670c-121">PARAMETERS</span></span>

### <span data-ttu-id="3670c-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3670c-122">-AsJob</span></span>
<span data-ttu-id="3670c-123">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="3670c-123">Run the command as a job</span></span>

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

### <span data-ttu-id="3670c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3670c-124">-DefaultProfile</span></span>
<span data-ttu-id="3670c-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3670c-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3670c-126">-EncryptionKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="3670c-126">-EncryptionKeyIdentifier</span></span>
<span data-ttu-id="3670c-127">Az adattitkosításhoz használt kulcskezelő kulcs URI-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3670c-127">The URI of the key vault key used to encrypt data.</span></span>

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

### <span data-ttu-id="3670c-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="3670c-128">-IdentityType</span></span>
<span data-ttu-id="3670c-129">A használt felügyelt identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="3670c-129">The type of managed identity used.</span></span>
<span data-ttu-id="3670c-130">Az "SystemAssignedAndUserAssigned" típus egy implicit módon létrehozott identitást és egy felhasználó által kiosztott identitást tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="3670c-130">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="3670c-131">A "nincs" típust eltávolítja a program az azonosítók közül.</span><span class="sxs-lookup"><span data-stu-id="3670c-131">The type 'None' will remove any identities.</span></span>

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

### <span data-ttu-id="3670c-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3670c-132">-InputObject</span></span>
<span data-ttu-id="3670c-133">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3670c-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3670c-134">-KeyVaultIdentityClientId</span><span class="sxs-lookup"><span data-stu-id="3670c-134">-KeyVaultIdentityClientId</span></span>
<span data-ttu-id="3670c-135">Annak az identitásnak az ügyfél azonosítója, amelyet a kulcsfájl eléréséhez használni fog.</span><span class="sxs-lookup"><span data-stu-id="3670c-135">The client id of the identity which will be used to access key vault.</span></span>

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

### <span data-ttu-id="3670c-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3670c-136">-Name</span></span>
<span data-ttu-id="3670c-137">A konfigurációs tároló neve.</span><span class="sxs-lookup"><span data-stu-id="3670c-137">The name of the configuration store.</span></span>

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

### <span data-ttu-id="3670c-138">-Várva</span><span class="sxs-lookup"><span data-stu-id="3670c-138">-NoWait</span></span>
<span data-ttu-id="3670c-139">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="3670c-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3670c-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3670c-140">-ResourceGroupName</span></span>
<span data-ttu-id="3670c-141">Annak az erőforráscsoportnek a neve, amelyhez a tároló beállításjegyzéke tartozik.</span><span class="sxs-lookup"><span data-stu-id="3670c-141">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="3670c-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="3670c-142">-Sku</span></span>
<span data-ttu-id="3670c-143">A konfigurációs tároló SKU-neve.</span><span class="sxs-lookup"><span data-stu-id="3670c-143">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="3670c-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3670c-144">-SubscriptionId</span></span>
<span data-ttu-id="3670c-145">A Microsoft Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3670c-145">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="3670c-146">-Címke</span><span class="sxs-lookup"><span data-stu-id="3670c-146">-Tag</span></span>
<span data-ttu-id="3670c-147">A kar erőforrás-címkéket.</span><span class="sxs-lookup"><span data-stu-id="3670c-147">The ARM resource tags.</span></span>

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

### <span data-ttu-id="3670c-148">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="3670c-148">-UserAssignedIdentity</span></span>
<span data-ttu-id="3670c-149">Az erőforráshoz társított felhasználó által hozzárendelt identitások listája.</span><span class="sxs-lookup"><span data-stu-id="3670c-149">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="3670c-150">A felhasználó által kiosztott identitás szótárai az űrlapon az "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}" típusú erőforrás-azonosítók lesznek.</span><span class="sxs-lookup"><span data-stu-id="3670c-150">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="3670c-151">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3670c-151">-Confirm</span></span>
<span data-ttu-id="3670c-152">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3670c-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3670c-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3670c-153">-WhatIf</span></span>
<span data-ttu-id="3670c-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3670c-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3670c-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3670c-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3670c-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3670c-156">CommonParameters</span></span>
<span data-ttu-id="3670c-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3670c-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3670c-158">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3670c-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3670c-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3670c-159">INPUTS</span></span>

### <span data-ttu-id="3670c-160">Microsoft. Azure. PowerShell. parancsmagok. AppConfiguration. models. IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="3670c-160">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="3670c-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3670c-161">OUTPUTS</span></span>

### <span data-ttu-id="3670c-162">Microsoft. Azure. PowerShell. parancsmagok. AppConfiguration. modellek. Api20200601. IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="3670c-162">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="3670c-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3670c-163">NOTES</span></span>

<span data-ttu-id="3670c-164">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="3670c-164">ALIASES</span></span>

<span data-ttu-id="3670c-165">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="3670c-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3670c-166">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="3670c-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3670c-167">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="3670c-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3670c-168">INPUTOBJECT <IAppConfigurationIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="3670c-168">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3670c-169">`[ConfigStoreName <String>]`: A konfigurációs tároló neve.</span><span class="sxs-lookup"><span data-stu-id="3670c-169">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="3670c-170">`[GroupName <String>]`: A magánjellegű kapcsolat erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="3670c-170">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="3670c-171">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="3670c-171">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3670c-172">`[PrivateEndpointConnectionName <String>]`: Privát végpont-kapcsolat neve</span><span class="sxs-lookup"><span data-stu-id="3670c-172">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="3670c-173">`[ResourceGroupName <String>]`: Annak az erőforráscsoport-csoportnak a neve, amelyhez a tároló beállításjegyzéke tartozik.</span><span class="sxs-lookup"><span data-stu-id="3670c-173">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="3670c-174">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3670c-174">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="3670c-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3670c-175">RELATED LINKS</span></span>



<span data-ttu-id="3670c-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0) 
 [Új – AzUserAssignedIdentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span><span class="sxs-lookup"><span data-stu-id="3670c-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0)
[New-AzUserAssignedIdentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span></span>

