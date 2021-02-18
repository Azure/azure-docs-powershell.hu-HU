---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: 5f47237088808fe8966d239f9a0de7c892301db0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100410718"
---
# <span data-ttu-id="aa69b-101">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="aa69b-101">Set-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="aa69b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa69b-102">SYNOPSIS</span></span>
<span data-ttu-id="aa69b-103">Megadja vagy módosítja egy felhasználó, alkalmazás vagy biztonsági csoport meglévő engedélyét, hogy műveleteket hajtson végre egy kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="aa69b-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

## <span data-ttu-id="aa69b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="aa69b-104">SYNTAX</span></span>

### <span data-ttu-id="aa69b-105">ByUserPrincipalName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aa69b-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa69b-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="aa69b-106">ByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa69b-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="aa69b-107">ByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa69b-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="aa69b-108">ByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa69b-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="aa69b-109">ForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa69b-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="aa69b-110">InputObjectByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa69b-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="aa69b-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa69b-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="aa69b-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa69b-113">InputObjectByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="aa69b-113">InputObjectByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa69b-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="aa69b-114">InputObjectForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa69b-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="aa69b-115">ResourceIdByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa69b-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="aa69b-116">ResourceIdByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa69b-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="aa69b-117">ResourceIdByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa69b-118">ResourceIdByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="aa69b-118">ResourceIdByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa69b-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="aa69b-119">ResourceIdForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aa69b-120">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="aa69b-120">DESCRIPTION</span></span>
<span data-ttu-id="aa69b-121">A **Set-AzKeyVaultAccessPolicy** parancsmag megadja vagy módosítja egy felhasználó, alkalmazás vagy biztonsági csoport meglévő engedélyét, hogy végrehajtsa a megadott műveleteket egy kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="aa69b-121">The **Set-AzKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="aa69b-122">Nem módosítja a többi felhasználó, alkalmazás vagy biztonsági csoport kulcstárra vonatkozó engedélyét.</span><span class="sxs-lookup"><span data-stu-id="aa69b-122">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>
<span data-ttu-id="aa69b-123">Ha egy biztonsági csoport engedélyét ad meg, ez a művelet csak az adott biztonsági csoport felhasználóit érinti.</span><span class="sxs-lookup"><span data-stu-id="aa69b-123">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>
<span data-ttu-id="aa69b-124">A következő címtáraknak mindnek azonos Azure-címtárnak kell lennie:</span><span class="sxs-lookup"><span data-stu-id="aa69b-124">The following directories must all be the same Azure directory:</span></span>
- <span data-ttu-id="aa69b-125">Annak az Azure-előfizetésnek az alapértelmezett címtára, amelyben a kulcstár található.</span><span class="sxs-lookup"><span data-stu-id="aa69b-125">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="aa69b-126">Az Azure-címtár, amely azt a felhasználót vagy alkalmazáscsoportot tartalmazza, amelyhez engedélyeket ad.</span><span class="sxs-lookup"><span data-stu-id="aa69b-126">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>
<span data-ttu-id="aa69b-127">Példák olyan esetekre, amikor ezek a feltételek nem teljesülnek, és ez a parancsmag nem működik:</span><span class="sxs-lookup"><span data-stu-id="aa69b-127">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span>
- <span data-ttu-id="aa69b-128">Egy másik szervezetből származó felhasználónak a kulcstár kezeléséhez való hozzáférése.</span><span class="sxs-lookup"><span data-stu-id="aa69b-128">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="aa69b-129">Mindegyik szervezetnek saját címtára van.</span><span class="sxs-lookup"><span data-stu-id="aa69b-129">Each organization has its own directory.</span></span>
- <span data-ttu-id="aa69b-130">Azure-fiókja több könyvtárral rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="aa69b-130">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="aa69b-131">Ha nem az alapértelmezett címtárban regisztrál egy alkalmazást, akkor nem engedélyezheti az alkalmazásnak a kulcstár használatát.</span><span class="sxs-lookup"><span data-stu-id="aa69b-131">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="aa69b-132">Az alkalmazásnak az alapértelmezett címtárban kell lennie.</span><span class="sxs-lookup"><span data-stu-id="aa69b-132">The application must be in the default directory.</span></span>
<span data-ttu-id="aa69b-133">Vegye figyelembe, hogy bár az erőforráscsoport megadása nem kötelező ehhez a parancsmaghoz, a jobb teljesítmény érdekében ezt kell megtennie.</span><span class="sxs-lookup"><span data-stu-id="aa69b-133">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

