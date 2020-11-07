---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-Azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: f5cd00e0ef8e8936a4c87ee313054ae4c084a879
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "93851041"
---
# <span data-ttu-id="e16cf-101">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e16cf-101">Remove-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="e16cf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e16cf-102">SYNOPSIS</span></span>
<span data-ttu-id="e16cf-103">Egy felhasználó vagy alkalmazás összes engedélyének eltávolítása egy kulcs-boltozatról.</span><span class="sxs-lookup"><span data-stu-id="e16cf-103">Removes all permissions for a user or application from a key vault.</span></span>

## <span data-ttu-id="e16cf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e16cf-104">SYNTAX</span></span>

### <span data-ttu-id="e16cf-105">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="e16cf-105">ByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e16cf-106">ByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="e16cf-106">ByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e16cf-107">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="e16cf-107">ByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e16cf-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="e16cf-108">ByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e16cf-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="e16cf-109">ForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e16cf-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="e16cf-110">DESCRIPTION</span></span>
<span data-ttu-id="e16cf-111">A **Remove-AzKeyVaultAccessPolicy** parancsmag eltávolítja a felhasználók vagy alkalmazások összes engedélyét, illetve a fő tárolók minden felhasználóját és alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="e16cf-111">The **Remove-AzKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="e16cf-112">Az Azure-előfizetés fő tárolóját tartalmazó Azure-előfizetés tulajdonosa még akkor is adhat hozzá engedélyeket a kulcs boltozatához, ha eltávolítja az összes engedélyt.</span><span class="sxs-lookup"><span data-stu-id="e16cf-112">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>

<span data-ttu-id="e16cf-113">Fontos tudni, hogy bár az erőforráscsoport beállítása nem kötelező ehhez a parancsmaghoz, a jobb teljesítmény érdekében ezt el kell végeznie.</span><span class="sxs-lookup"><span data-stu-id="e16cf-113">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="e16cf-114">Példák</span><span class="sxs-lookup"><span data-stu-id="e16cf-114">EXAMPLES</span></span>

### <span data-ttu-id="e16cf-115">1. példa: felhasználó engedélyeinek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e16cf-115">Example 1: Remove permissions for a user</span></span>
```
PS C:\>Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com'
```

<span data-ttu-id="e16cf-116">Ez a parancs eltávolítja az összes olyan engedélyt, amelyet a felhasználó a PattiFuller@contoso.com Contoso03Vault nevű kulcs-boltíven tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="e16cf-116">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>

### <span data-ttu-id="e16cf-117">2. példa: az alkalmazások engedélyeinek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e16cf-117">Example 2: Remove permissions for an application</span></span>
```
PS C:\>Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="e16cf-118">Ez a parancs eltávolítja az összes olyan engedélyt, amelyet az alkalmazás a Contoso03Vault nevű kulcs boltozaton tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="e16cf-118">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="e16cf-119">Ez a példa azonosítja az alkalmazást az Azure Active Directory szolgáltatásban regisztrált egyszerű szolgáltatásnév használatával `http://payroll.contoso.com` .</span><span class="sxs-lookup"><span data-stu-id="e16cf-119">This example identifies the application by using the service principal name registered in Azure Active Directory, `http://payroll.contoso.com`.</span></span>

### <span data-ttu-id="e16cf-120">3. példa: az alkalmazás engedélyeinek eltávolítása az objektum-azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="e16cf-120">Example 3: Remove permissions for an application by using its object ID</span></span>
```
PS C:\>Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="e16cf-121">Ez a parancs eltávolítja az összes olyan engedélyt, amelyet az alkalmazás a Contoso03Vault nevű kulcs boltozaton tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="e16cf-121">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="e16cf-122">Ez a példa azonosítja az alkalmazást a szolgáltatás megbízójának objektum-azonosítója alapján.</span><span class="sxs-lookup"><span data-stu-id="e16cf-122">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="e16cf-123">4. példa: engedélyek eltávolítása a Microsofthoz. számítási erőforrás-szolgáltató</span><span class="sxs-lookup"><span data-stu-id="e16cf-123">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```
PS C:\>Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="e16cf-124">Ez a parancs eltávolítja az engedélyt a Microsoft számára. az erőforrás-szolgáltató kiszámításához a Contoso03Vault titkait kell beszereznie.</span><span class="sxs-lookup"><span data-stu-id="e16cf-124">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="e16cf-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e16cf-125">PARAMETERS</span></span>

### <span data-ttu-id="e16cf-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e16cf-126">-ApplicationId</span></span>
<span data-ttu-id="e16cf-127">Jövőbeli használatra.</span><span class="sxs-lookup"><span data-stu-id="e16cf-127">For future use.</span></span>

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

