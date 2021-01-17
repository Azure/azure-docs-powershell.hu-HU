---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: ba82e1ddf8385f74b271feb9119280d48fc1b859
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479847"
---
# Get-AzRecoveryServicesBackupRecoveryLogChain

## SYNOPSIS
Ez a parancs felsorolja az adott biztonságimásolat-elem töretlen naplóláncának kezdő és záró pontjait. Segítségével megállapíthatja, hogy érvényes-e az az időpont, amelyre a felhasználó vissza szeretné állítani a adatbázis-adatbázist.

## SZINTAXIS

### NoFilterParameterSet (alapértelmezett)
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### DateTimeFilter
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzRecoveryServicesBackupRecoveryLogChain** parancsmag időben megkapja az időtartomány helyreállítási pontjait egy biztonsági másolatként használt Azure Biztonsági másolat elemhez.
Miután biztonságiolt egy elemet, az **AzRecoveryServicesBackupRecoveryLogChain** objektumnak egy vagy több helyreállítási időtartománya van.

## PÉLDÁK

### 1. példa
```powershell
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

Az első parancs hét nappal ezelőtti dátumot ad vissza, majd a $StartDate tárolja.
A második parancs megkapja a mai dátumot, majd a $EndDate tárolja.
A harmadik parancs lekérte az AzureWorkload biztonságimásolat-tárolókat, és tárolja őket a $Container változóban.
A negyedik parancs megkapja a biztonságimásolat-elemet, majd megosztja azt a bevezető parancsmagon keresztül biztonságimásolat-elem objektumként.
Az utolsó parancs lekérte az elem helyreállítási időtartományának tömbét a $BackupItem, majd tárolja őket a $RP változóban.

### 2. példa

Ez a parancs felsorolja az adott biztonságimásolat-elem töretlen naplóláncának kezdő és záró pontjait. (automatikusan generált)

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupRecoveryLogChain -Item $Item -VaultId $vault.ID
```

## PARAMETERS

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

### -EndDate
Annak az időtartománynak a vége, amelynek helyreállítási pontját le kell kérni

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Item
Védett elem objektum, amelyhez helyreállítási pontot kell lehívni

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StartDate
Annak az időtartománynak a kezdési ideje, amelyhez helyreállítási pontot kell lehívni

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 0
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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
System.String

## KIMENETEK

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
