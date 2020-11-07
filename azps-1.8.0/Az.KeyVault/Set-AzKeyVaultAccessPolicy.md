---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: 55cdc385c5cdf291db15399f4fd587b9b10ce308
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "93851030"
---
# <span data-ttu-id="d03e8-101">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d03e8-101">Set-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="d03e8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d03e8-102">SYNOPSIS</span></span>
<span data-ttu-id="d03e8-103">Meglévő engedélyeket ad vagy módosít a felhasználó, az alkalmazás vagy a biztonsági csoport számára a fő boltozattal végzett műveletek elvégzéséhez.</span><span class="sxs-lookup"><span data-stu-id="d03e8-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

## <span data-ttu-id="d03e8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d03e8-104">SYNTAX</span></span>

### <span data-ttu-id="d03e8-105">ByUserPrincipalName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d03e8-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d03e8-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="d03e8-106">ByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d03e8-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="d03e8-107">ByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d03e8-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="d03e8-108">ByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d03e8-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="d03e8-109">ForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d03e8-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="d03e8-110">InputObjectByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d03e8-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="d03e8-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d03e8-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d03e8-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d03e8-113">InputObjectByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="d03e8-113">InputObjectByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d03e8-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="d03e8-114">InputObjectForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d03e8-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="d03e8-115">ResourceIdByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d03e8-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="d03e8-116">ResourceIdByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d03e8-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d03e8-117">ResourceIdByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d03e8-118">ResourceIdByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="d03e8-118">ResourceIdByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d03e8-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="d03e8-119">ResourceIdForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d03e8-120">Leírás</span><span class="sxs-lookup"><span data-stu-id="d03e8-120">DESCRIPTION</span></span>
<span data-ttu-id="d03e8-121">A **set-AzKeyVaultAccessPolicy** parancsmag meglévő engedélyeket ad vagy módosít egy felhasználó, alkalmazás vagy biztonsági csoport számára, hogy a megadott műveleteket egy fő boltozattal végezze el.</span><span class="sxs-lookup"><span data-stu-id="d03e8-121">The **Set-AzKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="d03e8-122">Nem módosítja a többi felhasználó, alkalmazás vagy biztonsági csoport engedélyeit a kulcs boltozatán.</span><span class="sxs-lookup"><span data-stu-id="d03e8-122">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>
<span data-ttu-id="d03e8-123">Ha egy biztonsági csoportra vonatkozó engedélyeket állít be, ez a művelet csak a biztonsági csoport felhasználóit érinti.</span><span class="sxs-lookup"><span data-stu-id="d03e8-123">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>
<span data-ttu-id="d03e8-124">Az alábbi könyvtárak mindegyikének meg kell egyeznie az Azure-címtárral:</span><span class="sxs-lookup"><span data-stu-id="d03e8-124">The following directories must all be the same Azure directory:</span></span>
- <span data-ttu-id="d03e8-125">Annak az Azure-előfizetésnek az alapértelmezett könyvtára, amelyben a kulcs boltozata lakik.</span><span class="sxs-lookup"><span data-stu-id="d03e8-125">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="d03e8-126">Az Azure-címtár, amely az engedélyeket biztosító felhasználó vagy alkalmazás csoportját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d03e8-126">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>
<span data-ttu-id="d03e8-127">Példák azokra az esetekre, amikor ezek a feltételek nem teljesülnek, és a parancsmag nem fog működni:</span><span class="sxs-lookup"><span data-stu-id="d03e8-127">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span>
- <span data-ttu-id="d03e8-128">Másik szervezet felhasználóinak engedélyezése a kulcsfájl kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="d03e8-128">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="d03e8-129">Minden szervezetnek saját könyvtára van.</span><span class="sxs-lookup"><span data-stu-id="d03e8-129">Each organization has its own directory.</span></span>
- <span data-ttu-id="d03e8-130">Az Azure-fiók több könyvtárat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="d03e8-130">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="d03e8-131">Ha az alapértelmezett könyvtártól eltérő címtárban regisztrálja az alkalmazást, az alkalmazás nem engedélyezheti a kulcsfájl használatát.</span><span class="sxs-lookup"><span data-stu-id="d03e8-131">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="d03e8-132">Az alkalmazásnak az alapértelmezett címtárban kell lennie.</span><span class="sxs-lookup"><span data-stu-id="d03e8-132">The application must be in the default directory.</span></span>
<span data-ttu-id="d03e8-133">Fontos tudni, hogy bár az erőforráscsoport beállítása nem kötelező ehhez a parancsmaghoz, a jobb teljesítmény érdekében ezt el kell végeznie.</span><span class="sxs-lookup"><span data-stu-id="d03e8-133">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="d03e8-134">Példák</span><span class="sxs-lookup"><span data-stu-id="d03e8-134">EXAMPLES</span></span>