> [!NOTE]
> <span data-ttu-id="aa69b-134">Amikor egyszerű szolgáltatásnév használatával hozzáférési házirend-engedélyeket ad meg, a paramétert kell `-BypassObjectIdValidation` használnia.</span><span class="sxs-lookup"><span data-stu-id="aa69b-134">When using a service principal to grant access policy permissions, you must use the `-BypassObjectIdValidation` parameter.</span></span>

## <span data-ttu-id="aa69b-135">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="aa69b-135">EXAMPLES</span></span>

### <span data-ttu-id="aa69b-136">1. példa: Engedélyek megadása egy felhasználónak egy kulcstárhoz és az engedélyek módosítása</span><span class="sxs-lookup"><span data-stu-id="aa69b-136">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
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

<span data-ttu-id="aa69b-137">Az első parancs engedélyeket ad egy felhasználónak az Azure Active Directoryban, hogy műveleteket hajtson végre a kulcsokon és a titkosságon PattiFuller@contoso.com a Contoso03Vault nevű kulcstárban.</span><span class="sxs-lookup"><span data-stu-id="aa69b-137">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span> <span data-ttu-id="aa69b-138">A *PassThru paraméter* eredménye a frissített objektum, amelyet a parancsmag ad vissza.</span><span class="sxs-lookup"><span data-stu-id="aa69b-138">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>
<span data-ttu-id="aa69b-139">A második parancs módosítja az első parancsban megadott engedélyeket, hogy mostantól a beállításukon és törlésüken kívül titkosságokat is PattiFuller@contoso.com bevessen.</span><span class="sxs-lookup"><span data-stu-id="aa69b-139">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="aa69b-140">A kulcsműveletekkel kapcsolatos engedélyek a parancs után is változatlanok maradnak.</span><span class="sxs-lookup"><span data-stu-id="aa69b-140">The permissions to key operations remain unchanged after this command.</span></span>
<span data-ttu-id="aa69b-141">Az utolsó parancs tovább módosítja a kulcsműveletekkel kapcsolatos összes engedély eltávolítására vonatkozó PattiFuller@contoso.com meglévő engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="aa69b-141">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="aa69b-142">A titkos műveletekre vonatkozó engedélyek a parancs után is változatlanok maradnak.</span><span class="sxs-lookup"><span data-stu-id="aa69b-142">The permissions to secret operations remain unchanged after this command.</span></span>

