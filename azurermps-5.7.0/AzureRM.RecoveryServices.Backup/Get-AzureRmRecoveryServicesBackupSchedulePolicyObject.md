---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: 4a3602363436c396b0706d9c195569874a35fdf3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493063"
---
# Get-AzureRmRecoveryServicesBackupSchedulePolicyObject

## Áttekintés
Beolvassa a bázis ütemezése házirend-objektumot.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureRmRecoveryServicesBackupSchedulePolicyObject** parancsmag alap **AzureRMRecoveryServicesSchedulePolicyObject** kap.
Ez az objektum nem marad fenn a rendszerben.
Az ideiglenes objektum, amelyet az New-AzureRmRecoveryServicesBackupProtectionPolicy parancsmaggal kezelhet és használhat új biztonsági mentési házirend létrehozásához.

## Példák

### Példa 1: az ütemezés gyakoriságának beállítása hetente
```
PS C:\>$RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

Az első parancs megkapja az adatmegőrzési házirend objektumot, majd a $RetPol változóban tárolja.

A második parancs bekerül az ütemezési házirend-objektumba, majd a $SchPol változóban tárolja.

A harmadik parancs az ütemezési házirend gyakoriságát hetente módosítja.

Az utolsó parancs biztonsági mentési házirendet hoz létre a frissített ütemezéssel.

### 2. példa: a biztonsági mentés időpontjának beállítása
```
PS C:\>$SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

Az első parancs megkapja az ütemezési házirend-objektumot, majd a $SchPol változóban tárolja.

A második parancs eltávolítja az összes ütemezett futási időpontot a $SchPolból.

A harmadik parancs az aktuális dátumot és időpontot kapja, majd a $DT változóban tárolja.

A negyedik parancs a jelenlegi időpontra cseréli az ütemezett futási időpontokat.
Csak egyszer lehet biztonsági másolatot készíteni a AzureVM, így a biztonsági mentés időpontjának alaphelyzetbe állításához az eredeti ütemtervet kell cserélnie.

Az utolsó parancs az új időbeosztással hozza létre a biztonsági mentési házirendet.

## PARAMÉTEREK

### -BackupManagementType
A biztonságimásolat-kezelés típusát adja meg.
A paraméter elfogadható értékei a következők:

- AzureVM 
- AzureSQLDatabase

```yaml
Type: BackupManagementType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 1
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

### -WorkloadType
A munkaterhelés típusát adja meg.
A paraméter elfogadható értékei a következők:

- AzureVM 
- AzureSQLDatabase

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 0
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

### Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. SchedulePolicyBase

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmRecoveryServicesBackupProtectionPolicy](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[Set-AzureRmRecoveryServicesBackupProtectionPolicy](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


