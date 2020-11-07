---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
ms.openlocfilehash: 795840d7580d1e7dabb15cf3211ef16d0ccfb7b7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666207"
---
# <span data-ttu-id="deaf9-101">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="deaf9-101">Get-AzKeyVault</span></span>

## <span data-ttu-id="deaf9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="deaf9-102">SYNOPSIS</span></span>
<span data-ttu-id="deaf9-103">Kulcsos boltozatokat kap.</span><span class="sxs-lookup"><span data-stu-id="deaf9-103">Gets key vaults.</span></span>

## <span data-ttu-id="deaf9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="deaf9-104">SYNTAX</span></span>

### <span data-ttu-id="deaf9-105">GetVaultByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="deaf9-105">GetVaultByName (Default)</span></span>
```
Get-AzKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="deaf9-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="deaf9-106">ByDeletedVault</span></span>
```
Get-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="deaf9-107">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="deaf9-107">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="deaf9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="deaf9-108">DESCRIPTION</span></span>
<span data-ttu-id="deaf9-109">A **Get-AzKeyVault** parancsmag információkat kap az előfizetések fő boltozatáról.</span><span class="sxs-lookup"><span data-stu-id="deaf9-109">The **Get-AzKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="deaf9-110">Az előfizetésben megtekintheti az összes fontos boltozat-példányt, vagy szűrheti az eredményeket egy erőforráscsoport vagy egy adott kulcs boltozatával.</span><span class="sxs-lookup"><span data-stu-id="deaf9-110">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>
<span data-ttu-id="deaf9-111">Fontos tudni, hogy bár az erőforráscsoport beállítása nem kötelező a parancsmag számára, ha egyetlen kulcs típusú boltozatot kap, akkor a jobb teljesítmény érdekében ezt el kell végeznie.</span><span class="sxs-lookup"><span data-stu-id="deaf9-111">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="deaf9-112">Példák</span><span class="sxs-lookup"><span data-stu-id="deaf9-112">EXAMPLES</span></span>

### <span data-ttu-id="deaf9-113">Példa 1: a jelenlegi előfizetésben lévő összes kulcs boltozatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="deaf9-113">Example 1: Get all key vaults in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVault

Vault Name          : myvault1
Resource Group Name : myrg
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.Ke
                      yVault/vaults/myvault1
Tags                :


Vault Name          : myvault2
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault2
Tags                :

Vault Name          : myvault3
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault3
Tags                :
```

<span data-ttu-id="deaf9-114">Ez a parancs a jelenlegi előfizetésben a legfontosabb boltozatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="deaf9-114">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="deaf9-115">2. példa: adott kulcsos boltozat beszerzése</span><span class="sxs-lookup"><span data-stu-id="deaf9-115">Example 2: Get a specific key vault</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName 'myvault'

Vault Name                       : myvault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/myvault
Vault URI                        : https://myvault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : True
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
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
                                   setissuers, recover
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update

Tags                             :
```

<span data-ttu-id="deaf9-116">Ez a parancs a myvault nevű kulcs boltozatát kapja meg a jelenlegi előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="deaf9-116">This command gets the key vault named myvault in your current subscription.</span></span>

### <span data-ttu-id="deaf9-117">3. példa: kulcsos boltívek beszerzése erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="deaf9-117">Example 3: Get key vaults in a resource group</span></span>
```powershell
PS C:\> Get-AzKeyVault -ResourceGroupName 'myrg1'

Vault Name          : myvault2
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault2
Tags                :

Vault Name          : myvault3
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault3
Tags                :
```

<span data-ttu-id="deaf9-118">Ez a parancs a ContosoPayRollResourceGroup nevű erőforráscsoport minden fő boltozatát beolvassa.</span><span class="sxs-lookup"><span data-stu-id="deaf9-118">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="deaf9-119">4. példa: az összes törölt kulcsfájl beolvasása a jelenlegi előfizetésben</span><span class="sxs-lookup"><span data-stu-id="deaf9-119">Example 4: Get all deleted key vaults in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVault -InRemovedState

Vault Name           : myvault4
Location             : westus
Id                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/providers/Microsoft.KeyVault/locations/westu
                       s/deletedVaults/myvault4
Resource ID          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.K
                       eyVault/vaults/myvault4
