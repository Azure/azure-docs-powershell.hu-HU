---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverautobackupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: da85c91aea3c47c2b3ba0e9ff19938980dbc80d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502207"
---
# New-AzureRmVMSqlServerAutoBackupConfig

## Áttekintés
Konfigurációs objektum létrehozása az SQL Server automatikus biztonsági mentéséhez.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### StorageUriSqlServerAutoBackup (alapértelmezett)
```
New-AzureRmVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### StorageContextSqlServerAutoBackup
```
New-AzureRmVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageContext] <IStorageContext>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs]
 [-BackupScheduleType <String>] [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>]
 [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **New-AzureRmVMSqlServerAutoBackupConfig** parancsmag létrehoz egy konfigurációs OBJEKTUMOT az SQL Server automatikus biztonsági mentéséhez.

## Példák

### Példa 1: automatikus biztonsági másolat létrehozása a tárolási URI és a fiók kulccsal
```
PS C:\> $AutoBackupConfig = New-AzureRmVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

A parancs a tárterület-azonosító és a fiók kulcs megadásával automatikusan biztonsági másolatot készít a konfigurációs objektumról.
Az automatikus biztonsági mentés be van kapcsolva, és az automatikus biztonsági mentés 10 napig tart.
A parancs az eredményt a $AutoBackupConfig változóban tárolja.
Ezt a konfigurációs elemet más parancsmagok, például az Set-AzureRmVMSqlServerExtension parancsmag esetében is megadhatja.

### 2. példa: automatikus biztonságimásolat-konfiguráció létrehozása tárolási környezet használatával
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzureRmVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

Az első parancs létrehozza a tárolási környezetet, majd a $StorageContext változóban tárolja.
További információt az új AzureStorageContext című témakörben talál.
A második parancs az $StorageContext tárolási környezetének megadásával automatikusan biztonsági másolatot készít a konfigurációs objektumról.
Az automatikus biztonsági mentés be van kapcsolva, és az automatikus biztonsági mentés 10 napig tart.

### 3. példa: automatikus biztonsági másolat beállítása a tárolási környezettel a titkosítással és a jelszóval
```
PS C:\> $StorageContext = New-AzureRmVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

Ezzel a paranccsal létrehozhatja és tárolhatja az automatikus biztonságimásolat-konfiguráció objektumát.
A parancs az előző példában létrehozott tárterület-környezetet adja meg.
A parancs engedélyezi a titkosítást a jelszóval.
A jelszó korábban biztonságos karakterláncként volt tárolva a $CertificatePassword változóban.
Ha biztonságos karakterláncot szeretne létrehozni, használja az ConvertTo-SecureString parancsmagot.

## PARAMÉTEREK

### -BackupScheduleType
Biztonságimásolat-ütemezés típusa, kézi vagy automatizált

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Manual, Automated

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BackupSystemDbs
Biztonsági másolat rendszeradatbázisai

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CertificatePassword
Megadja azt a jelszót, amellyel titkosítható az SQL Server titkosított biztonsági mentéseit szolgáló tanúsítvány.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
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

### – Engedélyezés
Azt jelzi, hogy az SQL Server virtuális gép automatikus biztonsági másolata engedélyezve van.
Ha ezt a paramétert adja meg, akkor az automatikus biztonsági mentés az összes aktuális és új adatbázis biztonsági ütemezését állítja be.
Ezzel frissíti a felügyelt biztonságimásolat-beállításokat az ütemezés követéséhez.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnableEncryption
Azt jelzi, hogy ez a parancsmag engedélyezi a titkosítást.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FullBackupFrequency
SQL Server – teljes biztonsági mentés gyakorisága, naponta vagy hetente

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Weekly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FullBackupStartHour
A nap órája (0-23), amikor az SQL Server teljes biztonsági másolatát meg kell kezdeni

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FullBackupWindowInHours
Az SQL Server teljes biztonsági másolat ablaka órában

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LogBackupFrequencyInMinutes
SQL Server log Backup gyakorisága, 1-60 percenként

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
A virtuális gép erőforráscsoport-csoportjának nevét adja meg.

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

### -RetentionPeriodInDays
Azt adja meg, hogy hány napig maradjon a biztonsági másolat.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageContext
Azt a tárterületet adja meg, amelyet a biztonsági másolatok tárolására fog használni.
**AzureStorageContext** objektum beolvasásához használja az New-AzureStorageContext parancsmagot.
Az alapértelmezett érték az SQL Server virtuális géphez társított tárolási fiók.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageKey
A blob-tároló fiók tárolási kulcsát adja meg.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageUri
A blob-tároló fiók egységes erőforrás-azonosítóját adja meg.

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### System. Management. Automation. SwitchParameter

### System. Int32

### Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext

### System. URI

### System. Security. SecureString

### System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]

## KIMENETEK

### Microsoft. Azure. commands. kiszámítás. AutoBackupSettings

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureVMSqlServerAutoPatchingConfig](./New-AzureVMSqlServerAutoPatchingConfig.md)

[Set-AzureRmVMSqlServerExtension](./Set-AzureRMVMSqlServerExtension.md)