### <span data-ttu-id="d03e8-135">1. példa: engedélyek megadása egy felhasználó számára egy kulcs boltozatához és az engedélyek módosítása</span><span class="sxs-lookup"><span data-stu-id="d03e8-135">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
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

<span data-ttu-id="d03e8-136">Az első parancs engedélyeket ad az Azure Active Directory-beli felhasználóknak PattiFuller@contoso.com , hogy a Contoso03Vault nevű fő boltozattal végezze el a megfelelő műveleteket a kulcsok és a titkok területén.</span><span class="sxs-lookup"><span data-stu-id="d03e8-136">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span> <span data-ttu-id="d03e8-137">A *PassThru* paraméter a parancsmag által visszaadott frissített objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="d03e8-137">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>
<span data-ttu-id="d03e8-138">A második parancs módosítja az PattiFuller@contoso.com első parancsban megadott engedélyeket, így mostantól a beállítások megadásával és törlésével is lehetővé válik a titok beszerzése.</span><span class="sxs-lookup"><span data-stu-id="d03e8-138">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="d03e8-139">A fő műveletekre vonatkozó engedélyek a parancs után változatlanok maradnak.</span><span class="sxs-lookup"><span data-stu-id="d03e8-139">The permissions to key operations remain unchanged after this command.</span></span>
<span data-ttu-id="d03e8-140">A végleges parancs a meglévő engedélyeket tovább módosítja a PattiFuller@contoso.com legfontosabb műveletekhez tartozó összes engedély eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="d03e8-140">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="d03e8-141">A titkos műveletek engedélyei a parancs után változatlanok maradnak.</span><span class="sxs-lookup"><span data-stu-id="d03e8-141">The permissions to secret operations remain unchanged after this command.</span></span>