Deletion Date        : 5/24/2018 9:33:24 PM
Scheduled Purge Date : 8/22/2018 9:33:24 PM
Tags                 :
```

<span data-ttu-id="deaf9-120">Ez a parancs beolvassa a jelenlegi előfizetés összes törölt kulcsát.</span><span class="sxs-lookup"><span data-stu-id="deaf9-120">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="deaf9-121">Példa 5: törölt kulcsfájl beszerzése</span><span class="sxs-lookup"><span data-stu-id="deaf9-121">Example 5: Get a deleted key vault</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName 'myvault4'  -Location 'westus' -InRemovedState

Vault Name           : myvault4
Location             : westus
Id                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/providers/Microsoft.KeyVault/locations/westu
                       s/deletedVaults/myvault4
Resource ID          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.K
                       eyVault/vaults/myvault4
Deletion Date        : 5/24/2018 9:33:24 PM
Scheduled Purge Date : 8/22/2018 9:33:24 PM
Tags                 :
```

<span data-ttu-id="deaf9-122">Ez a parancs beolvassa a myvault4 nevű, az aktuális előfizetésben és a westus-régióban a törölt kulcs boltozattal kapcsolatos információkat.</span><span class="sxs-lookup"><span data-stu-id="deaf9-122">This command gets the deleted key vault information named myvault4 in your current subscription and in westus region.</span></span>

### <span data-ttu-id="deaf9-123">6. példa: kulcsos boltívek beszerzése szűréssel</span><span class="sxs-lookup"><span data-stu-id="deaf9-123">Example 6: Get key vaults using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName 'myvault*'

Vault Name          : myvault2
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault2
Tags                :

Vault Name          : myvault3
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault3
Tags                :
```

<span data-ttu-id="deaf9-124">Ez a parancs a "myvault" kezdetű előfizetésben a legfontosabb boltozatokat kapja.</span><span class="sxs-lookup"><span data-stu-id="deaf9-124">This command gets all the key vaults in the subscription that start with "myvault".</span></span>

## <span data-ttu-id="deaf9-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="deaf9-125">PARAMETERS</span></span>

### <span data-ttu-id="deaf9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deaf9-126">-DefaultProfile</span></span>
<span data-ttu-id="deaf9-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="deaf9-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="deaf9-128">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="deaf9-128">-InRemovedState</span></span>
<span data-ttu-id="deaf9-129">Itt adhatja meg, hogy megjelenjen-e a korábban törölt boltozatok a kimenetben.</span><span class="sxs-lookup"><span data-stu-id="deaf9-129">Specifies whether to show the previously deleted vaults in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deaf9-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="deaf9-130">-Location</span></span>
<span data-ttu-id="deaf9-131">A törölt boltozat helye.</span><span class="sxs-lookup"><span data-stu-id="deaf9-131">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="deaf9-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="deaf9-132">-ResourceGroupName</span></span>
<span data-ttu-id="deaf9-133">A lekérdezett fő boltozattal vagy a fő boltozatokkal társított erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="deaf9-133">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="deaf9-134">-Címke</span><span class="sxs-lookup"><span data-stu-id="deaf9-134">-Tag</span></span>
<span data-ttu-id="deaf9-135">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="deaf9-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="deaf9-136">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="deaf9-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="deaf9-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="deaf9-137">-VaultName</span></span>
<span data-ttu-id="deaf9-138">A fő pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="deaf9-138">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="deaf9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deaf9-139">CommonParameters</span></span>
<span data-ttu-id="deaf9-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="deaf9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deaf9-141">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="deaf9-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deaf9-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="deaf9-142">INPUTS</span></span>

### <span data-ttu-id="deaf9-143">System. String</span><span class="sxs-lookup"><span data-stu-id="deaf9-143">System.String</span></span>

### <span data-ttu-id="deaf9-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="deaf9-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="deaf9-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="deaf9-145">OUTPUTS</span></span>

### <span data-ttu-id="deaf9-146">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="deaf9-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="deaf9-147">Microsoft. Azure. Command. PSKeyVaultIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="deaf9-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="deaf9-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="deaf9-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="deaf9-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="deaf9-149">NOTES</span></span>

## <span data-ttu-id="deaf9-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="deaf9-150">RELATED LINKS</span></span>

[<span data-ttu-id="deaf9-151">Új – AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="deaf9-151">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="deaf9-152">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="deaf9-152">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
