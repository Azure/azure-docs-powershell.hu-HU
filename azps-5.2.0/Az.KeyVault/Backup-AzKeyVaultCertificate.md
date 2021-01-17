---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
ms.openlocfilehash: 51d322ea738a56e4b1fa24cccdb7bb59a6cd0d21
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351149"
---
# Backup-AzKeyVaultCertificate

## SYNOPSIS
Egy kulcstárolóban tárolt tanúsítvány biztonsági biztonsági ának biztonságira van berekedve.

## SZINTAXIS

### ByCertificateName (alapértelmezett)
```
Backup-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCertificate
```
Backup-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **Backup-AzKeyVaultCertificate** parancsmag egy adott tanúsítványról biztonsági másolatot készít egy kulcstárolóban letöltésével és egy fájlban való tárolásával.
Ha a tanúsítványnak több verziója van, annak összes verziója szerepelni fog a biztonsági másolatban.
Mivel a letöltött tartalom titkosítva van, nem használható az Azure-kulcstáron kívül.
Visszaállíthatja a biztonsági másolatként tárolt tanúsítványt az előfizetés bármely kulcstárába, amelyről biztonsági másolat lett, ha a tároló ugyanabban az Azure geographyban van.
A parancsmag használatának tipikus okai: 
- Meg szeretné őrizni a tanúsítvány offline másolatát arra az esetre, ha véletlenül törli az eredetit a tárolóból.
 
- A kulcstárolóval létrehozott egy tanúsítványt, és most egy másik Azure-régióba szeretné klónozni az objektumot, hogy az elosztott alkalmazás összes példányából használva használható.
A **Backup-AzKeyVaultCertificate** parancsmagot használva titkosított formátumban olvassa be a tanúsítványt, majd használja a **Restore-AzKeyVaultCertificate** parancsmagot, és adjon meg egy kulcstárolót a második régióban.

## PÉLDÁK

### 1. példa: Tanúsítvány biztonsági mentése automatikusan létrehozott fájlnévvel
```powershell
PS C:\Users\username\> Backup-AzKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

Ez a parancs beolvassa a MyCert nevű tanúsítványt a MyKeyVault nevű kulcstárolóból, és egy automatikusan elnevezett fájlba menti a tanúsítvány biztonsági másolatát, és megjeleníti a fájl nevét.

### 2. példa: Tanúsítvány biztonsági mentése egy megadott fájlnévre
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Ez a parancs beolvassa a MyCert nevű tanúsítványt a MyKeyVault nevű kulcstárolóból, és biztonsági másolatot készít a tanúsítványról egy Backup.blob nevű fájlba.

### 3. példa: Korábban lekért tanúsítvány biztonsági mentése egy megadott fájlnévre, a célfájl felülírása kérés nélkül.
```powershell
PS C:\> $cert = Get-AzKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Ezzel a paranccsal biztonsági másolatot készít a $cert. Név a tárolóban $cert. A Backup.blob nevű fájl VaultName fájlja, amely csendesen felülírja a fájlt, ha már létezik.

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

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

### -InputObject
Titkos adat, amelyről biztonsági hívást kell biztonságivinni, és a beolvasási hívás kimeneteként kell bevinni.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByCertificate
Aliases: Certificate

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Titkos név.
A parancsmag a tárolónévből ( jelenleg kijelölt környezetből és titkos névből ) egy titkos kulcs teljes tartománynevét építi fel.

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFile
Kimeneti fájl.
A tanúsítvány biztonsági másolatát tároló kimeneti fájl.
Ha nincs megadva, a rendszer létrehoz egy alapértelmezett fájlnevet.

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
Tároló neve.
A parancsmag a név és a jelenleg kijelölt környezet alapján építi fel egy tároló teljes tartománynevét.

```yaml
Type: System.String
Parameter Sets: ByCertificateName
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

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem

## KIMENETEK

### System.String

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
