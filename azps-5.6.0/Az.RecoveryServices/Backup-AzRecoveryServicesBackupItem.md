---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/backup-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 3ce18989f737a28cc0949027cb4ea827116b89a1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924537"
---
# Backup-AzRecoveryServicesBackupItem

## SYNOPSIS

Biztonsági másolat készítése biztonsági másolat készítése.

## SZINTAXIS

```
Backup-AzRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-BackupType <BackupType>]
 [-EnableCompression] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## LEÍRÁS

A **Backup-AzRecoveryServicesBackupItem** parancsmag biztonsági másolatot készít a védett Azure biztonsági másolatról. A parancsmag használatával a védelem engedélyezése után azonnal biztonsági másolatot is készíthet, illetve biztonsági másolatot is kezdhet, ha az ütemezett biztonsági másolat meghibásodik. Ez a parancsmag egyéni adatmegőrzéshez is használható lejárati dátummal vagy anélkül – további részletekért tanulmányozza a paraméterek súgószövegét. 

## PÉLDÁK

### 1. példa: Biztonsági másolat készítése biztonsági másolat készítése

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $NamedContainer = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -FriendlyName "pstestv2vm1" -VaultId $vault.ID
PS C:\> $Item = Get-AzRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $Job = Backup-AzRecoveryServicesBackupItem -Item $Item -VaultId $vault.ID
PS C:\> $Job
Operation        Status               StartTime            EndTime                   JOBID
------------     ---------            ------               ---------                 -------
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

Az első parancs lekérte a pstestv2vm1 nevű AzureVM típusú biztonságimásolat-tárolót, majd a $NamedContainer tárolja.
A második parancs lekérte a biztonsági másolatnak megfelelő elemet a $NamedContainer, majd tárolja azt a $Item változóban.
Az utolsó parancs elindítja a biztonságimásolat-elemet a $Item.

### 2. példa

Biztonsági másolat készítése biztonsági másolat készítése. (automatikusan generált)

```powershell <!-- Aladdin Generated Example --> 
Backup-AzRecoveryServicesBackupItem -ExpiryDateTimeUTC <DateTime> -Item $Item -VaultId $vault.ID
```

## PARAMETERS

### -BackupType

A biztonsági másolat hajtható végre

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupType
Parameter Sets: (All)
Aliases:
Accepted values: Full, Differential, Log, CopyOnlyFull

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

### -EnableCompression

Ha a tömörítés engedélyezése kötelező

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpiryDateTimeUTC

A helyreállítási pont lejárati idejét adja meg DateTime-objektumként, ha semmi sem veszi igénybe az alapértelmezett 30 napos értéket. Virtuális gépre, SQL-re (csak Copy-only-full backup type) és AFS biztonságimásolat-elemekre vonatkozik.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Item

Egy biztonságimásolat-elemet ad meg, amelynek a parancsmagja biztonsági másolatot készít.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -Confirm

A parancsmag futtatása előtt a rendszer megerősítést kér.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

A parancsmag futtatásakor a program megjeleníti, hogy mi történik.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase

### System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzRecoveryServicesBackupContainer](./Get-AzRecoveryServicesBackupContainer.md)

[Get-AzRecoveryServicesBackupItem](./Get-AzRecoveryServicesBackupItem.md)

[Restore-AzRecoveryServicesBackupItem](./Restore-AzRecoveryServicesBackupItem.md)
