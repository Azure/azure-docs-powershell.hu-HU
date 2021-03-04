---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: 77f6ac36f756e89859d38a0c608139dfe28c9667
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919906"
---
# <span data-ttu-id="fcebf-101">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fcebf-101">Set-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="fcebf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcebf-102">SYNOPSIS</span></span>
<span data-ttu-id="fcebf-103">Megadja vagy módosítja egy felhasználó, alkalmazás vagy biztonsági csoport meglévő engedélyét, hogy műveleteket hajtson végre egy kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="fcebf-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

## <span data-ttu-id="fcebf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fcebf-104">SYNTAX</span></span>

### <span data-ttu-id="fcebf-105">ByUserPrincipalName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fcebf-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcebf-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="fcebf-106">ByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcebf-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="fcebf-107">ByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcebf-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="fcebf-108">ByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcebf-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="fcebf-109">ForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcebf-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="fcebf-110">InputObjectByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcebf-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="fcebf-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcebf-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="fcebf-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcebf-113">InputObjectByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="fcebf-113">InputObjectByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcebf-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="fcebf-114">InputObjectForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcebf-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="fcebf-115">ResourceIdByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcebf-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="fcebf-116">ResourceIdByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcebf-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="fcebf-117">ResourceIdByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcebf-118">ResourceIdByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="fcebf-118">ResourceIdByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcebf-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="fcebf-119">ResourceIdForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fcebf-120">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fcebf-120">DESCRIPTION</span></span>
<span data-ttu-id="fcebf-121">A **Set-AzKeyVaultAccessPolicy** parancsmag megadja vagy módosítja egy felhasználó, alkalmazás vagy biztonsági csoport meglévő engedélyét, hogy végrehajtsa a megadott műveleteket egy kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="fcebf-121">The **Set-AzKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="fcebf-122">Nem módosítja azokat az engedélyeket, amelyek más felhasználók, alkalmazások vagy biztonsági csoportok számára a kulcstárban vannak.</span><span class="sxs-lookup"><span data-stu-id="fcebf-122">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>
<span data-ttu-id="fcebf-123">Ha egy biztonsági csoport engedélyét ad meg, ez a művelet csak az adott biztonsági csoport felhasználóit érinti.</span><span class="sxs-lookup"><span data-stu-id="fcebf-123">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>
<span data-ttu-id="fcebf-124">A következő címtáraknak mindnek azonos Azure-címtárnak kell lennie:</span><span class="sxs-lookup"><span data-stu-id="fcebf-124">The following directories must all be the same Azure directory:</span></span>
- <span data-ttu-id="fcebf-125">Annak az Azure-előfizetésnek az alapértelmezett címtára, amelyben a kulcstár található.</span><span class="sxs-lookup"><span data-stu-id="fcebf-125">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="fcebf-126">Az Azure-címtár, amely azt a felhasználót vagy alkalmazáscsoportot tartalmazza, amelyhez engedélyeket ad.</span><span class="sxs-lookup"><span data-stu-id="fcebf-126">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>
<span data-ttu-id="fcebf-127">Példák olyan esetekre, amikor ezek a feltételek nem teljesülnek, és ez a parancsmag nem működik:</span><span class="sxs-lookup"><span data-stu-id="fcebf-127">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span>
- <span data-ttu-id="fcebf-128">Egy másik szervezetből származó felhasználónak a kulcstár kezeléséhez való hozzáférése.</span><span class="sxs-lookup"><span data-stu-id="fcebf-128">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="fcebf-129">Mindegyik szervezetnek saját címtára van.</span><span class="sxs-lookup"><span data-stu-id="fcebf-129">Each organization has its own directory.</span></span>
- <span data-ttu-id="fcebf-130">Azure-fiókja több könyvtárral rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="fcebf-130">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="fcebf-131">Ha nem az alapértelmezett címtárban regisztrál egy alkalmazást, akkor nem engedélyezheti az alkalmazásnak a kulcstár használatát.</span><span class="sxs-lookup"><span data-stu-id="fcebf-131">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="fcebf-132">Az alkalmazásnak az alapértelmezett címtárban kell lennie.</span><span class="sxs-lookup"><span data-stu-id="fcebf-132">The application must be in the default directory.</span></span>
<span data-ttu-id="fcebf-133">Vegye figyelembe, hogy bár az erőforráscsoport megadása nem kötelező ehhez a parancsmaghoz, a jobb teljesítmény érdekében ezt kell megtennie.</span><span class="sxs-lookup"><span data-stu-id="fcebf-133">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

