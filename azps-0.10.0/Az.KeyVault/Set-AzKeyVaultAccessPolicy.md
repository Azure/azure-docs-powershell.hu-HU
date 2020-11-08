---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-Azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: a774c438f9be25dc55f48c5121031956374a2cb7
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017369"
---
# <span data-ttu-id="900f9-101">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="900f9-101">Set-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="900f9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="900f9-102">SYNOPSIS</span></span>
<span data-ttu-id="900f9-103">Meglévő engedélyeket ad vagy módosít a felhasználó, az alkalmazás vagy a biztonsági csoport számára a fő boltozattal végzett műveletek elvégzéséhez.</span><span class="sxs-lookup"><span data-stu-id="900f9-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

## <span data-ttu-id="900f9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="900f9-104">SYNTAX</span></span>

### <span data-ttu-id="900f9-105">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="900f9-105">ByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="900f9-106">ByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="900f9-106">ByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="900f9-107">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="900f9-107">ByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="900f9-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="900f9-108">ByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="900f9-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="900f9-109">ForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="900f9-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="900f9-110">DESCRIPTION</span></span>
<span data-ttu-id="900f9-111">A **set-AzKeyVaultAccessPolicy** parancsmag meglévő engedélyeket ad vagy módosít egy felhasználó, alkalmazás vagy biztonsági csoport számára, hogy a megadott műveleteket egy fő boltozattal végezze el.</span><span class="sxs-lookup"><span data-stu-id="900f9-111">The **Set-AzKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="900f9-112">Nem módosítja a többi felhasználó, alkalmazás vagy biztonsági csoport engedélyeit a kulcs boltozatán.</span><span class="sxs-lookup"><span data-stu-id="900f9-112">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>

<span data-ttu-id="900f9-113">Ha egy biztonsági csoportra vonatkozó engedélyeket állít be, ez a művelet csak a biztonsági csoport felhasználóit érinti.</span><span class="sxs-lookup"><span data-stu-id="900f9-113">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>

<span data-ttu-id="900f9-114">Az alábbi könyvtárak mindegyikének meg kell egyeznie az Azure-címtárral:</span><span class="sxs-lookup"><span data-stu-id="900f9-114">The following directories must all be the same Azure directory:</span></span>
- <span data-ttu-id="900f9-115">Annak az Azure-előfizetésnek az alapértelmezett könyvtára, amelyben a kulcs boltozata lakik.</span><span class="sxs-lookup"><span data-stu-id="900f9-115">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="900f9-116">Az Azure-címtár, amely az engedélyeket biztosító felhasználó vagy alkalmazás csoportját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="900f9-116">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>

<span data-ttu-id="900f9-117">Példák azokra az esetekre, amikor ezek a feltételek nem teljesülnek, és a parancsmag nem fog működni:</span><span class="sxs-lookup"><span data-stu-id="900f9-117">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span>

- <span data-ttu-id="900f9-118">Másik szervezet felhasználóinak engedélyezése a kulcsfájl kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="900f9-118">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="900f9-119">Minden szervezetnek saját könyvtára van.</span><span class="sxs-lookup"><span data-stu-id="900f9-119">Each organization has its own directory.</span></span>
- <span data-ttu-id="900f9-120">Az Azure-fiók több könyvtárat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="900f9-120">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="900f9-121">Ha az alapértelmezett könyvtártól eltérő címtárban regisztrálja az alkalmazást, az alkalmazás nem engedélyezheti a kulcsfájl használatát.</span><span class="sxs-lookup"><span data-stu-id="900f9-121">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="900f9-122">Az alkalmazásnak az alapértelmezett címtárban kell lennie.</span><span class="sxs-lookup"><span data-stu-id="900f9-122">The application must be in the default directory.</span></span>

<span data-ttu-id="900f9-123">Fontos tudni, hogy bár az erőforráscsoport beállítása nem kötelező ehhez a parancsmaghoz, a jobb teljesítmény érdekében ezt el kell végeznie.</span><span class="sxs-lookup"><span data-stu-id="900f9-123">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="900f9-124">Példák</span><span class="sxs-lookup"><span data-stu-id="900f9-124">EXAMPLES</span></span>

