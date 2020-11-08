---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 31b43930737627a3013f60a82c2ec30626b8518c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010808"
---
# <span data-ttu-id="8cf28-101">Update-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="8cf28-101">Update-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="8cf28-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8cf28-102">SYNOPSIS</span></span>
<span data-ttu-id="8cf28-103">Az Azure-webhely helyreállítási replikációs házirendjének frissítése</span><span class="sxs-lookup"><span data-stu-id="8cf28-103">Updates an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="8cf28-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8cf28-104">SYNTAX</span></span>

### <span data-ttu-id="8cf28-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8cf28-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8cf28-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="8cf28-106">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VMwareToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cf28-107">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="8cf28-107">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8cf28-108">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="8cf28-108">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToVMware] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cf28-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="8cf28-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-HyperVToAzure] -InputObject <ASRPolicy>
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8cf28-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="8cf28-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VmmToVmm] -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cf28-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="8cf28-111">DESCRIPTION</span></span>
<span data-ttu-id="8cf28-112">Az **Update-AzRecoveryServicesAsrPolicy** parancsmag frissíti a megadott Azure-webhely-helyreállítási replikációs házirendet.</span><span class="sxs-lookup"><span data-stu-id="8cf28-112">The **Update-AzRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="8cf28-113">Példák</span><span class="sxs-lookup"><span data-stu-id="8cf28-113">EXAMPLES</span></span>

### <span data-ttu-id="8cf28-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8cf28-114">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="8cf28-115">Elindítja az Update replikációs házirend-műveletet a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="8cf28-115">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="8cf28-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="8cf28-116">Example 2</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="8cf28-117">Elindítja az Azure-től az Azure Replication Policy műveletet a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="8cf28-117">Starts the update azure to azure replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="8cf28-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="8cf28-118">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -RecoveryPointRetentionInHours 20
```

<span data-ttu-id="8cf28-119">Elindítja az Azure-től az Azure replikációs házirendet a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="8cf28-119">Starts the update azure to azure replication policy using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="8cf28-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8cf28-120">PARAMETERS</span></span>

### <span data-ttu-id="8cf28-121">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="8cf28-121">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="8cf28-122">Annak a gyakoriságnak a gyakorisága (óra), amelyben az alkalmazások konzisztens helyreállítási pontja hozható létre.</span><span class="sxs-lookup"><span data-stu-id="8cf28-122">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf28-123">-Hitelesítés</span><span class="sxs-lookup"><span data-stu-id="8cf28-123">-Authentication</span></span>
<span data-ttu-id="8cf28-124">A használt hitelesítés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8cf28-124">Specifies the type of authentication used.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf28-125">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="8cf28-125">-AzureToAzure</span></span>
<span data-ttu-id="8cf28-126">Az Azure – Azure katasztrófa-helyreállítást adja meg.</span><span class="sxs-lookup"><span data-stu-id="8cf28-126">Specifies the Azure to Azure disaster recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf28-127">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="8cf28-127">-AzureToVMware</span></span>
<span data-ttu-id="8cf28-128">Az Azure a vMWare katasztrófa-helyreállítást adja meg.</span><span class="sxs-lookup"><span data-stu-id="8cf28-128">Specifies the Azure to vMWare disaster recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf28-129">-Tömörítés</span><span class="sxs-lookup"><span data-stu-id="8cf28-129">-Compression</span></span>
<span data-ttu-id="8cf28-130">Megadja, hogy engedélyezve kell-e a tömörítést.</span><span class="sxs-lookup"><span data-stu-id="8cf28-130">Specifies if compression should be enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf28-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cf28-131">-DefaultProfile</span></span>
<span data-ttu-id="8cf28-132">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8cf28-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8cf28-133">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="8cf28-133">-HyperVToAzure</span></span>
<span data-ttu-id="8cf28-134">Kapcsoló paraméter, amely azt jelzi, hogy a Hyper-V virtuális gépek az Azure-ra való replikálásához a megadott házirendet használja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="8cf28-134">Switch parameter indicating that the specified policy is used to replicate Hyper-V virtual machines to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf28-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8cf28-135">-InputObject</span></span>
<span data-ttu-id="8cf28-136">A parancsmag bemeneti objektuma: Itt adhatja meg az ASR replikációs házirend-objektumát, amely megfelel a frissítendő replikációs házirendnek.</span><span class="sxs-lookup"><span data-stu-id="8cf28-136">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8cf28-137">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="8cf28-137">-MultiVmSyncStatus</span></span>
<span data-ttu-id="8cf28-138">A házirend multiVm szinkronizálási állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8cf28-138">Specifies multiVm sync status for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf28-139">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="8cf28-139">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="8cf28-140">A megőrzendő szám-helyreállítási pontok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8cf28-140">Specifies the number recovery points to retain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf28-141">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8cf28-141">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="8cf28-142">A replikációs cél Azure Storage Account ID azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8cf28-142">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="8cf28-143">Akkor használható, ha a cél tárolási fiókja a replikáció, ha az New-AzRecoveryServicesASRReplicationProtectedItem parancsmaggal való engedélyezéskor a rendszer nem ad meg alternatív szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="8cf28-143">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>


```yaml
Type: System.String
Parameter Sets: Default, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf28-144">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="8cf28-144">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="8cf28-145">Órák száma órákban a létrehozás után a helyreállítási pontok megőrzéséhez.</span><span class="sxs-lookup"><span data-stu-id="8cf28-145">Time in hours to retain recovery points after creation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf28-146">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="8cf28-146">-ReplicaDeletion</span></span>
<span data-ttu-id="8cf28-147">Annak megadása, hogy a virtuális kópiát törölni kell-e a VMM felügyelt webhelyről a másikra történő replikáció letiltásával.</span><span class="sxs-lookup"><span data-stu-id="8cf28-147">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf28-148">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="8cf28-148">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="8cf28-149">A replikációs gyakoriság másodpercben megadott intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8cf28-149">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="8cf28-150">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="8cf28-150">Valid values are:</span></span>