### <span data-ttu-id="aa69b-143">2. példa: Engedélyek megadása egyszerű alkalmazásszolgáltatásnak a titkos kulcsok olvasására és írására</span><span class="sxs-lookup"><span data-stu-id="aa69b-143">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="aa69b-144">Ez a parancs engedélyeket ad az alkalmazásokhoz a Contoso03Vault nevű kulcstárhoz.</span><span class="sxs-lookup"><span data-stu-id="aa69b-144">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span>
<span data-ttu-id="aa69b-145">A *ServicePrincipalName paraméter* megadja az alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="aa69b-145">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="aa69b-146">Az alkalmazásnak regisztrálva kell lennie az Azure Active Directoryban.</span><span class="sxs-lookup"><span data-stu-id="aa69b-146">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="aa69b-147">A *ServicePrincipalName* paraméter értékének vagy az alkalmazás egyszerű szolgáltatásnevének vagy az alkalmazásazonosító GUID azonosítójának kell lennie.</span><span class="sxs-lookup"><span data-stu-id="aa69b-147">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>
<span data-ttu-id="aa69b-148">Ebben a példában az egyszerű szolgáltatásnevet adhatja meg, és a parancs hozzáférési engedélyt ad az alkalmazásnak a titkos kulcsok `http://payroll.contoso.com` olvasására és írására.</span><span class="sxs-lookup"><span data-stu-id="aa69b-148">This example specifies the service principal name `http://payroll.contoso.com`, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="aa69b-149">3. példa: Engedélyek megadása egy alkalmazáshoz az objektumazonosító használatával</span><span class="sxs-lookup"><span data-stu-id="aa69b-149">Example 3: Grant permissions for an application using its object ID</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="aa69b-150">Ez a parancs hozzáférési engedélyt ad az alkalmazásnak a titkos kulcsok olvasására és írására.</span><span class="sxs-lookup"><span data-stu-id="aa69b-150">This command grants the application permissions to read and write secrets.</span></span>
<span data-ttu-id="aa69b-151">Ebben a példában az alkalmazás az alkalmazás egyszerű szolgáltatásnévének objektumazonosítóját használja.</span><span class="sxs-lookup"><span data-stu-id="aa69b-151">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="aa69b-152">4. példa: Egyszerű felhasználónév engedélyeinek megadása</span><span class="sxs-lookup"><span data-stu-id="aa69b-152">Example 4: Grant permissions for a user principal name</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="aa69b-153">Ez a parancs hozzáférési, lista- és beállítási engedélyeket ad a megadott egyszerű felhasználónévhez a titkos információkhoz való hozzáféréshez.</span><span class="sxs-lookup"><span data-stu-id="aa69b-153">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="aa69b-154">5. példa: Annak engedélyezése, hogy a Microsoft.Compute erőforrásszolgáltató beolvassa a titkos adatokat egy kulcstárból</span><span class="sxs-lookup"><span data-stu-id="aa69b-154">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="aa69b-155">Ez a parancs megadja a Microsoft.Compute erőforrásszolgáltatója által a Contoso03Vault kulcstárból beolvasandó titkos információkhoz szükséges engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="aa69b-155">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="aa69b-156">6. példa: Engedélyek megadása biztonsági csoportnak</span><span class="sxs-lookup"><span data-stu-id="aa69b-156">Example 6: Grant permissions to a security group</span></span>
```powershell
PS C:\> Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys get, set -PermissionsToSecrets get, set
```

<span data-ttu-id="aa69b-157">Az első parancs a Get-AzADGroup parancsmagot használja az összes Active Directory-csoport be szerezni.</span><span class="sxs-lookup"><span data-stu-id="aa69b-157">The first command uses the Get-AzADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="aa69b-158">A kimenetben 3 visszaadott csoport látható, a **csoport1,** **a csoport2** és a **csoport3.**</span><span class="sxs-lookup"><span data-stu-id="aa69b-158">From the output, you see 3 groups returned, named **group1**, **group2**, and **group3**.</span></span> <span data-ttu-id="aa69b-159">Több csoportnak lehet ugyanaz a neve, de mindig egyedi ObjectId azonosítóval rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="aa69b-159">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="aa69b-160">Ha több, azonos nevű csoportot ad vissza, a kimenetben az ObjectId érték használatával azonosítsa a használni kívánt csoportot.</span><span class="sxs-lookup"><span data-stu-id="aa69b-160">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>
<span data-ttu-id="aa69b-161">Ezután használhatja a parancs kimenetét a Set-AzKeyVaultAccessPolicy, hogy engedélyeket adjon a group2 kulcstárának **(myownvault) számára.**</span><span class="sxs-lookup"><span data-stu-id="aa69b-161">You then use the output of this command with Set-AzKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="aa69b-162">Az alábbi példa a "group2" nevű csoportokat számba veszi ugyanabban a parancssorban.</span><span class="sxs-lookup"><span data-stu-id="aa69b-162">This example enumerates the groups named 'group2' inline in the same command line.</span></span>
<span data-ttu-id="aa69b-163">A visszaadott listában több "csoport2" nevű csoport is lehet.</span><span class="sxs-lookup"><span data-stu-id="aa69b-163">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="aa69b-164">Ez a példa a visszaadott listában a 0 index által jelzett \[ \] elsőt választja ki.</span><span class="sxs-lookup"><span data-stu-id="aa69b-164">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="aa69b-165">7. példa: Azure Information Protection-hozzáférés megadása az ügyfél által kezelt bérlői kulcshoz (BYOK)</span><span class="sxs-lookup"><span data-stu-id="aa69b-165">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="aa69b-166">Ez a parancs engedélyezi az Azure Information Protectionnek, hogy az Azure Information Protection bérlői kulcsként ügyfél által kezelt kulcsot (a saját kulcsát hozza magával, vagy a "BYOK" esetet) használjon.</span><span class="sxs-lookup"><span data-stu-id="aa69b-166">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>
<span data-ttu-id="aa69b-167">A parancs futtatásakor adja meg a saját kulcstárnevét, de meg kell adnia a *ServicePrincipalName* paramétert a GUID **00000012-0000-0000-c000-000000000000000** azonosítóval, és meg kell adnia a példában az engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="aa69b-167">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="aa69b-168">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa69b-168">PARAMETERS</span></span>

