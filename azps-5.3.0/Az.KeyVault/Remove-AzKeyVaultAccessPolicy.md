---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: e19565aa8ae249acf61fce67f0a2b54e20143758
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386342"
---
# <span data-ttu-id="5b532-101">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5b532-101">Remove-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="5b532-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b532-102">SYNOPSIS</span></span>
<span data-ttu-id="5b532-103">Eltávolítja egy felhasználó vagy alkalmazás összes engedélyét egy kulcstárból.</span><span class="sxs-lookup"><span data-stu-id="5b532-103">Removes all permissions for a user or application from a key vault.</span></span>

## <span data-ttu-id="5b532-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5b532-104">SYNTAX</span></span>

### <span data-ttu-id="5b532-105">ByUserPrincipalName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5b532-105">ByUserPrincipalName (Default)</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b532-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="5b532-106">ByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5b532-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="5b532-107">ByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5b532-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="5b532-108">ByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b532-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="5b532-109">ForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b532-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="5b532-110">InputObjectByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b532-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="5b532-111">InputObjectByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b532-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="5b532-112">InputObjectByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b532-113">InputObjectByEmail</span><span class="sxs-lookup"><span data-stu-id="5b532-113">InputObjectByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b532-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="5b532-114">InputObjectForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b532-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="5b532-115">ResourceIdByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b532-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="5b532-116">ResourceIdByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b532-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="5b532-117">ResourceIdByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b532-118">ResourceIdByEmail</span><span class="sxs-lookup"><span data-stu-id="5b532-118">ResourceIdByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b532-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="5b532-119">ResourceIdForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5b532-120">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5b532-120">DESCRIPTION</span></span>
<span data-ttu-id="5b532-121">A **Remove-AzKeyVaultAccessPolicy** parancsmag eltávolítja egy felhasználó vagy alkalmazás, illetve az összes felhasználó és alkalmazás összes engedélyét egy kulcstárból.</span><span class="sxs-lookup"><span data-stu-id="5b532-121">The **Remove-AzKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="5b532-122">Még ha az összes engedélyt eltávolítja is, a kulcstárat tartalmazó Azure-előfizetés tulajdonosa adhat hozzá engedélyeket a kulcstárhoz.</span><span class="sxs-lookup"><span data-stu-id="5b532-122">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>
<span data-ttu-id="5b532-123">Vegye figyelembe, hogy bár az erőforráscsoport megadása nem kötelező ehhez a parancsmaghoz, a jobb teljesítmény érdekében ezt kell megtennie.</span><span class="sxs-lookup"><span data-stu-id="5b532-123">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="5b532-124">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5b532-124">EXAMPLES</span></span>

### <span data-ttu-id="5b532-125">1. példa: Felhasználó engedélyeinek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="5b532-125">Example 1: Remove permissions for a user</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
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
                                   Permissions to Keys                        :
                                   Permissions to Secrets                     :
                                   Permissions to Certificates                : get, create
                                   Permissions to (Key Vault Managed) Storage :


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   :
                                   Virtual Network Rules                      :

Tags                             :
```

<span data-ttu-id="5b532-126">Ez a parancs eltávolítja a felhasználó összes olyan engedélyét, amely a PattiFuller@contoso.com Contoso03Vault nevű kulcstárban található.</span><span class="sxs-lookup"><span data-stu-id="5b532-126">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>  <span data-ttu-id="5b532-127">Ha a -PassThru érték meg van adva, a KeyVault objektum lesz az eredmény.</span><span class="sxs-lookup"><span data-stu-id="5b532-127">If -PassThru is specified, the KeyVault object is returned.</span></span>

### <span data-ttu-id="5b532-128">2. példa: Alkalmazás engedélyeinek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="5b532-128">Example 2: Remove permissions for an application</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="5b532-129">Ez a parancs eltávolítja az összes engedélyt, amely egy alkalmazás a Contoso03Vault nevű kulcstárban található.</span><span class="sxs-lookup"><span data-stu-id="5b532-129">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="5b532-130">Ebben a példában az Azure Active Directoryban regisztrált egyszerű szolgáltatásnév alapján azonosítjuk az `http://payroll.contoso.com` alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="5b532-130">This example identifies the application by using the service principal name registered in Azure Active Directory, `http://payroll.contoso.com`.</span></span>

### <span data-ttu-id="5b532-131">3. példa: Alkalmazás engedélyeinek eltávolítása az objektumazonosító használatával</span><span class="sxs-lookup"><span data-stu-id="5b532-131">Example 3: Remove permissions for an application by using its object ID</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="5b532-132">Ez a parancs eltávolítja az összes engedélyt, amely egy alkalmazás a Contoso03Vault nevű kulcstárban található.</span><span class="sxs-lookup"><span data-stu-id="5b532-132">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="5b532-133">Ez a példa azonosítja az alkalmazást a szolgáltatásnév objektumazonosítója alapján.</span><span class="sxs-lookup"><span data-stu-id="5b532-133">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="5b532-134">4. példa: A Microsoft.Compute erőforrásszolgáltató engedélyeinek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="5b532-134">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="5b532-135">Ez a parancs eltávolítja a Microsoft.Compute erőforrás-szolgáltató engedélyét a Contoso03Vault-adattitkok kiszabadítására.</span><span class="sxs-lookup"><span data-stu-id="5b532-135">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="5b532-136">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b532-136">PARAMETERS</span></span>

