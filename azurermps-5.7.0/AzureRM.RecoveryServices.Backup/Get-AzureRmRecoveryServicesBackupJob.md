---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 5e6555095563fd5c0589835b28ad293f395fffaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493078"
---
# Get-AzureRmRecoveryServicesBackupJob

## Áttekintés
Biztonsági mentési feladatokat kap.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmRecoveryServicesBackupJob** parancsmag Azure biztonságimásolat-készítési feladatokat kap egy adott boltozathoz.

Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.

## Példák

### Példa 1: minden folyamatban lévő feladat beolvasása
```
PS C:\>$Joblist = Get-AzureRMRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

Az első parancs a folyamatban lévő munka állapotát tömbként kapja, majd a $Joblist változóban tárolja.

A második parancs a $Joblist tömb első elemét jeleníti meg.

### 2. példa: az összes sikertelen feladat beolvasása az elmúlt 7 napban
```
PS C:\>Get-AzureRmRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

Ez a parancs a boltozat utolsó hetében sikertelen feladatokat kap.
A *from* paraméter egy, az UTC által megadott időpontban hét napot ad meg.
A parancs nem adja meg *a paraméter értékét* .
Ennek megfelelően az aktuális idő alapértelmezett értékét használja.

### 3. példa: folyamatban lévő munka beszerzése és várakozás a befejezésre
```
PS C:\> 
$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status InProgress
$Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $job = Get-AzureRmBackAzureRmRecoveryServicesBackupJob  -Job $Job
    }
    Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

Ez a parancsfájl az első olyan feladatot kérdezi le, amely jelenleg folyamatban van addig, amíg a projekt be nem fejeződik.

## PARAMÉTEREK

### -BackupManagementType
A biztonságimásolat-kezelés típusát adja meg.
Jelenleg csak a AzureVM támogatott.

```yaml
Type: BackupManagementType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -From
A parancsmag által beolvasott feladatok időtartományának kezdetét **datetime** -objektumként adja meg.
Ha **datetime** típusú objektumot szeretne beolvasni, használja az Get-Date parancsmagot.
A **datetime** -objektumokkal kapcsolatos további tudnivalókért írja be a következőt: `Get-Help Get-Date` .
A dátumok esetében az UTC formátumot használhatja.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
A beolvasott biztonságimásolat-feladat nevét adja meg.

```yaml
Type: JobBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId
Annak a projektnek az AZONOSÍTÓját adja meg, amely a parancsmagot kapja.
Az azonosító egy **AzureRmRecoveryServicesBackupJob** objektum InstanceId tulajdonsága.
**AzureRmRecoveryServicesBackupJob** -objektum beszerzéséhez használja a Get-AzureRmRecoveryServicesBackupJob.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Művelet
A parancsmag által kapott feladatok működését adja meg.
A paraméter elfogadható értékei a következők:

- Hát
- ConfigureBackup
- DeleteBackupData
- Regisztráció
- Visszaállítása
- Védtelen
- Regisztrációját

```yaml
Type: JobOperation
Parameter Sets: (All)
Aliases: 
Accepted values: Backup, Restore, ConfigureBackup, DisableBackup, DeleteBackupData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Állapot
A parancsmag által kapott feladatok állapotát adja meg.
A paraméter elfogadható értékei a következők:

- Előrehaladás
- Sikertelen
- Lemondott
- Értekezletének lemondása
- Kész
- CompletedWithWarnings

```yaml
Type: JobStatus
Parameter Sets: (All)
Aliases: 
Accepted values: InProgress, Cancelling, Cancelled, Completed, CompletedWithWarnings, Failed

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -To
Annak a projektnek az időtartományának a végét adja meg **datetime** -objektumként, amely a parancsmagot kapja.
Az alapértelmezett érték az aktuális rendszer idő.
Ha ezt a paramétert adja meg, a *from* paramétert is meg kell adnia.
A dátumok esetében az UTC formátumot használhatja.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase

### System. Collections. Generic. IList ' 1 [Microsoft. Azure. commands. RecoveryServices. backup. Parancsmags. models. JobBase]

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmRecoveryServicesBackupJobDetails](./Get-AzureRmRecoveryServicesBackupJobDetails.md)

[Stop-AzureRmRecoveryServicesBackupJob](./Stop-AzureRmRecoveryServicesBackupJob.md)

[Várjon-AzureRmRecoveryServicesBackupJob](./Wait-AzureRmRecoveryServicesBackupJob.md)


