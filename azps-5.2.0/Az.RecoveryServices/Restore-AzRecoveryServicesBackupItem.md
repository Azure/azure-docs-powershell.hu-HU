---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 593603e212c2ebfd709e5f4c70797ea369877b76
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360735"
---
# Restore-AzRecoveryServicesBackupItem

## SYNOPSIS

Visszaállítja egy biztonsági másolat adatait és konfigurációját a megadott helyreállítási pontra. A szükséges paraméterek a biztonsági másolat típusától függően változnak.
Ugyanez a parancs használható az Azure Virtuális gépek, az Azure Virtuális gépeken futó adatbázisok és az Azure-fájlmegosztások visszaállításához is.

## SZINTAXIS

### AzureVMParameterSet (alapértelmezett)
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### AzureVMManagedDiskParameterSet
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-TargetResourceGroupName] <String>
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureVMRestoreManagedAsUnmanaged
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureVMUnManagedDiskParameterSet
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureFileShareParameterSet
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureWorkloadParameterSet
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS

A **Restore-AzRecoveryServicesBackupItem** parancsmag visszaállítja egy Azure biztonságimásolat-elem adatait és konfigurációját egy megadott helyreállítási pontra.

**Biztonsági másolat az Azure VM-ről**

Ezzel a paranccsal biztonsági másolatot készíthet az Azure virtuális gépeiről, és visszaállíthatja a lemezeket (mind felügyelt, mind nem felügyelt). A visszaállítási művelet nem visszaállítja a teljes virtuális gépet.
Ha ez egy felügyelt lemezen lévő virtuális gép, meg kell adni egy célerőforrás-csoportot a visszaállított lemezeket tároló helyként. Ha a célerőforrás-csoport meg van adva, és a pillanatképek a biztonságimásolat-házirendben megadott erőforráscsoportban vannak, a visszaállítási művelet azonnal meg fog jelenni, és a lemezeket helyi pillanatképekből kell létrehozni, és célerőforrás-csoportban kell tartani. Arra is van lehetőség, hogy nem felügyelt lemezként állítsa vissza őket, de ez kihasználja az Azure helyreállítási szolgáltatások tárolóban lévő adatokat, és így sokkal lassabb lesz. A virtuális gép konfigurációja és a virtuális gépnek a visszaállított lemezből való létrehozásához használható telepítősablon letölti a megadott tárfiókba.
Ha ez egy nem felügyelt lemezes VM, akkor a pillanatfelvételek a lemez eredeti tárfiókban és/vagy a helyreállítási szolgáltatások tárolóban vannak. Ha a felhasználó lehetőséget ad az Eredeti tárfiók használatára a visszaállításhoz, akkor azonnali visszaállítás is lehetséges. Ellenkező esetben a rendszer adatokat hoz létre az Azure Helyreállítási szolgáltatások tárolóból, és a lemezeket a megadott tárfiókban hozza létre a virtuális gép és a telepítési sablon konfigurációja mellett.

> [!IMPORTANT]
> Az Azure VM alapértelmezés szerint minden lemezről biztonsági másolatot készít. Az Enable-Backup parancs használata során szelektíven biztonsági másolatot készíthet a kapcsolódó lemezről a kivételLista vagy az InclusionList paraméter használatával. A lemezeket szelektíven visszaállító lehetőség csak akkor érhető el, ha az egyikről szelektíven biztonsági másolat is van.

További információért tanulmányozza a különböző lehetséges paraméterkészleteket és paraméterszövegeket.

> [!NOTE]
> Ha a -VaultId paramétert használja, akkor a -VaultLocation paramétert is használnia kell.

**Biztonsági másolat az Azure-fájlok megosztásáról**

Visszaállíthat egy teljes fájlmegosztást vagy egy adott/több fájlt/mappát a megosztáson. Visszaállíthatja az eredeti helyet vagy egy másik helyet.

**Azure Workloads esetén**

Sql-DBs-fájlokat visszaállíthat az Azure-virtuális gépeken


## PÉLDÁK

### 1. példa: Egy biztonsági másolatból származó, felügyelt lemezről származó Azure VM lemezének visszaállítása egy adott helyreállítási pontból

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

Az első parancs lekérte a Helyreállítási szolgáltatások tárolót, és egy $vault tárolja.
A második parancs lekérte az AzureVM típusú biztonságimásolat-elemet (V2VM) a "V2VM" névvel, és tárolja azt a $BackupItem változóban.
A harmadik parancs a hét nappal korábbi dátumot kapja meg, majd a $StartDate tárolja.
A negyedik parancs megkapja az aktuális dátumot, majd a $EndDate tárolja.
Az ötödik parancs az adott biztonságimásolat-elem helyreállítási pontjainak listáját kapja meg, $StartDate és $EndDate.
Az utolsó parancs visszaállítja az összes lemezt a célerőforrás-csoport Target_RG, majd a DestRG erőforráscsoport tárolófiókjában biztosítja a VM konfigurációs adatait és a telepítési sablont.

