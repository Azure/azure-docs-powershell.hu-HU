---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautobackupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 952a9160a20492fe49e7f79019ca68e3bc241e57
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331373"
---
# New-AzVMSqlServerAutoBackupConfig

## SYNOPSIS
Konfigurációs objektumot hoz létre az SQL Server automatikus biztonsági mentéséhez.

## SZINTAXIS

### StorageUriSqlServerAutoBackup (alapértelmezett)
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### StorageContextSqlServerAutoBackup
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageContext] <IStorageContext>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **New-AzVMSqlServerAutoBackupConfig** parancsmag létrehoz egy konfigurációs objektumot az SQL Server automatikus biztonsági mentéséhez.

## PÉLDÁK

### 1. példa: Automatikus biztonságimásolat-konfiguráció létrehozása tárhely URI-jának és fiókkulcsának használatával
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

Ez a parancs a tárhely URI-jának és a fiókkulcsnak a megadásával létrehoz egy automatikus biztonságimásolat-konfigurációs objektumot.
Az automatikus biztonsági mentés engedélyezve van, az automatikus biztonsági mentések pedig 10 napig maradnak meg.
A parancs az eredményt a $AutoBackupConfig tárolja.
Ezt a konfigurációs elemet más parancsmagok, például a Set-AzVMSqlServerExtension is megadhatja.

### 2. példa: Automatikus biztonsági mentés beállítása tárterületkörnyezet használatával
```
PS C:\> $StorageContext = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

Az első parancs létrehoz egy tárterületkörnyezetet, majd a helyi $StorageContext tárolja.
További információ: New-AzStorageContext.
A második parancs egy automatikus biztonságimásolat-konfigurációs objektumot hoz létre a tárterület környezetének $StorageContext.
Az automatikus biztonsági mentés engedélyezve van, az automatikus biztonsági mentések pedig 10 napig maradnak meg.

### 3. példa: Automatikus biztonsági mentés beállítása titkosítással és jelszóval
```
PS C:\> $StorageContext = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

Ez a parancs létrehoz és tárol egy automatikus biztonságimásolat-konfigurációs objektumot.
A parancs megadja az előző példában létrehozott tárterületkörnyezetet.
A parancs jelszóval való titkosítást tesz lehetővé.
A jelszót korábban biztonságos karakterláncként tárolta a $CertificatePassword változóban.
Biztonságos karakterlánc létrehozásához használja a ConvertTo-SecureString parancsmagot.

## PARAMETERS

### -BackupScheduleType
Biztonsági mentési ütemezés típusa, kézi vagy automatizált

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
Rendszer-adatbázisok biztonsági mentése

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
Megadja a jelszót az SQL Server által titkosított biztonsági másolatok végrehajtásához használt tanúsítvány titkosításához.

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

### -Enable
Azt jelzi, hogy engedélyezve van az SQL Server virtuális gép automatikus biztonsági mentése.
Ha ezt a paramétert adja meg, az automatikus biztonsági mentés biztonsági mentési ütemezést állít be az összes aktuális és új adatbázishoz.
Ezzel frissíti a felügyelt biztonsági mentés beállításait, hogy kövessék ezt az ütemezést.

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
Azt jelzi, hogy ez a parancsmag lehetővé teszi a titkosítást.

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
Sql Server Full Backup frequency, daily or weekly

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
Az Sql Server teljes biztonsági mentésének indítási napja (0–23)

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
Sql Server Full Backup window in hours

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
Sql Server-napló biztonsági mentési gyakorisága, 1–60 percenként egyszer

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
A virtuális gép erőforráscsoportját adja meg.

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
Azt adja meg, hogy hány napig őrizze meg a biztonsági másolatokat.

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
Azt a tárfiókot adja meg, amely a biztonsági másolatok tárolására fog használni.
**AzureStorageContext-objektum** beszerzéséhez használja a New-AzStorageContext parancsmagot.
Az alapértelmezett érték az SQL Server virtuális géphez társított tárfiók.

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
A blobtároló-fiók tárkulcsát határozza meg.

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
A blobtároló fiók egységes erőforrás-azonosítóját (URI) adja meg.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### System.Management.Automation.SwitchParameter

### System.Int32

### Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext

### System.Uri

### System.Security.SecureString

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## KIMENETEK

### Microsoft.Azure.Commands.Compute.AutoBackupSettings

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[New-AzVMSqlServerAutoPatchingConfig](./New-AzVMSqlServerAutoPatchingConfig.md)

[Set-AzVMSqlServerExtension](./Set-AzVMSqlServerExtension.md)


