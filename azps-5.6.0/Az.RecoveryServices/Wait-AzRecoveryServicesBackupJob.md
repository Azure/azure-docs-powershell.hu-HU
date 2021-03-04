---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/wait-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: e0b3dc87ffdfc86f39f201b6384f38ce8ca1c70a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922689"
---
# Wait-AzRecoveryServicesBackupJob

## SYNOPSIS

Megvárja, amíg befejeződik a biztonsági mentési feladat.

## SZINTAXIS

```
Wait-AzRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS

A **Wait-AzRecoveryServicesBackup Job** parancsmag megvárja, amíg befejeződik az Azure Biztonsági másolat parancsmag.
A biztonsági mentési feladatok hosszú ideig is el tudnak tartani.
Ha egy parancsfájl részeként futtat biztonságimásolat-feladatot, előfordulhat, hogy kényszeríteni szeretné, hogy a parancsfájl várja meg, amíg befejeződik a feladat, mielőtt az más feladatokra folytatódik.
A parancsmagot tartalmazó parancsmag egyszerűbb lehet, mint az, amely a biztonsági másolat szolgáltatásban lekérdezi a feladat állapotát.
Állítsa be a tároló környezetét a -VaultId paraméter használatával.

## PÉLDÁK

### 1. példa: Várjon, amíg befejeződik egy feladat

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> Wait-AzRecoveryServicesBackupJob -Job $Jobs[0] -VaultId $vault.ID -Timeout 3600
```

Ez a parancsprogram lekérdezi az első folyamatban lévő feladatot, amíg a feladat be nem fejeződik, vagy amíg az 1 órás időkorlát el nem jár.

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

### -Job

Azt a feladatot adja meg, amelyig várni kell.
**Biztonságimásolat-objektum** beszerzéséhez használja a **Get-AzRecoveryServicesBackupServicesBackupService** parancsmagot.

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Timeout

Ez a parancsmag másodpercben megadott maximális idejét adja meg, amíg a feladat befejeződik.
Javasoljuk, hogy adjon meg egy időkorrektaértéket.

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
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

### System.Object

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzRecoveryServicesBackupService](./Get-AzRecoveryServicesBackupJob.md)
