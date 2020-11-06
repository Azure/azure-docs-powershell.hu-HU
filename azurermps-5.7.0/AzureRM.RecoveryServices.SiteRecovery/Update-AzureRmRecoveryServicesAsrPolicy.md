---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: bf049e18d75867f7dd9904e8d2ab2223dffdb0bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492212"
---
# Update-AzureRmRecoveryServicesAsrPolicy

## Áttekintés
Az Azure-webhely helyreállítási replikációs házirendjének frissítése

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### Alapértelmezett (alapértelmezett)
```
Update-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### VMwareToAzure
```
Update-AzureRmRecoveryServicesAsrPolicy [-VMwareToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureToAzure
```
Update-AzureRmRecoveryServicesAsrPolicy [-AzureToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### AzureToVMware
```
Update-AzureRmRecoveryServicesAsrPolicy [-AzureToVMware] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HyperVToAzure
```
Update-AzureRmRecoveryServicesAsrPolicy [-HyperVToAzure] -InputObject <ASRPolicy>
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### EnterpriseToEnterprise
```
Update-AzureRmRecoveryServicesAsrPolicy [-VmmToVmm] -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
Az **Update-AzureRmRecoveryServicesAsrPolicy** parancsmag frissíti a megadott Azure-webhely-helyreállítási replikációs házirendet.

## Példák

### Példa 1
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

Elindítja az Update replikációs házirend-műveletet a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.

### 2. példa
```
PS C:\> Update-AzureRmRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -ReplicationFrequencyInSeconds 900
```

Elindítja az Azure-től az Azure Replication Policy műveletet a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.

### 3. példa
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -RecoveryPointRetentionInHours 20
```

Elindítja az Azure-től az Azure replikációs házirendet a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.

## PARAMÉTEREK

### -ApplicationConsistentSnapshotFrequencyInHours
Annak a gyakoriságnak a gyakorisága (óra), amelyben az alkalmazások konzisztens helyreállítási pontja hozható létre.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hitelesítés
A használt hitelesítés típusát adja meg.

```yaml
Type: String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureToAzure
A Switch paraméter azt adja meg, hogy az Azure Virtual Machines rendszer két Azure-régió közötti replikálásához használt replikációs házirendet frissíti a rendszer.

```yaml
Type: SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureToVMware
Kapcsoló paraméter, amely azt jelzi, hogy a specfied házirendet az Azure-ban futó virtuális gépeken nem sikerült áthelyezni egy helyszíni VMware-webhelyre.

```yaml
Type: SwitchParameter
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tömörítés
Megadja, hogy engedélyezve kell-e a tömörítést.

```yaml
Type: String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.
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

### -Titkosítás
Megadja, hogy engedélyezve vagy le kell-e kapcsolni a titkosítást.

```yaml
Type: String
Parameter Sets: Default, HyperVToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HyperVToAzure
Kapcsoló paraméter, amely azt jelzi, hogy a specfied házirend a Hyper-V virtuális gépeket az Azure-ra replikálja.

```yaml
Type: SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
A parancsmag bemeneti objektuma: Itt adhatja meg az ASR replikációs házirend-objektumát, amely megfelel a frissítendő replikációs házirendnek.

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MultiVmSyncStatus
A házirend multiVm szinkronizálási állapotát adja meg.

```yaml
Type: String
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NumberOfRecoveryPointsToRetain
A megőrzendő szám-helyreállítási pontok számát adja meg.

```yaml
Type: Int32
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RPOWarningThresholdInMinutes
A RPO küszöbértéke percben, ahol a figyelmeztetés be van kapcsolva.

```yaml
Type: Int32
Parameter Sets: VMwareToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryAzureStorageAccountId
A replikációs cél Azure Storage Account ID azonosítóját adja meg. Akkor használható, ha a cél tárolási fiókja a replikáció, ha az New-AzureRmRecoveryServicesASRReplicationProtectedItem parancsmaggal való engedélyezéskor a rendszer nem ad meg alternatív szolgáltatást.


```yaml
Type: String
Parameter Sets: Default, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryPointRetentionInHours
Órák száma órákban a létrehozás után a helyreállítási pontok megőrzéséhez.

```yaml
Type: Int32
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicaDeletion
Annak megadása, hogy a virtuális kópiát törölni kell-e a VMM felügyelt webhelyről a másikra történő replikáció letiltásával.

```yaml
Type: String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationFrequencyInSeconds
A replikációs gyakoriság másodpercben megadott intervallumát adja meg.
Az érvényes értékek a következők:

- 30
- 300
- 900

```yaml
Type: String
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationMethod
A replikációs módszert adja meg.

```yaml
Type: String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationPort
A replikációhoz használt portot adja meg.

```yaml
Type: UInt16
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationStartTime
A replikációs kezdési időpontot adja meg.
A feladat elejétől legkésőbb 24 óráig kell szerepelnie.

```yaml
Type: TimeSpan
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMwareToAzure
Kapcsoló paraméter, amely azt jelzi, hogy a specfied-házirend a VMware Virtual Machines Azure rendszerre való replikálásához használatos.

```yaml
Type: SwitchParameter
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VmmToVmm
Kapcsoló paraméter, amely azt jelzi, hogy a specfied házirend a VMM felügyelt Hyper-V virtuális gépek két Hyper-V-webhelyre való replikálásához használatos.

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: 0
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

### Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRPolicy

## KIMENETEK

### System. Object (rendszer. objektum)

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
