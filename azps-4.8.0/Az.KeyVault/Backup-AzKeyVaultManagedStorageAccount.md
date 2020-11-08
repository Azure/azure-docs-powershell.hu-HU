---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c01d07f9408804b229921394c24e444b2a4deb8b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025308"
---
# Backup-AzKeyVaultManagedStorageAccount

## Áttekintés
Biztonsági másolatot készíthet egy parancssori tárolási fiókról.

## SZINTAXISA

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

## Leírás
A **biztonsági másolat-AzKeyVaultManagedStorageAccount** parancsmag egy megadott felügyelt tárterületet készít a kulcsfájl letöltésével és egy fájlban való tárolásával.
Mivel a letöltött tartalom titkosítva van, nem használható az Azure Key Vault-on kívül.
Visszaállíthat egy biztonsági mentett tárterületet az előfizetésben szereplő bármelyik kulcsos fiókba, amelyből biztonsági másolat készül, amíg a boltozat ugyanahhoz az Azure-földrajzhoz tartozik.
A parancsmag használatának tipikus okai a következők: 
- Szeretné megőrizni a tárolási fiók kapcsolat nélküli másolatát, ha véletlenül törli az eredetit a boltozatról.
 
- A tagkártya segítségével létrehozott egy felügyelt tárterületet, és most szeretné az objektumot egy másik Azure-területre beilleszteni, így a kiosztott alkalmazás minden példányában használhatja azt.
Használja a **Backup-AzKeyVaultManagedStorageAccount** parancsmagot a felügyelt tárterület titkosított formátumban való visszakereséséhez, majd használja a **Restore-AzKeyVaultManagedStorageAccount** parancsmagot, és adjon meg egy kulcspárt a második régióban.

## Példák

### 1. példa: felügyelt tárterületű fiók biztonsági mentése automatikusan generált fájlnévvel
```powershell
PS C:\Users\username\> Backup-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

Ez a parancs beolvassa a MyMSAK nevű felügyelt tárterületet a MyKeyVault nevű kulcs-tárolóból, és menti a távtárolású tárterület biztonsági másolatát egy automatikusan megnevezett fájlba, és megjeleníti a fájl nevét.

### 2. példa: felügyelt tárterület-fiók biztonsági mentése egy megadott fájlnévre
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Ez a parancs beolvassa a MyMSAK nevű felügyelt tárterületet a MyKeyVault nevű kulcskezelő-fiókból, és biztonsági másolatot ment a felügyelt tárterület-fiókról egy backup. blob nevű fájlra.

### 3. példa: biztonsági másolat készítése korábban lekérdezett felügyelt tárterületről egy megadott fájlnévre, a célfájl felülírása a kérdés kérése nélkül.
```powershell
PS C:\> $msak = Get-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Ez a parancs létrehoz egy biztonsági másolatot a $msak nevű felügyelt tárterület-fiókról. Nevezze el a $msak nevű boltozatot. VaultName egy backup. blob nevű fájlhoz, a fájl csendes felülírásával, ha már létezik.

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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
A raktározási fiók kötegének biztonsági mentése a lekérési hívás kimenetéről.

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

### -Name (név)
Titkos név.
A parancsmag a boltozat nevéből, az aktuálisan kijelölt környezetből és a titkos névvel elkészíti a titkos FQDN-t.

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
A kimeneti fájl a tárterület biztonsági másolatának tárolásához.
Ha nincs megadva, a program egy alapértelmezett fájlnevet hoz létre.

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
Boltozat neve.
A parancsmag a pince teljes tartománynevét a név és a jelenleg kijelölt környezet alapján építi fel.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### Microsoft. Azure. Command. PSKeyVaultManagedStorageAccountIdentityItem. models.

## KIMENETEK

### System. String

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