### <span data-ttu-id="d03e8-142">2. példa: az alkalmazásspecifikus szolgáltatók engedélyeinek megadása a titkok olvasásához és írásához</span><span class="sxs-lookup"><span data-stu-id="d03e8-142">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="d03e8-143">Ez a parancs engedélyeket ad az Contoso03Vault nevű fő Vault-alkalmazás engedélyeinek megadásához.</span><span class="sxs-lookup"><span data-stu-id="d03e8-143">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span>
<span data-ttu-id="d03e8-144">A *ServicePrincipalName* paraméter az alkalmazást adja meg.</span><span class="sxs-lookup"><span data-stu-id="d03e8-144">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="d03e8-145">Az alkalmazást be kell jegyeztetni az Azure Active Directoryban.</span><span class="sxs-lookup"><span data-stu-id="d03e8-145">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="d03e8-146">A *ServicePrincipalName* paraméter értéke csak az alkalmazás egyszerű szolgáltatásnév, vagy az ALKALMAZÁSSPECIFIKUS azonosító GUID értéke lehet.</span><span class="sxs-lookup"><span data-stu-id="d03e8-146">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>
<span data-ttu-id="d03e8-147">Ez a példa megadja az egyszerű szolgáltatásnév nevet `http://payroll.contoso.com` , és a parancs a titok olvasását és írását biztosítja az alkalmazás engedélyeinek.</span><span class="sxs-lookup"><span data-stu-id="d03e8-147">This example specifies the service principal name `http://payroll.contoso.com`, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="d03e8-148">3. példa: az alkalmazás engedélyeinek megadása az objektum azonosítójával</span><span class="sxs-lookup"><span data-stu-id="d03e8-148">Example 3: Grant permissions for an application using its object ID</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="d03e8-149">A parancs a titok olvasását és írását lehetővé tévő jogosultságokkal ruházza fel az alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="d03e8-149">This command grants the application permissions to read and write secrets.</span></span>
<span data-ttu-id="d03e8-150">Ez a példa azt adja meg, hogy az alkalmazás az alkalmazás Principal azonosítójával használja az alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="d03e8-150">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="d03e8-151">4. példa: engedélyek megadása egyszerű felhasználónévhez</span><span class="sxs-lookup"><span data-stu-id="d03e8-151">Example 4: Grant permissions for a user principal name</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="d03e8-152">Ez a parancs a beszerzés, a lista és az engedélyek beállítását adja meg a megadott egyszerű felhasználónévhez a titok eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="d03e8-152">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="d03e8-153">Példa: 5: a Microsoft. számítási erőforrás-szolgáltatónál a kulcsok beolvasásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="d03e8-153">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="d03e8-154">Ez a parancs megadja a titoknak azokat az engedélyeit, amelyeket a Microsoft. számítási erőforrás-szolgáltatótól kapott a Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="d03e8-154">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="d03e8-155">6. példa: engedélyek megadása egy biztonsági csoporthoz</span><span class="sxs-lookup"><span data-stu-id="d03e8-155">Example 6: Grant permissions to a security group</span></span>
```powershell
PS C:\> Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys get, set -PermissionsToSecrets get, set
```

<span data-ttu-id="d03e8-156">Az első parancs az Get-AzADGroup parancsmagot használja az Active Directory-csoportok beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="d03e8-156">The first command uses the Get-AzADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="d03e8-157">A kimenetben 3 csoport, a **Group1** , az **Group2** és a **Group3** nevű csoport látható.</span><span class="sxs-lookup"><span data-stu-id="d03e8-157">From the output, you see 3 groups returned, named **group1** , **group2** , and **group3**.</span></span> <span data-ttu-id="d03e8-158">Több csoportnak ugyanazt a nevet kell használnia, de minden esetben egyedi ObjectId kell lennie.</span><span class="sxs-lookup"><span data-stu-id="d03e8-158">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="d03e8-159">Ha egynél több, ugyanazt a nevet tartalmazó csoportot ad eredményül, a kimenetben lévő ObjectId segítségével határozza meg, hogy melyiket szeretné használni.</span><span class="sxs-lookup"><span data-stu-id="d03e8-159">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>
<span data-ttu-id="d03e8-160">Ezután a parancs kimenete Set-AzKeyVaultAccessPolicy segítségével engedélyeket adhat a Group2, a **myownvault** nevű kulcshoz.</span><span class="sxs-lookup"><span data-stu-id="d03e8-160">You then use the output of this command with Set-AzKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="d03e8-161">Ez a példa a "Group2" szövegközi csoportokat ugyanazon a parancssorban sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="d03e8-161">This example enumerates the groups named 'group2' inline in the same command line.</span></span>
<span data-ttu-id="d03e8-162">Előfordulhat, hogy a visszaadott lista több olyan csoportba tartozik, amely "Group2" névvel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="d03e8-162">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="d03e8-163">Ez a példa a \[ visszatérési listában az első indexet jelölte ki \] .</span><span class="sxs-lookup"><span data-stu-id="d03e8-163">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="d03e8-164">7. példa: hozzáférés biztosítása az Azure Information Protectionhez az ügyfél által felügyelt bérlői kulcshoz (BYOK)</span><span class="sxs-lookup"><span data-stu-id="d03e8-164">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="d03e8-165">Ez a parancs engedélyezi az Azure Information Protectiont az ügyfél által felügyelt kulcs (a saját kulcs vagy a "BYOK" forgatókönyv) használatához az Azure Information Protection bérlői kulccsal.</span><span class="sxs-lookup"><span data-stu-id="d03e8-165">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>
<span data-ttu-id="d03e8-166">Ha futtatja ezt a parancsot, adja meg a saját kulcs boltozatát, de meg kell adnia a *ServicePrincipalName* paramétert a GUID **00000012-0000-0000 – C000 – 000000000000 értéket** , és meg kell adnia a példában szereplő engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="d03e8-166">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="d03e8-167">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d03e8-167">PARAMETERS</span></span>