- <span data-ttu-id="8cf28-151">30</span><span class="sxs-lookup"><span data-stu-id="8cf28-151">30</span></span>
- <span data-ttu-id="8cf28-152">300</span><span class="sxs-lookup"><span data-stu-id="8cf28-152">300</span></span>
- <span data-ttu-id="8cf28-153">900</span><span class="sxs-lookup"><span data-stu-id="8cf28-153">900</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf28-154">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="8cf28-154">-ReplicationMethod</span></span>
<span data-ttu-id="8cf28-155">A replikációs módszert adja meg.</span><span class="sxs-lookup"><span data-stu-id="8cf28-155">Specifies the replication method.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf28-156">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="8cf28-156">-ReplicationPort</span></span>
<span data-ttu-id="8cf28-157">A replikációhoz használt portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="8cf28-157">Specifies the port used for replication.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf28-158">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="8cf28-158">-ReplicationStartTime</span></span>
<span data-ttu-id="8cf28-159">A replikációs kezdési időpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="8cf28-159">Specifies the replication start time.</span></span>
<span data-ttu-id="8cf28-160">A feladat elejétől legkésőbb 24 óráig kell szerepelnie.</span><span class="sxs-lookup"><span data-stu-id="8cf28-160">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf28-161">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="8cf28-161">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="8cf28-162">A RPO küszöbértéke percben, ahol a figyelmeztetés be van kapcsolva.</span><span class="sxs-lookup"><span data-stu-id="8cf28-162">The RPO threshold value in minutes to warn on.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf28-163">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="8cf28-163">-VmmToVmm</span></span>
<span data-ttu-id="8cf28-164">Kapcsoló paraméter, amely azt jelzi, hogy a megadott házirend a VMM felügyelt Hyper-V virtuális gépek két Hyper-V-webhelyre való replikálásához használatos.</span><span class="sxs-lookup"><span data-stu-id="8cf28-164">Switch parameter indicating that the specified policy is used to replicate VMM managed Hyper-V virtual machines between two Hyper-V sites.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf28-165">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="8cf28-165">-VMwareToAzure</span></span>
<span data-ttu-id="8cf28-166">Kapcsoló paraméter, amely azt jelzi, hogy a megadott házirend a VMware Virtual Machines Azure rendszerhez való replikálásához használatos.</span><span class="sxs-lookup"><span data-stu-id="8cf28-166">Switch parameter indicating that the specified policy is used to replicate VMware virtual machines to Azure.</span></span>

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

### <span data-ttu-id="8cf28-167">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8cf28-167">-Confirm</span></span>
<span data-ttu-id="8cf28-168">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8cf28-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cf28-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cf28-169">-WhatIf</span></span>
<span data-ttu-id="8cf28-170">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8cf28-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8cf28-171">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8cf28-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cf28-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cf28-172">CommonParameters</span></span>
<span data-ttu-id="8cf28-173">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8cf28-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cf28-174">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8cf28-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cf28-175">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8cf28-175">INPUTS</span></span>

### <span data-ttu-id="8cf28-176">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="8cf28-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="8cf28-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8cf28-177">OUTPUTS</span></span>

### <span data-ttu-id="8cf28-178">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8cf28-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8cf28-179">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8cf28-179">NOTES</span></span>

## <span data-ttu-id="8cf28-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8cf28-180">RELATED LINKS</span></span>