> [!NOTE]
> <span data-ttu-id="fcebf-134">Amikor egyszerű szolgáltatásnév használatával hozzáférési házirend-engedélyeket ad meg, a paramétert kell `-BypassObjectIdValidation` használnia.</span><span class="sxs-lookup"><span data-stu-id="fcebf-134">When using a service principal to grant access policy permissions, you must use the `-BypassObjectIdValidation` parameter.</span></span>

## <span data-ttu-id="fcebf-135">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fcebf-135">EXAMPLES</span></span>

### <span data-ttu-id="fcebf-136">1. példa: Engedélyek megadása egy felhasználónak egy kulcstárhoz és az engedélyek módosítása</span><span class="sxs-lookup"><span data-stu-id="fcebf-136">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets set,delete -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : create, import, delete, list
                                   Permissions to Secrets                     : set, delete
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :

PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : create, import, delete, list
                                   Permissions to Secrets                     : set, delete, get
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :

PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        :
                                   Permissions to Secrets                     : set, delete, get
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :
```

<span data-ttu-id="fcebf-137">Az első parancs engedélyeket ad egy felhasználónak az Azure Active Directoryban, hogy műveleteket hajtson végre a kulcsokon és a titkosságon PattiFuller@contoso.com a Contoso03Vault nevű kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="fcebf-137">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span> <span data-ttu-id="fcebf-138">A *PassThru paraméter* eredménye a frissített objektum, amelyet a parancsmag ad vissza.</span><span class="sxs-lookup"><span data-stu-id="fcebf-138">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>
<span data-ttu-id="fcebf-139">A második parancs módosítja az első parancsban megadott engedélyeket, így mostantól a beállításukon és törlésüken kívül lehetővé teszi a titkos adatok PattiFuller@contoso.com beszerzését.</span><span class="sxs-lookup"><span data-stu-id="fcebf-139">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="fcebf-140">A kulcsműveletekkel kapcsolatos engedélyek a parancs után is változatlanok maradnak.</span><span class="sxs-lookup"><span data-stu-id="fcebf-140">The permissions to key operations remain unchanged after this command.</span></span>
<span data-ttu-id="fcebf-141">Az utolsó parancs tovább módosítja a kulcsműveletekkel kapcsolatos összes engedély eltávolításának meglévő PattiFuller@contoso.com engedélyét.</span><span class="sxs-lookup"><span data-stu-id="fcebf-141">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="fcebf-142">A titkos műveletekre vonatkozó engedélyek a parancs után is változatlanok maradnak.</span><span class="sxs-lookup"><span data-stu-id="fcebf-142">The permissions to secret operations remain unchanged after this command.</span></span>

### <span data-ttu-id="fcebf-143">2. példa: Engedélyek megadása egyszerű alkalmazásszolgáltatásnak a titkos kulcsok olvasására és írására</span><span class="sxs-lookup"><span data-stu-id="fcebf-143">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="fcebf-144">Ez a parancs engedélyeket ad az alkalmazásokhoz a Contoso03Vault nevű kulcstárhoz.</span><span class="sxs-lookup"><span data-stu-id="fcebf-144">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span>
<span data-ttu-id="fcebf-145">A *ServicePrincipalName paraméter* megadja az alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="fcebf-145">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="fcebf-146">Az alkalmazásnak regisztrálva kell lennie az Azure Active Directoryban.</span><span class="sxs-lookup"><span data-stu-id="fcebf-146">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="fcebf-147">A *ServicePrincipalName* paraméter értékének vagy az alkalmazás egyszerű szolgáltatásnevének vagy a GUID azonosítónak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="fcebf-147">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>
<span data-ttu-id="fcebf-148">Ebben a példában az egyszerű szolgáltatásnevet adhatja meg, és a parancs olvasási és írási engedélyeket ad az `http://payroll.contoso.com` alkalmazásnak.</span><span class="sxs-lookup"><span data-stu-id="fcebf-148">This example specifies the service principal name `http://payroll.contoso.com`, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="fcebf-149">3. példa: Engedélyek megadása egy alkalmazáshoz az objektumazonosító használatával</span><span class="sxs-lookup"><span data-stu-id="fcebf-149">Example 3: Grant permissions for an application using its object ID</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="fcebf-150">Ez a parancs hozzáférési engedélyt ad az alkalmazásnak a titkos kulcsok olvasására és írására.</span><span class="sxs-lookup"><span data-stu-id="fcebf-150">This command grants the application permissions to read and write secrets.</span></span>
<span data-ttu-id="fcebf-151">Ebben a példában az alkalmazás az alkalmazás egyszerű szolgáltatásnévének objektumazonosítóját használja.</span><span class="sxs-lookup"><span data-stu-id="fcebf-151">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="fcebf-152">4. példa: Egyszerű felhasználónév engedélyeinek megadása</span><span class="sxs-lookup"><span data-stu-id="fcebf-152">Example 4: Grant permissions for a user principal name</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="fcebf-153">Ez a parancs hozzáférési, lista- és beállítási engedélyeket ad a megadott egyszerű felhasználónévnek a titkos információkhoz való hozzáféréshez.</span><span class="sxs-lookup"><span data-stu-id="fcebf-153">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="fcebf-154">5. példa: Annak engedélyezése, hogy a Microsoft.Compute erőforrásszolgáltató beolvassa a titkos adatokat egy kulcstárból</span><span class="sxs-lookup"><span data-stu-id="fcebf-154">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="fcebf-155">Ez a parancs megadja a Microsoft.Compute erőforrásszolgáltatója által a Contoso03Vault kulcstárból beolvasandó titkos információkhoz szükséges engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="fcebf-155">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="fcebf-156">6. példa: Engedélyek megadása biztonsági csoportnak</span><span class="sxs-lookup"><span data-stu-id="fcebf-156">Example 6: Grant permissions to a security group</span></span>
```powershell
PS C:\> Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys get, set -PermissionsToSecrets get, set
```