### <span data-ttu-id="d03e8-168">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d03e8-168">-ApplicationId</span></span>
<span data-ttu-id="d03e8-169">Jövőbeli használatra.</span><span class="sxs-lookup"><span data-stu-id="d03e8-169">For future use.</span></span>

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

### <span data-ttu-id="d03e8-170">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="d03e8-170">-BypassObjectIdValidation</span></span>
<span data-ttu-id="d03e8-171">Lehetővé teszi az objektumazonosítók megadását anélkül, hogy az az Azure Active Directoryban létezik.</span><span class="sxs-lookup"><span data-stu-id="d03e8-171">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>
<span data-ttu-id="d03e8-172">Csak akkor használja ezt a paramétert, ha hozzáférést szeretne adni a kulcsfájl egy olyan objektum-AZONOSÍTÓhoz, amely egy másik Azure-bérlőtől származó meghatalmazott biztonsági csoportra hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="d03e8-172">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

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

### <span data-ttu-id="d03e8-173">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d03e8-173">-DefaultProfile</span></span>
<span data-ttu-id="d03e8-174">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d03e8-174">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d03e8-175">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="d03e8-175">-EmailAddress</span></span>
<span data-ttu-id="d03e8-176">Annak a felhasználónak a felhasználói e-mail-címét adja meg, akinek engedélyt szeretne adni.</span><span class="sxs-lookup"><span data-stu-id="d03e8-176">Specifies the user email address of the user to whom to grant permissions.</span></span>
<span data-ttu-id="d03e8-177">Ennek az e-mail-címnek meg kell egyeznie az aktuális előfizetéshez társított címtárban, és egyedinek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="d03e8-177">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

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

### <span data-ttu-id="d03e8-178">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="d03e8-178">-EnabledForDeployment</span></span>
<span data-ttu-id="d03e8-179">A Microsoft. számítási erőforrás-szolgáltatója kinyerheti a titkokat ebből a kulcsfájlból, ha ez a kulcs boltozata az erőforrás létrehozásakor, például virtuális gép létrehozásakor jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="d03e8-179">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="d03e8-180">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="d03e8-180">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="d03e8-181">Lehetővé teszi, hogy az Azure Disk Encryption szolgáltatás a kulcsok kijavítását és kicsomagolását a kulcsból.</span><span class="sxs-lookup"><span data-stu-id="d03e8-181">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="d03e8-182">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="d03e8-182">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="d03e8-183">Lehetővé teszi az Azure Resource Manager számára, hogy ebből a kulcsfájlból kiírja a titkot, ha ezt a kulcspárt a sablonok központi telepítéséhez hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="d03e8-183">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="d03e8-184">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d03e8-184">-InputObject</span></span>
<span data-ttu-id="d03e8-185">Fő pince objektum</span><span class="sxs-lookup"><span data-stu-id="d03e8-185">Key Vault Object</span></span>

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

