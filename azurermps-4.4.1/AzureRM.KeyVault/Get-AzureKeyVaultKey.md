---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://go.microsoft.com/fwlink/?LinkId=690297
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
ms.openlocfilehash: 48d050623ea75bed1aee1b78a26bf81bf3305e06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493498"
---
# Get-AzureKeyVaultKey

## Áttekintés
Beolvassa a kulcsok kulcsát.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByVaultName (alapértelmezett)
```
Get-AzureKeyVaultKey [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByKeyName
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByKeyVersions
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByDeletedKey
```
Get-AzureKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureKeyVaultKey** parancsmag Azure Key Vault-kulcsokat kap.
Ez a parancsmag a **Microsoft. Azure. commands. kulcskezelő. models.** vagy a kulcsfájl vagy **az összes kulcskezelő** objektum listáját adja meg egy kulcs-boltozatban vagy egy verzióban.

## Példák

### 1. példa: a billentyűk lekérése a fő boltozaton
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso'
```

Ez a parancs a contoso nevű fő boltozat összes kulcsát kinyeri.

### 2. példa: a kulcs aktuális verziójának beszerzése
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx'
```

Ez a parancs beolvassa a ITPfx nevű kulcs aktuális verzióját a contoso nevű kulcs boltozatában.

### 3. példa: a kulcsok minden verziójának beolvasása
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -IncludeVersions
```

Ez a parancs a ITPfx nevű kulcsot a contoso vaultnamed kulcsában kapja meg.

### Példa 4: a kulcs meghatározott verziójának beszerzése
```
PS C:\>$Key = Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -Version '5A12A276385949DB8B5F82AFEE85CAED'
```

Ez a parancs beolvassa a ITPfx nevű kulcs egy bizonyos verzióját a contoso nevű kulcs boltozatában.
Miután futtatta ezt a parancsot, a $Key objektumban való navigálással ellenőrizheti a billentyűk különböző tulajdonságait.

### 5. példa: a kulcsfájl által törölt, de nem törölt billentyűk beolvasása.
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -InRemovedState
```

Ez a parancs az összes korábban törölt, de nem törölt billentyűt beilleszti a contoso nevű billentyűvel.

### 6. példa: a kulcsfájl a ITPfx, amelyet töröltek, de nem tisztítják meg.
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -InRemovedState
```

Ez a parancs a contoso nevű kulcsfájl által korábban törölt, de el nem távolított kulcs ITPfx kapja meg.
Ez a parancs metaadatokat ad vissza, például a törlési dátumot, valamint a törölt kulcs ütemezett leöblítési dátumát.

## PARAMÉTEREK

### -IncludeVersions
Azt jelzi, hogy ez a parancsmag a kulcsok minden verzióját bekapja.
A kulcsok jelenlegi verziója az első a listán.
Ha ezt a paramétert adja meg, a *nevet* és a *VaultName* paramétereket is meg kell adnia.

Ha nem adja meg a *IncludeVersions* paramétert, ez a parancsmag a megadott *nevű* kulcs aktuális verzióját kapja meg.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByKeyVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InRemovedState
Itt adhatja meg, hogy megjelenjen-e a korábban törölt kulcsok a kimenetben.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedKey
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A beolvasott kulcs kötegének nevét adja meg.

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedKey
Aliases: KeyName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Annak a kulcsnak a nevét adja meg, amelyből a parancsmag kulcsokat kap.
Ez a parancsmag a kulcsfájl teljesen minősített tartománynevét (FQDN) építi fel a paraméter által megadott név és a kijelölt környezet alapján.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Verzió
A kulcs verziószámát adja meg.
Ez a parancsmag a kulcs teljes tartománynevét, az aktuálisan kijelölt környezetet, a kulcs nevét és a kulcs verziószámát építi fel.

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyVersion

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### Karakterlánc

## KIMENETEK

### Lista<Microsoft. Azure. commands. KeyIdentityItem. models.>, Microsoft. Azure. commands.-Vault. models. debundle, List<Microsoft. Azure. Command. DeletedKeyBundle. DeletedKeyIdentityItem>, Microsoft. Azure. Command.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureKeyVaultKey](./Add-AzureKeyVaultKey.md)

[Remove-AzureKeyVaultKey](./Remove-AzureKeyVaultKey.md)

[Visszavonás – AzureKeyVaultKeyRemoval](./Undo-AzureKeyVaultKeyRemoval.md)

[Set-AzureKeyVaultKeyAttribute](./Set-AzureKeyVaultKeyAttribute.md)

