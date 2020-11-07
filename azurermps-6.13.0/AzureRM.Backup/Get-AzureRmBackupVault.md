---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 95FF3F7A-5CC6-4AA6-A393-5EBB5579D9A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
ms.openlocfilehash: c11170e6bee80b9eaa19135ad604d8bf70e1baab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679185"
---
# Get-AzureRmBackupVault

## Áttekintés
Biztonsági mentési boltozatokat kap.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmBackupVault [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmBackupVault** parancsmag Azure Backup-boltozatokat kap.
Ez a parancsmag a más parancsmagokkal használható **AzureRmBackupVault** -objektumokat számítja ki.

## Példák

### Példa 1: az összes biztonságimásolat-boltozat megtekintése
```
PS C:\>Get-AzureRmBackupVault
```

Ez a parancs minden Azure biztonságimásolat-tárolót kap.

### 2. példa: a West US-ban létrehozott összes boltozat megtekintése
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Region -eq "westus" }
```

Ez a parancs a biztonságimásolat-tárolókat kapja meg.
A parancs a csővezeték-kezelő segítségével átadja őket a Where-Object parancsmagnak.
Az adott parancsmag a **régió** tulajdonság alapján szűri az eredményeket.
További információért írja be a következőt: `Get-Help Where-Object` .

### 3. példa: speciális boltozat beszerzése
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup011/providers/Microsoft.Backup
                    /BackupVault/Vault
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

Ez a parancs a Vault03 nevű boltozatot kapja.

### Példa 4: a helyileg redundáns tárterületet tartalmazó boltozatok számának megszámolása
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Storage -match "LocallyRedundant" } | Measure-Object
Count    : 4
Average  : 
Sum      : 
Maximum  : 
Minimum  : 
Property :
```

Ez a parancs minden Azure biztonságimásolat-tárolót kap.
A parancs átadja azokat a **Where-Object** értékre, amely a **tárolási** tulajdonság alapján szűri az eredményeket.
A parancs átadja azokat az értékeket, amelyek LocallyRedundant a Measure-Object parancsmagnak, amely megszámolja a találatokat.
További információért írja be a következőt: `Get-Help Measure-Object` .

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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

### -Name (név)
Itt adhatja meg annak a biztonságimásolat-tárolónak a nevét, amely a parancsmagot kapja.
Ha egynél több biztonságimásolat-tárolóval rendelkezik, akkor ez a parancsmag mindet visszaadja.
Adja meg a *ResourceGroupName* paramétert egy egyedi boltozat beszerzéséhez.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az Azure-erőforrásnak a nevét adja meg, amelyben ez a parancsmag biztonsági mentési boltozatot kap.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. Command. AzureBackup. models. AzureRMBackupVault

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[Új – AzureRmBackupVault](./New-AzureRmBackupVault.md)

[Remove-AzureRmBackupVault](./Remove-AzureRmBackupVault.md)

[Set-AzureRmBackupVault](./Set-AzureRmBackupVault.md)


