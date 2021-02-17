---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 5dab5eaca48152dc573caf75f5d80737802bfcdf
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399821"
---
# Get-AzRecoveryServicesBackupJob

## SYNOPSIS
Biztonsági mentési feladatokat kap.

## SZINTAXIS

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzRecoveryServicesBackupServicesBackupService** parancsmag azure biztonsági mentési feladatokat kap egy adott tárolóhoz.
Az aktuális parancsmag használata előtt állítsa be a tároló környezetét a Set-AzRecoveryServicesVaultContext parancsmag használatával.

## PÉLDÁK

### 1. példa: Az összes folyamatban lévő feladat lekérte
```
PS C:\>$Joblist = Get-AzRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

Az első parancs egy folyamatban lévő feladat állapotát tömbként kapja meg, majd a folyamatban lévő $Joblist tárolja.
A második parancs a tömb első elemét $Joblist jeleníti meg.

### 2. példa: Az összes sikertelen feladat be szerezze az elmúlt 7 napban
```
PS C:\>Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

Ez a parancs sikertelen feladatokat kap a tároló utolsó hetében.
A *From* paraméter az UTC-ben megadott múltbeli hét napot ad meg.
A parancs nem ad meg értéket a *To paraméternek.*
Ezért az aktuális idő alapértelmezett értékét használja.

### 3. példa: Folyamatban lévő feladat elvégzése és várakozás a befejezésre
```
PS C:\> 
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress
$Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $job = Get-AzBackAzureRmRecoveryServicesBackupJob  -Job $Job
    }
    Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

Ez a parancsprogram lekérdezi az első folyamatban lévő feladatot, amíg a feladat be nem fejeződik.

## PARAMETERS

### -BackupManagementType
A biztonsági mentés kezelési típusát adja meg.
Jelenleg csak az AzureVM, az AzureStorage támogatott.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: Named
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

### -From
A parancsmag által begyakorolt feladatok időtartományának **kezdését adja** meg DateTime-objektumként.
**DateTime-objektum** beszerzéséhez használja a Get-Date parancsmagot.
A DateTime-objektumokról a **következőt** írja be: `Get-Help Get-Date` .
Dátumokhoz használja az UTC formátumot.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
A lekért biztonsági másolati feladat nevét adja meg.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId
A parancsmag által lekért feladat azonosítója.
Az azonosító egy **AzureRmRecoveryServicesBackupServicesBackupService objektum InstanceId tulajdonsága.**
**AzureRmRecoveryServicesBackupServices Object** beszerzéséhez használja a Get-AzRecoveryServicesBackupService-t.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Operation
A parancsmag által lekért feladatok műveletét adja meg.
A paraméter elfogadható értékei a következőek:
- Biztonsági másolat
- ConfigureBackup
- DeleteBackupData
- Regisztráció
- Visszaállítás
- Védelem feloldása
- Regisztrációt nem lehet

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobOperation]
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
Megadja a parancsmag által begyabatolt feladatok állapotát.
A paraméter elfogadható értékei a következőek:
- InProgress
- Sikertelen
- Megszakítva
- Lemondás
- Befejezve
- CompletedWithWarnings

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobStatus]
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
A parancsmag által lekért feladatok időtartományának **DateTime-objektumként** való végét adja meg.
Az alapértelmezett érték a rendszer aktuális ideje.
Ha ezt a paramétert adja meg, a From paramétert *is meg kell adnia.*
Dátumokhoz használja az UTC formátumot.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultId
ARM helyreállítási szolgáltatások tárolójának azonosítója.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK


[Stop-AzRecoveryServicesBackupService](./Stop-AzRecoveryServicesBackupJob.md)

[Wait-AzRecoveryServicesBackupService](./Wait-AzRecoveryServicesBackupJob.md)