### 2. példa: Egy biztonsági másolatból származó, felügyelt lemezről származó Azure VM adott lemezének visszaállítása egy adott helyreállítási pontból

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

Az első parancs lekérte a Helyreállítási szolgáltatások tárolót, és egy $vault tárolja.
A második parancs lekérte az AzureVM típusú biztonságimásolat-elemet (V2VM) a "V2VM" névvel, és tárolja azt a $BackupItem változóban.
A harmadik parancs a hét nappal korábbi dátumot kapja meg, majd a $StartDate tárolja.
A negyedik parancs megkapja az aktuális dátumot, majd a $EndDate tárolja.
Az ötödik parancs az adott biztonságimásolat-elem helyreállítási pontjainak listáját kapja meg, $StartDate és $EndDate.
A hatodik parancs a visszaállítandó lemezlistát tárolja a restoreDiskLUN változóban.
Az utolsó parancs visszaállítja a megadott LUN-okat a célerőforrás-csoport Target_RG-jára, majd a DestRG erőforráscsoport tárfiókjában adja meg a VM konfigurációs adatait és a telepítési sablont.

### 3. példa: Felügyelt virtuális gép lemezeinek visszaállítása nem felügyelt lemezként

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -RestoreAsUnmanagedDisks -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

Az első parancs lekérte a RecoveryServices tárolót, és egy $vault tárolja.
A második parancs lekérte a biztonságimásolat-elemet, majd a $BackupItem tárolja.
A harmadik parancs a hét nappal korábbi dátumot kapja meg, majd a $StartDate tárolja.
A negyedik parancs megkapja az aktuális dátumot, majd a $EndDate tárolja.
Az ötödik parancs az adott biztonságimásolat-elem helyreállítási pontjainak listáját kapja meg, $StartDate és $EndDate.
A hatodik parancs a lemezeket nemmanaged lemezként visszaállítja.

### 4. példa: Nemmanaged VM visszaállítása nemmanaged Disksként az eredeti tárfiók használatával

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -Name "UnManagedVM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -UseOriginalStorageAccount -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

Az első parancs lekérte a RecoveryServices tárolót, és egy $vault tárolja.
A második parancs lekérte a biztonságimásolat-elemet, majd a $BackupItem tárolja.
A harmadik parancs a hét nappal korábbi dátumot kapja meg, majd a $StartDate tárolja.
A negyedik parancs megkapja az aktuális dátumot, majd a $EndDate tárolja.
Az ötödik parancs az adott biztonságimásolat-elem helyreállítási pontjainak listáját kapja meg, $StartDate és $EndDate.
A hatodik parancs a lemezeket nemmanaged lemezként visszaállítja az eredeti tárhelyfiókjukba.

### 5. példa: AzureFileShare-elem több fájlának visszaállítása

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureStorage -WorkloadType AzureVM -VaultId $vault.ID -Name "fileshareitem"
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -VaultId $vault.ID
PS C:\> $files = ("file1.txt", "file2.txt")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -MultipleSourceFilePath $files -SourceFileType File -ResolveConflict Overwrite -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    fileshareitem   Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

Az első parancs lekérte a Helyreállítási szolgáltatások tárolót, és egy $vault tárolja.
A második parancs lekérte a fileshareitem nevű biztonságimásolat-elemet, majd a $BackupItem tárolja.
A harmadik parancs lekérte az adott biztonságimásolat-elem helyreállítási pontjainak listáját.
A negyedik parancs megadja, hogy mely fájlokat kell visszaállítani és egy változóban $files.
Az utolsó parancs visszaállítja a megadott fájlokat az eredeti helyére.

### 6. példa: SQL DB visszaállítása egy Azure VM-en belül egy másik cél VIRTUÁLIS GÉPre egy külön teljes helyreállítási pont számára

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureWorkload -WorkloadType MSSQL -VaultId $vault.ID -Name "MSSQLSERVER;model"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $FullRP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $TargetInstance = Get-AzRecoveryServicesBackupProtectableItem -WorkloadType MSSQL -ItemType SQLInstance -Name "<SQLInstance Name>" -ServerName "<SQL VM name>" -VaultId $vault.ID
PS C:\> $AnotherInstanceWithFullConfig = Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -RecoveryPoint $FullRP -TargetItem $TargetInstance -AlternateWorkloadRestore -VaultId $vault.ID
PS C:\> Restore-AzRecoveryServicesBackupItem -WLRecoveryConfig $AnotherInstanceWithLogConfig -VaultId $vault.ID
    WorkloadName       Operation        Status            StartTime                 EndTime          JobID
    ------------       ---------        ------            ---------                 -------          -----
    MSSQLSERVER/m...   Restore          InProgress        3/17/2019 10:02:45 AM                      3274xg2b-e4fg-5952-89b4-8cb566gc1748

