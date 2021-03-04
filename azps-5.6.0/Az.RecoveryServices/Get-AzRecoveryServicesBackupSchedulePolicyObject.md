---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: 5bf91aafffb1c6fd650b5fd88f343897afc6c5d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932330"
---
# Get-AzRecoveryServicesBackupSchedulePolicyObject

## SYNOPSIS
Alapütemterv-házirendobjektumot kap.

## SZINTAXIS

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzRecoveryServicesBackupSchedulePolicyObject** parancsmag egy alap **AzureRMRecoveryServicesSchedulePolicyObject** parancsmagot kap.
Ez az objektum nem marad meg a rendszerben.
Ez egy ideiglenes objektum, amely a New-AzRecoveryServicesBackupProtectionPolicy parancsmaggal egy új biztonságimásolat-védelmi házirend létrehozásához használható.

## PÉLDÁK

### 1. példa: Az ütemezés gyakoriságának beállítása hetente
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

Az első parancs megkapja az adatmegőrzési házirend-objektumot, majd a $RetPol tárolja.
A második parancs beveszi az ütemezési házirendobjektumot, majd a $SchPol tárolja.
A harmadik parancs heti rendszerességgel módosítja az ütemezési házirend gyakoriságát.
Az utolsó parancs létrehoz egy biztonságimásolat-védelmi házirendet a frissített ütemezéssel.

### 2. példa: A biztonsági mentés időének beállítása
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

Az első parancs megkapja az ütemezési házirendobjektumot, majd a $SchPol tárolja.
A második parancs minden ütemezett futási időt eltávolít a $SchPol.
A harmadik parancs bekérte az aktuális dátumot és időpontot, majd tárolja azt a $DT változóban.
A negyedik parancs az ütemezett futtatás idejét az aktuális időpontra cseréli.
Naponta csak egyszer lehet biztonsági másolatot készíteni az AzureVM-ről, így a biztonsági mentés alaphelyzetbe állításának idejét az eredeti ütemezést kell lecserélnie.
Az utolsó parancs egy biztonságimásolat-védelmi házirendet hoz létre az új ütemezés használatával.

## PARAMETERS

### -BackupManagementType
A védett erőforrások osztálya. A paraméter elfogadható értékei a következőek:
- AzureVM 
- AzureStorage
- AzureWorkload

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload

Required: False
Position: 1
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

### -WorkloadType
Az erőforrás terheléstípusa. A paraméter elfogadható értékei a következőek:
- AzureVM 
- AzureFiles
- MSSQL


```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[New-AzRecoveryServicesBackupProtectionPolicy](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[Set-AzRecoveryServicesBackupProtectionPolicy](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