### <span data-ttu-id="900f9-125">1. példa: engedélyek megadása egy felhasználó számára egy kulcs boltozatához és az engedélyek módosítása</span><span class="sxs-lookup"><span data-stu-id="900f9-125">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets set,delete
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru
```

<span data-ttu-id="900f9-126">Az első parancs engedélyeket ad az Azure Active Directory-beli felhasználóknak PattiFuller@contoso.com , hogy a Contoso03Vault nevű fő boltozattal végezze el a megfelelő műveleteket a kulcsok és a titkok területén.</span><span class="sxs-lookup"><span data-stu-id="900f9-126">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span>

<span data-ttu-id="900f9-127">A második parancs módosítja az PattiFuller@contoso.com első parancsban megadott engedélyeket, így mostantól a beállítások megadásával és törlésével is lehetővé válik a titok beszerzése.</span><span class="sxs-lookup"><span data-stu-id="900f9-127">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="900f9-128">A fő műveletekre vonatkozó engedélyek a parancs után változatlanok maradnak.</span><span class="sxs-lookup"><span data-stu-id="900f9-128">The permissions to key operations remain unchanged after this command.</span></span> <span data-ttu-id="900f9-129">A *PassThru* paraméter a parancsmag által visszaadott frissített objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="900f9-129">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

<span data-ttu-id="900f9-130">A végleges parancs a meglévő engedélyeket tovább módosítja a PattiFuller@contoso.com legfontosabb műveletekhez tartozó összes engedély eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="900f9-130">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="900f9-131">A titkos műveletek engedélyei a parancs után változatlanok maradnak.</span><span class="sxs-lookup"><span data-stu-id="900f9-131">The permissions to secret operations remain unchanged after this command.</span></span> <span data-ttu-id="900f9-132">A *PassThru* paraméter a parancsmag által visszaadott frissített objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="900f9-132">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

### <span data-ttu-id="900f9-133">2. példa: az alkalmazásspecifikus szolgáltatók engedélyeinek megadása a titkok olvasásához és írásához</span><span class="sxs-lookup"><span data-stu-id="900f9-133">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="900f9-134">Ez a parancs engedélyeket ad az Contoso03Vault nevű fő Vault-alkalmazás engedélyeinek megadásához.</span><span class="sxs-lookup"><span data-stu-id="900f9-134">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span>

<span data-ttu-id="900f9-135">A *ServicePrincipalName* paraméter az alkalmazást adja meg.</span><span class="sxs-lookup"><span data-stu-id="900f9-135">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="900f9-136">Az alkalmazást be kell jegyeztetni az Azure Active Directoryban.</span><span class="sxs-lookup"><span data-stu-id="900f9-136">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="900f9-137">A *ServicePrincipalName* paraméter értéke csak az alkalmazás egyszerű szolgáltatásnév, vagy az ALKALMAZÁSSPECIFIKUS azonosító GUID értéke lehet.</span><span class="sxs-lookup"><span data-stu-id="900f9-137">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>

<span data-ttu-id="900f9-138">Ez a példa megadja az egyszerű szolgáltatásnév nevet `http://payroll.contoso.com` , és a parancs a titok olvasását és írását biztosítja az alkalmazás engedélyeinek.</span><span class="sxs-lookup"><span data-stu-id="900f9-138">This example specifies the service principal name `http://payroll.contoso.com`, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="900f9-139">3. példa: az alkalmazás engedélyeinek megadása az objektum azonosítójával</span><span class="sxs-lookup"><span data-stu-id="900f9-139">Example 3: Grant permissions for an application using its object ID</span></span>
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="900f9-140">A parancs a titok olvasását és írását lehetővé tévő jogosultságokkal ruházza fel az alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="900f9-140">This command grants the application permissions to read and write secrets.</span></span>

