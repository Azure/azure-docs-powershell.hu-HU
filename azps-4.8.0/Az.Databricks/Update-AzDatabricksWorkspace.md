---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/update-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
ms.openlocfilehash: 0d213dd18ea2423c90dec6446e4551cbcd8d161a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182811"
---
# <span data-ttu-id="d6ea0-101">Update-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="d6ea0-101">Update-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="d6ea0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6ea0-102">SYNOPSIS</span></span>
<span data-ttu-id="d6ea0-103">Munkaterületet frissít.</span><span class="sxs-lookup"><span data-stu-id="d6ea0-103">Updates a workspace.</span></span>

## <span data-ttu-id="d6ea0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6ea0-104">SYNTAX</span></span>

### <span data-ttu-id="d6ea0-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d6ea0-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyName <String>] [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>]
 [-EncryptionKeyVersion <String>] [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d6ea0-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d6ea0-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-EncryptionKeyName <String>]
 [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>] [-EncryptionKeyVersion <String>]
 [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="d6ea0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6ea0-107">DESCRIPTION</span></span>
<span data-ttu-id="d6ea0-108">Munkaterületet frissít.</span><span class="sxs-lookup"><span data-stu-id="d6ea0-108">Updates a workspace.</span></span>

## <span data-ttu-id="d6ea0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d6ea0-109">EXAMPLES</span></span>

### <span data-ttu-id="d6ea0-110">Példa 1: a Databricks-munkaterület címkéit frissíti</span><span class="sxs-lookup"><span data-stu-id="d6ea0-110">Example 1: Updates the tags of a Databricks workspace</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceopsc46 -Tag @{'key'=1}
PS C:\> Update-AzDatabricksWorkspace -InputObject $dbr -Tag @{key="value"}

Name            Location Managed Resource Group ID
----            -------- -------------------------
workspaceopsc46 eastus   /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceopsc46-wfgp3ayhu6jkn
```

<span data-ttu-id="d6ea0-111">Ez a parancs frissíti a Databricks-munkaterület címkéit.</span><span class="sxs-lookup"><span data-stu-id="d6ea0-111">This command updates the tags of a Databricks workspace.</span></span>

### <span data-ttu-id="d6ea0-112">2. példa: a titkosítás engedélyezése Databricks-munkaterületeken</span><span class="sxs-lookup"><span data-stu-id="d6ea0-112">Example 2: Enable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -PrepareEncryption
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Microsoft.KeyVault' -EncryptionKeyVaultUri https://keyvalult-j3kube.vault.azure.net/ -EncryptionKeyName key-p3bjsf -EncryptionKeyVersion 853999da89714fb4a1408681945135fd

Name            Location       Managed Resource Group ID
----            --------       -------------------------
workspaceypae6l East US 2 EUAP /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceypae6l-wzefrgv2b075t
```

<span data-ttu-id="d6ea0-113">A titkosítás engedélyezésének Databricks-munkaterülete három lépésből áll:</span><span class="sxs-lookup"><span data-stu-id="d6ea0-113">Enabling encryption on a Databricks workspace takes three steps:</span></span>
1.
<span data-ttu-id="d6ea0-114">Frissítse a munkaterületet `-PrepareEncryption` (ha még nem hozta létre).</span><span class="sxs-lookup"><span data-stu-id="d6ea0-114">Update the workspace with `-PrepareEncryption` (if it was not created so).</span></span>
1.
<span data-ttu-id="d6ea0-115">Keresse meg az `StorageAccountIdentityPrincipalId` utolsó lépés kimenetét.</span><span class="sxs-lookup"><span data-stu-id="d6ea0-115">Find `StorageAccountIdentityPrincipalId` in the output of the last step.</span></span>
<span data-ttu-id="d6ea0-116">Adjon meg kulcs-engedélyeket a megbízónak.</span><span class="sxs-lookup"><span data-stu-id="d6ea0-116">Grant key permissions to the principal.</span></span>
1.
<span data-ttu-id="d6ea0-117">A titkosítási kulccsal kapcsolatos információk kitöltéséhez frissítse újra a munkaterületet:</span><span class="sxs-lookup"><span data-stu-id="d6ea0-117">Update the workspace again to fill in information about the encryption key:</span></span>
    - `-EncryptionKeySource`
    - `-EncryptionKeyVaultUri`
    - `-EncryptionKeyName`
    - `-EncryptionKeyVersion`

### <span data-ttu-id="d6ea0-118">3. példa: a titkosítás letiltása Databricks-munkaterületen</span><span class="sxs-lookup"><span data-stu-id="d6ea0-118">Example 3: Disable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Default'
```

<span data-ttu-id="d6ea0-119">A titkosítás letiltásához egyszerűen állítsa be `-EncryptionKeySource` `'Default'` .</span><span class="sxs-lookup"><span data-stu-id="d6ea0-119">To disable encryption, simply set `-EncryptionKeySource` to `'Default'`.</span></span>

## <span data-ttu-id="d6ea0-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6ea0-120">PARAMETERS</span></span>

### <span data-ttu-id="d6ea0-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6ea0-121">-AsJob</span></span>
<span data-ttu-id="d6ea0-122">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="d6ea0-122">Run the command as a job</span></span>

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

### <span data-ttu-id="d6ea0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6ea0-123">-DefaultProfile</span></span>
<span data-ttu-id="d6ea0-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6ea0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6ea0-125">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="d6ea0-125">-EncryptionKeyName</span></span>
<span data-ttu-id="d6ea0-126">A Key Vault-kulcs neve.</span><span class="sxs-lookup"><span data-stu-id="d6ea0-126">The name of Key Vault key.</span></span>

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

### <span data-ttu-id="d6ea0-127">-EncryptionKeySource</span><span class="sxs-lookup"><span data-stu-id="d6ea0-127">-EncryptionKeySource</span></span>
<span data-ttu-id="d6ea0-128">A titkosítási forrás (szolgáltató).</span><span class="sxs-lookup"><span data-stu-id="d6ea0-128">The encryption keySource (provider).</span></span>
<span data-ttu-id="d6ea0-129">Lehetséges értékek (kis-és nagybetűk megkülönböztetése): alapértelmezett, Microsoft.-boltozat</span><span class="sxs-lookup"><span data-stu-id="d6ea0-129">Possible values (case-insensitive): Default, Microsoft.Keyvault</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Support.KeySource
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6ea0-130">-EncryptionKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="d6ea0-130">-EncryptionKeyVaultUri</span></span>
<span data-ttu-id="d6ea0-131">A kulcs-pince URI-ja (DNS-neve).</span><span class="sxs-lookup"><span data-stu-id="d6ea0-131">The URI (DNS name) of the Key Vault.</span></span>

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

### <span data-ttu-id="d6ea0-132">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="d6ea0-132">-EncryptionKeyVersion</span></span>
<span data-ttu-id="d6ea0-133">A kulcskezelő kulcs verziója.</span><span class="sxs-lookup"><span data-stu-id="d6ea0-133">The version of KeyVault key.</span></span>

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

### <span data-ttu-id="d6ea0-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6ea0-134">-InputObject</span></span>
<span data-ttu-id="d6ea0-135">Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="d6ea0-135">Identity parameter.</span></span>
<span data-ttu-id="d6ea0-136">A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="d6ea0-136">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6ea0-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d6ea0-137">-Name</span></span>
<span data-ttu-id="d6ea0-138">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="d6ea0-138">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6ea0-139">-Várva</span><span class="sxs-lookup"><span data-stu-id="d6ea0-139">-NoWait</span></span>
<span data-ttu-id="d6ea0-140">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="d6ea0-140">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d6ea0-141">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="d6ea0-141">-PrepareEncryption</span></span>
<span data-ttu-id="d6ea0-142">A munkaterület előkészítése titkosításhoz.</span><span class="sxs-lookup"><span data-stu-id="d6ea0-142">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="d6ea0-143">Engedélyezi a felügyelt tárterület-fiók felügyelt identitását.</span><span class="sxs-lookup"><span data-stu-id="d6ea0-143">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="d6ea0-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6ea0-144">-ResourceGroupName</span></span>
<span data-ttu-id="d6ea0-145">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d6ea0-145">The name of the resource group.</span></span>
<span data-ttu-id="d6ea0-146">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="d6ea0-146">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d6ea0-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d6ea0-147">-SubscriptionId</span></span>
<span data-ttu-id="d6ea0-148">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d6ea0-148">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d6ea0-149">-Címke</span><span class="sxs-lookup"><span data-stu-id="d6ea0-149">-Tag</span></span>
<span data-ttu-id="d6ea0-150">Erőforrás-címkék.</span><span class="sxs-lookup"><span data-stu-id="d6ea0-150">Resource tags.</span></span>

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

### <span data-ttu-id="d6ea0-151">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d6ea0-151">-Confirm</span></span>
<span data-ttu-id="d6ea0-152">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d6ea0-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6ea0-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6ea0-153">-WhatIf</span></span>
<span data-ttu-id="d6ea0-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d6ea0-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6ea0-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d6ea0-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6ea0-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6ea0-156">CommonParameters</span></span>
<span data-ttu-id="d6ea0-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6ea0-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6ea0-158">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d6ea0-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6ea0-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6ea0-159">INPUTS</span></span>

### <span data-ttu-id="d6ea0-160">Microsoft. Azure. PowerShell. parancsmagok. Databricks. models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="d6ea0-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="d6ea0-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6ea0-161">OUTPUTS</span></span>

### <span data-ttu-id="d6ea0-162">Microsoft. Azure. PowerShell. parancsmagok. Databricks. modellek. Api20180401. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="d6ea0-162">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="d6ea0-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6ea0-163">NOTES</span></span>

<span data-ttu-id="d6ea0-164">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d6ea0-164">ALIASES</span></span>

<span data-ttu-id="d6ea0-165">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="d6ea0-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d6ea0-166">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="d6ea0-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d6ea0-167">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="d6ea0-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d6ea0-168">INPUTOBJECT <IDatabricksIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="d6ea0-168">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="d6ea0-169">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="d6ea0-169">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d6ea0-170">`[PeeringName <String>]`: A munkaterület vNete.</span><span class="sxs-lookup"><span data-stu-id="d6ea0-170">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="d6ea0-171">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d6ea0-171">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d6ea0-172">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="d6ea0-172">The name is case insensitive.</span></span>
  - <span data-ttu-id="d6ea0-173">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d6ea0-173">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d6ea0-174">`[WorkspaceName <String>]`: A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="d6ea0-174">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="d6ea0-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6ea0-175">RELATED LINKS</span></span>