### <span data-ttu-id="d03e8-186">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d03e8-186">-ObjectId</span></span>
<span data-ttu-id="d03e8-187">Annak az Azure Active Directory-fióknak az objektum-AZONOSÍTÓját adja meg, amelyre engedélyt szeretne adni.</span><span class="sxs-lookup"><span data-stu-id="d03e8-187">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

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

### <span data-ttu-id="d03e8-188">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d03e8-188">-PassThru</span></span>
<span data-ttu-id="d03e8-189">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="d03e8-189">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d03e8-190">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="d03e8-190">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d03e8-191">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="d03e8-191">-PermissionsToCertificates</span></span>
<span data-ttu-id="d03e8-192">A felhasználók vagy a szolgáltatók számára megadható tanúsítvány-engedélyek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d03e8-192">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="d03e8-193">A paraméter elfogadható értékei:</span><span class="sxs-lookup"><span data-stu-id="d03e8-193">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="d03e8-194">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="d03e8-194">Get</span></span>
- <span data-ttu-id="d03e8-195">Lista</span><span class="sxs-lookup"><span data-stu-id="d03e8-195">List</span></span>
- <span data-ttu-id="d03e8-196">Törlése</span><span class="sxs-lookup"><span data-stu-id="d03e8-196">Delete</span></span>
- <span data-ttu-id="d03e8-197">Létrehozása</span><span class="sxs-lookup"><span data-stu-id="d03e8-197">Create</span></span>
- <span data-ttu-id="d03e8-198">Importálása</span><span class="sxs-lookup"><span data-stu-id="d03e8-198">Import</span></span>
- <span data-ttu-id="d03e8-199">Frissítés</span><span class="sxs-lookup"><span data-stu-id="d03e8-199">Update</span></span>
- <span data-ttu-id="d03e8-200">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="d03e8-200">Managecontacts</span></span>
- <span data-ttu-id="d03e8-201">Getissuers</span><span class="sxs-lookup"><span data-stu-id="d03e8-201">Getissuers</span></span>
- <span data-ttu-id="d03e8-202">Listissuers</span><span class="sxs-lookup"><span data-stu-id="d03e8-202">Listissuers</span></span>
- <span data-ttu-id="d03e8-203">Setissuers</span><span class="sxs-lookup"><span data-stu-id="d03e8-203">Setissuers</span></span>
- <span data-ttu-id="d03e8-204">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="d03e8-204">Deleteissuers</span></span>
- <span data-ttu-id="d03e8-205">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="d03e8-205">Manageissuers</span></span>
- <span data-ttu-id="d03e8-206">Visszaszerez</span><span class="sxs-lookup"><span data-stu-id="d03e8-206">Recover</span></span>
- <span data-ttu-id="d03e8-207">Hát</span><span class="sxs-lookup"><span data-stu-id="d03e8-207">Backup</span></span>
- <span data-ttu-id="d03e8-208">Visszaállítása</span><span class="sxs-lookup"><span data-stu-id="d03e8-208">Restore</span></span>
- <span data-ttu-id="d03e8-209">Véglegesen</span><span class="sxs-lookup"><span data-stu-id="d03e8-209">Purge</span></span>

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