<span data-ttu-id="900f9-141">Ez a példa azt adja meg, hogy az alkalmazás az alkalmazás Principal azonosítójával használja az alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="900f9-141">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="900f9-142">4. példa: engedélyek megadása egyszerű felhasználónévhez</span><span class="sxs-lookup"><span data-stu-id="900f9-142">Example 4: Grant permissions for a user principal name</span></span>
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="900f9-143">Ez a parancs a beszerzés, a lista és az engedélyek beállítását adja meg a megadott egyszerű felhasználónévhez a titok eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="900f9-143">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="900f9-144">Példa: 5: a Microsoft. számítási erőforrás-szolgáltató segítségével beolvassa a titkot.</span><span class="sxs-lookup"><span data-stu-id="900f9-144">Example 5: Enable secrets to be retrieved from a key vault vault by the Microsoft.Compute resource provider</span></span>
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="900f9-145">Ez a parancs megadja a titoknak azokat az engedélyeit, amelyeket a Microsoft. számítási erőforrás-szolgáltatótól kapott a Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="900f9-145">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="900f9-146">6. példa: engedélyek megadása egy biztonsági csoporthoz</span><span class="sxs-lookup"><span data-stu-id="900f9-146">Example 6: Grant permissions to a security group</span></span>
```
PS C:\>Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys All -PermissionsToSecrets All
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
group1                                                        96a0daa6-9841-4a9c-bdeb-e7062276c688
group2                                                        b8a401eb-63ad-4a30-b0e1-a7461969fe54
group3                                                        da07a6be-2c1e-4e42-934d-ceb57cf652b4
```

<span data-ttu-id="900f9-147">Az első parancs az Get-AzADGroup parancsmagot használja az Active Directory-csoportok beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="900f9-147">The first command uses the Get-AzADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="900f9-148">A kimenetben 3 csoport, a **Group1** , az **Group2** és a **Group3** nevű csoport látható.</span><span class="sxs-lookup"><span data-stu-id="900f9-148">From the output, you see 3 groups returned, named **group1** , **group2** , and **group3**.</span></span> <span data-ttu-id="900f9-149">Több csoportnak ugyanazt a nevet kell használnia, de minden esetben egyedi ObjectId kell lennie.</span><span class="sxs-lookup"><span data-stu-id="900f9-149">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="900f9-150">Ha egynél több, ugyanazt a nevet tartalmazó csoportot ad eredményül, a kimenetben lévő ObjectId segítségével határozza meg, hogy melyiket szeretné használni.</span><span class="sxs-lookup"><span data-stu-id="900f9-150">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>

<span data-ttu-id="900f9-151">Ezután a parancs kimenete Set-AzKeyVaultAccessPolicy segítségével engedélyeket adhat a Group2, a **myownvault** nevű kulcshoz.</span><span class="sxs-lookup"><span data-stu-id="900f9-151">You then use the output of this command with Set-AzKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="900f9-152">Ez a példa a "Group2" szövegközi csoportokat ugyanazon a parancssorban sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="900f9-152">This example enumerates the groups named 'group2' inline in the same command line.</span></span>

<span data-ttu-id="900f9-153">Előfordulhat, hogy a visszaadott lista több olyan csoportba tartozik, amely "Group2" névvel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="900f9-153">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="900f9-154">Ez a példa a \[ visszatérési listában az első indexet jelölte ki \] .</span><span class="sxs-lookup"><span data-stu-id="900f9-154">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="900f9-155">7. példa: hozzáférés biztosítása az Azure Information Protectionhez az ügyfél által felügyelt bérlői kulcshoz (BYOK)</span><span class="sxs-lookup"><span data-stu-id="900f9-155">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="900f9-156">Ez a parancs engedélyezi az Azure Information Protectiont az ügyfél által felügyelt kulcs (a saját kulcs vagy a "BYOK" forgatókönyv) használatához az Azure Information Protection bérlői kulccsal.</span><span class="sxs-lookup"><span data-stu-id="900f9-156">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>

<span data-ttu-id="900f9-157">Ha futtatja ezt a parancsot, adja meg a saját kulcs boltozatát, de meg kell adnia a *ServicePrincipalName* paramétert a GUID **00000012-0000-0000 – C000 – 000000000000 értéket** , és meg kell adnia a példában szereplő engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="900f9-157">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="900f9-158">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="900f9-158">PARAMETERS</span></span>

### <span data-ttu-id="900f9-159">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="900f9-159">-ApplicationId</span></span>
<span data-ttu-id="900f9-160">Jövőbeli használatra.</span><span class="sxs-lookup"><span data-stu-id="900f9-160">For future use.</span></span>