### <span data-ttu-id="aa69b-169">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="aa69b-169">-ApplicationId</span></span>
<span data-ttu-id="aa69b-170">Későbbi használatra.</span><span class="sxs-lookup"><span data-stu-id="aa69b-170">For future use.</span></span>

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

### <span data-ttu-id="aa69b-171">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="aa69b-171">-BypassObjectIdValidation</span></span>
<span data-ttu-id="aa69b-172">Lehetővé teszi az objektumazonosítók megadását anélkül, hogy érvényesíte volna az objektum Azure Active Directoryban való létezik-e.</span><span class="sxs-lookup"><span data-stu-id="aa69b-172">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>
<span data-ttu-id="aa69b-173">Ezt a paramétert csak akkor használja, ha hozzáférést szeretne a kulcstárhoz egy olyan objektumazonosítóhoz, amely egy másik Azure-bérlő delegált biztonsági csoportjára hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="aa69b-173">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

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

### <span data-ttu-id="aa69b-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa69b-174">-DefaultProfile</span></span>
<span data-ttu-id="aa69b-175">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="aa69b-175">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa69b-176">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="aa69b-176">-EmailAddress</span></span>
<span data-ttu-id="aa69b-177">Annak a felhasználónak az e-mail-címét adja meg, akinek engedélyt kell kiadó felhasználónak.</span><span class="sxs-lookup"><span data-stu-id="aa69b-177">Specifies the user email address of the user to whom to grant permissions.</span></span>
<span data-ttu-id="aa69b-178">Ennek az e-mail-címnek az aktuális előfizetéshez társított címtárban kell lennie, és egyedinek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="aa69b-178">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

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

### <span data-ttu-id="aa69b-179">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="aa69b-179">-EnabledForDeployment</span></span>
<span data-ttu-id="aa69b-180">Lehetővé teszi a Microsoft.Compute erőforrásszolgáltatónak, hogy beolvassa a titkos értékeket ebből a kulcstárból, amikor erre a kulcstárra hivatkozik az erőforrás-létrehozás során, például virtuális gép létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="aa69b-180">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="aa69b-181">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="aa69b-181">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="aa69b-182">Lehetővé teszi az Azure lemeztitkosítási szolgáltatásának, hogy titkos adatokat és kulcsokat olvasson le ebből a kulcstárból.</span><span class="sxs-lookup"><span data-stu-id="aa69b-182">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="aa69b-183">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="aa69b-183">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="aa69b-184">Lehetővé teszi az Azure Resource Manager számára, hogy titkos titkos szolgáltatásokat rejtsen ebből a kulcstárból, amikor erre a kulcstárra hivatkozik egy sablon központi telepítésében.</span><span class="sxs-lookup"><span data-stu-id="aa69b-184">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="aa69b-185">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa69b-185">-InputObject</span></span>
<span data-ttu-id="aa69b-186">Key Vault objektum</span><span class="sxs-lookup"><span data-stu-id="aa69b-186">Key Vault Object</span></span>

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