<span data-ttu-id="fcebf-157">Az első parancs a Get-AzADGroup parancsmagot használja az összes Active Directory-csoport be szerezni.</span><span class="sxs-lookup"><span data-stu-id="fcebf-157">The first command uses the Get-AzADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="fcebf-158">A kimenetben 3 visszaadott csoport látható, a **csoport1,** **a csoport2** és a **csoport3.**</span><span class="sxs-lookup"><span data-stu-id="fcebf-158">From the output, you see 3 groups returned, named **group1**, **group2**, and **group3**.</span></span> <span data-ttu-id="fcebf-159">Több csoportnak lehet ugyanaz a neve, de mindig egyedi ObjectId azonosítóval rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="fcebf-159">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="fcebf-160">Ha több, azonos nevű csoportot ad vissza, a kimenetben az ObjectId érték használatával azonosítsa a használni kívánt csoportot.</span><span class="sxs-lookup"><span data-stu-id="fcebf-160">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>
<span data-ttu-id="fcebf-161">Ezután használhatja a parancs kimenetét a Set-AzKeyVaultAccessPolicy, hogy engedélyeket adjon a group2 kulcstárának **(myownvault) számára.**</span><span class="sxs-lookup"><span data-stu-id="fcebf-161">You then use the output of this command with Set-AzKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="fcebf-162">Az alábbi példa a "group2" nevű csoportokat számba veszi ugyanabban a parancssorban.</span><span class="sxs-lookup"><span data-stu-id="fcebf-162">This example enumerates the groups named 'group2' inline in the same command line.</span></span>
<span data-ttu-id="fcebf-163">A visszaadott listában több "csoport2" nevű csoport is lehet.</span><span class="sxs-lookup"><span data-stu-id="fcebf-163">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="fcebf-164">Ebben a példában az elsőt választjuk ki, amelyet a 0 index jelez \[ a \] visszaadott listában.</span><span class="sxs-lookup"><span data-stu-id="fcebf-164">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="fcebf-165">7. példa: Azure Information Protection-hozzáférés megadása az ügyfél által kezelt bérlői kulcshoz (BYOK)</span><span class="sxs-lookup"><span data-stu-id="fcebf-165">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="fcebf-166">Ez a parancs engedélyezi az Azure Information Protectionnek, hogy az Azure Information Protection bérlői kulcsként ügyfél által kezelt kulcsot (a saját kulcsát hozza magával, vagy a "BYOK" esetet) használjon.</span><span class="sxs-lookup"><span data-stu-id="fcebf-166">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>
<span data-ttu-id="fcebf-167">A parancs futtatásakor meg kell adnia a saját kulcstárnevét, de meg kell adnia a *ServicePrincipalName* paramétert a GUID **00000012-0000-0000-c000-00000000000000** azonosítóval, és meg kell adnia a példában az engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="fcebf-167">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="fcebf-168">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fcebf-168">PARAMETERS</span></span>