```yaml
Type: Guid
Parameter Sets: ByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="900f9-161">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="900f9-161">-BypassObjectIdValidation</span></span>
<span data-ttu-id="900f9-162">Lehetővé teszi az objektumazonosítók megadását anélkül, hogy az az Azure Active Directoryban létezik.</span><span class="sxs-lookup"><span data-stu-id="900f9-162">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>

<span data-ttu-id="900f9-163">Csak akkor használja ezt a paramétert, ha hozzáférést szeretne adni a kulcsfájl egy olyan objektum-AZONOSÍTÓhoz, amely egy másik Azure-bérlőtől származó meghatalmazott biztonsági csoportra hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="900f9-163">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="900f9-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="900f9-164">-DefaultProfile</span></span>
<span data-ttu-id="900f9-165">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="900f9-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="900f9-166">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="900f9-166">-EmailAddress</span></span>
<span data-ttu-id="900f9-167">Annak a felhasználónak a felhasználói e-mail-címét adja meg, akinek engedélyt szeretne adni.</span><span class="sxs-lookup"><span data-stu-id="900f9-167">Specifies the user email address of the user to whom to grant permissions.</span></span>

<span data-ttu-id="900f9-168">Ennek az e-mail-címnek meg kell egyeznie az aktuális előfizetéshez társított címtárban, és egyedinek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="900f9-168">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

```yaml
Type: String
Parameter Sets: ByEmailAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="900f9-169">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="900f9-169">-EnabledForDeployment</span></span>
<span data-ttu-id="900f9-170">A Microsoft. számítási erőforrás-szolgáltatója kinyerheti a titkokat ebből a kulcsfájlból, ha ez a kulcs boltozata az erőforrás létrehozásakor, például virtuális gép létrehozásakor jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="900f9-170">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="900f9-171">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="900f9-171">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="900f9-172">Lehetővé teszi, hogy az Azure Disk Encryption szolgáltatás a kulcsok kijavítását és kicsomagolását a kulcsból.</span><span class="sxs-lookup"><span data-stu-id="900f9-172">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="900f9-173">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="900f9-173">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="900f9-174">Lehetővé teszi az Azure Resource Manager számára, hogy ebből a kulcsfájlból kiírja a titkot, ha ezt a kulcspárt a sablonok központi telepítéséhez hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="900f9-174">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="900f9-175">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="900f9-175">-ObjectId</span></span>
<span data-ttu-id="900f9-176">Annak az Azure Active Directory-fióknak az objektum-AZONOSÍTÓját adja meg, amelyre engedélyt szeretne adni.</span><span class="sxs-lookup"><span data-stu-id="900f9-176">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="900f9-177">-PassThru</span><span class="sxs-lookup"><span data-stu-id="900f9-177">-PassThru</span></span>
<span data-ttu-id="900f9-178">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="900f9-178">Returns an object representing the item with which you are working.</span></span>