### <span data-ttu-id="aa69b-187">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="aa69b-187">-ObjectId</span></span>
<span data-ttu-id="aa69b-188">Annak a felhasználónak vagy szolgáltatásnévnek az objektumazonosítóját adja meg az Azure Active Directoryban, amelynek az engedélyét meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="aa69b-188">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

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

### <span data-ttu-id="aa69b-189">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa69b-189">-PassThru</span></span>
<span data-ttu-id="aa69b-190">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="aa69b-190">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="aa69b-191">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="aa69b-191">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="aa69b-192">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="aa69b-192">-PermissionsToCertificates</span></span>
<span data-ttu-id="aa69b-193">Egy felhasználónak vagy egyszerű szolgáltatásnak adható tanúsítványengedélyek tömbje.</span><span class="sxs-lookup"><span data-stu-id="aa69b-193">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="aa69b-194">A paraméter elfogadható értékei:</span><span class="sxs-lookup"><span data-stu-id="aa69b-194">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="aa69b-195">Bej.le</span><span class="sxs-lookup"><span data-stu-id="aa69b-195">Get</span></span>
- <span data-ttu-id="aa69b-196">Lista</span><span class="sxs-lookup"><span data-stu-id="aa69b-196">List</span></span>
- <span data-ttu-id="aa69b-197">Törlés</span><span class="sxs-lookup"><span data-stu-id="aa69b-197">Delete</span></span>
- <span data-ttu-id="aa69b-198">Létrehozás</span><span class="sxs-lookup"><span data-stu-id="aa69b-198">Create</span></span>
- <span data-ttu-id="aa69b-199">Importálás</span><span class="sxs-lookup"><span data-stu-id="aa69b-199">Import</span></span>
- <span data-ttu-id="aa69b-200">Frissítés</span><span class="sxs-lookup"><span data-stu-id="aa69b-200">Update</span></span>
- <span data-ttu-id="aa69b-201">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="aa69b-201">Managecontacts</span></span>
- <span data-ttu-id="aa69b-202">Getissuers</span><span class="sxs-lookup"><span data-stu-id="aa69b-202">Getissuers</span></span>
- <span data-ttu-id="aa69b-203">Listissuers</span><span class="sxs-lookup"><span data-stu-id="aa69b-203">Listissuers</span></span>
- <span data-ttu-id="aa69b-204">Setissuers</span><span class="sxs-lookup"><span data-stu-id="aa69b-204">Setissuers</span></span>
- <span data-ttu-id="aa69b-205">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="aa69b-205">Deleteissuers</span></span>
- <span data-ttu-id="aa69b-206">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="aa69b-206">Manageissuers</span></span>
- <span data-ttu-id="aa69b-207">Helyreállítás</span><span class="sxs-lookup"><span data-stu-id="aa69b-207">Recover</span></span>
- <span data-ttu-id="aa69b-208">Biztonsági másolat</span><span class="sxs-lookup"><span data-stu-id="aa69b-208">Backup</span></span>
- <span data-ttu-id="aa69b-209">Visszaállítás</span><span class="sxs-lookup"><span data-stu-id="aa69b-209">Restore</span></span>
- <span data-ttu-id="aa69b-210">Végleges végleges végleges</span><span class="sxs-lookup"><span data-stu-id="aa69b-210">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, backup, restore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa69b-211">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="aa69b-211">-PermissionsToKeys</span></span>
<span data-ttu-id="aa69b-212">Egy felhasználónak vagy egyszerű szolgáltatásnak adható kulcsműveleti engedélyek tömbje.</span><span class="sxs-lookup"><span data-stu-id="aa69b-212">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="aa69b-213">A paraméter elfogadható értékei:</span><span class="sxs-lookup"><span data-stu-id="aa69b-213">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="aa69b-214">Visszafejtése</span><span class="sxs-lookup"><span data-stu-id="aa69b-214">Decrypt</span></span>
- <span data-ttu-id="aa69b-215">Titkosítás</span><span class="sxs-lookup"><span data-stu-id="aa69b-215">Encrypt</span></span>
- <span data-ttu-id="aa69b-216">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="aa69b-216">UnwrapKey</span></span>
- <span data-ttu-id="aa69b-217">WrapKey</span><span class="sxs-lookup"><span data-stu-id="aa69b-217">WrapKey</span></span>
- <span data-ttu-id="aa69b-218">Ellenőrzés</span><span class="sxs-lookup"><span data-stu-id="aa69b-218">Verify</span></span>
- <span data-ttu-id="aa69b-219">Aláírás</span><span class="sxs-lookup"><span data-stu-id="aa69b-219">Sign</span></span>
- <span data-ttu-id="aa69b-220">Bej.le</span><span class="sxs-lookup"><span data-stu-id="aa69b-220">Get</span></span>
- <span data-ttu-id="aa69b-221">Lista</span><span class="sxs-lookup"><span data-stu-id="aa69b-221">List</span></span>
- <span data-ttu-id="aa69b-222">Frissítés</span><span class="sxs-lookup"><span data-stu-id="aa69b-222">Update</span></span>
- <span data-ttu-id="aa69b-223">Létrehozás</span><span class="sxs-lookup"><span data-stu-id="aa69b-223">Create</span></span>
- <span data-ttu-id="aa69b-224">Importálás</span><span class="sxs-lookup"><span data-stu-id="aa69b-224">Import</span></span>
- <span data-ttu-id="aa69b-225">Törlés</span><span class="sxs-lookup"><span data-stu-id="aa69b-225">Delete</span></span>
- <span data-ttu-id="aa69b-226">Biztonsági másolat</span><span class="sxs-lookup"><span data-stu-id="aa69b-226">Backup</span></span>
- <span data-ttu-id="aa69b-227">Visszaállítás</span><span class="sxs-lookup"><span data-stu-id="aa69b-227">Restore</span></span>
- <span data-ttu-id="aa69b-228">Helyreállítás</span><span class="sxs-lookup"><span data-stu-id="aa69b-228">Recover</span></span>
- <span data-ttu-id="aa69b-229">Végleges végleges végleges</span><span class="sxs-lookup"><span data-stu-id="aa69b-229">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa69b-230">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="aa69b-230">-PermissionsToSecrets</span></span>
<span data-ttu-id="aa69b-231">Egy felhasználónak vagy egyszerű szolgáltatásnak adható titkos műveletekre vonatkozó engedélyek tömbje.</span><span class="sxs-lookup"><span data-stu-id="aa69b-231">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="aa69b-232">A paraméter elfogadható értékei:</span><span class="sxs-lookup"><span data-stu-id="aa69b-232">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="aa69b-233">Bej.le</span><span class="sxs-lookup"><span data-stu-id="aa69b-233">Get</span></span>
- <span data-ttu-id="aa69b-234">Lista</span><span class="sxs-lookup"><span data-stu-id="aa69b-234">List</span></span>
- <span data-ttu-id="aa69b-235">Beállítás</span><span class="sxs-lookup"><span data-stu-id="aa69b-235">Set</span></span>
- <span data-ttu-id="aa69b-236">Törlés</span><span class="sxs-lookup"><span data-stu-id="aa69b-236">Delete</span></span>
- <span data-ttu-id="aa69b-237">Biztonsági másolat</span><span class="sxs-lookup"><span data-stu-id="aa69b-237">Backup</span></span>
- <span data-ttu-id="aa69b-238">Visszaállítás</span><span class="sxs-lookup"><span data-stu-id="aa69b-238">Restore</span></span>
- <span data-ttu-id="aa69b-239">Helyreállítás</span><span class="sxs-lookup"><span data-stu-id="aa69b-239">Recover</span></span>
- <span data-ttu-id="aa69b-240">Végleges végleges végleges</span><span class="sxs-lookup"><span data-stu-id="aa69b-240">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, set, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa69b-241">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="aa69b-241">-PermissionsToStorage</span></span>
<span data-ttu-id="aa69b-242">A felügyelt tárfiókra és a SaS-definíciós műveletre vonatkozó engedélyeket adja meg, amelyek a felhasználónak vagy a szolgáltatásnévnek adhatók.</span><span class="sxs-lookup"><span data-stu-id="aa69b-242">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, recover, backup, restore, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa69b-243">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa69b-243">-ResourceGroupName</span></span>
<span data-ttu-id="aa69b-244">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa69b-244">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="aa69b-245">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa69b-245">-ResourceId</span></span>
<span data-ttu-id="aa69b-246">Key Vault Resource Id</span><span class="sxs-lookup"><span data-stu-id="aa69b-246">Key Vault Resource Id</span></span>

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

