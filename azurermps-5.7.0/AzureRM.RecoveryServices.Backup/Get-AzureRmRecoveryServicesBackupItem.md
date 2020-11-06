---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: 9b836a4c4c056699e2c74bcb4d5b373f5bfe170e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493077"
---
# Get-AzureRmRecoveryServicesBackupItem

## Áttekintés
Beolvassa az elemeket egy tárolóból a biztonsági másolatból.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### GetItemsForContainer (alapértelmezett)
```
Get-AzureRmRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetItemsForVault
```
Get-AzureRmRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmRecoveryServicesBackupItem** parancsmag a tárolóban lévő elemeket, illetve az Azure biztonsági másolatban szereplő elemeket, valamint az elemek védelmi állapotát kapja meg.

Az Azure Recovery Services-tárolók számára regisztrált tárolók tartalmazhatnak egy vagy több olyan elemet, amely védett lehet.
Azure virtuális gépek esetében a virtuálisgép-tárolóban csak egy biztonságimásolat-elem lehet.

Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.

## Példák

### Példa 1: elem beszerzése biztonsági tárolóból
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM
```

Az első parancs beolvassa a AzureVM típusú dobozt, majd a $Container változóban tárolja.

A második parancs beolvassa a V2VM nevű biztonsági másolatot a $Container, majd a $BackupItem változóban tárolja.

## PARAMÉTEREK

### -BackupManagementType
A biztonságimásolat-kezelés típusát adja meg.
A paraméter elfogadható értékei a következők:

- AzureVM 
- MARS 
- SCDPM 
- AzureBackupServer AzureSQL

```yaml
Type: BackupManagementType
Parameter Sets: GetItemsForVault
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Container
Azt a tároló objektumot adja meg, amelyből a parancsmag biztonsági mentési elemeket kap.
Ha **AzureRmRecoveryServicesBackupContainer** szeretne beolvasni, használja az Get-AzureRmRecoveryServicesBackupContainer parancsmagot.

```yaml
Type: ContainerBase
Parameter Sets: GetItemsForContainer
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Name (név)
A tároló nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectionState
A védelmi államot adja meg.
A paraméter elfogadható értékei a következők:

- IRPending.
A kezdeti szinkronizálás még nem kezdődött el, és még nincs helyreállítási pont. 
- Védett.
A védelem folyamatban van. 
- ProtectionError.
Van egy védelmi hiba.
- ProtectionStopped.
A védelem le van tiltva.

```yaml
Type: ItemProtectionState
Parameter Sets: (All)
Aliases: 
Accepted values: IRPending, ProtectionError, Protected, ProtectionStopped

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectionStatus
A tároló elemeinek általános védelmi állapotát adja meg.
A paraméter elfogadható értékei a következők:

- Egészséges
- Egészségtelen

```yaml
Type: ItemProtectionStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Healthy, Unhealthy

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkloadType
A munkaterhelés típusát adja meg. A paraméter elfogadható értékei a következők:

- AzureVM 
- AzureSQLDatabase

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 5
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

### Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ItemBase

### System. Collections. Generic. IList ' 1 [Microsoft. Azure. commands. RecoveryServices. backup. Parancsmags. models. ItemBase]

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Backup-AzureRmRecoveryServicesBackupItem](./Backup-AzureRmRecoveryServicesBackupItem.md)

[Disable-AzureRmRecoveryServicesBackupProtection](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[Get-AzureRmRecoveryServicesBackupRecoveryPoint](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)

[Restore-AzureRmRecoveryServicesBackupItem](./Restore-AzureRmRecoveryServicesBackupItem.md)


