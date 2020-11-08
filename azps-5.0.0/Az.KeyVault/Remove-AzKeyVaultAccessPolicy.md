---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: e19565aa8ae249acf61fce67f0a2b54e20143758
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185301"
---
# <span data-ttu-id="9b24a-101">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9b24a-101">Remove-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="9b24a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9b24a-102">SYNOPSIS</span></span>
<span data-ttu-id="9b24a-103">Egy felhasználó vagy alkalmazás összes engedélyének eltávolítása egy kulcs-boltozatról.</span><span class="sxs-lookup"><span data-stu-id="9b24a-103">Removes all permissions for a user or application from a key vault.</span></span>

## <span data-ttu-id="9b24a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9b24a-104">SYNTAX</span></span>

### <span data-ttu-id="9b24a-105">ByUserPrincipalName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9b24a-105">ByUserPrincipalName (Default)</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b24a-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="9b24a-106">ByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b24a-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="9b24a-107">ByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b24a-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="9b24a-108">ByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b24a-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="9b24a-109">ForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b24a-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="9b24a-110">InputObjectByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b24a-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="9b24a-111">InputObjectByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b24a-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="9b24a-112">InputObjectByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b24a-113">InputObjectByEmail</span><span class="sxs-lookup"><span data-stu-id="9b24a-113">InputObjectByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b24a-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="9b24a-114">InputObjectForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b24a-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="9b24a-115">ResourceIdByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b24a-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="9b24a-116">ResourceIdByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b24a-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="9b24a-117">ResourceIdByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b24a-118">ResourceIdByEmail</span><span class="sxs-lookup"><span data-stu-id="9b24a-118">ResourceIdByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b24a-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="9b24a-119">ResourceIdForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b24a-120">Leírás</span><span class="sxs-lookup"><span data-stu-id="9b24a-120">DESCRIPTION</span></span>
<span data-ttu-id="9b24a-121">A **Remove-AzKeyVaultAccessPolicy** parancsmag eltávolítja a felhasználók vagy alkalmazások összes engedélyét, illetve a fő tárolók minden felhasználóját és alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="9b24a-121">The **Remove-AzKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="9b24a-122">Az Azure-előfizetés fő tárolóját tartalmazó Azure-előfizetés tulajdonosa még akkor is adhat hozzá engedélyeket a kulcs boltozatához, ha eltávolítja az összes engedélyt.</span><span class="sxs-lookup"><span data-stu-id="9b24a-122">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>
<span data-ttu-id="9b24a-123">Fontos tudni, hogy bár az erőforráscsoport beállítása nem kötelező ehhez a parancsmaghoz, a jobb teljesítmény érdekében ezt el kell végeznie.</span><span class="sxs-lookup"><span data-stu-id="9b24a-123">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="9b24a-124">Példák</span><span class="sxs-lookup"><span data-stu-id="9b24a-124">EXAMPLES</span></span>

### <span data-ttu-id="9b24a-125">1. példa: felhasználó engedélyeinek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9b24a-125">Example 1: Remove permissions for a user</span></span>
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

<span data-ttu-id="9b24a-126">Ez a parancs eltávolítja az összes olyan engedélyt, amelyet a felhasználó a PattiFuller@contoso.com Contoso03Vault nevű kulcs-boltíven tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="9b24a-126">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>  <span data-ttu-id="9b24a-127">Ha-PassThru van megadva, a program a parancssori objektumot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="9b24a-127">If -PassThru is specified, the KeyVault object is returned.</span></span>

### <span data-ttu-id="9b24a-128">2. példa: az alkalmazások engedélyeinek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9b24a-128">Example 2: Remove permissions for an application</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="9b24a-129">Ez a parancs eltávolítja az összes olyan engedélyt, amelyet az alkalmazás a Contoso03Vault nevű kulcs boltozaton tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="9b24a-129">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="9b24a-130">Ez a példa azonosítja az alkalmazást az Azure Active Directory szolgáltatásban regisztrált egyszerű szolgáltatásnév használatával `http://payroll.contoso.com` .</span><span class="sxs-lookup"><span data-stu-id="9b24a-130">This example identifies the application by using the service principal name registered in Azure Active Directory, `http://payroll.contoso.com`.</span></span>

### <span data-ttu-id="9b24a-131">3. példa: az alkalmazás engedélyeinek eltávolítása az objektum-azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="9b24a-131">Example 3: Remove permissions for an application by using its object ID</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="9b24a-132">Ez a parancs eltávolítja az összes olyan engedélyt, amelyet az alkalmazás a Contoso03Vault nevű kulcs boltozaton tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="9b24a-132">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="9b24a-133">Ez a példa azonosítja az alkalmazást a szolgáltatás megbízójának objektum-azonosítója alapján.</span><span class="sxs-lookup"><span data-stu-id="9b24a-133">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="9b24a-134">4. példa: engedélyek eltávolítása a Microsofthoz. számítási erőforrás-szolgáltató</span><span class="sxs-lookup"><span data-stu-id="9b24a-134">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="9b24a-135">Ez a parancs eltávolítja az engedélyt a Microsoft számára. az erőforrás-szolgáltató kiszámításához a Contoso03Vault titkait kell beszereznie.</span><span class="sxs-lookup"><span data-stu-id="9b24a-135">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="9b24a-136">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9b24a-136">PARAMETERS</span></span>

### <span data-ttu-id="9b24a-137">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="9b24a-137">-ApplicationId</span></span>
<span data-ttu-id="9b24a-138">Annak az alkalmazásnak az AZONOSÍTÓját adja meg, amelynek az engedélyeit el kell távolítani</span><span class="sxs-lookup"><span data-stu-id="9b24a-138">Specifies the ID of application whose permissions should be removed</span></span>

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