### <span data-ttu-id="aa69b-247">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="aa69b-247">-ServicePrincipalName</span></span>
<span data-ttu-id="aa69b-248">Annak az alkalmazásnak a egyszerű szolgáltatásnevét adja meg, amelyhez engedélyeket ad.</span><span class="sxs-lookup"><span data-stu-id="aa69b-248">Specifies the service principal name of the application to which to grant permissions.</span></span>
<span data-ttu-id="aa69b-249">Adja meg az alkalmazáshoz az AzureActive Directoryban regisztrált alkalmazásazonosítót ( más néven ügyfélazonosítót).</span><span class="sxs-lookup"><span data-stu-id="aa69b-249">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="aa69b-250">A paraméterként megadott egyszerű szolgáltatásnévvel megadott alkalmazást az aktuális előfizetést tartalmazó Azure-címtárban kell regisztrálni.</span><span class="sxs-lookup"><span data-stu-id="aa69b-250">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

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

### <span data-ttu-id="aa69b-251">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="aa69b-251">-UserPrincipalName</span></span>
<span data-ttu-id="aa69b-252">Annak a felhasználónak a felhasználó egyszerű felhasználónevét adja meg, akinek az engedélyeket ki kell ad.</span><span class="sxs-lookup"><span data-stu-id="aa69b-252">Specifies the user principal name of the user to whom to grant permissions.</span></span>
<span data-ttu-id="aa69b-253">Az egyszerű felhasználónévnek az aktuális előfizetéshez társított címtárban kell lennie.</span><span class="sxs-lookup"><span data-stu-id="aa69b-253">This user principal name must exist in the directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="aa69b-254">-VaultName</span><span class="sxs-lookup"><span data-stu-id="aa69b-254">-VaultName</span></span>
<span data-ttu-id="aa69b-255">Egy kulcstár nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa69b-255">Specifies the name of a key vault.</span></span>
<span data-ttu-id="aa69b-256">Ez a parancsmag módosítja a paraméter által megadott kulcstár hozzáférési házirendját.</span><span class="sxs-lookup"><span data-stu-id="aa69b-256">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="aa69b-257">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa69b-257">-Confirm</span></span>
<span data-ttu-id="aa69b-258">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="aa69b-258">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa69b-259">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa69b-259">-WhatIf</span></span>
<span data-ttu-id="aa69b-260">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="aa69b-260">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aa69b-261">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aa69b-261">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa69b-262">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa69b-262">CommonParameters</span></span>
<span data-ttu-id="aa69b-263">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa69b-263">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa69b-264">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa69b-264">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa69b-265">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aa69b-265">INPUTS</span></span>

### <span data-ttu-id="aa69b-266">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="aa69b-266">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="aa69b-267">System.String</span><span class="sxs-lookup"><span data-stu-id="aa69b-267">System.String</span></span>

## <span data-ttu-id="aa69b-268">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa69b-268">OUTPUTS</span></span>

### <span data-ttu-id="aa69b-269">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="aa69b-269">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="aa69b-270">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="aa69b-270">NOTES</span></span>

## <span data-ttu-id="aa69b-271">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa69b-271">RELATED LINKS</span></span>

[<span data-ttu-id="aa69b-272">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="aa69b-272">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="aa69b-273">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="aa69b-273">Remove-AzKeyVaultAccessPolicy</span></span>](./Remove-AzKeyVaultAccessPolicy.md)

