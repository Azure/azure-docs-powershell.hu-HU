---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: cd5e869b1f1d367002b33c5976434f16b22744e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835781"
---
# Backup-AzKeyVaultKey

## Áttekintés
Biztonsági másolatot készíthet egy kulcsról a boltívben.

## SZINTAXISA

### ByKeyName (alapértelmezett)
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByKey
```
Backup-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **biztonsági másolat-AzKeyVaultKey** parancsmag a megadott kulcs biztonsági másolatát biztonsági másolatokkal, letöltéssel és fájlba való tárolással támogatja.
Ha a kulcs több verziója is létezik, az összes verzió megtalálható a biztonsági másolatban.
Mivel a letöltött tartalom titkosítva van, nem használható az Azure Key Vault-on kívül.
A mentett billentyűket visszaállíthatja annak az előfizetésnek a fő boltozatára, amelyről biztonsági másolatot készített.
A parancsmag használatának tipikus okai a következők: 
- Szeretne a kulcs egy példányát letétbe helyezni, hogy legyen kapcsolat nélküli példánya, ha véletlenül törli a billentyűt a kulcs-boltozatban.
 
- A Key Vault segítségével létrehozta a kulcsot, és most szeretné egy másik Azure-területre beilleszteni a kulcsot, így a kiosztott alkalmazás minden példányában használhatja azt.
Használja a **Backup-AzKeyVaultKey** parancsmagot a kulcs titkosított formátumban való visszakereséséhez, majd használja az Restore-AzKeyVaultKey parancsmagot, és adja meg a második régióban a kulcs boltozatát.

## Példák

### 1. példa: kulcs biztonsági mentése automatikusan generált fájlnévvel
```powershell
PS C:\Users\username\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'

C:\Users\username\mykeyvault-mykey-1527029447.01191
```

Ez a parancs beolvassa a MyKey nevű kulcsot a MyKeyVault nevű kulcskezelő szolgáltatásból, és menti az adott kulcs biztonsági másolatát egy automatikusan megnevezett fájlba, és megjeleníti a fájl nevét.

### 2. példa: kulcs biztonsági mentése megadott fájlnévre
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Ez a parancs beolvassa a MyKey nevű kulcsot a vaultnamed MyKeyVault, és menti az adott kulcs biztonsági másolatát egy backup. blob nevű fájlba.

### 3. példa: biztonsági másolat készítése korábban lekérdezett kulcsról egy megadott fájlnévre, a célfájl felülírása a kérdés kérése nélkül.
```powershell
PS C:\> $key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\> Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Ez a parancs létrehoz egy biztonsági másolatot a $key nevű kulcsról. Nevezze el a $key nevű boltozatot. VaultName egy backup. blob nevű fájlhoz, a fájl csendes felülírásával, ha már létezik.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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
A megadott fájl felülírása ha létezik

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

### -InputObject
Fontos köteg a lekérési hívás kimenetéről való biztonsági mentéshez.

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

### -Name (név)
Annak a kulcsnak a neve, amelyről biztonsági másolatot szeretne készíteni.

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFile
Azt a kimeneti fájlt adja meg, amelyben a biztonsági másolat blobja van tárolva.
Ha nem adja meg ezt a paramétert, ez a parancsmag létrehoz egy fájlnevet.
Ha megad egy meglévő kimeneti fájl nevét, a művelet nem fejeződik be, és egy hibaüzenet jelenik meg, amely szerint már létezik a biztonságimásolat-fájl.

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
Annak a kulcsnak a neve, amely a biztonsági másolatot tartalmazó kulcsot tartalmazza.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. Command. PSKeyVaultKeyIdentityItem. models.

## KIMENETEK

### System. String

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzKeyVaultKey](./Add-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

[Restore-AzKeyVaultKey](./Restore-AzKeyVaultKey.md)

