---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvaultaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 421a2becff4c32f4c29990f32cbf1a4c6e9a3e84
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848205"
---
# <span data-ttu-id="7d4e0-101">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7d4e0-101">Remove-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="7d4e0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7d4e0-102">SYNOPSIS</span></span>
<span data-ttu-id="7d4e0-103">Egy felhasználó vagy alkalmazás összes engedélyének eltávolítása egy kulcs-boltozatról.</span><span class="sxs-lookup"><span data-stu-id="7d4e0-103">Removes all permissions for a user or application from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d4e0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7d4e0-104">SYNTAX</span></span>

### <span data-ttu-id="7d4e0-105">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="7d4e0-105">ByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d4e0-106">ByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="7d4e0-106">ByUserPrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d4e0-107">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="7d4e0-107">ByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d4e0-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="7d4e0-108">ByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d4e0-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="7d4e0-109">ForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d4e0-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="7d4e0-110">DESCRIPTION</span></span>
<span data-ttu-id="7d4e0-111">A **Remove-AzureRmKeyVaultAccessPolicy** parancsmag eltávolítja a felhasználók vagy alkalmazások összes engedélyét, illetve a fő tárolók minden felhasználóját és alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="7d4e0-111">The **Remove-AzureRmKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="7d4e0-112">Az Azure-előfizetés fő tárolóját tartalmazó Azure-előfizetés tulajdonosa még akkor is adhat hozzá engedélyeket a kulcs boltozatához, ha eltávolítja az összes engedélyt.</span><span class="sxs-lookup"><span data-stu-id="7d4e0-112">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>

<span data-ttu-id="7d4e0-113">Fontos tudni, hogy bár az erőforráscsoport beállítása nem kötelező ehhez a parancsmaghoz, a jobb teljesítmény érdekében ezt el kell végeznie.</span><span class="sxs-lookup"><span data-stu-id="7d4e0-113">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="7d4e0-114">Példák</span><span class="sxs-lookup"><span data-stu-id="7d4e0-114">EXAMPLES</span></span>

