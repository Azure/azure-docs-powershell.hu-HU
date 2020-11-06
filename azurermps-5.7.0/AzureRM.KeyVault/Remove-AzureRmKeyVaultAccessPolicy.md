---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: ca175d0873b74d8b13d1755f3d0986580c5853ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498939"
---
# <span data-ttu-id="36ba1-101">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="36ba1-101">Remove-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="36ba1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="36ba1-102">SYNOPSIS</span></span>
<span data-ttu-id="36ba1-103">Egy felhasználó vagy alkalmazás összes engedélyének eltávolítása egy kulcs-boltozatról.</span><span class="sxs-lookup"><span data-stu-id="36ba1-103">Removes all permissions for a user or application from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36ba1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="36ba1-104">SYNTAX</span></span>

### <span data-ttu-id="36ba1-105">ByUserPrincipalName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="36ba1-105">ByUserPrincipalName (Default)</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36ba1-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="36ba1-106">ByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36ba1-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="36ba1-107">ByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36ba1-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="36ba1-108">ByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36ba1-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="36ba1-109">ForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36ba1-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="36ba1-110">InputObjectByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36ba1-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="36ba1-111">InputObjectByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36ba1-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="36ba1-112">InputObjectByUserPrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36ba1-113">InputObjectByEmail</span><span class="sxs-lookup"><span data-stu-id="36ba1-113">InputObjectByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36ba1-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="36ba1-114">InputObjectForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36ba1-115">Leírás</span><span class="sxs-lookup"><span data-stu-id="36ba1-115">DESCRIPTION</span></span>
<span data-ttu-id="36ba1-116">A **Remove-AzureRmKeyVaultAccessPolicy** parancsmag eltávolítja a felhasználók vagy alkalmazások összes engedélyét, illetve a fő tárolók minden felhasználóját és alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="36ba1-116">The **Remove-AzureRmKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="36ba1-117">Az Azure-előfizetés fő tárolóját tartalmazó Azure-előfizetés tulajdonosa még akkor is adhat hozzá engedélyeket a kulcs boltozatához, ha eltávolítja az összes engedélyt.</span><span class="sxs-lookup"><span data-stu-id="36ba1-117">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>

<span data-ttu-id="36ba1-118">Fontos tudni, hogy bár az erőforráscsoport beállítása nem kötelező ehhez a parancsmaghoz, a jobb teljesítmény érdekében ezt el kell végeznie.</span><span class="sxs-lookup"><span data-stu-id="36ba1-118">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="36ba1-119">Példák</span><span class="sxs-lookup"><span data-stu-id="36ba1-119">EXAMPLES</span></span>