### <span data-ttu-id="d03e8-210">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="d03e8-210">-PermissionsToKeys</span></span>
<span data-ttu-id="d03e8-211">A felhasználó vagy a szolgáltatás megbízójának megadni kívánt fő műveleti engedélyek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d03e8-211">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="d03e8-212">A paraméter elfogadható értékei:</span><span class="sxs-lookup"><span data-stu-id="d03e8-212">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="d03e8-213">Visszafejtése</span><span class="sxs-lookup"><span data-stu-id="d03e8-213">Decrypt</span></span>
- <span data-ttu-id="d03e8-214">Beavatkozik</span><span class="sxs-lookup"><span data-stu-id="d03e8-214">Encrypt</span></span>
- <span data-ttu-id="d03e8-215">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="d03e8-215">UnwrapKey</span></span>
- <span data-ttu-id="d03e8-216">WrapKey</span><span class="sxs-lookup"><span data-stu-id="d03e8-216">WrapKey</span></span>
- <span data-ttu-id="d03e8-217">Ellenőrizze</span><span class="sxs-lookup"><span data-stu-id="d03e8-217">Verify</span></span>
- <span data-ttu-id="d03e8-218">Jel</span><span class="sxs-lookup"><span data-stu-id="d03e8-218">Sign</span></span>
- <span data-ttu-id="d03e8-219">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="d03e8-219">Get</span></span>
- <span data-ttu-id="d03e8-220">Lista</span><span class="sxs-lookup"><span data-stu-id="d03e8-220">List</span></span>
- <span data-ttu-id="d03e8-221">Frissítés</span><span class="sxs-lookup"><span data-stu-id="d03e8-221">Update</span></span>
- <span data-ttu-id="d03e8-222">Létrehozása</span><span class="sxs-lookup"><span data-stu-id="d03e8-222">Create</span></span>
- <span data-ttu-id="d03e8-223">Importálása</span><span class="sxs-lookup"><span data-stu-id="d03e8-223">Import</span></span>
- <span data-ttu-id="d03e8-224">Törlése</span><span class="sxs-lookup"><span data-stu-id="d03e8-224">Delete</span></span>
- <span data-ttu-id="d03e8-225">Hát</span><span class="sxs-lookup"><span data-stu-id="d03e8-225">Backup</span></span>
- <span data-ttu-id="d03e8-226">Visszaállítása</span><span class="sxs-lookup"><span data-stu-id="d03e8-226">Restore</span></span>
- <span data-ttu-id="d03e8-227">Visszaszerez</span><span class="sxs-lookup"><span data-stu-id="d03e8-227">Recover</span></span>
- <span data-ttu-id="d03e8-228">Véglegesen</span><span class="sxs-lookup"><span data-stu-id="d03e8-228">Purge</span></span>

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

### <span data-ttu-id="d03e8-229">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="d03e8-229">-PermissionsToSecrets</span></span>
<span data-ttu-id="d03e8-230">A felhasználó vagy a szolgáltatás megbízójának megadni kívánt titkos műveleti engedélyek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d03e8-230">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="d03e8-231">A paraméter elfogadható értékei:</span><span class="sxs-lookup"><span data-stu-id="d03e8-231">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="d03e8-232">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="d03e8-232">Get</span></span>
- <span data-ttu-id="d03e8-233">Lista</span><span class="sxs-lookup"><span data-stu-id="d03e8-233">List</span></span>
- <span data-ttu-id="d03e8-234">Beállítása</span><span class="sxs-lookup"><span data-stu-id="d03e8-234">Set</span></span>
- <span data-ttu-id="d03e8-235">Törlése</span><span class="sxs-lookup"><span data-stu-id="d03e8-235">Delete</span></span>
- <span data-ttu-id="d03e8-236">Hát</span><span class="sxs-lookup"><span data-stu-id="d03e8-236">Backup</span></span>
- <span data-ttu-id="d03e8-237">Visszaállítása</span><span class="sxs-lookup"><span data-stu-id="d03e8-237">Restore</span></span>
- <span data-ttu-id="d03e8-238">Visszaszerez</span><span class="sxs-lookup"><span data-stu-id="d03e8-238">Recover</span></span>
- <span data-ttu-id="d03e8-239">Véglegesen</span><span class="sxs-lookup"><span data-stu-id="d03e8-239">Purge</span></span>

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

### <span data-ttu-id="d03e8-240">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="d03e8-240">-PermissionsToStorage</span></span>
<span data-ttu-id="d03e8-241">A felügyelt tárterület-fiók és a SaS-definíciós műveleti engedélyeket adja meg a felhasználó vagy a szolgáltatás megbízójának.</span><span class="sxs-lookup"><span data-stu-id="d03e8-241">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

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

