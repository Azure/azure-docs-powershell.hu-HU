---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/update-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
ms.openlocfilehash: 0d213dd18ea2423c90dec6446e4551cbcd8d161a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365985"
---
# <span data-ttu-id="88365-101">Update-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="88365-101">Update-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="88365-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88365-102">SYNOPSIS</span></span>
<span data-ttu-id="88365-103">Frissíti a munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="88365-103">Updates a workspace.</span></span>

## <span data-ttu-id="88365-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="88365-104">SYNTAX</span></span>

### <span data-ttu-id="88365-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="88365-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyName <String>] [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>]
 [-EncryptionKeyVersion <String>] [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="88365-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="88365-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-EncryptionKeyName <String>]
 [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>] [-EncryptionKeyVersion <String>]
 [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="88365-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="88365-107">DESCRIPTION</span></span>
<span data-ttu-id="88365-108">Frissíti a munkaterületet.</span><span class="sxs-lookup"><span data-stu-id="88365-108">Updates a workspace.</span></span>

## <span data-ttu-id="88365-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="88365-109">EXAMPLES</span></span>

### <span data-ttu-id="88365-110">1. példa: Az Adatkapcsolatok munkaterület címkéinek frissítése</span><span class="sxs-lookup"><span data-stu-id="88365-110">Example 1: Updates the tags of a Databricks workspace</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceopsc46 -Tag @{'key'=1}
PS C:\> Update-AzDatabricksWorkspace -InputObject $dbr -Tag @{key="value"}

Name            Location Managed Resource Group ID
----            -------- -------------------------
workspaceopsc46 eastus   /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceopsc46-wfgp3ayhu6jkn
```

<span data-ttu-id="88365-111">Ez a parancs frissíti az Adatkapcsolatok munkaterület címkéit.</span><span class="sxs-lookup"><span data-stu-id="88365-111">This command updates the tags of a Databricks workspace.</span></span>

### <span data-ttu-id="88365-112">2. példa: Titkosítás engedélyezése Datab ssl-munkaterületen</span><span class="sxs-lookup"><span data-stu-id="88365-112">Example 2: Enable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -PrepareEncryption
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Microsoft.KeyVault' -EncryptionKeyVaultUri https://keyvalult-j3kube.vault.azure.net/ -EncryptionKeyName key-p3bjsf -EncryptionKeyVersion 853999da89714fb4a1408681945135fd

Name            Location       Managed Resource Group ID
----            --------       -------------------------
workspaceypae6l East US 2 EUAP /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceypae6l-wzefrgv2b075t
```

<span data-ttu-id="88365-113">A titkosítás engedélyezése a Datab workspace-munkaterületen három lépésből áll:</span><span class="sxs-lookup"><span data-stu-id="88365-113">Enabling encryption on a Databricks workspace takes three steps:</span></span>
1.
<span data-ttu-id="88365-114">Frissítse a munkaterületet `-PrepareEncryption` (ha nem így hozták létre).</span><span class="sxs-lookup"><span data-stu-id="88365-114">Update the workspace with `-PrepareEncryption` (if it was not created so).</span></span>
1.
<span data-ttu-id="88365-115">Keresse `StorageAccountIdentityPrincipalId` meg az utolsó lépés kimenetét.</span><span class="sxs-lookup"><span data-stu-id="88365-115">Find `StorageAccountIdentityPrincipalId` in the output of the last step.</span></span>
<span data-ttu-id="88365-116">Adjon meg kulcsengedélyeket a tőketitkos számára.</span><span class="sxs-lookup"><span data-stu-id="88365-116">Grant key permissions to the principal.</span></span>
1.
<span data-ttu-id="88365-117">Frissítse ismét a munkaterületet a titkosítási kulcs információinak kitöltéséhez:</span><span class="sxs-lookup"><span data-stu-id="88365-117">Update the workspace again to fill in information about the encryption key:</span></span>
    - `-EncryptionKeySource`
    - `-EncryptionKeyVaultUri`
    - `-EncryptionKeyName`
    - `-EncryptionKeyVersion`

### <span data-ttu-id="88365-118">3. példa: Titkosítás letiltása Datab workspace-munkaterületen</span><span class="sxs-lookup"><span data-stu-id="88365-118">Example 3: Disable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Default'
```

<span data-ttu-id="88365-119">A titkosítás letiltásához egyszerűen állítsa a `-EncryptionKeySource` `'Default'` .</span><span class="sxs-lookup"><span data-stu-id="88365-119">To disable encryption, simply set `-EncryptionKeySource` to `'Default'`.</span></span>

## <span data-ttu-id="88365-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88365-120">PARAMETERS</span></span>

### <span data-ttu-id="88365-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88365-121">-AsJob</span></span>
<span data-ttu-id="88365-122">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="88365-122">Run the command as a job</span></span>

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

### <span data-ttu-id="88365-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88365-123">-DefaultProfile</span></span>
<span data-ttu-id="88365-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="88365-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88365-125">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="88365-125">-EncryptionKeyName</span></span>
<span data-ttu-id="88365-126">A kulcstár kulcsának neve.</span><span class="sxs-lookup"><span data-stu-id="88365-126">The name of Key Vault key.</span></span>

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

### <span data-ttu-id="88365-127">-EncryptionKeySource</span><span class="sxs-lookup"><span data-stu-id="88365-127">-EncryptionKeySource</span></span>
<span data-ttu-id="88365-128">The encryption keySource (provider).</span><span class="sxs-lookup"><span data-stu-id="88365-128">The encryption keySource (provider).</span></span>
<span data-ttu-id="88365-129">Lehetséges értékek (a kis- és</span><span class="sxs-lookup"><span data-stu-id="88365-129">Possible values (case-insensitive): Default, Microsoft.Keyvault</span></span>

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

### <span data-ttu-id="88365-130">-EncryptionKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="88365-130">-EncryptionKeyVaultUri</span></span>
<span data-ttu-id="88365-131">A kulcstár URI-ja (DNS-neve).</span><span class="sxs-lookup"><span data-stu-id="88365-131">The URI (DNS name) of the Key Vault.</span></span>

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

### <span data-ttu-id="88365-132">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="88365-132">-EncryptionKeyVersion</span></span>
<span data-ttu-id="88365-133">A KeyVault billentyű verziója.</span><span class="sxs-lookup"><span data-stu-id="88365-133">The version of KeyVault key.</span></span>

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

### <span data-ttu-id="88365-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88365-134">-InputObject</span></span>
<span data-ttu-id="88365-135">Identity paraméter.</span><span class="sxs-lookup"><span data-stu-id="88365-135">Identity parameter.</span></span>
<span data-ttu-id="88365-136">Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.</span><span class="sxs-lookup"><span data-stu-id="88365-136">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="88365-137">-Name</span><span class="sxs-lookup"><span data-stu-id="88365-137">-Name</span></span>
<span data-ttu-id="88365-138">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="88365-138">The name of the workspace.</span></span>

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

### <span data-ttu-id="88365-139">-NoWait</span><span class="sxs-lookup"><span data-stu-id="88365-139">-NoWait</span></span>
<span data-ttu-id="88365-140">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="88365-140">Run the command asynchronously</span></span>

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

### <span data-ttu-id="88365-141">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="88365-141">-PrepareEncryption</span></span>
<span data-ttu-id="88365-142">Készítse elő a munkaterületet titkosításra.</span><span class="sxs-lookup"><span data-stu-id="88365-142">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="88365-143">Engedélyezi a Felügyelt identitást felügyelt tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="88365-143">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="88365-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88365-144">-ResourceGroupName</span></span>
<span data-ttu-id="88365-145">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="88365-145">The name of the resource group.</span></span>
<span data-ttu-id="88365-146">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="88365-146">The name is case insensitive.</span></span>

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

### <span data-ttu-id="88365-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="88365-147">-SubscriptionId</span></span>
<span data-ttu-id="88365-148">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="88365-148">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="88365-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="88365-149">-Tag</span></span>
<span data-ttu-id="88365-150">Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="88365-150">Resource tags.</span></span>

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

### <span data-ttu-id="88365-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88365-151">-Confirm</span></span>
<span data-ttu-id="88365-152">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="88365-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88365-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88365-153">-WhatIf</span></span>
<span data-ttu-id="88365-154">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="88365-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88365-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="88365-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88365-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88365-156">CommonParameters</span></span>
<span data-ttu-id="88365-157">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88365-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88365-158">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88365-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88365-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="88365-159">INPUTS</span></span>

### <span data-ttu-id="88365-160">Microsoft.Azure.PowerShell.Cmdlets.Databfüzets.Models.IDatabdatasIdentity</span><span class="sxs-lookup"><span data-stu-id="88365-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="88365-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88365-161">OUTPUTS</span></span>

### <span data-ttu-id="88365-162">Microsoft.Azure.PowerShell.Cmdlets.Databfüzets.Models.Api20180401.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="88365-162">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="88365-163">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="88365-163">NOTES</span></span>

<span data-ttu-id="88365-164">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="88365-164">ALIASES</span></span>

<span data-ttu-id="88365-165">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="88365-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="88365-166">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="88365-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="88365-167">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="88365-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="88365-168">INPUTOBJECT: <IDatabricksIdentity> Identity paraméter.</span><span class="sxs-lookup"><span data-stu-id="88365-168">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="88365-169">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="88365-169">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="88365-170">`[PeeringName <String>]`: A munkaterületi vNet-társviszony neve.</span><span class="sxs-lookup"><span data-stu-id="88365-170">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="88365-171">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="88365-171">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="88365-172">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="88365-172">The name is case insensitive.</span></span>
  - <span data-ttu-id="88365-173">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="88365-173">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="88365-174">`[WorkspaceName <String>]`: A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="88365-174">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="88365-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88365-175">RELATED LINKS</span></span>

