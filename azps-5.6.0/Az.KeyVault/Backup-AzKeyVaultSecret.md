---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/powershell/module/az.keyvault/backup-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
ms.openlocfilehash: ae60c2d10c8b186db22fb9fc9cd0a1e66aa1c07d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923618"
---
# Backup-AzKeyVaultSecret

## SYNOPSIS
Egy kulcstárban tárolt kulcsról biztonsági biztonsági ként biztonsági szerepet bevetve.

## SZINTAXIS

### BySecretName (alapértelmezett)
```
Backup-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### BySecret
```
Backup-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **Backup-AzKeyVaultSecret** parancsmag egy adott titkos kulcsról biztonsági másolatot készít egy kulcstárban letöltésével és egy fájlban való tárolásával.
Ha a titkos fájlnak több verziója is van, az összes verzió szerepelni fog a biztonsági másolatban.
Mivel a letöltött tartalom titkosítva van, nem használható az Azure-kulcstáron kívül.
Visszaállíthatja a biztonsági másolatokat az előfizetés bármely kulcstárába, amelyről biztonsági másolat volt.
A parancsmag használatának tipikus okai:
- El szeretné tartani a titkos másolata másolatát, hogy offline példánya legyen arra az esetre, ha véletlenül töröl egy titkos példányt a kulcstárból.
- Felvett egy titkos kulcsot egy kulcstárba, és most egy másik Azure-régióba szeretné azt klónozni, hogy az elosztott alkalmazás összes példányából használva használható. A Backup-AzKeyVaultSecret parancsmag használatával titkosított formátumban olvassa be a titkos kulcsot, majd a Restore-AzKeyVaultSecret parancsmagot használva adjon meg egy kulcstárat a második régióban. (Ne feledje, hogy a régióknak ugyanannak a földrajzi helynek kell lennie.)

## PÉLDÁK

### 1. példa: Titkos fájl biztonsági mentése automatikusan létrehozott fájlnévvel
```powershell
PS C:\Users\username\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'

C:\Users\username\mykeyvault-mysecret-1527029447.01191
```

Ez a parancs beolvassa a MyKeyVault nevű kulcstárból a MySecret nevű titkos másolatot, és egy automatikusan elnevezett fájlba menti annak biztonsági másolatát, és megjeleníti a fájl nevét.

### 2. példa: Titkos fájl biztonsági mentése egy megadott fájlnévre, a meglévő fájl felülírása rákérdezés nélkül
```powershell
PS C:\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Ez a parancs beolvassa a MySecret nevű titkos fájlt a MyKeyVault nevű kulcstárból, és biztonsági másolatot készít róla egy Backup.blob nevű fájlba.

### 3. példa: Korábban egy megadott fájlnévre lekért titkos fájl biztonsági mentése
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\> Backup-AzKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Ez a parancs a $secret objektum tárolónevét és nevét használva beolvassa a titkos fájlt, és a biztonsági másolatát egy Backup.blob nevű fájlba menti.

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés

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

### -Force
Ha létezik ilyen, a kimeneti fájl felülírása előtt megerősítést kér.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Titkos adat, amelyről biztonsági hívást kell biztonságivinni, és a beolvasási hívás kimeneteként kell bevinni.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: BySecret
Aliases: Secret

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Megadja a biztonságimentő titkos fájl nevét.

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFile
Azt a kimeneti fájlt adja meg, amelyben a biztonságimásolat-blob található.
Ha nem adja meg ezt a paramétert, ez a parancsmag létrehoz egy fájlnevet.
Ha megadja egy meglévő kimeneti fájl nevét, a művelet nem fejeződik be, és hibaüzenetet ad vissza arról, hogy a biztonsági másolat már létezik.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
Annak a kulcstárnak a nevét adja meg, amely a biztonsági adatokat tartalmazó titkos kulcsot tartalmazza.

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem

## KIMENETEK

### System.String

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Set-AzKeyVaultSecret](./Set-AzKeyVaultSecret.md)

[Get-AzKeyVaultSecret](./Get-AzKeyVaultSecret.md)

[Remove-AzKeyVaultSecret](./Remove-AzKeyVaultSecret.md)

[Restore-AzKeyVaultSecret](./Restore-AzKeyVaultSecret.md)