### <span data-ttu-id="36ba1-120">1. példa: felhasználó engedélyeinek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="36ba1-120">Example 1: Remove permissions for a user</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com'
```

<span data-ttu-id="36ba1-121">Ez a parancs eltávolítja az összes olyan engedélyt, amelyet a felhasználó a PattiFuller@contoso.com Contoso03Vault nevű kulcs-boltíven tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="36ba1-121">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>

### <span data-ttu-id="36ba1-122">2. példa: az alkalmazások engedélyeinek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="36ba1-122">Example 2: Remove permissions for an application</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="36ba1-123">Ez a parancs eltávolítja az összes olyan engedélyt, amelyet az alkalmazás a Contoso03Vault nevű kulcs boltozaton tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="36ba1-123">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="36ba1-124">Ez a példa azonosítja az alkalmazást az Azure Active Directory szolgáltatásban regisztrált egyszerű szolgáltatásnév használatával http://payroll.contoso.com .</span><span class="sxs-lookup"><span data-stu-id="36ba1-124">This example identifies the application by using the service principal name registered in Azure Active Directory, http://payroll.contoso.com.</span></span>

### <span data-ttu-id="36ba1-125">3. példa: az alkalmazás engedélyeinek eltávolítása az objektum-azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="36ba1-125">Example 3: Remove permissions for an application by using its object ID</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="36ba1-126">Ez a parancs eltávolítja az összes olyan engedélyt, amelyet az alkalmazás a Contoso03Vault nevű kulcs boltozaton tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="36ba1-126">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="36ba1-127">Ez a példa azonosítja az alkalmazást a szolgáltatás megbízójának objektum-azonosítója alapján.</span><span class="sxs-lookup"><span data-stu-id="36ba1-127">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="36ba1-128">4. példa: engedélyek eltávolítása a Microsofthoz. számítási erőforrás-szolgáltató</span><span class="sxs-lookup"><span data-stu-id="36ba1-128">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="36ba1-129">Ez a parancs eltávolítja az engedélyt a Microsoft számára. az erőforrás-szolgáltató kiszámításához a Contoso03Vault titkait kell beszereznie.</span><span class="sxs-lookup"><span data-stu-id="36ba1-129">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="36ba1-130">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="36ba1-130">PARAMETERS</span></span>

### <span data-ttu-id="36ba1-131">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="36ba1-131">-ApplicationId</span></span>
<span data-ttu-id="36ba1-132">Annak az alkalmazásnak az AZONOSÍTÓját adja meg, amelynek az engedélyeit el kell távolítani</span><span class="sxs-lookup"><span data-stu-id="36ba1-132">Specifies the ID of application whose permissions should be removed</span></span>

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

### <span data-ttu-id="36ba1-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36ba1-133">-DefaultProfile</span></span>
<span data-ttu-id="36ba1-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="36ba1-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36ba1-135">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="36ba1-135">-EmailAddress</span></span>
<span data-ttu-id="36ba1-136">Annak a felhasználónak a felhasználói e-mail-címét adja meg, akinek az elérését el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="36ba1-136">Specifies the user email address of the user whose access you want to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByEmail, InputObjectByEmail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36ba1-137">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="36ba1-137">-EnabledForDeployment</span></span>
<span data-ttu-id="36ba1-138">Ha meg van adva, azzal letiltja a titkot ebből a kulcsfájlból a Microsofttól. kiszámítja az erőforrás-szolgáltatót, ha az erőforrás létrehozásakor hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="36ba1-138">If specified, disables the retrieval of secrets from this key vault by the Microsoft.Compute resource provider when referenced in resource creation.</span></span>

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

### <span data-ttu-id="36ba1-139">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="36ba1-139">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="36ba1-140">Ha meg van adva, akkor az Azure Disk Encryption segítségével letilthatja a titkos kulcsok e kulcsból való lekérését.</span><span class="sxs-lookup"><span data-stu-id="36ba1-140">If specified, disables the retrieval of secrets from this key vault by Azure Disk Encryption.</span></span>

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

### <span data-ttu-id="36ba1-141">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="36ba1-141">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="36ba1-142">Ha meg van adva, akkor a sablonok esetén az Azure Resource Manager letiltja a titkok e kulcsból való lekérését.</span><span class="sxs-lookup"><span data-stu-id="36ba1-142">If specified, disables the retrieval of secrets from this key vault by Azure Resource Manager when referenced in templates.</span></span>

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

### <span data-ttu-id="36ba1-143">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36ba1-143">-InputObject</span></span>
<span data-ttu-id="36ba1-144">A Key Vault objektum.</span><span class="sxs-lookup"><span data-stu-id="36ba1-144">Key Vault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmail, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36ba1-145">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="36ba1-145">-ObjectId</span></span>
<span data-ttu-id="36ba1-146">Annak az Azure Active Directory-fióknak az objektum-AZONOSÍTÓját adja meg, amelynek az engedélyeit el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="36ba1-146">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

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

### <span data-ttu-id="36ba1-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36ba1-147">-PassThru</span></span>
<span data-ttu-id="36ba1-148">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="36ba1-148">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="36ba1-149">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="36ba1-149">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="36ba1-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36ba1-150">-ResourceGroupName</span></span>
<span data-ttu-id="36ba1-151">Annak a kulcsfájl-csoportnak a nevét adja meg, amelynek a hozzáférési házirendjét módosították.</span><span class="sxs-lookup"><span data-stu-id="36ba1-151">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="36ba1-152">Ha nem adja meg, ez a parancsmag az aktuális előfizetésben keresi a fő boltozatot.</span><span class="sxs-lookup"><span data-stu-id="36ba1-152">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36ba1-153">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="36ba1-153">-ServicePrincipalName</span></span>
<span data-ttu-id="36ba1-154">Annak az alkalmazásnak az egyszerű szolgáltatásnevet adja meg, akinek az engedélyeit el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="36ba1-154">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="36ba1-155">Adja meg az Azure Active Directory alkalmazásban regisztrált alkalmazás-azonosítót (más néven ügyfél-azonosítót).</span><span class="sxs-lookup"><span data-stu-id="36ba1-155">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

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

### <span data-ttu-id="36ba1-156">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="36ba1-156">-UserPrincipalName</span></span>
<span data-ttu-id="36ba1-157">Annak a felhasználónak az egyszerű felhasználónevét adja meg, akinek az elérését el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="36ba1-157">Specifies the user principal name of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="36ba1-158">-VaultName</span><span class="sxs-lookup"><span data-stu-id="36ba1-158">-VaultName</span></span>
<span data-ttu-id="36ba1-159">A fő pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="36ba1-159">Specifies the name of the key vault.</span></span>
<span data-ttu-id="36ba1-160">Ez a parancsmag eltávolítja az engedélyeket a kulcsfájl számára, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="36ba1-160">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36ba1-161">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="36ba1-161">-Confirm</span></span>
<span data-ttu-id="36ba1-162">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="36ba1-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36ba1-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36ba1-163">-WhatIf</span></span>
<span data-ttu-id="36ba1-164">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="36ba1-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36ba1-165">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="36ba1-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36ba1-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36ba1-166">CommonParameters</span></span>
<span data-ttu-id="36ba1-167">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="36ba1-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36ba1-168">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36ba1-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36ba1-169">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="36ba1-169">INPUTS</span></span>

### <span data-ttu-id="36ba1-170">Nincs</span><span class="sxs-lookup"><span data-stu-id="36ba1-170">None</span></span>
<span data-ttu-id="36ba1-171">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="36ba1-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="36ba1-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36ba1-172">OUTPUTS</span></span>

### <span data-ttu-id="36ba1-173">Microsoft. Azure. Command. PSKeyVault. models.</span><span class="sxs-lookup"><span data-stu-id="36ba1-173">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="36ba1-174">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="36ba1-174">NOTES</span></span>

## <span data-ttu-id="36ba1-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36ba1-175">RELATED LINKS</span></span>

[<span data-ttu-id="36ba1-176">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="36ba1-176">Set-AzureRmKeyVaultAccessPolicy</span></span>](./Set-AzureRmKeyVaultAccessPolicy.md)