### <span data-ttu-id="5b532-137">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="5b532-137">-ApplicationId</span></span>
<span data-ttu-id="5b532-138">Annak az alkalmazásnak az azonosítóját adja meg, amelynek az engedélyét el kell távolítani.</span><span class="sxs-lookup"><span data-stu-id="5b532-138">Specifies the ID of application whose permissions should be removed</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b532-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b532-139">-DefaultProfile</span></span>
<span data-ttu-id="5b532-140">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5b532-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b532-141">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="5b532-141">-EmailAddress</span></span>
<span data-ttu-id="5b532-142">Annak a felhasználónak az e-mail-címét adja meg, akinek a hozzáférését el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="5b532-142">Specifies the user email address of the user whose access you want to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByEmail, InputObjectByEmail, ResourceIdByEmail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b532-143">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="5b532-143">-EnabledForDeployment</span></span>
<span data-ttu-id="5b532-144">Ha meg van adva, a Microsoft.Compute erőforrásszolgáltató letiltja a titkos titkos adatok beolvasását ebből a kulcstárból, amikor az erőforrás-létrehozás során hivatkozik rá.</span><span class="sxs-lookup"><span data-stu-id="5b532-144">If specified, disables the retrieval of secrets from this key vault by the Microsoft.Compute resource provider when referenced in resource creation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b532-145">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="5b532-145">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="5b532-146">Ha meg van adva, az Azure Lemeztitkosítás letiltja a titkos titkos adatok beolvasását a kulcstárból.</span><span class="sxs-lookup"><span data-stu-id="5b532-146">If specified, disables the retrieval of secrets from this key vault by Azure Disk Encryption.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b532-147">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="5b532-147">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="5b532-148">Ha meg van adva, az Azure Resource Manager letiltja a titkos kulcsok lekérését ebből a kulcstárból, amikor sablonokban hivatkoznak rá.</span><span class="sxs-lookup"><span data-stu-id="5b532-148">If specified, disables the retrieval of secrets from this key vault by Azure Resource Manager when referenced in templates.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b532-149">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b532-149">-InputObject</span></span>
<span data-ttu-id="5b532-150">Key Vault objektum.</span><span class="sxs-lookup"><span data-stu-id="5b532-150">Key Vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmail, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b532-151">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="5b532-151">-ObjectId</span></span>
<span data-ttu-id="5b532-152">Annak a felhasználónak vagy szolgáltatásnévnek az objektumazonosítóját adja meg az Azure Active Directoryban, amelynek engedélyét el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="5b532-152">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b532-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b532-153">-PassThru</span></span>
<span data-ttu-id="5b532-154">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="5b532-154">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5b532-155">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="5b532-155">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5b532-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b532-156">-ResourceGroupName</span></span>
<span data-ttu-id="5b532-157">Annak a kulcstárnak a nevét adja meg, amelynek a hozzáférési házirendje módosul.</span><span class="sxs-lookup"><span data-stu-id="5b532-157">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="5b532-158">Ha nincs megadva, ez a parancsmag megkeresi a kulcstárat az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="5b532-158">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b532-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b532-159">-ResourceId</span></span>
<span data-ttu-id="5b532-160">KeyVault-erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5b532-160">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmail, ResourceIdForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b532-161">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="5b532-161">-ServicePrincipalName</span></span>
<span data-ttu-id="5b532-162">Annak az alkalmazásnak az egyszerű szolgáltatásnevét adja meg, amelynek az engedélyét el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="5b532-162">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="5b532-163">Adja meg az alkalmazáshoz az Azure Active Directoryban regisztrált alkalmazásazonosítót ( más néven ügyfélazonosítót).</span><span class="sxs-lookup"><span data-stu-id="5b532-163">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServicePrincipalName, InputObjectByServicePrincipalName, ResourceIdByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b532-164">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="5b532-164">-UserPrincipalName</span></span>
<span data-ttu-id="5b532-165">Annak a felhasználónak a felhasználó egyszerű felhasználónevét adja meg, akinek a hozzáférését el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="5b532-165">Specifies the user principal name of the user whose access you want to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, InputObjectByUserPrincipalName, ResourceIdByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b532-166">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5b532-166">-VaultName</span></span>
<span data-ttu-id="5b532-167">A kulcstár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b532-167">Specifies the name of the key vault.</span></span>
<span data-ttu-id="5b532-168">Ez a parancsmag eltávolítja a paraméter által megadott kulcstár engedélyét.</span><span class="sxs-lookup"><span data-stu-id="5b532-168">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b532-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b532-169">-Confirm</span></span>
<span data-ttu-id="5b532-170">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5b532-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b532-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b532-171">-WhatIf</span></span>
<span data-ttu-id="5b532-172">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5b532-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b532-173">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5b532-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b532-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b532-174">CommonParameters</span></span>
<span data-ttu-id="5b532-175">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b532-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b532-176">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b532-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b532-177">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5b532-177">INPUTS</span></span>

### <span data-ttu-id="5b532-178">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="5b532-178">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="5b532-179">System.String</span><span class="sxs-lookup"><span data-stu-id="5b532-179">System.String</span></span>

## <span data-ttu-id="5b532-180">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b532-180">OUTPUTS</span></span>

### <span data-ttu-id="5b532-181">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="5b532-181">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="5b532-182">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5b532-182">NOTES</span></span>

## <span data-ttu-id="5b532-183">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b532-183">RELATED LINKS</span></span>

[<span data-ttu-id="5b532-184">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5b532-184">Set-AzKeyVaultAccessPolicy</span></span>](./Set-AzKeyVaultAccessPolicy.md)