```

### 7. példa: SQL DB visszaállítása egy Azure VM-en belül egy másik cél VM-re egy napló-helyreállítási ponthoz

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureWorkload -WorkloadType MSSQL -VaultId $vault.ID -Name "MSSQLSERVER;model"
PS C:\> $PointInTime = Get-Date -Date "2019-03-20 01:00:00Z"
PS C:\> $TargetInstance = Get-AzRecoveryServicesBackupProtectableItem -WorkloadType MSSQL -ItemType SQLInstance -Name "<SQLInstance Name>" -ServerName "<SQL VM name>" -VaultId $vault.ID
PS C:\> $AnotherInstanceWithLogConfig = Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -PointInTime $PointInTime -Item $BackupItem -AlternateWorkloadRestore -VaultId $vault.ID
PS C:\> Restore-AzRecoveryServicesBackupItem -WLRecoveryConfig $AnotherInstanceWithLogConfig -VaultId $vault.ID
    WorkloadName     Operation      Status           StartTime                 EndTime           JobID
    ------------     ---------      ------           ---------                 -------           -----
    MSSQLSERVER/m... Restore        InProgress       3/17/2019 10:02:45 AM                       3274xg2b-e4fg-5952-89b4-8cb566gc1748

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

### -MultipleSourceFilePath
Több fájl visszaállítása fájlmegosztásból. A fájlmegosztáson belül visszaállítható elemek elérési útjai.

```yaml
Type: System.String[]
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryPoint

Azt a helyreállítási pontot adja meg, amelybe vissza kell állítani a biztonságimásolat-elemet.
**AzureRmRecoveryServicesBackupRecoveryPoint-objektum** beszerzéséhez használja a **Get-AzRecoveryServicesBackupRecoveryPoint** parancsmagot.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: AzureVMParameterSet, AzureFileParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResolveConflict

Abban az esetben, ha a visszaállított elem is létezik a célhelyen, ezzel a mezővel jelezheti, hogy felül kell-e írnia vagy sem.
A paraméter elfogadható értékei a következőek:

- Felülírás
- Kihagyás

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RestoreFSResolveConflictOption
Parameter Sets: AzureFileParameterSet
Aliases:
Accepted values: Overwrite, Skip

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestoreAsUnmanagedDisks
Ezzel a kapcsolóval megadhatja, hogy a visszaállítás nem használt lemezként történt-e

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMRestoreAsUnmanaged
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestoreDiskList
Adja meg, hogy mely lemezeket kell helyreállítani a biztonságimentett virtuális gépről

```yaml
Type: System.String[]
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestoreOnlyOSDisk
Ezzel a kapcsolóval csak a biztonsági másolatokat tároló virtuális gép operációs rendszer lemezei állíthatók vissza

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceFilePath

Egy adott elem fájlmegosztásból való visszaállításához használható. A fájlmegosztáson belül visszaállítani kívánt elem elérési útja.

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

Egy adott elem fájlmegosztásból való visszaállításához használható. A fájlmegosztáson belül visszaállítani kívánt elem típusa.
A paraméter elfogadható értékei a következőek:

- Fájl
- Címtár

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SourceFileType]
Parameter Sets: AzureFileParameterSet
Aliases:
Accepted values: File, Directory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName

Az előfizetésben a célként megadott tárfiók nevét adja meg.
A visszaállítási folyamat részeként ez a parancsmag ebben a Tárfiókban tárolja a lemezeket és a konfigurációs adatokat.

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountResourceGroupName

Annak az erőforráscsoportnak a neve, amely az előfizetésben a céltárfiókot tartalmazza.
A visszaállítási folyamat részeként ez a parancsmag ebben a Tárfiókban tárolja a lemezeket és a konfigurációs adatokat.

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetFileShareName

Az a fájlmegosztás, amelyre a fájlmegosztást vissza kell állítani.

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

Az a mappa, amelyben a fájlmegosztást vissza kell állítani a TargetFileShareName fájlon belül. Ha a biztonsági másolat tartalmát vissza kell állítani egy gyökérmappába, a célmappa értékeit adja meg üres karakterláncként.

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

Az erőforráscsoport, amelybe a felügyelt lemezeket visszaállítja a rendszer. Virtuális gép felügyelt lemezekkel való biztonsági mentésére alkalmazható

```yaml
Type: System.String
Parameter Sets: AzureVMTargetRGParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetStorageAccountName

Az a tárfiók, amelybe vissza kell állítani a fájlmegosztást.

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

Akkor használja ezt a kapcsolót, ha a helyreállítási pontról származó lemezeket vissza kell állítani az eredeti tárhelyfiókjukba.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: Named
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

### -VaultLocation

A helyreállítási szolgáltatások tárolója.

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

### -WLRecoveryConfig

Helyreállítási konfigurációs

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase
Parameter Sets: AzureWorkloadParameterSet
Aliases:

Required: True
Position: 0
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

### System.String

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase

## KIMENETEK

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Backup-AzRecoveryServicesBackupItem](./Backup-AzRecoveryServicesBackupItem.md)

[Get-AzRecoveryServicesBackupItem](./Get-AzRecoveryServicesBackupItem.md)

[Get-AzRecoveryServicesBackupRecoveryPoint](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
