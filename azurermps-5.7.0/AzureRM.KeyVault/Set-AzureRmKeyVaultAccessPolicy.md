---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurermkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: 20a36e35c509ecca889d4059bd7e74ccafa22dc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494473"
---
# <span data-ttu-id="3b9f6-101">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3b9f6-101">Set-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="3b9f6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3b9f6-102">SYNOPSIS</span></span>
<span data-ttu-id="3b9f6-103">Meglévő engedélyeket ad vagy módosít a felhasználó, az alkalmazás vagy a biztonsági csoport számára a fő boltozattal végzett műveletek elvégzéséhez.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b9f6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3b9f6-104">SYNTAX</span></span>

### <span data-ttu-id="3b9f6-105">ByUserPrincipalName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3b9f6-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b9f6-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="3b9f6-106">ByObjectId</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b9f6-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="3b9f6-107">ByServicePrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b9f6-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="3b9f6-108">ByEmailAddress</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b9f6-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="3b9f6-109">ForVault</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b9f6-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="3b9f6-110">InputObjectByObjectId</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b9f6-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="3b9f6-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b9f6-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="3b9f6-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b9f6-113">InputObjectByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="3b9f6-113">InputObjectByEmailAddress</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b9f6-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="3b9f6-114">InputObjectForVault</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b9f6-115">Leírás</span><span class="sxs-lookup"><span data-stu-id="3b9f6-115">DESCRIPTION</span></span>
<span data-ttu-id="3b9f6-116">A **set-AzureRmKeyVaultAccessPolicy** parancsmag meglévő engedélyeket ad vagy módosít egy felhasználó, alkalmazás vagy biztonsági csoport számára, hogy a megadott műveleteket egy fő boltozattal végezze el.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-116">The **Set-AzureRmKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="3b9f6-117">Nem módosítja a többi felhasználó, alkalmazás vagy biztonsági csoport engedélyeit a kulcs boltozatán.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-117">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>

<span data-ttu-id="3b9f6-118">Ha egy biztonsági csoportra vonatkozó engedélyeket állít be, ez a művelet csak a biztonsági csoport felhasználóit érinti.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-118">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>

<span data-ttu-id="3b9f6-119">Az alábbi könyvtárak mindegyikének meg kell egyeznie az Azure-címtárral:</span><span class="sxs-lookup"><span data-stu-id="3b9f6-119">The following directories must all be the same Azure directory:</span></span> 
- <span data-ttu-id="3b9f6-120">Annak az Azure-előfizetésnek az alapértelmezett könyvtára, amelyben a kulcs boltozata lakik.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-120">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="3b9f6-121">Az Azure-címtár, amely az engedélyeket biztosító felhasználó vagy alkalmazás csoportját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-121">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>

<span data-ttu-id="3b9f6-122">Példák azokra az esetekre, amikor ezek a feltételek nem teljesülnek, és a parancsmag nem fog működni:</span><span class="sxs-lookup"><span data-stu-id="3b9f6-122">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span> 

- <span data-ttu-id="3b9f6-123">Másik szervezet felhasználóinak engedélyezése a kulcsfájl kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-123">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="3b9f6-124">Minden szervezetnek saját könyvtára van.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-124">Each organization has its own directory.</span></span> 
- <span data-ttu-id="3b9f6-125">Az Azure-fiók több könyvtárat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-125">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="3b9f6-126">Ha az alapértelmezett könyvtártól eltérő címtárban regisztrálja az alkalmazást, az alkalmazás nem engedélyezheti a kulcsfájl használatát.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-126">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="3b9f6-127">Az alkalmazásnak az alapértelmezett címtárban kell lennie.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-127">The application must be in the default directory.</span></span>

<span data-ttu-id="3b9f6-128">Fontos tudni, hogy bár az erőforráscsoport beállítása nem kötelező ehhez a parancsmaghoz, a jobb teljesítmény érdekében ezt el kell végeznie.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-128">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="3b9f6-129">Példák</span><span class="sxs-lookup"><span data-stu-id="3b9f6-129">EXAMPLES</span></span>