<span data-ttu-id="900f9-179">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="900f9-179">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="900f9-180">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="900f9-180">-PermissionsToCertificates</span></span>
<span data-ttu-id="900f9-181">A felhasználók vagy a szolgáltatók számára megadható tanúsítvány-engedélyek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="900f9-181">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="900f9-182">A paraméter elfogadható értékei:</span><span class="sxs-lookup"><span data-stu-id="900f9-182">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="900f9-183">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="900f9-183">Get</span></span>
- <span data-ttu-id="900f9-184">Lista</span><span class="sxs-lookup"><span data-stu-id="900f9-184">List</span></span>
- <span data-ttu-id="900f9-185">Törlése</span><span class="sxs-lookup"><span data-stu-id="900f9-185">Delete</span></span>
- <span data-ttu-id="900f9-186">Létrehozása</span><span class="sxs-lookup"><span data-stu-id="900f9-186">Create</span></span>
- <span data-ttu-id="900f9-187">Importálása</span><span class="sxs-lookup"><span data-stu-id="900f9-187">Import</span></span>
- <span data-ttu-id="900f9-188">Frissítés</span><span class="sxs-lookup"><span data-stu-id="900f9-188">Update</span></span>
- <span data-ttu-id="900f9-189">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="900f9-189">Managecontacts</span></span>
- <span data-ttu-id="900f9-190">Getissuers</span><span class="sxs-lookup"><span data-stu-id="900f9-190">Getissuers</span></span>
- <span data-ttu-id="900f9-191">Listissuers</span><span class="sxs-lookup"><span data-stu-id="900f9-191">Listissuers</span></span>
- <span data-ttu-id="900f9-192">Setissuers</span><span class="sxs-lookup"><span data-stu-id="900f9-192">Setissuers</span></span>
- <span data-ttu-id="900f9-193">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="900f9-193">Deleteissuers</span></span>
- <span data-ttu-id="900f9-194">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="900f9-194">Manageissuers</span></span>

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases:
Accepted values: get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="900f9-195">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="900f9-195">-PermissionsToKeys</span></span>
<span data-ttu-id="900f9-196">A felhasználó vagy a szolgáltatás megbízójának megadni kívánt fő műveleti engedélyek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="900f9-196">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="900f9-197">A paraméter elfogadható értékei:</span><span class="sxs-lookup"><span data-stu-id="900f9-197">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="900f9-198">Visszafejtése</span><span class="sxs-lookup"><span data-stu-id="900f9-198">Decrypt</span></span>
- <span data-ttu-id="900f9-199">Beavatkozik</span><span class="sxs-lookup"><span data-stu-id="900f9-199">Encrypt</span></span>
- <span data-ttu-id="900f9-200">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="900f9-200">UnwrapKey</span></span>
- <span data-ttu-id="900f9-201">WrapKey</span><span class="sxs-lookup"><span data-stu-id="900f9-201">WrapKey</span></span>
- <span data-ttu-id="900f9-202">Ellenőrizze</span><span class="sxs-lookup"><span data-stu-id="900f9-202">Verify</span></span>
- <span data-ttu-id="900f9-203">Jel</span><span class="sxs-lookup"><span data-stu-id="900f9-203">Sign</span></span>
- <span data-ttu-id="900f9-204">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="900f9-204">Get</span></span>
- <span data-ttu-id="900f9-205">Lista</span><span class="sxs-lookup"><span data-stu-id="900f9-205">List</span></span>
- <span data-ttu-id="900f9-206">Frissítés</span><span class="sxs-lookup"><span data-stu-id="900f9-206">Update</span></span>
- <span data-ttu-id="900f9-207">Létrehozása</span><span class="sxs-lookup"><span data-stu-id="900f9-207">Create</span></span>
- <span data-ttu-id="900f9-208">Importálása</span><span class="sxs-lookup"><span data-stu-id="900f9-208">Import</span></span>
- <span data-ttu-id="900f9-209">Törlése</span><span class="sxs-lookup"><span data-stu-id="900f9-209">Delete</span></span>
- <span data-ttu-id="900f9-210">Hát</span><span class="sxs-lookup"><span data-stu-id="900f9-210">Backup</span></span>
- <span data-ttu-id="900f9-211">Visszaállítása</span><span class="sxs-lookup"><span data-stu-id="900f9-211">Restore</span></span>
- <span data-ttu-id="900f9-212">Visszaszerez</span><span class="sxs-lookup"><span data-stu-id="900f9-212">Recover</span></span>
- <span data-ttu-id="900f9-213">Véglegesen</span><span class="sxs-lookup"><span data-stu-id="900f9-213">Purge</span></span>

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases:
Accepted values: decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="900f9-214">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="900f9-214">-PermissionsToSecrets</span></span>
<span data-ttu-id="900f9-215">A felhasználó vagy a szolgáltatás megbízójának megadni kívánt titkos műveleti engedélyek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="900f9-215">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="900f9-216">A paraméter elfogadható értékei:</span><span class="sxs-lookup"><span data-stu-id="900f9-216">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="900f9-217">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="900f9-217">Get</span></span>
- <span data-ttu-id="900f9-218">Lista</span><span class="sxs-lookup"><span data-stu-id="900f9-218">List</span></span>
- <span data-ttu-id="900f9-219">Beállítása</span><span class="sxs-lookup"><span data-stu-id="900f9-219">Set</span></span>
- <span data-ttu-id="900f9-220">Törlése</span><span class="sxs-lookup"><span data-stu-id="900f9-220">Delete</span></span>
- <span data-ttu-id="900f9-221">Hát</span><span class="sxs-lookup"><span data-stu-id="900f9-221">Backup</span></span>
- <span data-ttu-id="900f9-222">Visszaállítása</span><span class="sxs-lookup"><span data-stu-id="900f9-222">Restore</span></span>
- <span data-ttu-id="900f9-223">Visszaszerez</span><span class="sxs-lookup"><span data-stu-id="900f9-223">Recover</span></span>
- <span data-ttu-id="900f9-224">Véglegesen</span><span class="sxs-lookup"><span data-stu-id="900f9-224">Purge</span></span>

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases:
Accepted values: get, list, set, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="900f9-225">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="900f9-225">-PermissionsToStorage</span></span>
<span data-ttu-id="900f9-226">A felügyelt tárterület-fiók és a SaS-definíciós műveleti engedélyeket adja meg a felhasználó vagy a szolgáltatás megbízójának.</span><span class="sxs-lookup"><span data-stu-id="900f9-226">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases:
Accepted values: get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="900f9-227">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="900f9-227">-ResourceGroupName</span></span>
<span data-ttu-id="900f9-228">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="900f9-228">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="900f9-229">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="900f9-229">-ServicePrincipalName</span></span>
<span data-ttu-id="900f9-230">Annak az alkalmazásnak az egyszerű szolgáltatásnevet adja meg, amelyre engedélyt szeretne adni.</span><span class="sxs-lookup"><span data-stu-id="900f9-230">Specifies the service principal name of the application to which to grant permissions.</span></span>

