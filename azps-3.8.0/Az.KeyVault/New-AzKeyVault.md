---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: 067928930474d6210d96491a870d85226d2fd732
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010683"
---
# <span data-ttu-id="7e186-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="7e186-101">New-AzKeyVault</span></span>

## <span data-ttu-id="7e186-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7e186-102">SYNOPSIS</span></span>
<span data-ttu-id="7e186-103">Egy fő boltozatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7e186-103">Creates a key vault.</span></span>

## <span data-ttu-id="7e186-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7e186-104">SYNTAX</span></span>

```
New-AzKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete] [-EnablePurgeProtection]
 [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7e186-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7e186-105">DESCRIPTION</span></span>
<span data-ttu-id="7e186-106">A **New-AzKeyVault** parancsmag létrehoz egy fő boltozatot a megadott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="7e186-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="7e186-107">Ez a parancsmag az aktuálisan bejelentkezett felhasználó engedélyeit is feljogosítja a kulcsfájl hozzáadására, eltávolítására, illetve a kulcsok és a titok megadására.</span><span class="sxs-lookup"><span data-stu-id="7e186-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>
<span data-ttu-id="7e186-108">Megjegyzés: Ha a hiba megjelenik, **az előfizetéshez nincs regisztrálva a "Microsoft. kulcskezelő" névtér használata** az új kulcsfájl létrehozásakor, futtassa a **Register-AzResourceProvider-ProviderNamespace "Microsoft. kulcskezelő"** parancsot, majd futtassa újra a **New-AzKeyVault** parancsot.</span><span class="sxs-lookup"><span data-stu-id="7e186-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="7e186-109">További információt a Register-AzResourceProvider című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7e186-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="7e186-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7e186-110">EXAMPLES</span></span>

### <span data-ttu-id="7e186-111">Példa 1: normál kulcsú boltozat létrehozása</span><span class="sxs-lookup"><span data-stu-id="7e186-111">Example 1: Create a Standard key vault</span></span>
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

<span data-ttu-id="7e186-112">Ez a parancs létrehoz egy Contoso03Vault nevű kulcs boltozatot az Azure régióban, a Kelet-Amerikai Egyesült Államokban.</span><span class="sxs-lookup"><span data-stu-id="7e186-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="7e186-113">A parancs hozzáadja a fő boltozatot a Group14 nevű erőforráscsoport csoportjához.</span><span class="sxs-lookup"><span data-stu-id="7e186-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="7e186-114">Mivel a parancs nem ad meg értéket a *SKU* paraméterhez, létrehoz egy standard kulcs boltozatot.</span><span class="sxs-lookup"><span data-stu-id="7e186-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="7e186-115">2. példa: prémium kulcsú boltozat létrehozása</span><span class="sxs-lookup"><span data-stu-id="7e186-115">Example 2: Create a Premium key vault</span></span>
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

<span data-ttu-id="7e186-116">Ez a parancs az előző példához hasonlóan létrehoz egy fő boltozatot.</span><span class="sxs-lookup"><span data-stu-id="7e186-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="7e186-117">A prémium kulcsú boltozatot azonban a *SKU* paraméterhez tartozó prémium értékkel adja meg.</span><span class="sxs-lookup"><span data-stu-id="7e186-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

## <span data-ttu-id="7e186-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7e186-118">PARAMETERS</span></span>

### <span data-ttu-id="7e186-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e186-119">-DefaultProfile</span></span>
<span data-ttu-id="7e186-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7e186-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e186-121">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="7e186-121">-EnabledForDeployment</span></span>
<span data-ttu-id="7e186-122">A Microsoft. számítási erőforrás-szolgáltatója kinyerheti a titkokat ebből a kulcsfájlból, ha ez a kulcs boltozata az erőforrás létrehozásakor, például virtuális gép létrehozásakor jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="7e186-122">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="7e186-123">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="7e186-123">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="7e186-124">Lehetővé teszi, hogy az Azure Disk Encryption szolgáltatás a kulcsok kijavítását és kicsomagolását a kulcsból.</span><span class="sxs-lookup"><span data-stu-id="7e186-124">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="7e186-125">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="7e186-125">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="7e186-126">Lehetővé teszi az Azure Resource Manager számára, hogy ebből a kulcsfájlból kiírja a titkot, ha ezt a kulcspárt a sablonok központi telepítéséhez hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="7e186-126">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="7e186-127">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="7e186-127">-EnablePurgeProtection</span></span>
<span data-ttu-id="7e186-128">Ha meg van adva, az azonnali törlés elleni védelem engedélyezve van ehhez a boltozathoz; szükség esetén a finom törlést is engedélyezni kell.</span><span class="sxs-lookup"><span data-stu-id="7e186-128">If specified, protection against immediate deletion is enabled for this vault; requires soft delete to be enabled as well.</span></span>

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

### <span data-ttu-id="7e186-129">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="7e186-129">-EnableSoftDelete</span></span>
<span data-ttu-id="7e186-130">Itt adhatja meg, hogy engedélyezve van-e a finom törlés funkció ehhez a kulcshoz.</span><span class="sxs-lookup"><span data-stu-id="7e186-130">Specifies that the soft-delete functionality is enabled for this key vault.</span></span> <span data-ttu-id="7e186-131">Ha a Soft-delete beállítás engedélyezve van, a türelmi időszakra visszaállíthatja a fő boltozatot és annak tartalmát a törlés után.</span><span class="sxs-lookup"><span data-stu-id="7e186-131">When soft-delete is enabled, for a grace period, you can recover this key vault and its contents after it is deleted.</span></span>
<span data-ttu-id="7e186-132">A funkcióról további információt az [Azure Key Vault Soft-delete – áttekintés](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7e186-132">For more information about this functionality, see [Azure Key Vault soft-delete overview](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete).</span></span> <span data-ttu-id="7e186-133">Útmutatásért olvassa el a következő témakört: [Hogyan lehet használni a kulcsfájl Soft-deletet a PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell)segítségével.</span><span class="sxs-lookup"><span data-stu-id="7e186-133">For how-to instructions, see [How to use Key Vault soft-delete with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span></span>

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

### <span data-ttu-id="7e186-134">-Hely</span><span class="sxs-lookup"><span data-stu-id="7e186-134">-Location</span></span>
<span data-ttu-id="7e186-135">Azt az Azure-területet adja meg, amelyben a fő pince hozható létre.</span><span class="sxs-lookup"><span data-stu-id="7e186-135">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="7e186-136">Használja a [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) parancsot a lehetőségek megjelenítéséhez.</span><span class="sxs-lookup"><span data-stu-id="7e186-136">Use the command [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) to see your choices.</span></span>

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

### <span data-ttu-id="7e186-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7e186-137">-Name</span></span>
<span data-ttu-id="7e186-138">A létrehozandó fő pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7e186-138">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="7e186-139">A név lehet betűk, számjegyek és kötőjelek tetszőleges kombinációja.</span><span class="sxs-lookup"><span data-stu-id="7e186-139">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="7e186-140">A névnek betűvel vagy számmal kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="7e186-140">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="7e186-141">A névnek univerzálisan egyedinek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="7e186-141">The name must be universally unique.</span></span>

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

### <span data-ttu-id="7e186-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e186-142">-ResourceGroupName</span></span>
<span data-ttu-id="7e186-143">Annak a meglévő erőforrás-csoportnak a nevét adja meg, amelybe a kulcs boltozatát létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="7e186-143">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="7e186-144">-SKU</span><span class="sxs-lookup"><span data-stu-id="7e186-144">-Sku</span></span>
<span data-ttu-id="7e186-145">A fő boltozat-példány SKU-ának meghatározása.</span><span class="sxs-lookup"><span data-stu-id="7e186-145">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="7e186-146">Ha tudni kívánja, hogy mely funkciók érhetők el az egyes SKU-hoz, olvassa el az Azure Key Vault árképzési webhelye című témakört https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="7e186-146">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

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

### <span data-ttu-id="7e186-147">-Címke</span><span class="sxs-lookup"><span data-stu-id="7e186-147">-Tag</span></span>
<span data-ttu-id="7e186-148">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="7e186-148">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7e186-149">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="7e186-149">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7e186-150">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7e186-150">-Confirm</span></span>
<span data-ttu-id="7e186-151">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7e186-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e186-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e186-152">-WhatIf</span></span>
<span data-ttu-id="7e186-153">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7e186-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e186-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7e186-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e186-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e186-155">CommonParameters</span></span>
<span data-ttu-id="7e186-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7e186-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e186-157">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7e186-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e186-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e186-158">INPUTS</span></span>

### <span data-ttu-id="7e186-159">System. String</span><span class="sxs-lookup"><span data-stu-id="7e186-159">System.String</span></span>

### <span data-ttu-id="7e186-160">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7e186-160">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="7e186-161">Microsoft. Azure. Management. kulcskezelő. models. SkuName</span><span class="sxs-lookup"><span data-stu-id="7e186-161">Microsoft.Azure.Management.KeyVault.Models.SkuName</span></span>

### <span data-ttu-id="7e186-162">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7e186-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7e186-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e186-163">OUTPUTS</span></span>

### <span data-ttu-id="7e186-164">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="7e186-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="7e186-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7e186-165">NOTES</span></span>

## <span data-ttu-id="7e186-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e186-166">RELATED LINKS</span></span>

[<span data-ttu-id="7e186-167">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="7e186-167">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="7e186-168">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="7e186-168">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