### <span data-ttu-id="3b9f6-130">1. példa: engedélyek megadása egy felhasználó számára egy kulcs boltozatához és az engedélyek módosítása</span><span class="sxs-lookup"><span data-stu-id="3b9f6-130">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets set,delete
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru
```

<span data-ttu-id="3b9f6-131">Az első parancs engedélyeket ad az Azure Active Directory-beli felhasználóknak PattiFuller@contoso.com , hogy a Contoso03Vault nevű fő boltozattal végezze el a megfelelő műveleteket a kulcsok és a titkok területén.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-131">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span>

<span data-ttu-id="3b9f6-132">A második parancs módosítja az PattiFuller@contoso.com első parancsban megadott engedélyeket, így mostantól a beállítások megadásával és törlésével is lehetővé válik a titok beszerzése.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-132">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="3b9f6-133">A fő műveletekre vonatkozó engedélyek a parancs után változatlanok maradnak.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-133">The permissions to key operations remain unchanged after this command.</span></span> <span data-ttu-id="3b9f6-134">A *PassThru* paraméter a parancsmag által visszaadott frissített objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-134">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

<span data-ttu-id="3b9f6-135">A végleges parancs a meglévő engedélyeket tovább módosítja a PattiFuller@contoso.com legfontosabb műveletekhez tartozó összes engedély eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-135">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="3b9f6-136">A titkos műveletek engedélyei a parancs után változatlanok maradnak.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-136">The permissions to secret operations remain unchanged after this command.</span></span> <span data-ttu-id="3b9f6-137">A *PassThru* paraméter a parancsmag által visszaadott frissített objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-137">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

### <span data-ttu-id="3b9f6-138">2. példa: az alkalmazásspecifikus szolgáltatók engedélyeinek megadása a titkok olvasásához és írásához</span><span class="sxs-lookup"><span data-stu-id="3b9f6-138">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="3b9f6-139">Ez a parancs engedélyeket ad az Contoso03Vault nevű fő Vault-alkalmazás engedélyeinek megadásához.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-139">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span> 

<span data-ttu-id="3b9f6-140">A *ServicePrincipalName* paraméter az alkalmazást adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-140">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="3b9f6-141">Az alkalmazást be kell jegyeztetni az Azure Active Directoryban.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-141">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="3b9f6-142">A *ServicePrincipalName* paraméter értéke csak az alkalmazás egyszerű szolgáltatásnév, vagy az ALKALMAZÁSSPECIFIKUS azonosító GUID értéke lehet.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-142">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>

<span data-ttu-id="3b9f6-143">Ez a példa megadja az egyszerű szolgáltatásnév nevet http://payroll.contoso.com , és a parancs a titok olvasását és írását biztosítja az alkalmazás engedélyeinek.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-143">This example specifies the service principal name http://payroll.contoso.com, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="3b9f6-144">3. példa: az alkalmazás engedélyeinek megadása az objektum azonosítójával</span><span class="sxs-lookup"><span data-stu-id="3b9f6-144">Example 3: Grant permissions for an application using its object ID</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="3b9f6-145">A parancs a titok olvasását és írását lehetővé tévő jogosultságokkal ruházza fel az alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-145">This command grants the application permissions to read and write secrets.</span></span>

<span data-ttu-id="3b9f6-146">Ez a példa azt adja meg, hogy az alkalmazás az alkalmazás Principal azonosítójával használja az alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-146">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="3b9f6-147">4. példa: engedélyek megadása egyszerű felhasználónévhez</span><span class="sxs-lookup"><span data-stu-id="3b9f6-147">Example 4: Grant permissions for a user principal name</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="3b9f6-148">Ez a parancs a beszerzés, a lista és az engedélyek beállítását adja meg a megadott egyszerű felhasználónévhez a titok eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-148">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="3b9f6-149">Példa: 5: a Microsoft. számítási erőforrás-szolgáltatónál a kulcsok beolvasásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-149">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="3b9f6-150">Ez a parancs megadja a titoknak azokat az engedélyeit, amelyeket a Microsoft. számítási erőforrás-szolgáltatótól kapott a Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-150">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="3b9f6-151">6. példa: engedélyek megadása egy biztonsági csoporthoz</span><span class="sxs-lookup"><span data-stu-id="3b9f6-151">Example 6: Grant permissions to a security group</span></span>
```
PS C:\>Get-AzureRmADGroup
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzureRmADGroup -SearchString 'group2')[0].Id -PermissionsToKeys All -PermissionsToSecrets All
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
group1                                                        96a0daa6-9841-4a9c-bdeb-e7062276c688
group2                                                        b8a401eb-63ad-4a30-b0e1-a7461969fe54
group3                                                        da07a6be-2c1e-4e42-934d-ceb57cf652b4
```

<span data-ttu-id="3b9f6-152">Az első parancs az Get-AzureRmADGroup parancsmagot használja az Active Directory-csoportok beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-152">The first command uses the Get-AzureRmADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="3b9f6-153">A kimenetben 3 csoport, a **Group1** , az **Group2** és a **Group3** nevű csoport látható.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-153">From the output, you see 3 groups returned, named **group1** , **group2** , and **group3**.</span></span> <span data-ttu-id="3b9f6-154">Több csoportnak ugyanazt a nevet kell használnia, de minden esetben egyedi ObjectId kell lennie.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-154">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="3b9f6-155">Ha egynél több, ugyanazt a nevet tartalmazó csoportot ad eredményül, a kimenetben lévő ObjectId segítségével határozza meg, hogy melyiket szeretné használni.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-155">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>

<span data-ttu-id="3b9f6-156">Ezután a parancs kimenete Set-AzureRmKeyVaultAccessPolicy segítségével engedélyeket adhat a Group2, a **myownvault** nevű kulcshoz.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-156">You then use the output of this command with Set-AzureRmKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="3b9f6-157">Ez a példa a "Group2" szövegközi csoportokat ugyanazon a parancssorban sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-157">This example enumerates the groups named 'group2' inline in the same command line.</span></span>

<span data-ttu-id="3b9f6-158">Előfordulhat, hogy a visszaadott lista több olyan csoportba tartozik, amely "Group2" névvel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-158">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="3b9f6-159">Ez a példa a \[ visszatérési listában az első indexet jelölte ki \] .</span><span class="sxs-lookup"><span data-stu-id="3b9f6-159">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="3b9f6-160">7. példa: hozzáférés biztosítása az Azure Information Protectionhez az ügyfél által felügyelt bérlői kulcshoz (BYOK)</span><span class="sxs-lookup"><span data-stu-id="3b9f6-160">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="3b9f6-161">Ez a parancs engedélyezi az Azure Information Protectiont az ügyfél által felügyelt kulcs (a saját kulcs vagy a "BYOK" forgatókönyv) használatához az Azure Information Protection bérlői kulccsal.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-161">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>

<span data-ttu-id="3b9f6-162">Ha futtatja ezt a parancsot, adja meg a saját kulcs boltozatát, de meg kell adnia a *ServicePrincipalName* paramétert a GUID **00000012-0000-0000 – C000 – 000000000000 értéket** , és meg kell adnia a példában szereplő engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-162">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="3b9f6-163">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3b9f6-163">PARAMETERS</span></span>

### <span data-ttu-id="3b9f6-164">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3b9f6-164">-ApplicationId</span></span>
<span data-ttu-id="3b9f6-165">Jövőbeli használatra.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-165">For future use.</span></span>

```yaml
Type: Guid
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b9f6-166">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="3b9f6-166">-BypassObjectIdValidation</span></span>
<span data-ttu-id="3b9f6-167">Lehetővé teszi az objektumazonosítók megadását anélkül, hogy az az Azure Active Directoryban létezik.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-167">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>