<span data-ttu-id="900f9-231">Adja meg az alkalmazáshoz az AzureActive-címtárban regisztrált alkalmazás-azonosítót (más néven ügyfél-azonosító).</span><span class="sxs-lookup"><span data-stu-id="900f9-231">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="900f9-232">A paraméter által megadott szolgáltatásnevet tartalmazó alkalmazásnak regisztrálnia kell a jelenlegi előfizetést tartalmazó Azure-címtárban.</span><span class="sxs-lookup"><span data-stu-id="900f9-232">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="900f9-233">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="900f9-233">-UserPrincipalName</span></span>
<span data-ttu-id="900f9-234">Annak a felhasználónak az egyszerű felhasználónevét adja meg, akinek engedélyt szeretne adni.</span><span class="sxs-lookup"><span data-stu-id="900f9-234">Specifies the user principal name of the user to whom to grant permissions.</span></span>

<span data-ttu-id="900f9-235">Ez az egyszerű felhasználónév csak az aktuális előfizetéshez társított címtárban található.</span><span class="sxs-lookup"><span data-stu-id="900f9-235">This user principal name must exist in the directory associated with the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="900f9-236">-VaultName</span><span class="sxs-lookup"><span data-stu-id="900f9-236">-VaultName</span></span>
<span data-ttu-id="900f9-237">A kulcsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="900f9-237">Specifies the name of a key vault.</span></span>

<span data-ttu-id="900f9-238">Ez a parancsmag módosítja a hozzáférési házirendet annak a kulcsfájl számára, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="900f9-238">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="900f9-239">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="900f9-239">-Confirm</span></span>
<span data-ttu-id="900f9-240">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="900f9-240">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="900f9-241">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="900f9-241">-WhatIf</span></span>
<span data-ttu-id="900f9-242">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="900f9-242">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="900f9-243">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="900f9-243">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="900f9-244">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="900f9-244">CommonParameters</span></span>
<span data-ttu-id="900f9-245">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="900f9-245">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="900f9-246">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="900f9-246">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="900f9-247">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="900f9-247">INPUTS</span></span>

### <span data-ttu-id="900f9-248">Karakterlánc, GUID, string [], kapcsoló</span><span class="sxs-lookup"><span data-stu-id="900f9-248">String, Guid, String[], Switch</span></span>

## <span data-ttu-id="900f9-249">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="900f9-249">OUTPUTS</span></span>

### <span data-ttu-id="900f9-250">Microsoft. Azure. Command. PSVault. models.</span><span class="sxs-lookup"><span data-stu-id="900f9-250">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="900f9-251">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="900f9-251">NOTES</span></span>

## <span data-ttu-id="900f9-252">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="900f9-252">RELATED LINKS</span></span>

[<span data-ttu-id="900f9-253">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="900f9-253">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="900f9-254">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="900f9-254">Remove-AzKeyVaultAccessPolicy</span></span>](./Remove-AzKeyVaultAccessPolicy.md)

