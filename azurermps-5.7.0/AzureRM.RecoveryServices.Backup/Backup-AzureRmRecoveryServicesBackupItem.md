---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/backup-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: a7451855f62a9e0eab63936107d8431342badfb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502511"
---
# Backup-AzureRmRecoveryServicesBackupItem

## Áttekintés
Biztonságimásolat-elem biztonsági másolatának indítása

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Backup-AzureRmRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **Backup-AzureRmRecoveryServicesBackupItem** parancsmag egy olyan védett Azure biztonsági másolat biztonsági másolatát indítja el, amely nincs a biztonsági ütemtervhez kötve.
A kezdeti biztonsági mentés után azonnal elvégezheti a biztonsági mentést, ha az ütemezett biztonsági mentés után nem tud biztonsági másolatot indítani.

Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.

## Példák

### 1. példa: biztonsági másolat készítése biztonsági elemről
```
PS C:\> $NamedContainer = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "pstestv2vm1" 
PS C:\> $Item = Get-AzureRmRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM 
PS C:\> $Job = Backup-AzureRmRecoveryServicesItem -Item $Item
Operation        Status               StartTime            EndTime                   JOBID                           
------------     ---------            ------               ---------                 -------                                         
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

Az első parancs a AzureVM nevű pstestv2vm1 nevű tartalék tárolót kapja, majd a $NamedContainer változóban tárolja.

A második parancs a $NamedContainer tárolóhoz tartozó biztonsági másolatot kapja, majd a $Item változóban tárolja.

Az utolsó parancs elindítja a biztonsági mentési feladatot a $Itemban.

## PARAMÉTEREK

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

### -ExpiryDateTimeUTC
A lejárat időpontját **datetime** -objektumként adja meg.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Elem
Annak a biztonságimásolat-elemnek a megadása, amelyhez ez a parancsmag elindítja a biztonsági mentési műveletet.

```yaml
Type: ItemBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut. A parancsmag nem fut.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### DateTime
A ' ExpiryDateTimeUTC ' paraméter a pipeline "DateTime" típusú értékét fogadja el.

### ItemBase
A "tétel" paraméter értéke az "ItemBase" típusú értéket fogadja el a csővezetékről

## KIMENETEK

### Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmRecoveryServicesBackupContainer](./Get-AzureRmRecoveryServicesBackupContainer.md)

[Get-AzureRmRecoveryServicesBackupItem](./Get-AzureRmRecoveryServicesBackupItem.md)

[Restore-AzureRmRecoveryServicesBackupItem](./Restore-AzureRmRecoveryServicesBackupItem.md)