### <span data-ttu-id="9b24a-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b24a-139">-DefaultProfile</span></span>
<span data-ttu-id="9b24a-140">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9b24a-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b24a-141">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="9b24a-141">-EmailAddress</span></span>
<span data-ttu-id="9b24a-142">Annak a felhasználónak a felhasználói e-mail-címét adja meg, akinek az elérését el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="9b24a-142">Specifies the user email address of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="9b24a-143">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="9b24a-143">-EnabledForDeployment</span></span>
<span data-ttu-id="9b24a-144">Ha meg van adva, azzal letiltja a titkot ebből a kulcsfájlból a Microsofttól. kiszámítja az erőforrás-szolgáltatót, ha az erőforrás létrehozásakor hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="9b24a-144">If specified, disables the retrieval of secrets from this key vault by the Microsoft.Compute resource provider when referenced in resource creation.</span></span>

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

### <span data-ttu-id="9b24a-145">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="9b24a-145">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="9b24a-146">Ha meg van adva, akkor az Azure Disk Encryption segítségével letilthatja a titkos kulcsok e kulcsból való lekérését.</span><span class="sxs-lookup"><span data-stu-id="9b24a-146">If specified, disables the retrieval of secrets from this key vault by Azure Disk Encryption.</span></span>

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

### <span data-ttu-id="9b24a-147">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="9b24a-147">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="9b24a-148">Ha meg van adva, akkor a sablonok esetén az Azure Resource Manager letiltja a titkok e kulcsból való lekérését.</span><span class="sxs-lookup"><span data-stu-id="9b24a-148">If specified, disables the retrieval of secrets from this key vault by Azure Resource Manager when referenced in templates.</span></span>

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

### <span data-ttu-id="9b24a-149">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b24a-149">-InputObject</span></span>
<span data-ttu-id="9b24a-150">A Key Vault objektum.</span><span class="sxs-lookup"><span data-stu-id="9b24a-150">Key Vault object.</span></span>

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

### <span data-ttu-id="9b24a-151">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="9b24a-151">-ObjectId</span></span>
<span data-ttu-id="9b24a-152">Annak az Azure Active Directory-fióknak az objektum-AZONOSÍTÓját adja meg, amelynek az engedélyeit el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="9b24a-152">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

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

### <span data-ttu-id="9b24a-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b24a-153">-PassThru</span></span>
<span data-ttu-id="9b24a-154">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="9b24a-154">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9b24a-155">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="9b24a-155">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9b24a-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b24a-156">-ResourceGroupName</span></span>
<span data-ttu-id="9b24a-157">Annak a kulcsfájl-csoportnak a nevét adja meg, amelynek a hozzáférési házirendjét módosították.</span><span class="sxs-lookup"><span data-stu-id="9b24a-157">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="9b24a-158">Ha nem adja meg, ez a parancsmag az aktuális előfizetésben keresi a fő boltozatot.</span><span class="sxs-lookup"><span data-stu-id="9b24a-158">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

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

### <span data-ttu-id="9b24a-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b24a-159">-ResourceId</span></span>
<span data-ttu-id="9b24a-160">A főkészlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9b24a-160">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="9b24a-161">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="9b24a-161">-ServicePrincipalName</span></span>
<span data-ttu-id="9b24a-162">Annak az alkalmazásnak az egyszerű szolgáltatásnevet adja meg, akinek az engedélyeit el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="9b24a-162">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="9b24a-163">Adja meg az Azure Active Directory alkalmazásban regisztrált alkalmazás-azonosítót (más néven ügyfél-azonosítót).</span><span class="sxs-lookup"><span data-stu-id="9b24a-163">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

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

### <span data-ttu-id="9b24a-164">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="9b24a-164">-UserPrincipalName</span></span>
<span data-ttu-id="9b24a-165">Annak a felhasználónak az egyszerű felhasználónevét adja meg, akinek az elérését el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="9b24a-165">Specifies the user principal name of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="9b24a-166">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9b24a-166">-VaultName</span></span>
<span data-ttu-id="9b24a-167">A fő pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9b24a-167">Specifies the name of the key vault.</span></span>
<span data-ttu-id="9b24a-168">Ez a parancsmag eltávolítja az engedélyeket a kulcsfájl számára, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="9b24a-168">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="9b24a-169">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9b24a-169">-Confirm</span></span>
<span data-ttu-id="9b24a-170">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9b24a-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b24a-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b24a-171">-WhatIf</span></span>
<span data-ttu-id="9b24a-172">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9b24a-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b24a-173">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9b24a-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b24a-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b24a-174">CommonParameters</span></span>
<span data-ttu-id="9b24a-175">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9b24a-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b24a-176">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9b24a-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b24a-177">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b24a-177">INPUTS</span></span>

### <span data-ttu-id="9b24a-178">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="9b24a-178">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="9b24a-179">System. String</span><span class="sxs-lookup"><span data-stu-id="9b24a-179">System.String</span></span>

## <span data-ttu-id="9b24a-180">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b24a-180">OUTPUTS</span></span>

### <span data-ttu-id="9b24a-181">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="9b24a-181">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="9b24a-182">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9b24a-182">NOTES</span></span>

## <span data-ttu-id="9b24a-183">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9b24a-183">RELATED LINKS</span></span>

[<span data-ttu-id="9b24a-184">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9b24a-184">Set-AzKeyVaultAccessPolicy</span></span>](./Set-AzKeyVaultAccessPolicy.md)