### <span data-ttu-id="d03e8-242">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d03e8-242">-ResourceGroupName</span></span>
<span data-ttu-id="d03e8-243">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d03e8-243">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d03e8-244">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d03e8-244">-ResourceId</span></span>
<span data-ttu-id="d03e8-245">Fő pince-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="d03e8-245">Key Vault Resource Id</span></span>

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

### <span data-ttu-id="d03e8-246">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="d03e8-246">-ServicePrincipalName</span></span>
<span data-ttu-id="d03e8-247">Annak az alkalmazásnak az egyszerű szolgáltatásnevet adja meg, amelyre engedélyt szeretne adni.</span><span class="sxs-lookup"><span data-stu-id="d03e8-247">Specifies the service principal name of the application to which to grant permissions.</span></span>
<span data-ttu-id="d03e8-248">Adja meg az alkalmazáshoz az AzureActive-címtárban regisztrált alkalmazás-azonosítót (más néven ügyfél-azonosító).</span><span class="sxs-lookup"><span data-stu-id="d03e8-248">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="d03e8-249">A paraméter által megadott szolgáltatásnevet tartalmazó alkalmazásnak regisztrálnia kell a jelenlegi előfizetést tartalmazó Azure-címtárban.</span><span class="sxs-lookup"><span data-stu-id="d03e8-249">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

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

### <span data-ttu-id="d03e8-250">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d03e8-250">-UserPrincipalName</span></span>
<span data-ttu-id="d03e8-251">Annak a felhasználónak az egyszerű felhasználónevét adja meg, akinek engedélyt szeretne adni.</span><span class="sxs-lookup"><span data-stu-id="d03e8-251">Specifies the user principal name of the user to whom to grant permissions.</span></span>
<span data-ttu-id="d03e8-252">Ez az egyszerű felhasználónév csak az aktuális előfizetéshez társított címtárban található.</span><span class="sxs-lookup"><span data-stu-id="d03e8-252">This user principal name must exist in the directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="d03e8-253">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d03e8-253">-VaultName</span></span>
<span data-ttu-id="d03e8-254">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d03e8-254">Specifies the name of a key vault.</span></span>
<span data-ttu-id="d03e8-255">Ez a parancsmag módosítja a hozzáférési házirendet annak a kulcsfájl számára, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="d03e8-255">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="d03e8-256">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d03e8-256">-Confirm</span></span>
<span data-ttu-id="d03e8-257">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d03e8-257">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d03e8-258">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d03e8-258">-WhatIf</span></span>
<span data-ttu-id="d03e8-259">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d03e8-259">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d03e8-260">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d03e8-260">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d03e8-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d03e8-261">CommonParameters</span></span>
<span data-ttu-id="d03e8-262">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d03e8-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d03e8-263">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d03e8-263">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d03e8-264">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d03e8-264">INPUTS</span></span>

### <span data-ttu-id="d03e8-265">Microsoft. Azure. Command. PSKeyVaultIdentityItem. models.</span><span class="sxs-lookup"><span data-stu-id="d03e8-265">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="d03e8-266">System. String</span><span class="sxs-lookup"><span data-stu-id="d03e8-266">System.String</span></span>

## <span data-ttu-id="d03e8-267">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d03e8-267">OUTPUTS</span></span>

### <span data-ttu-id="d03e8-268">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="d03e8-268">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="d03e8-269">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d03e8-269">NOTES</span></span>

## <span data-ttu-id="d03e8-270">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d03e8-270">RELATED LINKS</span></span>

[<span data-ttu-id="d03e8-271">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="d03e8-271">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="d03e8-272">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d03e8-272">Remove-AzKeyVaultAccessPolicy</span></span>](./Remove-AzKeyVaultAccessPolicy.md)

