---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: 88decaffa736f015b8e65aa1217eab4899b07c7c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351930"
---
# Backup-AzKeyVaultKey

## SYNOPSIS
Kulcs biztonsági biztonsági hátramentve a kulcstárban.

## SZINTAXIS

### ByKeyName (alapértelmezett)
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmByKeyName
```
Backup-AzKeyVaultKey -HsmName <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByKey
```
Backup-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **Backup-AzKeyVaultKey** parancsmag egy adott kulcsról biztonsági másolatot készít egy kulcstárban úgy, hogy letölti és egy fájlban tárolja azt.
Ha a kulcsnak több verziója is van, az összes verzió szerepelni fog a biztonsági másolatban.
Mivel a letöltött tartalom titkosítva van, nem használható az Azure-kulcstáron kívül.
Az előfizetés bármely kulcstárában visszaállíthat egy biztonsági másolati kulcsot, amelyről biztonsági másolat volt.
A parancsmag használatának tipikus okai: 
- A kulcs egy példányát el szeretné escrow-nak, hogy offline példánya legyen arra az esetre, ha véletlenül törli a kulcsot a kulcstárban.
 
- A kulcstár segítségével létrehozott egy kulcsot, és most egy másik Azure-régióba szeretné a kulcsot klónozni, hogy az elosztott alkalmazás összes példányából használva használható.
A **Backup-AzKeyVaultKey** parancsmag használatával titkosított formátumban olvassa be a kulcsot, majd használja a Restore-AzKeyVaultKey-parancsmagot, és adjon meg egy kulcstárat a második régióban.

## PÉLDÁK

### 1. példa: Kulcs biztonsági mentése automatikusan létrehozott fájlnévvel
```powershell
PS C:\Users\username\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'

C:\Users\username\mykeyvault-mykey-1527029447.01191
```

Ez a parancs beolvassa a MyKeyVault nevű kulcstárból a MyKeyVault nevű kulcsot, és egy automatikusan elnevezett fájlba menti a kulcs biztonsági másolatát, és megjeleníti a fájl nevét.

### 2. példa: Kulcs biztonsági mentése egy megadott fájlnévre
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Ez a parancs lekéri a MyKey nevű kulcskulcsot a MyKeyVault nevű kulcstárból, és biztonsági másolatot készít róla egy Backup.blob nevű fájlba.

### 3. példa: Korábban lekért kulcs biztonsági mentése egy megadott fájlnévre, a célfájl felülírása kérés nélkül.
```powershell
PS C:\> $key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\> Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Ezzel a paranccsal biztonsági másolatot készít a $key. Név a tárolóban $key. A Backup.blob nevű fájl VaultName fájlja, amely csendesen felülírja a fájlt, ha már létezik.

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
A megadott fájl felülírása( ha létezik)

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

### -HsmName
HSM-név. A parancsmag a felügyelt HSM teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.

```yaml
Type: System.String
Parameter Sets: HsmByKeyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Key bundle to back up, pipelined in from the output of a retrieval call.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
A biztonságimentő kulcs nevét adja meg.

```yaml
Type: System.String
Parameter Sets: ByKeyName, HsmByKeyName
Aliases: KeyName

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
Annak a kulcstárnak a nevét adja meg, amely a biztonsági adatokat tartalmazó kulcsot tartalmazza.

```yaml
Type: System.String
Parameter Sets: ByKeyName
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem

## KIMENETEK

### System.String

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzKeyVaultKey](./Add-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

[Restore-AzKeyVaultKey](./Restore-AzKeyVaultKey.md)

