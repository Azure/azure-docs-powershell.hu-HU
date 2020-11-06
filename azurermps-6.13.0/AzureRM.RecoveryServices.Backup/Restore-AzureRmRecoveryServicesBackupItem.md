---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/restore-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: b454f77bc3ad00ddf604e13672d61a7445c44fed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491882"
---
# Restore-AzureRmRecoveryServicesBackupItem

## Áttekintés
Egy biztonsági elem adatainak és konfigurációjának visszaállítása a helyreállítási pontra.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### AzureVMParameterSet (alapértelmezett)
```
Restore-AzureRmRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureFileParameterSet
```
Restore-AzureRmRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 -ResolveConflict <RestoreFSResolveConfictOption> [-SourceFilePath <String>] [-SourceFileType <SourceFileType>]
 [-TargetStorageAccountName <String>] [-TargetFileShareName <String>] [-TargetFolder <String>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **Restore-AzureRmRecoveryServicesBackupItem** parancsmag visszaállítja az Azure Backup-elemek adatát és konfigurációját egy megadott helyreállítási pontra.
Ez a parancsmag a helyreállítási szolgáltatások boltozatról az ügyfél tárterületére való visszaállítást indítja el.
A visszaállítási művelet nem állítja vissza a teljes virtuális gépet.
Visszaállítja a lemez adatait és a konfigurációs információkat.
A visszaállítási művelet befejeződése után létre kell hoznia a virtuális gépet, és el kell indítania.
Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.

## Példák

### 1. példa: elem visszaállítása helyreállítási pontra
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() 
PS C:\> $RestoreJob = Restore-AzureRmRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG"
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

Az első parancs a AzureVM típusú biztonsági tárolót kapja, majd a $Container változóban tárolja.
A második parancs beolvassa a V2VM nevű biztonsági másolatot a $Containerból, majd a $BackupItem változóban tárolja.
A harmadik parancs hét nappal korábban kapja meg a dátumot, majd a $StartDate változóban tárolja.
A negyedik parancs a jelenlegi dátumot kapja, majd a $EndDate változóban tárolja.
Az ötödik parancs beolvassa az $StartDate és a $EndDate által szűrt adott biztonsági másolat helyreállítási pontjainak listáját.
Az itt megadott dátumtartomány az elmúlt 7 nap.
Az utolsó parancs visszaállítja a lemezeket a TARGET Storage DestAccount a DestRG erőforráscsoporthoz.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryPoint
Annak a helyreállítási pontnak a meghatározása, amelyre a virtuális gépet vissza szeretné állítani.
**AzureRmRecoveryServicesBackupRecoveryPoint** objektum beolvasásához használja az Get-AzureRmRecoveryServicesBackupRecoveryPoint parancsmagot.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResolveConflict
Abban az esetben, ha a visszaállított elem a célhelyen is megtalálható, ezzel jelezheti, hogy felülírja-e vagy sem.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RestoreFSResolveConfictOption
Parameter Sets: AzureFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceFilePath
A fájl-megosztásból egy adott elemre való visszaállításhoz használható. Annak az elemnek az elérési útvonala, amelyet a fájlmegosztás során vissza kell állítani.

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceFileType
A fájl-megosztásból egy adott elemre való visszaállításhoz használható. Annak az elemnek az elérési útvonala, amelyet a fájlmegosztás során vissza kell állítani.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SourceFileType
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
Az előfizetésben a TARGET Storage fiók nevét adja meg.
A visszaállítási folyamat részeként ez a parancsmag tárolja a lemezeket és a konfigurációs információkat ebben a tárolási fiókban.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountResourceGroupName
Az előfizetésben a TARGET Storage-fiókot tartalmazó erőforráscsoport nevét adja meg.
A visszaállítási folyamat részeként ez a parancsmag tárolja a lemezeket és a konfigurációs információkat ebben a tárolási fiókban.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetFileShareName
Annak a fájlnak a megosztása, amelyre a fájl megosztását vissza kell állítani.

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetFolder
A mappa, amelyben a megosztást vissza szeretné állítani a targetFileShareName. hagyja üresen az üres változót a root mappa alatti visszaállításhoz.

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetResourceGroupName
Az erőforráscsoport, amelyre a kezelt lemezek visszaállíthatók. A VM biztonsági másolatának a kezelt lemezekkel való megadására vonatkozó lehetőség

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetStorageAccountName
Az a tárolási fiók, amelyre a fájl megosztását vissza kell állítani.

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseOriginalStorageAccount
Ezt a kapcsolót akkor használja, ha a helyreállítási pontból származó lemezeket vissza szeretné állítani az eredeti tárolási fiókjába.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
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

### -VaultLocation
A helyreállítási szolgáltatások boltozatának helye.

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

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

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
Annak megjelenítése, hogy mi történik, ha a parancsmag fut. A parancsmag nem fut.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String
Paraméterek: VaultId (ByValue), VaultLocation (ByValue)

### Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. RecoveryPointBase
Paraméterek: RecoveryPoint (ByValue)

## KIMENETEK

### Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Backup-AzureRmRecoveryServicesBackupItem](./Backup-AzureRmRecoveryServicesBackupItem.md)

[Get-AzureRmRecoveryServicesBackupItem](./Get-AzureRmRecoveryServicesBackupItem.md)

[Get-AzureRmRecoveryServicesBackupRecoveryPoint](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)