### <span data-ttu-id="e16cf-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e16cf-128">-DefaultProfile</span></span>
<span data-ttu-id="e16cf-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e16cf-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e16cf-130">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="e16cf-130">-EmailAddress</span></span>
<span data-ttu-id="e16cf-131">Annak a felhasználónak a felhasználói e-mail-címét adja meg, akinek az elérését el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="e16cf-131">Specifies the user email address of the user whose access you want to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByEmail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e16cf-132">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="e16cf-132">-EnabledForDeployment</span></span>
<span data-ttu-id="e16cf-133">A Microsoft. számítási erőforrás-szolgáltatója kinyerheti a titkokat ebből a kulcsfájlból, ha ez a kulcs boltozata az erőforrás létrehozásakor, például virtuális gép létrehozásakor jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="e16cf-133">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="e16cf-134">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="e16cf-134">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="e16cf-135">Lehetővé teszi, hogy az Azure Disk Encryption szolgáltatás a kulcsok kijavítását és kicsomagolását a kulcsból.</span><span class="sxs-lookup"><span data-stu-id="e16cf-135">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="e16cf-136">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="e16cf-136">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="e16cf-137">Lehetővé teszi az Azure Resource Manager számára, hogy ebből a kulcsfájlból kiírja a titkot, ha ezt a kulcspárt a sablonok központi telepítéséhez hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="e16cf-137">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="e16cf-138">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e16cf-138">-ObjectId</span></span>
<span data-ttu-id="e16cf-139">Annak az Azure Active Directory-fióknak az objektum-AZONOSÍTÓját adja meg, amelynek az engedélyeit el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="e16cf-139">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

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

### <span data-ttu-id="e16cf-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e16cf-140">-PassThru</span></span>
<span data-ttu-id="e16cf-141">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="e16cf-141">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e16cf-142">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="e16cf-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e16cf-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e16cf-143">-ResourceGroupName</span></span>
<span data-ttu-id="e16cf-144">Annak a kulcsfájl-csoportnak a nevét adja meg, amelynek a hozzáférési házirendjét módosították.</span><span class="sxs-lookup"><span data-stu-id="e16cf-144">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="e16cf-145">Ha nem adja meg, ez a parancsmag az aktuális előfizetésben keresi a fő boltozatot.</span><span class="sxs-lookup"><span data-stu-id="e16cf-145">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

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

### <span data-ttu-id="e16cf-146">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="e16cf-146">-ServicePrincipalName</span></span>
<span data-ttu-id="e16cf-147">Annak az alkalmazásnak az egyszerű szolgáltatásnevet adja meg, akinek az engedélyeit el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="e16cf-147">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="e16cf-148">Adja meg az Azure Active Directory alkalmazásban regisztrált alkalmazás-azonosítót (más néven ügyfél-azonosítót).</span><span class="sxs-lookup"><span data-stu-id="e16cf-148">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

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

### <span data-ttu-id="e16cf-149">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="e16cf-149">-UserPrincipalName</span></span>
<span data-ttu-id="e16cf-150">Annak a felhasználónak az egyszerű felhasználónevét adja meg, akinek az elérését el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="e16cf-150">Specifies the user principal name of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="e16cf-151">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e16cf-151">-VaultName</span></span>
<span data-ttu-id="e16cf-152">A fő pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e16cf-152">Specifies the name of the key vault.</span></span>
<span data-ttu-id="e16cf-153">Ez a parancsmag eltávolítja az engedélyeket a kulcsfájl számára, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="e16cf-153">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="e16cf-154">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e16cf-154">-Confirm</span></span>
<span data-ttu-id="e16cf-155">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e16cf-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e16cf-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e16cf-156">-WhatIf</span></span>
<span data-ttu-id="e16cf-157">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e16cf-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e16cf-158">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e16cf-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e16cf-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e16cf-159">CommonParameters</span></span>
<span data-ttu-id="e16cf-160">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e16cf-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e16cf-161">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e16cf-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e16cf-162">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e16cf-162">INPUTS</span></span>

### <span data-ttu-id="e16cf-163">Nincs</span><span class="sxs-lookup"><span data-stu-id="e16cf-163">None</span></span>
<span data-ttu-id="e16cf-164">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="e16cf-164">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e16cf-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e16cf-165">OUTPUTS</span></span>

### <span data-ttu-id="e16cf-166">Microsoft. Azure. Command. PSVault. models.</span><span class="sxs-lookup"><span data-stu-id="e16cf-166">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="e16cf-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e16cf-167">NOTES</span></span>

## <span data-ttu-id="e16cf-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e16cf-168">RELATED LINKS</span></span>

[<span data-ttu-id="e16cf-169">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e16cf-169">Set-AzKeyVaultAccessPolicy</span></span>](./Set-AzKeyVaultAccessPolicy.md)