### <span data-ttu-id="fcebf-169">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="fcebf-169">-ApplicationId</span></span>
<span data-ttu-id="fcebf-170">Későbbi használatra.</span><span class="sxs-lookup"><span data-stu-id="fcebf-170">For future use.</span></span>

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

### <span data-ttu-id="fcebf-171">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="fcebf-171">-BypassObjectIdValidation</span></span>
<span data-ttu-id="fcebf-172">Lehetővé teszi az objektumazonosítók megadását anélkül, hogy érvényesíte volna az objektum Azure Active Directoryban való létezik-e.</span><span class="sxs-lookup"><span data-stu-id="fcebf-172">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>
<span data-ttu-id="fcebf-173">Ezt a paramétert csak akkor használja, ha hozzáférést szeretne a kulcstárhoz egy olyan objektumazonosítóhoz, amely egy másik Azure-bérlő delegált biztonsági csoportjára hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="fcebf-173">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcebf-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcebf-174">-DefaultProfile</span></span>
<span data-ttu-id="fcebf-175">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fcebf-175">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fcebf-176">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="fcebf-176">-EmailAddress</span></span>
<span data-ttu-id="fcebf-177">Annak a felhasználónak az e-mail-címét adja meg, akinek engedélyt kell kiadó felhasználónak.</span><span class="sxs-lookup"><span data-stu-id="fcebf-177">Specifies the user email address of the user to whom to grant permissions.</span></span>
<span data-ttu-id="fcebf-178">Ennek az e-mail-címnek az aktuális előfizetéshez társított címtárban kell lennie, és egyedinek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="fcebf-178">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