<span data-ttu-id="3b9f6-168">Csak akkor használja ezt a paramétert, ha hozzáférést szeretne adni a kulcsfájl egy olyan objektum-AZONOSÍTÓhoz, amely egy másik Azure-bérlőtől származó meghatalmazott biztonsági csoportra hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-168">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b9f6-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b9f6-169">-DefaultProfile</span></span>
<span data-ttu-id="3b9f6-170">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3b9f6-170">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9f6-171">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="3b9f6-171">-EmailAddress</span></span>
<span data-ttu-id="3b9f6-172">Annak a felhasználónak a felhasználói e-mail-címét adja meg, akinek engedélyt szeretne adni.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-172">Specifies the user email address of the user to whom to grant permissions.</span></span>

<span data-ttu-id="3b9f6-173">Ennek az e-mail-címnek meg kell egyeznie az aktuális előfizetéshez társított címtárban, és egyedinek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-173">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

```yaml
Type: String
Parameter Sets: ByEmailAddress, InputObjectByEmailAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b9f6-174">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="3b9f6-174">-EnabledForDeployment</span></span>
<span data-ttu-id="3b9f6-175">A Microsoft. számítási erőforrás-szolgáltatója kinyerheti a titkokat ebből a kulcsfájlból, ha ez a kulcs boltozata az erőforrás létrehozásakor, például virtuális gép létrehozásakor jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-175">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b9f6-176">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="3b9f6-176">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="3b9f6-177">Lehetővé teszi, hogy az Azure Disk Encryption szolgáltatás a kulcsok kijavítását és kicsomagolását a kulcsból.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-177">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b9f6-178">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="3b9f6-178">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="3b9f6-179">Lehetővé teszi az Azure Resource Manager számára, hogy ebből a kulcsfájlból kiírja a titkot, ha ezt a kulcspárt a sablonok központi telepítéséhez hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-179">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b9f6-180">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b9f6-180">-InputObject</span></span>
<span data-ttu-id="3b9f6-181">Fő pince objektum</span><span class="sxs-lookup"><span data-stu-id="3b9f6-181">Key Vault Object</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b9f6-182">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3b9f6-182">-ObjectId</span></span>
<span data-ttu-id="3b9f6-183">Annak az Azure Active Directory-fióknak az objektum-AZONOSÍTÓját adja meg, amelyre engedélyt szeretne adni.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-183">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b9f6-184">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b9f6-184">-PassThru</span></span>
<span data-ttu-id="3b9f6-185">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-185">Returns an object representing the item with which you are working.</span></span>

<span data-ttu-id="3b9f6-186">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-186">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9f6-187">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="3b9f6-187">-PermissionsToCertificates</span></span>
<span data-ttu-id="3b9f6-188">A felhasználók vagy a szolgáltatók számára megadható tanúsítvány-engedélyek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-188">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="3b9f6-189">A paraméter elfogadható értékei:</span><span class="sxs-lookup"><span data-stu-id="3b9f6-189">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="3b9f6-190">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="3b9f6-190">Get</span></span>
- <span data-ttu-id="3b9f6-191">Lista</span><span class="sxs-lookup"><span data-stu-id="3b9f6-191">List</span></span>
- <span data-ttu-id="3b9f6-192">Törlése</span><span class="sxs-lookup"><span data-stu-id="3b9f6-192">Delete</span></span>
- <span data-ttu-id="3b9f6-193">Létrehozása</span><span class="sxs-lookup"><span data-stu-id="3b9f6-193">Create</span></span>
- <span data-ttu-id="3b9f6-194">Importálása</span><span class="sxs-lookup"><span data-stu-id="3b9f6-194">Import</span></span>
- <span data-ttu-id="3b9f6-195">Frissítés</span><span class="sxs-lookup"><span data-stu-id="3b9f6-195">Update</span></span>
- <span data-ttu-id="3b9f6-196">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="3b9f6-196">Managecontacts</span></span>
- <span data-ttu-id="3b9f6-197">Getissuers</span><span class="sxs-lookup"><span data-stu-id="3b9f6-197">Getissuers</span></span>
- <span data-ttu-id="3b9f6-198">Listissuers</span><span class="sxs-lookup"><span data-stu-id="3b9f6-198">Listissuers</span></span>
- <span data-ttu-id="3b9f6-199">Setissuers</span><span class="sxs-lookup"><span data-stu-id="3b9f6-199">Setissuers</span></span>
- <span data-ttu-id="3b9f6-200">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="3b9f6-200">Deleteissuers</span></span>
- <span data-ttu-id="3b9f6-201">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="3b9f6-201">Manageissuers</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b9f6-202">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="3b9f6-202">-PermissionsToKeys</span></span>
<span data-ttu-id="3b9f6-203">A felhasználó vagy a szolgáltatás megbízójának megadni kívánt fő műveleti engedélyek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-203">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="3b9f6-204">A paraméter elfogadható értékei:</span><span class="sxs-lookup"><span data-stu-id="3b9f6-204">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="3b9f6-205">Visszafejtése</span><span class="sxs-lookup"><span data-stu-id="3b9f6-205">Decrypt</span></span>
- <span data-ttu-id="3b9f6-206">Beavatkozik</span><span class="sxs-lookup"><span data-stu-id="3b9f6-206">Encrypt</span></span>
- <span data-ttu-id="3b9f6-207">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="3b9f6-207">UnwrapKey</span></span>
- <span data-ttu-id="3b9f6-208">WrapKey</span><span class="sxs-lookup"><span data-stu-id="3b9f6-208">WrapKey</span></span>
- <span data-ttu-id="3b9f6-209">Ellenőrizze</span><span class="sxs-lookup"><span data-stu-id="3b9f6-209">Verify</span></span>
- <span data-ttu-id="3b9f6-210">Jel</span><span class="sxs-lookup"><span data-stu-id="3b9f6-210">Sign</span></span>
- <span data-ttu-id="3b9f6-211">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="3b9f6-211">Get</span></span>
- <span data-ttu-id="3b9f6-212">Lista</span><span class="sxs-lookup"><span data-stu-id="3b9f6-212">List</span></span>
- <span data-ttu-id="3b9f6-213">Frissítés</span><span class="sxs-lookup"><span data-stu-id="3b9f6-213">Update</span></span>
- <span data-ttu-id="3b9f6-214">Létrehozása</span><span class="sxs-lookup"><span data-stu-id="3b9f6-214">Create</span></span>
- <span data-ttu-id="3b9f6-215">Importálása</span><span class="sxs-lookup"><span data-stu-id="3b9f6-215">Import</span></span>
- <span data-ttu-id="3b9f6-216">Törlése</span><span class="sxs-lookup"><span data-stu-id="3b9f6-216">Delete</span></span>
- <span data-ttu-id="3b9f6-217">Hát</span><span class="sxs-lookup"><span data-stu-id="3b9f6-217">Backup</span></span>
- <span data-ttu-id="3b9f6-218">Visszaállítása</span><span class="sxs-lookup"><span data-stu-id="3b9f6-218">Restore</span></span>
- <span data-ttu-id="3b9f6-219">Visszaszerez</span><span class="sxs-lookup"><span data-stu-id="3b9f6-219">Recover</span></span>
- <span data-ttu-id="3b9f6-220">Véglegesen</span><span class="sxs-lookup"><span data-stu-id="3b9f6-220">Purge</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b9f6-221">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="3b9f6-221">-PermissionsToSecrets</span></span>
<span data-ttu-id="3b9f6-222">A felhasználó vagy a szolgáltatás megbízójának megadni kívánt titkos műveleti engedélyek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-222">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="3b9f6-223">A paraméter elfogadható értékei:</span><span class="sxs-lookup"><span data-stu-id="3b9f6-223">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="3b9f6-224">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="3b9f6-224">Get</span></span>
- <span data-ttu-id="3b9f6-225">Lista</span><span class="sxs-lookup"><span data-stu-id="3b9f6-225">List</span></span>
- <span data-ttu-id="3b9f6-226">Beállítása</span><span class="sxs-lookup"><span data-stu-id="3b9f6-226">Set</span></span>
- <span data-ttu-id="3b9f6-227">Törlése</span><span class="sxs-lookup"><span data-stu-id="3b9f6-227">Delete</span></span>
- <span data-ttu-id="3b9f6-228">Hát</span><span class="sxs-lookup"><span data-stu-id="3b9f6-228">Backup</span></span>
- <span data-ttu-id="3b9f6-229">Visszaállítása</span><span class="sxs-lookup"><span data-stu-id="3b9f6-229">Restore</span></span>
- <span data-ttu-id="3b9f6-230">Visszaszerez</span><span class="sxs-lookup"><span data-stu-id="3b9f6-230">Recover</span></span>
- <span data-ttu-id="3b9f6-231">Véglegesen</span><span class="sxs-lookup"><span data-stu-id="3b9f6-231">Purge</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: get, list, set, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b9f6-232">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="3b9f6-232">-PermissionsToStorage</span></span>
<span data-ttu-id="3b9f6-233">A felügyelt tárterület-fiók és a SaS-definíciós műveleti engedélyeket adja meg a felhasználó vagy a szolgáltatás megbízójának.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-233">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b9f6-234">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b9f6-234">-ResourceGroupName</span></span>
<span data-ttu-id="3b9f6-235">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-235">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b9f6-236">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="3b9f6-236">-ServicePrincipalName</span></span>
<span data-ttu-id="3b9f6-237">Annak az alkalmazásnak az egyszerű szolgáltatásnevet adja meg, amelyre engedélyt szeretne adni.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-237">Specifies the service principal name of the application to which to grant permissions.</span></span>

<span data-ttu-id="3b9f6-238">Adja meg az alkalmazáshoz az AzureActive-címtárban regisztrált alkalmazás-azonosítót (más néven ügyfél-azonosító).</span><span class="sxs-lookup"><span data-stu-id="3b9f6-238">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="3b9f6-239">A paraméter által megadott szolgáltatásnevet tartalmazó alkalmazásnak regisztrálnia kell a jelenlegi előfizetést tartalmazó Azure-címtárban.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-239">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByServicePrincipalName, InputObjectByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b9f6-240">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="3b9f6-240">-UserPrincipalName</span></span>
<span data-ttu-id="3b9f6-241">Annak a felhasználónak az egyszerű felhasználónevét adja meg, akinek engedélyt szeretne adni.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-241">Specifies the user principal name of the user to whom to grant permissions.</span></span>

<span data-ttu-id="3b9f6-242">Ez az egyszerű felhasználónév csak az aktuális előfizetéshez társított címtárban található.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-242">This user principal name must exist in the directory associated with the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, InputObjectByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b9f6-243">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3b9f6-243">-VaultName</span></span>
<span data-ttu-id="3b9f6-244">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-244">Specifies the name of a key vault.</span></span>

<span data-ttu-id="3b9f6-245">Ez a parancsmag módosítja a hozzáférési házirendet annak a kulcsfájl számára, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-245">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b9f6-246">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3b9f6-246">-Confirm</span></span>
<span data-ttu-id="3b9f6-247">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-247">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9f6-248">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b9f6-248">-WhatIf</span></span>
<span data-ttu-id="3b9f6-249">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-249">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b9f6-250">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-250">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9f6-251">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b9f6-251">CommonParameters</span></span>
<span data-ttu-id="3b9f6-252">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3b9f6-252">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b9f6-253">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b9f6-253">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b9f6-254">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b9f6-254">INPUTS</span></span>

### <span data-ttu-id="3b9f6-255">Karakterlánc, GUID, string [], kapcsoló</span><span class="sxs-lookup"><span data-stu-id="3b9f6-255">String, Guid, String[], Switch</span></span>

## <span data-ttu-id="3b9f6-256">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b9f6-256">OUTPUTS</span></span>

### <span data-ttu-id="3b9f6-257">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="3b9f6-257">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="3b9f6-258">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3b9f6-258">NOTES</span></span>

## <span data-ttu-id="3b9f6-259">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b9f6-259">RELATED LINKS</span></span>

[<span data-ttu-id="3b9f6-260">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="3b9f6-260">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="3b9f6-261">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3b9f6-261">Remove-AzureRmKeyVaultAccessPolicy</span></span>](./Remove-AzureRmKeyVaultAccessPolicy.md)

