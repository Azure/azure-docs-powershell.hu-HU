---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c01d07f9408804b229921394c24e444b2a4deb8b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203824"
---
# Backup-AzKeyVaultManagedStorageAccount

## SYNOPSIS
A KeyVault által felügyelt tárfiók biztonsági biztonsági létrehozása.

## SZINTAXIS

### ByStorageAccountName (alapértelmezett)
```
Backup-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByStorageAccount
```
Backup-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## LEÍRÁS
A **Backup-AzKeyVaultManagedStorageAccount** parancsmag egy adott felügyelt tárfiókról biztonsági másolatot készít egy kulcstárolóban úgy, hogy letölti és egy fájlban tárolja azt.
Mivel a letöltött tartalom titkosítva van, nem használható az Azure-kulcstáron kívül.
Visszaállíthat egy biztonsági másolattal tárolt tárfiókot az előfizetés bármely kulcstárába, amelyről biztonsági másolat lett, felhasználhatja, ha a tároló ugyanabban az Azure geographyban van.
A parancsmag használatának tipikus okai: 
- Meg szeretné őrizni a tárfiók offline példányát arra az esetre, ha véletlenül törli az eredetit a tárolóból.
 
- A kulcstár használatával létrehozott egy felügyelt tárfiókot, és most egy másik Azure-régióba szeretné klónozni az objektumot, hogy az elosztott alkalmazás összes példányából használva tudja használni.
Az **AzKeyVaultManagedStorageAccount** parancsmaggal titkosított formátumban olvassa be a felügyelt tárfiókot, majd használja a **Restore-AzKeyVaultManagedStorageAccount** parancsmagot, és adjon meg egy kulcstárat a második régióban.

## PÉLDÁK

### 1. példa: Felügyelt tárfiók biztonsági mentése automatikusan létrehozott fájlnévvel
```powershell
PS C:\Users\username\> Backup-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

Ez a parancs beolvassa a MyMSAK nevű felügyelt tárfiókot a MyKeyVault nevű kulcstárból, és egy automatikusan elnevezett fájlba menti a felügyelt tárfiók biztonsági másolatát, és megjeleníti a fájl nevét.

### 2. példa: Felügyelt tárfiók biztonsági mentése egy megadott fájlnévre
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Ez a parancs beolvassa a MyMSAK nevű felügyelt tárfiókot a MyKeyVault nevű kulcstárból, és biztonsági másolatot készít a felügyelt tárfiókról egy Backup.blob nevű fájlba.

### 3. példa: Korábban lekért felügyelt tárfiók biztonsági mentése egy megadott fájlnévre, a célfájl felülírása kérés nélkül.
```powershell
PS C:\> $msak = Get-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Ez a parancs biztonsági másolatot készít a $msak. Név a tárolóban $msak. A VaultName paramétert a Backup.blob nevű fájlhoz írja, és ha már létezik, csendesen felülírja a fájlt.

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
Tárfiók kötege biztonsági ként való biztonsági híváshoz, amely a beolvasási hívás kimeneteként lesz befutva.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByStorageAccount
Aliases: StorageAccount

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
Parameter Sets: ByStorageAccountName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFile
Kimeneti fájl.
A tárfiók biztonsági mentését tároló kimeneti fájl.
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
Parameter Sets: ByStorageAccountName
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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem

## KIMENETEK

### System.String

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
