---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: bb1c63b41d27f92991a3504cdd5c2fd8fe547298
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921641"
---
# Get-AzRecoveryServicesBackupRetentionPolicyObject

## SYNOPSIS
Alap adatmegőrzési házirend-objektumot kap.

## SZINTAXIS

```
Get-AzRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzRecoveryServicesBackupRetentionPolicyObject** parancsmag egy alap **AzureRMRecoveryServicesRetentionPolicyObject** parancsmagot kap.
Ez az objektum nem marad meg a rendszerben.
Ez egy ideiglenes objektum, amely a New-AzRecoveryServicesBackupProtectionPolicy segítségével új biztonságimásolat-házirendet hozhat létre.

## PÉLDÁK

### 1. példa: Biztonságimásolat-védelmi házirend létrehozása
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

Az első parancs megkapja az adatmegőrzési házirend-objektumot, majd a $RetPol tárolja.
A második parancs 365 napra állítja az adatmegőrzési házirend-objektum időtartamát.
A harmadik parancs megkapja az ütemezési házirendobjektumot, majd a $SchPol tárolja.
Az utolsó parancs egy biztonságimásolat-védelmi házirendet hoz létre az adatmegőrzési házirend és az előző parancsokkal létrehozott ütemezési házirend használatával.

## PARAMETERS

### -BackupManagementType
A védett erőforrások osztálya. A paraméter elfogadható értékei a következőek:
- AzureVM 
- AzureWorkload
- AzureStorage

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

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzRecoveryServicesBackupSchedulePolicyObject](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[New-AzRecoveryServicesBackupProtectionPolicy](./New-AzRecoveryServicesBackupProtectionPolicy.md)