```yaml
Type: System.String
Parameter Sets: ByEmailAddress, InputObjectByEmailAddress, ResourceIdByEmailAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcebf-179">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="fcebf-179">-EnabledForDeployment</span></span>
<span data-ttu-id="fcebf-180">Lehetővé teszi a Microsoft.Compute erőforrásszolgáltatónak, hogy beolvassa a titkos értékeket ebből a kulcstárból, amikor erre a kulcstárra hivatkozik az erőforrás-létrehozás során, például virtuális gép létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="fcebf-180">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="fcebf-181">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="fcebf-181">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="fcebf-182">Lehetővé teszi az Azure lemeztitkosítási szolgáltatásának, hogy titkos adatokat és kulcsokat olvasson le ebből a kulcstárból.</span><span class="sxs-lookup"><span data-stu-id="fcebf-182">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="fcebf-183">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="fcebf-183">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="fcebf-184">Lehetővé teszi az Azure Resource Manager számára, hogy titkos titkos szolgáltatásokat rejtsen ebből a kulcstárból, amikor erre a kulcstárra hivatkozik egy sablon központi telepítésében.</span><span class="sxs-lookup"><span data-stu-id="fcebf-184">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="fcebf-185">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcebf-185">-InputObject</span></span>
<span data-ttu-id="fcebf-186">Key Vault objektum</span><span class="sxs-lookup"><span data-stu-id="fcebf-186">Key Vault Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fcebf-187">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="fcebf-187">-ObjectId</span></span>
<span data-ttu-id="fcebf-188">Annak a felhasználónak vagy szolgáltatásnévnek az objektumazonosítóját adja meg az Azure Active Directoryban, amelynek az engedélyét meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="fcebf-188">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

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

### <span data-ttu-id="fcebf-189">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fcebf-189">-PassThru</span></span>
<span data-ttu-id="fcebf-190">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="fcebf-190">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fcebf-191">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="fcebf-191">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fcebf-192">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="fcebf-192">-PermissionsToCertificates</span></span>
<span data-ttu-id="fcebf-193">Egy felhasználónak vagy egyszerű szolgáltatásnak adható tanúsítványengedélyek tömbje.</span><span class="sxs-lookup"><span data-stu-id="fcebf-193">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="fcebf-194">A paraméter elfogadható értékei:</span><span class="sxs-lookup"><span data-stu-id="fcebf-194">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="fcebf-195">Mind</span><span class="sxs-lookup"><span data-stu-id="fcebf-195">All</span></span>
- <span data-ttu-id="fcebf-196">Bej.le</span><span class="sxs-lookup"><span data-stu-id="fcebf-196">Get</span></span>
- <span data-ttu-id="fcebf-197">Lista</span><span class="sxs-lookup"><span data-stu-id="fcebf-197">List</span></span>
- <span data-ttu-id="fcebf-198">Törlés</span><span class="sxs-lookup"><span data-stu-id="fcebf-198">Delete</span></span>
- <span data-ttu-id="fcebf-199">Létrehozás</span><span class="sxs-lookup"><span data-stu-id="fcebf-199">Create</span></span>
- <span data-ttu-id="fcebf-200">Importálás</span><span class="sxs-lookup"><span data-stu-id="fcebf-200">Import</span></span>
- <span data-ttu-id="fcebf-201">Frissítés</span><span class="sxs-lookup"><span data-stu-id="fcebf-201">Update</span></span>
- <span data-ttu-id="fcebf-202">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="fcebf-202">Managecontacts</span></span>
- <span data-ttu-id="fcebf-203">Getissuers</span><span class="sxs-lookup"><span data-stu-id="fcebf-203">Getissuers</span></span>
- <span data-ttu-id="fcebf-204">Listissuers</span><span class="sxs-lookup"><span data-stu-id="fcebf-204">Listissuers</span></span>
- <span data-ttu-id="fcebf-205">Setissuers</span><span class="sxs-lookup"><span data-stu-id="fcebf-205">Setissuers</span></span>
- <span data-ttu-id="fcebf-206">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="fcebf-206">Deleteissuers</span></span>
- <span data-ttu-id="fcebf-207">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="fcebf-207">Manageissuers</span></span>
- <span data-ttu-id="fcebf-208">Helyreállítás</span><span class="sxs-lookup"><span data-stu-id="fcebf-208">Recover</span></span>
- <span data-ttu-id="fcebf-209">Biztonsági másolat</span><span class="sxs-lookup"><span data-stu-id="fcebf-209">Backup</span></span>
- <span data-ttu-id="fcebf-210">Visszaállítás</span><span class="sxs-lookup"><span data-stu-id="fcebf-210">Restore</span></span>
- <span data-ttu-id="fcebf-211">Végleges végleges végleges</span><span class="sxs-lookup"><span data-stu-id="fcebf-211">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, backup, restore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcebf-212">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="fcebf-212">-PermissionsToKeys</span></span>
<span data-ttu-id="fcebf-213">Egy felhasználónak vagy egyszerű szolgáltatásnak adható kulcsműveleti engedélyek tömbje.</span><span class="sxs-lookup"><span data-stu-id="fcebf-213">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="fcebf-214">A paraméter elfogadható értékei:</span><span class="sxs-lookup"><span data-stu-id="fcebf-214">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="fcebf-215">Mind</span><span class="sxs-lookup"><span data-stu-id="fcebf-215">All</span></span>
- <span data-ttu-id="fcebf-216">Visszafejtése</span><span class="sxs-lookup"><span data-stu-id="fcebf-216">Decrypt</span></span>
- <span data-ttu-id="fcebf-217">Titkosítás</span><span class="sxs-lookup"><span data-stu-id="fcebf-217">Encrypt</span></span>
- <span data-ttu-id="fcebf-218">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="fcebf-218">UnwrapKey</span></span>
- <span data-ttu-id="fcebf-219">WrapKey</span><span class="sxs-lookup"><span data-stu-id="fcebf-219">WrapKey</span></span>
- <span data-ttu-id="fcebf-220">Ellenőrzés</span><span class="sxs-lookup"><span data-stu-id="fcebf-220">Verify</span></span>
- <span data-ttu-id="fcebf-221">Aláírás</span><span class="sxs-lookup"><span data-stu-id="fcebf-221">Sign</span></span>
- <span data-ttu-id="fcebf-222">Bej.le</span><span class="sxs-lookup"><span data-stu-id="fcebf-222">Get</span></span>
- <span data-ttu-id="fcebf-223">Lista</span><span class="sxs-lookup"><span data-stu-id="fcebf-223">List</span></span>
- <span data-ttu-id="fcebf-224">Frissítés</span><span class="sxs-lookup"><span data-stu-id="fcebf-224">Update</span></span>
- <span data-ttu-id="fcebf-225">Létrehozás</span><span class="sxs-lookup"><span data-stu-id="fcebf-225">Create</span></span>
- <span data-ttu-id="fcebf-226">Importálás</span><span class="sxs-lookup"><span data-stu-id="fcebf-226">Import</span></span>
- <span data-ttu-id="fcebf-227">Törlés</span><span class="sxs-lookup"><span data-stu-id="fcebf-227">Delete</span></span>
- <span data-ttu-id="fcebf-228">Biztonsági másolat</span><span class="sxs-lookup"><span data-stu-id="fcebf-228">Backup</span></span>
- <span data-ttu-id="fcebf-229">Visszaállítás</span><span class="sxs-lookup"><span data-stu-id="fcebf-229">Restore</span></span>
- <span data-ttu-id="fcebf-230">Helyreállítás</span><span class="sxs-lookup"><span data-stu-id="fcebf-230">Recover</span></span>
- <span data-ttu-id="fcebf-231">Végleges végleges végleges</span><span class="sxs-lookup"><span data-stu-id="fcebf-231">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcebf-232">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="fcebf-232">-PermissionsToSecrets</span></span>
<span data-ttu-id="fcebf-233">Egy felhasználónak vagy egyszerű szolgáltatásnak adható titkos műveletekre vonatkozó engedélyek tömbje.</span><span class="sxs-lookup"><span data-stu-id="fcebf-233">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="fcebf-234">A paraméter elfogadható értékei:</span><span class="sxs-lookup"><span data-stu-id="fcebf-234">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="fcebf-235">Mind</span><span class="sxs-lookup"><span data-stu-id="fcebf-235">All</span></span>
- <span data-ttu-id="fcebf-236">Bej.le</span><span class="sxs-lookup"><span data-stu-id="fcebf-236">Get</span></span>
- <span data-ttu-id="fcebf-237">Lista</span><span class="sxs-lookup"><span data-stu-id="fcebf-237">List</span></span>
- <span data-ttu-id="fcebf-238">Beállítás</span><span class="sxs-lookup"><span data-stu-id="fcebf-238">Set</span></span>
- <span data-ttu-id="fcebf-239">Törlés</span><span class="sxs-lookup"><span data-stu-id="fcebf-239">Delete</span></span>
- <span data-ttu-id="fcebf-240">Biztonsági másolat</span><span class="sxs-lookup"><span data-stu-id="fcebf-240">Backup</span></span>
- <span data-ttu-id="fcebf-241">Visszaállítás</span><span class="sxs-lookup"><span data-stu-id="fcebf-241">Restore</span></span>
- <span data-ttu-id="fcebf-242">Helyreállítás</span><span class="sxs-lookup"><span data-stu-id="fcebf-242">Recover</span></span>
- <span data-ttu-id="fcebf-243">Végleges végleges végleges</span><span class="sxs-lookup"><span data-stu-id="fcebf-243">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, set, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcebf-244">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="fcebf-244">-PermissionsToStorage</span></span>
<span data-ttu-id="fcebf-245">A felügyelt tárfiókra és a SaS-definíciós műveletre vonatkozó engedélyeket adja meg, amelyek a felhasználónak vagy a szolgáltatásnévnek adhatók.</span><span class="sxs-lookup"><span data-stu-id="fcebf-245">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="fcebf-246">A paraméter elfogadható értékei:</span><span class="sxs-lookup"><span data-stu-id="fcebf-246">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="fcebf-247">mind</span><span class="sxs-lookup"><span data-stu-id="fcebf-247">all</span></span>
- <span data-ttu-id="fcebf-248">get</span><span class="sxs-lookup"><span data-stu-id="fcebf-248">get</span></span>
- <span data-ttu-id="fcebf-249">lista</span><span class="sxs-lookup"><span data-stu-id="fcebf-249">list</span></span>
- <span data-ttu-id="fcebf-250">törlés</span><span class="sxs-lookup"><span data-stu-id="fcebf-250">delete</span></span>
- <span data-ttu-id="fcebf-251">beállítás</span><span class="sxs-lookup"><span data-stu-id="fcebf-251">set</span></span>
- <span data-ttu-id="fcebf-252">frissítés</span><span class="sxs-lookup"><span data-stu-id="fcebf-252">update</span></span>
- <span data-ttu-id="fcebf-253">regeneratekey</span><span class="sxs-lookup"><span data-stu-id="fcebf-253">regeneratekey</span></span>
- <span data-ttu-id="fcebf-254">getsas</span><span class="sxs-lookup"><span data-stu-id="fcebf-254">getsas</span></span>
- <span data-ttu-id="fcebf-255">listsas</span><span class="sxs-lookup"><span data-stu-id="fcebf-255">listsas</span></span>
- <span data-ttu-id="fcebf-256">deletesas</span><span class="sxs-lookup"><span data-stu-id="fcebf-256">deletesas</span></span>
- <span data-ttu-id="fcebf-257">setsas</span><span class="sxs-lookup"><span data-stu-id="fcebf-257">setsas</span></span>
- <span data-ttu-id="fcebf-258">helyreállítás</span><span class="sxs-lookup"><span data-stu-id="fcebf-258">recover</span></span>
- <span data-ttu-id="fcebf-259">biztonsági mentés</span><span class="sxs-lookup"><span data-stu-id="fcebf-259">backup</span></span>
- <span data-ttu-id="fcebf-260">visszaállítás</span><span class="sxs-lookup"><span data-stu-id="fcebf-260">restore</span></span>
- <span data-ttu-id="fcebf-261">végleges végleges végleges</span><span class="sxs-lookup"><span data-stu-id="fcebf-261">purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, recover, backup, restore, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcebf-262">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcebf-262">-ResourceGroupName</span></span>
<span data-ttu-id="fcebf-263">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fcebf-263">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcebf-264">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fcebf-264">-ResourceId</span></span>
<span data-ttu-id="fcebf-265">Key Vault Resource Id</span><span class="sxs-lookup"><span data-stu-id="fcebf-265">Key Vault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress, ResourceIdForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcebf-266">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="fcebf-266">-ServicePrincipalName</span></span>
<span data-ttu-id="fcebf-267">Annak az alkalmazásnak a egyszerű szolgáltatásnevét adja meg, amelyhez engedélyeket ad.</span><span class="sxs-lookup"><span data-stu-id="fcebf-267">Specifies the service principal name of the application to which to grant permissions.</span></span>
<span data-ttu-id="fcebf-268">Adja meg az alkalmazáshoz az AzureActive Directoryban regisztrált alkalmazásazonosítót ( más néven ügyfélazonosítót).</span><span class="sxs-lookup"><span data-stu-id="fcebf-268">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="fcebf-269">A paraméterként megadott egyszerű szolgáltatásnévvel megadott alkalmazást az aktuális előfizetést tartalmazó Azure-címtárban kell regisztrálni.</span><span class="sxs-lookup"><span data-stu-id="fcebf-269">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

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

### <span data-ttu-id="fcebf-270">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="fcebf-270">-UserPrincipalName</span></span>
<span data-ttu-id="fcebf-271">Annak a felhasználónak a felhasználó egyszerű felhasználónevét adja meg, akinek az engedélyeket ki kell ad.</span><span class="sxs-lookup"><span data-stu-id="fcebf-271">Specifies the user principal name of the user to whom to grant permissions.</span></span>
<span data-ttu-id="fcebf-272">Az egyszerű felhasználónévnek az aktuális előfizetéshez társított címtárban kell lennie.</span><span class="sxs-lookup"><span data-stu-id="fcebf-272">This user principal name must exist in the directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="fcebf-273">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fcebf-273">-VaultName</span></span>
<span data-ttu-id="fcebf-274">Egy kulcstár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fcebf-274">Specifies the name of a key vault.</span></span>
<span data-ttu-id="fcebf-275">Ez a parancsmag módosítja a paraméter által megadott kulcstár hozzáférési házirendét.</span><span class="sxs-lookup"><span data-stu-id="fcebf-275">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcebf-276">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fcebf-276">-Confirm</span></span>
<span data-ttu-id="fcebf-277">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fcebf-277">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcebf-278">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcebf-278">-WhatIf</span></span>
<span data-ttu-id="fcebf-279">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fcebf-279">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fcebf-280">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fcebf-280">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcebf-281">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcebf-281">CommonParameters</span></span>
<span data-ttu-id="fcebf-282">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcebf-282">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcebf-283">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fcebf-283">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcebf-284">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fcebf-284">INPUTS</span></span>

### <span data-ttu-id="fcebf-285">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="fcebf-285">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="fcebf-286">System.String</span><span class="sxs-lookup"><span data-stu-id="fcebf-286">System.String</span></span>

## <span data-ttu-id="fcebf-287">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fcebf-287">OUTPUTS</span></span>

### <span data-ttu-id="fcebf-288">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="fcebf-288">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="fcebf-289">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fcebf-289">NOTES</span></span>

## <span data-ttu-id="fcebf-290">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fcebf-290">RELATED LINKS</span></span>

[<span data-ttu-id="fcebf-291">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="fcebf-291">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="fcebf-292">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fcebf-292">Remove-AzKeyVaultAccessPolicy</span></span>](./Remove-AzKeyVaultAccessPolicy.md)

