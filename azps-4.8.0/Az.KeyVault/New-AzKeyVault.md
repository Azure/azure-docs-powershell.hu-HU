---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: a11e962e2af6beaa3f3004cec104530f7603bb3a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181736"
---
# <span data-ttu-id="d22ea-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="d22ea-101">New-AzKeyVault</span></span>

## <span data-ttu-id="d22ea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d22ea-102">SYNOPSIS</span></span>
<span data-ttu-id="d22ea-103">Egy fő boltozatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d22ea-103">Creates a key vault.</span></span>

## <span data-ttu-id="d22ea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d22ea-104">SYNTAX</span></span>

```
New-AzKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-DisableSoftDelete] [-EnablePurgeProtection]
 [-EnableRbacAuthorization] [-SoftDeleteRetentionInDays <Int32>] [-Sku <SkuName>] [-Tag <Hashtable>]
 [-NetworkRuleSet <PSKeyVaultNetworkRuleSet>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d22ea-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d22ea-105">DESCRIPTION</span></span>
<span data-ttu-id="d22ea-106">A **New-AzKeyVault** parancsmag létrehoz egy fő boltozatot a megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="d22ea-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="d22ea-107">Ez a parancsmag az aktuálisan bejelentkezett felhasználó engedélyeit is feljogosítja a kulcsfájl hozzáadására, eltávolítására, illetve a kulcsok és a titok megadására.</span><span class="sxs-lookup"><span data-stu-id="d22ea-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>
<span data-ttu-id="d22ea-108">Megjegyzés: Ha a hiba megjelenik, **az előfizetéshez nincs regisztrálva a "Microsoft. kulcskezelő" névtér használata** az új kulcsfájl létrehozásakor, futtassa a **Register-AzResourceProvider-ProviderNamespace "Microsoft. kulcskezelő"** parancsot, majd futtassa újra a **New-AzKeyVault** parancsot.</span><span class="sxs-lookup"><span data-stu-id="d22ea-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="d22ea-109">További információt a Register-AzResourceProvider című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d22ea-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="d22ea-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d22ea-110">EXAMPLES</span></span>

### <span data-ttu-id="d22ea-111">Példa 1: normál kulcsú boltozat létrehozása</span><span class="sxs-lookup"><span data-stu-id="d22ea-111">Example 1: Create a Standard key vault</span></span>
```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'

Vault Name                       : contoso03vault
Resource Group Name              : group14
Location                         : East US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/group14/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore

Tags                             :
```

<span data-ttu-id="d22ea-112">Ez a parancs létrehoz egy Contoso03Vault nevű kulcs boltozatot az Azure régióban, a Kelet-Amerikai Egyesült Államokban.</span><span class="sxs-lookup"><span data-stu-id="d22ea-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="d22ea-113">A parancs hozzáadja a fő boltozatot a Group14 nevű erőforráscsoport csoportjához.</span><span class="sxs-lookup"><span data-stu-id="d22ea-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="d22ea-114">Mivel a parancs nem ad meg értéket a *SKU* paraméterhez, létrehoz egy standard kulcs boltozatot.</span><span class="sxs-lookup"><span data-stu-id="d22ea-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="d22ea-115">2. példa: prémium kulcsú boltozat létrehozása</span><span class="sxs-lookup"><span data-stu-id="d22ea-115">Example 2: Create a Premium key vault</span></span>
```powershell
PS C:\>New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'

Vault Name                       : contoso03vault
Resource Group Name              : group14
Location                         : East US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/group14/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Premium
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore

Tags                             :
```

<span data-ttu-id="d22ea-116">Ez a parancs az előző példához hasonlóan létrehoz egy fő boltozatot.</span><span class="sxs-lookup"><span data-stu-id="d22ea-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="d22ea-117">A prémium kulcsú boltozatot azonban a *SKU* paraméterhez tartozó prémium értékkel adja meg.</span><span class="sxs-lookup"><span data-stu-id="d22ea-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

### <span data-ttu-id="d22ea-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="d22ea-118">Example 3</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="d22ea-119">A kulcsfájl létrehozása és a hálózati szabályok megadása, amelyek lehetővé teszik a megadott IP-cím elérését az $myNetworkResId által azonosított virtuális hálózatból.</span><span class="sxs-lookup"><span data-stu-id="d22ea-119">Creating a key vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span> <span data-ttu-id="d22ea-120">`New-AzKeyVaultNetworkRuleSetObject`További információt itt talál.</span><span class="sxs-lookup"><span data-stu-id="d22ea-120">See `New-AzKeyVaultNetworkRuleSetObject` for more information.</span></span>

## <span data-ttu-id="d22ea-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d22ea-121">PARAMETERS</span></span>

### <span data-ttu-id="d22ea-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d22ea-122">-DefaultProfile</span></span>
<span data-ttu-id="d22ea-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d22ea-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d22ea-124">-DisableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="d22ea-124">-DisableSoftDelete</span></span>
<span data-ttu-id="d22ea-125">Ha meg van adva, akkor a "puha Törlés" funkció le van tiltva ehhez a kulcs boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="d22ea-125">If specified, 'soft delete' functionality is disabled for this key vault.</span></span>

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

### <span data-ttu-id="d22ea-126">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="d22ea-126">-EnabledForDeployment</span></span>
<span data-ttu-id="d22ea-127">A Microsoft. számítási erőforrás-szolgáltatója kinyerheti a titkokat ebből a kulcsfájlból, ha ez a kulcs boltozata az erőforrás létrehozásakor, például virtuális gép létrehozásakor jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="d22ea-127">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d22ea-128">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="d22ea-128">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="d22ea-129">Lehetővé teszi, hogy az Azure Disk Encryption szolgáltatás a kulcsok kijavítását és kicsomagolását a kulcsból.</span><span class="sxs-lookup"><span data-stu-id="d22ea-129">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d22ea-130">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="d22ea-130">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="d22ea-131">Lehetővé teszi az Azure Resource Manager számára, hogy ebből a kulcsfájlból kiírja a titkot, ha ezt a kulcspárt a sablonok központi telepítéséhez hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="d22ea-131">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d22ea-132">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="d22ea-132">-EnablePurgeProtection</span></span>
<span data-ttu-id="d22ea-133">Ha meg van adva, az azonnali törlés elleni védelem engedélyezve van ehhez a boltozathoz; szükség esetén a finom törlést is engedélyezni kell.</span><span class="sxs-lookup"><span data-stu-id="d22ea-133">If specified, protection against immediate deletion is enabled for this vault; requires soft delete to be enabled as well.</span></span>

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

### <span data-ttu-id="d22ea-134">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="d22ea-134">-EnableRbacAuthorization</span></span>
<span data-ttu-id="d22ea-135">Ha meg van adva, engedélyezze az adatműveletek engedélyezését szerepköralapú hozzáférés-vezérlés (RBAC) szerint, majd a boltozat tulajdonságai párbeszédpanelen megadott hozzáférési házirendek figyelmen kívül maradnak.</span><span class="sxs-lookup"><span data-stu-id="d22ea-135">If specified, enables to authorize data actions by Role Based Access Control (RBAC), and then the access policies specified in vault properties will be ignored.</span></span> <span data-ttu-id="d22ea-136">Felhívjuk a figyelmét arra, hogy a RBAC-ban mindig engedélyezve vannak a kezelési műveletek.</span><span class="sxs-lookup"><span data-stu-id="d22ea-136">Note that management actions are always authorized with RBAC.</span></span>

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

### <span data-ttu-id="d22ea-137">-Hely</span><span class="sxs-lookup"><span data-stu-id="d22ea-137">-Location</span></span>
<span data-ttu-id="d22ea-138">Azt az Azure-területet adja meg, amelyben a fő pince hozható létre.</span><span class="sxs-lookup"><span data-stu-id="d22ea-138">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="d22ea-139">Használja a [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) parancsot a lehetőségek megjelenítéséhez.</span><span class="sxs-lookup"><span data-stu-id="d22ea-139">Use the command [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) to see your choices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d22ea-140">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d22ea-140">-Name</span></span>
<span data-ttu-id="d22ea-141">A létrehozandó fő pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d22ea-141">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="d22ea-142">A név lehet betűk, számjegyek és kötőjelek tetszőleges kombinációja.</span><span class="sxs-lookup"><span data-stu-id="d22ea-142">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="d22ea-143">A névnek betűvel vagy számmal kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="d22ea-143">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="d22ea-144">A névnek univerzálisan egyedinek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="d22ea-144">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VaultName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d22ea-145">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d22ea-145">-NetworkRuleSet</span></span>
<span data-ttu-id="d22ea-146">A boltozat hálózati szabályát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d22ea-146">Specifies the network rule set of the vault.</span></span> <span data-ttu-id="d22ea-147">Az adott hálózati helyekről a fő boltozat kisegítő lehetőségeit szabályozza.</span><span class="sxs-lookup"><span data-stu-id="d22ea-147">It governs the accessibility of the key vault from specific network locations.</span></span> <span data-ttu-id="d22ea-148">Létrehozta `New-AzKeyVaultNetworkRuleSetObject` .</span><span class="sxs-lookup"><span data-stu-id="d22ea-148">Created by `New-AzKeyVaultNetworkRuleSetObject`.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22ea-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d22ea-149">-ResourceGroupName</span></span>
<span data-ttu-id="d22ea-150">Annak a meglévő erőforrás-csoportnak a nevét adja meg, amelybe a kulcs boltozatát létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="d22ea-150">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d22ea-151">-SKU</span><span class="sxs-lookup"><span data-stu-id="d22ea-151">-Sku</span></span>
<span data-ttu-id="d22ea-152">A fő boltozat-példány SKU-ának meghatározása.</span><span class="sxs-lookup"><span data-stu-id="d22ea-152">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="d22ea-153">Ha tudni kívánja, hogy mely funkciók érhetők el az egyes SKU-hoz, olvassa el az Azure Key Vault árképzési webhelye című témakört https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="d22ea-153">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

```yaml
Type: Microsoft.Azure.Management.KeyVault.Models.SkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d22ea-154">-SoftDeleteRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="d22ea-154">-SoftDeleteRetentionInDays</span></span>
<span data-ttu-id="d22ea-155">Itt adhatja meg, hogy a törölt erőforrások mennyi ideig maradnak, és mennyi ideig maradjon, amíg el nem távolítható egy boltozat vagy objektum a törölt állapotban.</span><span class="sxs-lookup"><span data-stu-id="d22ea-155">Specifies how long deleted resources are retained, and how long until a vault or an object in the deleted state can be purged.</span></span> <span data-ttu-id="d22ea-156">Az alapértelmezett érték 90 nap.</span><span class="sxs-lookup"><span data-stu-id="d22ea-156">The default is 90 days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22ea-157">-Címke</span><span class="sxs-lookup"><span data-stu-id="d22ea-157">-Tag</span></span>
<span data-ttu-id="d22ea-158">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="d22ea-158">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d22ea-159">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="d22ea-159">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d22ea-160">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d22ea-160">-Confirm</span></span>
<span data-ttu-id="d22ea-161">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d22ea-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d22ea-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d22ea-162">-WhatIf</span></span>
<span data-ttu-id="d22ea-163">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d22ea-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d22ea-164">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d22ea-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d22ea-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d22ea-165">CommonParameters</span></span>
<span data-ttu-id="d22ea-166">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d22ea-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d22ea-167">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d22ea-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d22ea-168">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d22ea-168">INPUTS</span></span>

### <span data-ttu-id="d22ea-169">System. String</span><span class="sxs-lookup"><span data-stu-id="d22ea-169">System.String</span></span>

### <span data-ttu-id="d22ea-170">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d22ea-170">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="d22ea-171">Microsoft. Azure. Management. kulcskezelő. models. SkuName</span><span class="sxs-lookup"><span data-stu-id="d22ea-171">Microsoft.Azure.Management.KeyVault.Models.SkuName</span></span>

### <span data-ttu-id="d22ea-172">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d22ea-172">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d22ea-173">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d22ea-173">OUTPUTS</span></span>

### <span data-ttu-id="d22ea-174">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="d22ea-174">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="d22ea-175">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d22ea-175">NOTES</span></span>

## <span data-ttu-id="d22ea-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d22ea-176">RELATED LINKS</span></span>

[<span data-ttu-id="d22ea-177">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="d22ea-177">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="d22ea-178">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="d22ea-178">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
