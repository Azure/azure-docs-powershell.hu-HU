---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
ms.openlocfilehash: b14e97ba09cba70a9ec571b2fbf1273de7157930
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843889"
---
# Get-AzKeyVaultSecret

## Áttekintés
Megnyeri a titkot egy kulcs boltozaton.

## SZINTAXISA

### ByVaultName (alapértelmezett)
```
Get-AzKeyVaultSecret [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BySecretName
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BySecretVersions
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByDeletedSecrets
```
Get-AzKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzKeyVaultSecret** parancsmag a kulcsok egy fő boltozatát adja meg.
Ez a parancsmag adott titkos vagy minden titkot kap a kulcs boltozatában.

## Példák

### Példa 1: az összes titok jelenlegi verziójának beszerzése a kulcs boltozatára
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso'
```

Ez a parancs az összes titok aktuális verzióját a contoso nevű fő boltívben kapja meg.

### 2. példa: egy adott titok összes verziójának beszerzése
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -IncludeVersions
```

Ez a parancs a contoso nevű ITSecret a titkos nevű titkos verzió összes verzióját megkapja.

### 3. példa: egy adott titok aktuális verziójának beszerzése
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
```

Ez a parancs a contoso nevű ITSecret a titkos nevű titkos verzió jelenlegi verzióját kapja meg.

### Példa 4: adott titok meghatározott verziójának beszerzése
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -Version '6A12A286385949DB8B5F82AFEF85CAE9'
```

Ez a parancs a contoso nevű ITSecret a titkos nevű titkos verzió adott verzióját kapja meg.

### Példa 5: egy adott titok aktuális verziójának egyszerű szöveges értékének beszerzése
```
PS C:\>$secret = Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is: " $secret.SecretValueText
```

Ezek a parancsok beolvassák a titkos nevű ITSecret aktuális verzióját, majd megjelenítik az adott titok egyszerű szöveges értékét.

### 6. példa: a kulcsfájl minden törölt, de el nem távolított titkát beolvassa.
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -InRemovedState
```

Ez a parancs minden korábban törölt, de nem törölt titkot kap a contoso nevű fő boltozatban.

### 7. példa: a kulcsfájl által törölt, de meg nem tisztított titkos ITSecret kapja meg.
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -KeyName 'ITSecret' -InRemovedState
```

Ez a parancs a contoso nevű kulcsfájl által korábban törölt, de el nem távolított titkos ITSecret kapja meg.
Ez a parancs metaadatokat ad vissza, például a törlési dátumot, valamint a törölt titok ütemezett végleges dátumát.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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

### -IncludeVersions
Azt jelzi, hogy ez a parancsmag minden titkos verziót kap.
A titok jelenlegi verziója az első a listán.
Ha ezt a paramétert adja meg, a *nevet* és a *VaultName* paramétereket is meg kell adnia.

Ha nem adja meg a *IncludeVersions* paramétert, ez a parancsmag a megadott *néven* a titok aktuális verzióját kapja meg.

```yaml
Type: SwitchParameter
Parameter Sets: BySecretVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InRemovedState
Megadja, hogy megjelenjen-e a korábban törölt titok a kimenetben

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedSecrets
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A beolvasott titok nevét adja meg.

```yaml
Type: String
Parameter Sets: BySecretName, BySecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedSecrets
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Annak a fő boltozatnak a neve, amelyhez a titok tartozik.
Ez a parancsmag a kulcsfájl teljes tartománynevét (FQDN) építi fel a paraméter által megadott név és a jelenlegi környezet alapján.

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

### -Verzió
A titkos verziót adja meg.
Ez a parancsmag a titkos név, az aktuálisan kijelölt környezet, a titkos név és a titkos verzió alapján építi be a titok teljes tartománynevét.

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Karakterlánc

## KIMENETEK

### Lista<Microsoft. Azure. commands. SecretIdentityItem. models.>, Microsoft. Azure. commands.-Vault. models. Secret, List<Microsoft. Azure. Command. DeletedSecret. DeletedSecretIdentityItem>, Microsoft. Azure. Command.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Remove-AzKeyVaultSecret](./Remove-AzKeyVaultSecret.md)

[Visszavonás – AzKeyVaultSecretRemoval](./Undo-AzKeyVaultSecretRemoval.md)

[Set-AzKeyVaultSecret](./Set-AzKeyVaultSecret.md)

