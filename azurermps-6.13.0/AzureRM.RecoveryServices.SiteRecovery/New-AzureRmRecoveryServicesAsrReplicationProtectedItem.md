---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 6a35620b7a4d8952b10973f181c2ab50f5d958b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491873"
---
# New-AzureRmRecoveryServicesAsrReplicationProtectedItem

## Áttekintés
Az ASR-védelemmel ellátott elemek replikálásának engedélyezése replikációs védelemmel ellátott elem létrehozásával.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### EnterpriseToEnterprise (alapértelmezett)
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### VMwareToAzure
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] -ProcessServer <ASRProcessServer> [-RecoveryAzureNetworkId <String>]
 [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String> [-ReplicationGroupName <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### EnterpriseToAzure
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HyperVSiteToAzure
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### AzureToAzure
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure]
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> -AzureVmId <String>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryResourceGroupId <String> [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureToAzureWithoutDiskDetails
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure] -AzureVmId <String> -Name <String>
 [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureStorageAccountId <String>] -LogStorageAccountId <String> -RecoveryResourceGroupId <String>
 [-RecoveryAvailabilitySetId <String>] [-RecoveryBootDiagStorageAccountId <String>] [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** parancsmag új replikációs védelemmel ellátott elemet hoz létre.
Ezzel a parancsmaggal engedélyezheti az ASR-védelemmel ellátott elemek replikálását.

## Példák

### Példa 1
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

Elindítja a védett ASR-elem replikációs védett elem létrehozásának műveletét, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.

### 2. példa
```
PS C:\>$job = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $pi -Name $rpiName -ProtectionContainerMapping $pcm `
-RecoveryAzureStorageAccountId $RecoveryAzureStorageAccountId -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-ProcessServer $fabric.fabricSpecificDetails.ProcessServers[0] -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

Elindítja a védett ASR-elem replikációs védett elem létrehozásának műveletét, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot (vmWare – Azure eset).

### 3. példa
```
PS C:>$job = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzureVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

Elindítja a védett ASR-elem replikációs védett elem létrehozásának műveletét, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot (Azure – Azure forgatókönyv).

### 4. példa
```
PS C:\> $disk1 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

Elindítja a megadott VmId replikációs védett elem létrehozása műveletet, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül (Azure – Azure forgatókönyv).

## PARAMÉTEREK

### -Fiók
A Futtatás mint fiók, amellyel szükség esetén lenyomhatja a mobil szolgáltatást. Az ASR-anyagban a Run as (futtatási) fiókból kell lennie.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureToAzure
A paramétert leválasztva megadhatja, hogy a replikált elem a helyreállítási Azure-területre replikált Azure virtuális gép.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureToAzureDiskReplicationConfiguration
A replikálni kívánt virtuálisgép-lemezek listáját adja meg, valamint a gyorsítótár-tárolási fiókot és a helyreállítási tárterületet, amelyet a lemez replikálásához kell használni.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureVmId
A replikálni kívánt Azure VM-azonosítót adja meg.

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.


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

### -HyperVToAzure
Váltson paramétert a replikált elem megadásához: egy olyan Hyper-V virtuális gép, amely az Azure-ra replikálódik.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeDiskId
A replikációra felvenni kívánt lemezek listája. Alapértelmezés szerint az összes lemez megtalálható.

```yaml
Type: System.String[]
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LogStorageAccountId
A replikációs naplók tárolásához használható naplófájl-vagy gyorsítótár-tárolási fiók azonosítóját adja meg.

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
Az ASR replikációs szolgáltatása által védett elem nevét adja meg. A névnek a boltozaton belül egyedinek kell lennie.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OS
Az operációs rendszer családját adja meg.
A paraméter elfogadható értékei a következők: Windows vagy Linux.

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OSDiskName
Az operációs rendszer lemezének nevét adja meg.

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProcessServer
A gép replikálásához használt folyamat kiszolgálója. Adja meg az ASR-anyagnak megfelelő folyamat-kiszolgálók listáját az ASR-szövetben, amely a beállítási kiszolgálónak megfelelő.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectableItem
Annak az ASR-elemnek az objektumát adja meg, amelyhez a replikáció engedélyezve van.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ProtectionContainerMapping
Az ASR-védelmi tároló társítása objektum, amely megfelel a replikációhoz használandó replikációs házirendnek.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryAvailabilitySetId
A AvailabilitySet azonosítója, amellyel visszaállíthatja a gépet feladatátvétel esetén.

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryAzureNetworkId
Az Azure virtuális hálózat azonosítója, amellyel a gépet feladatátvétel esetén helyreállíthatja.

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryAzureStorageAccountId
A replikálni kívánt Azure Storage-fiók AZONOSÍTÓját adja meg.

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryAzureSubnetName
A helyreállítási Azure virtuális hálózaton belül az alhálózat, amelyre a sikertelen virtuális gépet csatolni kell a feladatátvétel esetén.

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryBootDiagStorageAccountId
A helyreállítás Azure VM rendszerindítási diagnosztika tárolási fiókját adja meg.

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryCloudServiceId
A helyreállítási felhő szolgáltatás erőforrás-AZONOSÍTÓját adja meg a virtuális gép feladatátvételéhez.

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryResourceGroupId
Meghatározza annak az erőforráscsoport-azonosítónak az azonosítóját, amelyben a virtuális gépet feladatátvétel esetén létrehozzák.

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryVmName
A feladatátvétel után létrejövő helyreállítási VM-név.

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationGroupName
Annak a replikációs csoportnak a nevét adja meg, amely a több VM egységes helyreállítási pontok létrehozására használható. Alapértelmezés szerint az egyes replikációs védelemmel ellátott elemek a saját és a több VM-es konzisztens helyreállítási pontok csoportjába jönnek létre. Ezt a lehetőséget csak akkor használja, ha több VM-es konzisztens helyreállítási pontot kell létrehoznia a számítógépeken, ha az összes gépet ugyanabba a replikációs csoportba kívánja védeni. 

```yaml
Type: System.String
Parameter Sets: VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VmmToVmm
Kapcsoló paraméter a replikált elem megadásához: egy olyan Hyper-V virtuális gép, amely a VMM felügyelt Hyper-V-webhelyek között replikálódik.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMwareToAzure
Váltson paramétert a replikált elem megadásához egy olyan VMware Virtual Machine vagy fizikai kiszolgáló, amely az Azure-ra replikálódni fog.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitForCompletion
Azt adja meg, hogy a parancsmagnak a művelet befejezésekor várnia kell.

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

### – Megerősítés
Megerősítés kérése a művelet megkezdése előtt.

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
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

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

### Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRProtectableItem

## KIMENETEK

### Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmRecoveryServicesAsrReplicationProtectedItem](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[Set-AzureRmRecoveryServicesAsrReplicationProtectedItem](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