### <span data-ttu-id="7d4e0-115">1. példa: felhasználó engedélyeinek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7d4e0-115">Example 1: Remove permissions for a user</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com'
```

<span data-ttu-id="7d4e0-116">Ez a parancs eltávolítja az összes olyan engedélyt, amelyet a felhasználó a PattiFuller@contoso.com Contoso03Vault nevű kulcs-boltíven tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="7d4e0-116">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>

### <span data-ttu-id="7d4e0-117">2. példa: az alkalmazások engedélyeinek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7d4e0-117">Example 2: Remove permissions for an application</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="7d4e0-118">Ez a parancs eltávolítja az összes olyan engedélyt, amelyet az alkalmazás a Contoso03Vault nevű kulcs boltozaton tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="7d4e0-118">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="7d4e0-119">Ez a példa azonosítja az alkalmazást az Azure Active Directory szolgáltatásban regisztrált egyszerű szolgáltatásnév használatával http://payroll.contoso.com .</span><span class="sxs-lookup"><span data-stu-id="7d4e0-119">This example identifies the application by using the service principal name registered in Azure Active Directory, http://payroll.contoso.com.</span></span>

### <span data-ttu-id="7d4e0-120">3. példa: az alkalmazás engedélyeinek eltávolítása az objektum-azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="7d4e0-120">Example 3: Remove permissions for an application by using its object ID</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="7d4e0-121">Ez a parancs eltávolítja az összes olyan engedélyt, amelyet az alkalmazás a Contoso03Vault nevű kulcs boltozaton tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="7d4e0-121">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="7d4e0-122">Ez a példa azonosítja az alkalmazást a szolgáltatás megbízójának objektum-azonosítója alapján.</span><span class="sxs-lookup"><span data-stu-id="7d4e0-122">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="7d4e0-123">4. példa: engedélyek eltávolítása a Microsofthoz. számítási erőforrás-szolgáltató</span><span class="sxs-lookup"><span data-stu-id="7d4e0-123">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="7d4e0-124">Ez a parancs eltávolítja az engedélyt a Microsoft számára. az erőforrás-szolgáltató kiszámításához a Contoso03Vault titkait kell beszereznie.</span><span class="sxs-lookup"><span data-stu-id="7d4e0-124">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="7d4e0-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7d4e0-125">PARAMETERS</span></span>

### <span data-ttu-id="7d4e0-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7d4e0-126">-ApplicationId</span></span>
<span data-ttu-id="7d4e0-127">Jövőbeli használatra.</span><span class="sxs-lookup"><span data-stu-id="7d4e0-127">For future use.</span></span>

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

### <span data-ttu-id="7d4e0-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d4e0-128">-DefaultProfile</span></span>
<span data-ttu-id="7d4e0-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7d4e0-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d4e0-130">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="7d4e0-130">-EmailAddress</span></span>
<span data-ttu-id="7d4e0-131">Annak a felhasználónak a felhasználói e-mail-címét adja meg, akinek az elérését el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="7d4e0-131">Specifies the user email address of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="7d4e0-132">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="7d4e0-132">-EnabledForDeployment</span></span>
<span data-ttu-id="7d4e0-133">A Microsoft. számítási erőforrás-szolgáltatója kinyerheti a titkokat ebből a kulcsfájlból, ha ez a kulcs boltozata az erőforrás létrehozásakor, például virtuális gép létrehozásakor jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="7d4e0-133">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="7d4e0-134">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="7d4e0-134">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="7d4e0-135">Lehetővé teszi, hogy az Azure Disk Encryption szolgáltatás a kulcsok kijavítását és kicsomagolását a kulcsból.</span><span class="sxs-lookup"><span data-stu-id="7d4e0-135">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="7d4e0-136">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="7d4e0-136">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="7d4e0-137">Lehetővé teszi az Azure Resource Manager számára, hogy ebből a kulcsfájlból kiírja a titkot, ha ezt a kulcspárt a sablonok központi telepítéséhez hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="7d4e0-137">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="7d4e0-138">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7d4e0-138">-ObjectId</span></span>
<span data-ttu-id="7d4e0-139">Annak az Azure Active Directory-fióknak az objektum-AZONOSÍTÓját adja meg, amelynek az engedélyeit el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="7d4e0-139">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

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

### <span data-ttu-id="7d4e0-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d4e0-140">-PassThru</span></span>
<span data-ttu-id="7d4e0-141">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="7d4e0-141">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7d4e0-142">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="7d4e0-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7d4e0-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d4e0-143">-ResourceGroupName</span></span>
<span data-ttu-id="7d4e0-144">Annak a kulcsfájl-csoportnak a nevét adja meg, amelynek a hozzáférési házirendjét módosították.</span><span class="sxs-lookup"><span data-stu-id="7d4e0-144">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="7d4e0-145">Ha nem adja meg, ez a parancsmag az aktuális előfizetésben keresi a fő boltozatot.</span><span class="sxs-lookup"><span data-stu-id="7d4e0-145">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

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

### <span data-ttu-id="7d4e0-146">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="7d4e0-146">-ServicePrincipalName</span></span>
<span data-ttu-id="7d4e0-147">Annak az alkalmazásnak az egyszerű szolgáltatásnevet adja meg, akinek az engedélyeit el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="7d4e0-147">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="7d4e0-148">Adja meg az Azure Active Directory alkalmazásban regisztrált alkalmazás-azonosítót (más néven ügyfél-azonosítót).</span><span class="sxs-lookup"><span data-stu-id="7d4e0-148">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

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

### <span data-ttu-id="7d4e0-149">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="7d4e0-149">-UserPrincipalName</span></span>
<span data-ttu-id="7d4e0-150">Annak a felhasználónak az egyszerű felhasználónevét adja meg, akinek az elérését el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="7d4e0-150">Specifies the user principal name of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="7d4e0-151">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7d4e0-151">-VaultName</span></span>
<span data-ttu-id="7d4e0-152">A fő pince nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7d4e0-152">Specifies the name of the key vault.</span></span>
<span data-ttu-id="7d4e0-153">Ez a parancsmag eltávolítja az engedélyeket a kulcsfájl számára, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="7d4e0-153">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="7d4e0-154">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7d4e0-154">-Confirm</span></span>
<span data-ttu-id="7d4e0-155">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7d4e0-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d4e0-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d4e0-156">-WhatIf</span></span>
<span data-ttu-id="7d4e0-157">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7d4e0-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d4e0-158">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7d4e0-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d4e0-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d4e0-159">CommonParameters</span></span>
<span data-ttu-id="7d4e0-160">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7d4e0-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d4e0-161">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d4e0-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d4e0-162">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d4e0-162">INPUTS</span></span>

## <span data-ttu-id="7d4e0-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d4e0-163">OUTPUTS</span></span>

### <span data-ttu-id="7d4e0-164">Microsoft. Azure. Command. PSVault. models.</span><span class="sxs-lookup"><span data-stu-id="7d4e0-164">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="7d4e0-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7d4e0-165">NOTES</span></span>

## <span data-ttu-id="7d4e0-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d4e0-166">RELATED LINKS</span></span>

[<span data-ttu-id="7d4e0-167">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7d4e0-167">Set-AzureRmKeyVaultAccessPolicy</span></span>](./Set-AzureRmKeyVaultAccessPolicy.md)

