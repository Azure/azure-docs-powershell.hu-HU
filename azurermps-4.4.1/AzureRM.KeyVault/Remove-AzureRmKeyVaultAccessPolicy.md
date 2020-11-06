---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://go.microsoft.com/fwlink/?LinkId=690164
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: 4e46c100984a9e50794130b3de6e30ce5f664ea4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502699"
---
# Remove-AzureRmKeyVaultAccessPolicy

## Áttekintés
Egy felhasználó vagy alkalmazás összes engedélyének eltávolítása egy kulcs-boltozatról.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByServicePrincipalName
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByUserPrincipalName
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByObjectId
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByEmail
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ForVault
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **Remove-AzureRmKeyVaultAccessPolicy** parancsmag eltávolítja a felhasználók vagy alkalmazások összes engedélyét, illetve a fő tárolók minden felhasználóját és alkalmazást.
Az Azure-előfizetés fő tárolóját tartalmazó Azure-előfizetés tulajdonosa még akkor is adhat hozzá engedélyeket a kulcs boltozatához, ha eltávolítja az összes engedélyt.

Fontos tudni, hogy bár az erőforráscsoport beállítása nem kötelező ehhez a parancsmaghoz, a jobb teljesítmény érdekében ezt el kell végeznie.

## Példák

### 1. példa: felhasználó engedélyeinek eltávolítása
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com'
```

Ez a parancs eltávolítja az összes olyan engedélyt, amelyet a felhasználó a PattiFuller@contoso.com Contoso03Vault nevű kulcs-boltíven tartalmaz.

### 2. példa: az alkalmazások engedélyeinek eltávolítása
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

Ez a parancs eltávolítja az összes olyan engedélyt, amelyet az alkalmazás a Contoso03Vault nevű kulcs boltozaton tartalmaz.
Ez a példa azonosítja az alkalmazást az Azure Active Directory szolgáltatásban regisztrált egyszerű szolgáltatásnév használatával http://payroll.contoso.com .

### 3. példa: az alkalmazás engedélyeinek eltávolítása az objektum-azonosító használatával
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

Ez a parancs eltávolítja az összes olyan engedélyt, amelyet az alkalmazás a Contoso03Vault nevű kulcs boltozaton tartalmaz.
Ez a példa azonosítja az alkalmazást a szolgáltatás megbízójának objektum-azonosítója alapján.

### 4. példa: engedélyek eltávolítása a Microsofthoz. számítási erőforrás-szolgáltató
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

Ez a parancs eltávolítja az engedélyt a Microsoft számára. az erőforrás-szolgáltató kiszámításához a Contoso03Vault titkait kell beszereznie.

## PARAMÉTEREK

### -ApplicationId
Jövőbeli használatra.

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByObjectId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EmailAddress
Annak a felhasználónak a felhasználói e-mail-címét adja meg, akinek az elérését el szeretné távolítani.

```yaml
Type: System.String
Parameter Sets: ByEmail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnabledForDeployment
A Microsoft. számítási erőforrás-szolgáltatója kinyerheti a titkokat ebből a kulcsfájlból, ha ez a kulcs boltozata az erőforrás létrehozásakor, például virtuális gép létrehozásakor jelenik meg.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnabledForDiskEncryption
Lehetővé teszi, hogy az Azure Disk Encryption szolgáltatás a kulcsok kijavítását és kicsomagolását a kulcsból.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnabledForTemplateDeployment
Lehetővé teszi az Azure Resource Manager számára, hogy ebből a kulcsfájlból kiírja a titkot, ha ezt a kulcspárt a sablonok központi telepítéséhez hivatkozik.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
Annak az Azure Active Directory-fióknak az objektum-AZONOSÍTÓját adja meg, amelynek az engedélyeit el szeretné távolítani.

```yaml
Type: System.String
Parameter Sets: ByObjectId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.
Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.

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

### -ResourceGroupName
Annak a kulcsfájl-csoportnak a nevét adja meg, amelynek a hozzáférési házirendjét módosították.
Ha nem adja meg, ez a parancsmag az aktuális előfizetésben keresi a fő boltozatot.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
Annak az alkalmazásnak az egyszerű szolgáltatásnevet adja meg, akinek az engedélyeit el szeretné távolítani.
Adja meg az Azure Active Directory alkalmazásban regisztrált alkalmazás-azonosítót (más néven ügyfél-azonosítót).

```yaml
Type: System.String
Parameter Sets: ByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserPrincipalName
Annak a felhasználónak az egyszerű felhasználónevét adja meg, akinek az elérését el szeretné távolítani.

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
A fő pince nevét adja meg.
Ez a parancsmag eltávolítja az engedélyeket a kulcsfájl számára, amelyet a paraméter határoz meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

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

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

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

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. Azure. Command. PSVault. models.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Set-AzureRmKeyVaultAccessPolicy](./Set-AzureRmKeyVaultAccessPolicy.md)

