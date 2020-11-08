---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 358d3da36996c9b020db3a805889b7098b9c36ec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184702"
---
# Get-AzRecoveryServicesBackupItem

## Áttekintés

Beolvassa az elemeket egy tárolóból a biztonsági másolatból.

## SZINTAXISA

### GetItemsForContainer (alapértelmezett)
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetItemsForVault
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetItemsForPolicy
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás

A **Get-AzRecoveryServicesBackupItem** parancsmag egy tárolóban lévő védett elemek listáját és az elemek védettségi állapotát kapja meg.
Az Azure Recovery Services-tárolók számára regisztrált tárolók tartalmazhatnak egy vagy több olyan elemet, amely védett lehet.
Azure virtuális gépek esetében a virtuálisgép-tárolóban csak egy biztonságimásolat-elem lehet.
Állítsa be a boltozat környezetét a-VaultId paraméter használatával.

## Példák

### Példa 1: elem beszerzése biztonsági tárolóból

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

Az első parancs beolvassa a AzureVM típusú dobozt, majd a $Container változóban tárolja.
A második parancs beolvassa a V2VM nevű biztonsági másolatot a $Container, majd a $BackupItem változóban tárolja.

### 2. példa: Azure-fájlmegosztás elemének beszerzése a típusú megjelenített

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureStorage -Status Registered -Name "StorageAccount1" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureFiles -VaultId $vault.ID -FriendlyName "FileShareName"
```

Az első parancs beolvassa a AzureStorage típusú dobozt, majd a $Container változóban tárolja.
A második parancs azt a biztonsági másolatot kapja, amelynek a típusú megjelenített megegyezik a típusú megjelenített paraméterben átadott értékkel, majd a $BackupItem változóban tárolja.
A típusú megjelenített paraméter használata több Azure-fájlmegosztás visszaadásához vezethet. Az ilyen esetekben a parancsmagot úgy kell végrehajtania, hogy a Name (név) paramétert átviszi a név tulajdonságra az $BackupItem eredményhalmazban.

## PARAMÉTEREK

### -BackupManagementType

A védelemmel ellátott erőforrások osztálya. A paraméter elfogadható értékei a következők:

- AzureVM
- Mohácsi
- AzureStorage
- AzureWorkload

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases:
Accepted values: AzureVM, MARS, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Container

Azt a tároló objektumot adja meg, amelyből a parancsmag biztonsági mentési elemeket kap.
**AzureRmRecoveryServicesBackupContainer** beszerzéséhez használja a **Get-AzRecoveryServicesBackupContainer** parancsmagot.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeleteState
Az elem deletestate adja meg, hogy a paraméter elfogadható értékei a következők:

- ToBeDeleted
- NotDeleted

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemDeleteState
Parameter Sets: (All)
Aliases:
Accepted values: ToBeDeleted, NotDeleted

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Típusú megjelenített
A mentett elem típusú megjelenített

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)

A biztonságimásolat-elem nevét adja meg. Fájlmegosztás esetén adja meg a védett fájlmegosztás egyedi AZONOSÍTÓját.

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

### -Házirend

Protection Policy objektum.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: GetItemsForPolicy
Aliases:

Required: True
Position: 1
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
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemProtectionState
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
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemProtectionStatus
Parameter Sets: (All)
Aliases:
Accepted values: Healthy, Unhealthy

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultId

A helyreállítási szolgáltatások boltozatának azonosítója

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

### -WorkloadType

Az erőforrás terhelési típusa. A paraméter elfogadható értékei a következők:

- AzureVM
- AzureFiles
- MSSQL

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: GetItemsForContainer, GetItemsForVault
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ContainerBase

### System. String

## KIMENETEK

### Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ItemBase

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Backup-AzRecoveryServicesBackupItem](./Backup-AzRecoveryServicesBackupItem.md)

[Disable-AzRecoveryServicesBackupProtection](./Disable-AzRecoveryServicesBackupProtection.md)

[Get-AzRecoveryServicesBackupRecoveryPoint](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[Restore-AzRecoveryServicesBackupItem](./Restore-AzRecoveryServicesBackupItem.md)
