---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 98031226919b143431206fd9e3b512e6c653b8a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838553"
---
# <span data-ttu-id="f9539-101">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="f9539-101">New-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="f9539-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f9539-102">SYNOPSIS</span></span>
<span data-ttu-id="f9539-103">Azure-webhely-helyreállítási replikációs házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f9539-103">Creates an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="f9539-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f9539-104">SYNTAX</span></span>

### <span data-ttu-id="f9539-105">HyperVToAzure (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f9539-105">HyperVToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrPolicy [-HyperVToAzure] -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9539-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="f9539-106">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrPolicy [-VMwareToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f9539-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="f9539-107">AzureToVMware</span></span>
```
New-AzRecoveryServicesAsrPolicy [-AzureToVMware] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f9539-108">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="f9539-108">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrPolicy [-AzureToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9539-109">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="f9539-109">EnterpriseToEnterprise</span></span>
```
New-AzRecoveryServicesAsrPolicy [-VmmToVmm] -Name <String> -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String>
 [-NumberOfRecoveryPointsToRetain <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-Compression <String>] -ReplicationPort <UInt16> [-Authentication <String>]
 [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9539-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="f9539-110">DESCRIPTION</span></span>
<span data-ttu-id="f9539-111">A **New-AzRecoveryServicesAsrPolicy** parancsmag létrehoz egy Azure-webhely-helyreállítási replikációs házirendet.</span><span class="sxs-lookup"><span data-stu-id="f9539-111">The **New-AzRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="f9539-112">A replikációs házirend segítségével megadhatja a replikációs beállításokat, például a replikációs gyakoriságot és a helyreállítási pontok számát.</span><span class="sxs-lookup"><span data-stu-id="f9539-112">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="f9539-113">Példák</span><span class="sxs-lookup"><span data-stu-id="f9539-113">EXAMPLES</span></span>

### <span data-ttu-id="f9539-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f9539-114">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name "abc" -ReplicationProvider HyperVReplicaAzure -ReplicationFrequencyInSeconds 30 -NumberOfRecoveryPointsToRetain 10
```

<span data-ttu-id="f9539-115">A megadott paraméterekkel elindítja a replikációs házirend-létrehozási műveletet, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="f9539-115">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="f9539-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="f9539-116">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name "abc122" -ReplicationProvider HyperVReplica2012R2 -ReplicationFrequencyInSeconds 300 -ReplicationPort 211

Name             : 1c609a5b-324e-461c-866f-ad58f944df25
ID               : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationJobs/1c609a5b-324e-461c-866f-ad58f944df25
Type             :
JobType          : AddProtectionProfile
DisplayName      : Create replication policy
ClientRequestId  : b10c83ee-fee2-42d4-ad1d-dfc3e166faab ActivityId: 67e8453c-fae0-465f-801c-dfa2e6e6ee23
State            : Succeeded
StateDescription : Completed
StartTime        : 8/29/2017 10:18:10 AM
EndTime          : 8/29/2017 10:18:11 AM
TargetObjectId   : bb8e8c57-221d-5668-9d82-b15a3e19a6a3
TargetObjectType : ProtectionProfile
TargetObjectName : abc122
AllowedActions   :
Tasks            : {Prerequisites check for creating the replication policy, Creating the replication policy}
Errors           : {}
```

<span data-ttu-id="f9539-117">A megadott paraméterekkel elindítja a replikációs házirend-létrehozási műveletet, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="f9539-117">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="f9539-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="f9539-118">Example 3</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name $policyName1 -ReplicationProvider InMageAzureV2 -RecoveryPoints 40  -RPOWarningThresholdInMinutes 5 -ApplicationConsistentSnapshotFrequencyInMinutes 15
Name             : ed69e451-878b-4f19-9c0f-73184be05eaf
ID               : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationJobs/ed69e451-878b-4f19-9c0f-73184be05eaf
Type             :
JobType          :
DisplayName      :
ClientRequestId  : d8922fa2-303c-4eb4-b556-e07969ea6fba ActivityId: 9e946cdf-2351-44c2-9aef-70ef2eab29b4
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

### <span data-ttu-id="f9539-119">4. példa</span><span class="sxs-lookup"><span data-stu-id="f9539-119">Example 4</span></span>
```
PS C:\>  $Job = New-AzRecoveryServicesAsrPolicy -Name $TestPolicy1 -AzToAzure -RecoveryPointRetentionInHours 10  -ApplicationConsistentSnapshotFrequencyInHours 5 
PS C:\>  Get-AsrJob -name $Job.id
```

<span data-ttu-id="f9539-120">A megadott paraméterekkel elindítja a replikációs házirend-létrehozási műveletet, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="f9539-120">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f9539-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f9539-121">PARAMETERS</span></span>

### <span data-ttu-id="f9539-122">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="f9539-122">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="f9539-123">Annak a gyakoriságnak a gyakorisága (óra), amelyben az alkalmazások konzisztens helyreállítási pontja hozható létre.</span><span class="sxs-lookup"><span data-stu-id="f9539-123">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="f9539-124">-Hitelesítés</span><span class="sxs-lookup"><span data-stu-id="f9539-124">-Authentication</span></span>
<span data-ttu-id="f9539-125">A használt hitelesítés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9539-125">Specifies the type of authentication used.</span></span>
<span data-ttu-id="f9539-126">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="f9539-126">Valid values are:</span></span>

- <span data-ttu-id="f9539-127">Tanúsítvány</span><span class="sxs-lookup"><span data-stu-id="f9539-127">Certificate</span></span>
-  <span data-ttu-id="f9539-128">Kerberos</span><span class="sxs-lookup"><span data-stu-id="f9539-128">Kerberos</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9539-129">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="f9539-129">-AzureToAzure</span></span>
<span data-ttu-id="f9539-130">{{Fill AzureToAzure Description}}</span><span class="sxs-lookup"><span data-stu-id="f9539-130">{{Fill AzureToAzure Description}}</span></span>

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

### <span data-ttu-id="f9539-131">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="f9539-131">-AzureToVMware</span></span>
<span data-ttu-id="f9539-132">{{Fill AzureToVMware Description}}</span><span class="sxs-lookup"><span data-stu-id="f9539-132">{{Fill AzureToVMware Description}}</span></span>

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

### <span data-ttu-id="f9539-133">-Tömörítés</span><span class="sxs-lookup"><span data-stu-id="f9539-133">-Compression</span></span>
<span data-ttu-id="f9539-134">Megadja, hogy engedélyezve kell-e a tömörítést.</span><span class="sxs-lookup"><span data-stu-id="f9539-134">Specifies if compression should be enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9539-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9539-135">-DefaultProfile</span></span>
<span data-ttu-id="f9539-136">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f9539-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f9539-137">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="f9539-137">-HyperVToAzure</span></span>
<span data-ttu-id="f9539-138">Kapcsoló paraméter megadása: a házirendet a Hyper-V virtuális gépek az Azure-ra való replikálásához használja.</span><span class="sxs-lookup"><span data-stu-id="f9539-138">Switch parameter to specify policy is to be used to replicate Hyper-V virtual machines to Azure</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9539-139">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="f9539-139">-MultiVmSyncStatus</span></span>
<span data-ttu-id="f9539-140">A házirend multiVm szinkronizálási állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9539-140">Specifies multiVm sync status for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, AzureToVMware, AzureToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9539-141">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f9539-141">-Name</span></span>
<span data-ttu-id="f9539-142">Az ASR-replikációs házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9539-142">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="f9539-143">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="f9539-143">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="f9539-144">A megőrzendő szám-helyreállítási pontok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9539-144">Specifies the number recovery points to retain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9539-145">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f9539-145">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="f9539-146">A replikálni kívánt Azure Storage-fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9539-146">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9539-147">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="f9539-147">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="f9539-148">Megtartja a helyreállítási pontokat órákban megadott idő alatt.</span><span class="sxs-lookup"><span data-stu-id="f9539-148">Retain the recovery points for given time in hours.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware, AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9539-149">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="f9539-149">-ReplicaDeletion</span></span>
<span data-ttu-id="f9539-150">Annak megadása, hogy a virtuális kópiát törölni kell-e a VMM felügyelt webhelyről a másikra történő replikáció letiltásával.</span><span class="sxs-lookup"><span data-stu-id="f9539-150">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9539-151">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="f9539-151">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="f9539-152">A replikációs gyakoriság másodpercben megadott intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9539-152">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="f9539-153">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="f9539-153">Valid values are:</span></span>

- <span data-ttu-id="f9539-154">30</span><span class="sxs-lookup"><span data-stu-id="f9539-154">30</span></span>
- <span data-ttu-id="f9539-155">300</span><span class="sxs-lookup"><span data-stu-id="f9539-155">300</span></span>
- <span data-ttu-id="f9539-156">900</span><span class="sxs-lookup"><span data-stu-id="f9539-156">900</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9539-157">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="f9539-157">-ReplicationMethod</span></span>
<span data-ttu-id="f9539-158">A replikációs módszert adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9539-158">Specifies the replication method.</span></span>
<span data-ttu-id="f9539-159">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="f9539-159">Valid values are:</span></span>

- <span data-ttu-id="f9539-160">Online</span><span class="sxs-lookup"><span data-stu-id="f9539-160">Online</span></span>
- <span data-ttu-id="f9539-161">Offline</span><span class="sxs-lookup"><span data-stu-id="f9539-161">Offline</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9539-162">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="f9539-162">-ReplicationPort</span></span>
<span data-ttu-id="f9539-163">A replikációhoz használt portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9539-163">Specifies the port used for replication.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9539-164">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="f9539-164">-ReplicationProvider</span></span>
<span data-ttu-id="f9539-165">A házirend replikációs szolgáltatóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9539-165">Specifies the replication provider for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9539-166">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="f9539-166">-ReplicationStartTime</span></span>
<span data-ttu-id="f9539-167">A replikációs kezdési időpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9539-167">Specifies the replication start time.</span></span>
<span data-ttu-id="f9539-168">A feladat elejétől legkésőbb 24 óráig kell szerepelnie.</span><span class="sxs-lookup"><span data-stu-id="f9539-168">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9539-169">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="f9539-169">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="f9539-170">A RPO küszöbértéke percben, ahol a figyelmeztetés be van kapcsolva.</span><span class="sxs-lookup"><span data-stu-id="f9539-170">The RPO threshold value in minutes to warn on.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9539-171">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="f9539-171">-VmmToVmm</span></span>
<span data-ttu-id="f9539-172">A paramétert választva megadhatja, hogy milyen házirendet szeretne használni a VMM-kiszolgáló által felügyelt Hyper-V-webhelyek közötti replikáláshoz.</span><span class="sxs-lookup"><span data-stu-id="f9539-172">Switch parameter to specify policy is to be used to replicate between Hyper-V sites managed by a VMM server.</span></span>

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

### <span data-ttu-id="f9539-173">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="f9539-173">-VMwareToAzure</span></span>
<span data-ttu-id="f9539-174">Kapcsoló paraméter, amely azt adja meg, hogy a létrehozott replikációs házirendet a rendszer a VMware virtuális gépek és/vagy fizikai kiszolgálók Azure-ra való replikálására használja.</span><span class="sxs-lookup"><span data-stu-id="f9539-174">Switch parameter specifying that the replication policy being created will be used to replicate VMware virtual machines and/or Physical servers to Azure.</span></span>

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

### <span data-ttu-id="f9539-175">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f9539-175">-Confirm</span></span>
<span data-ttu-id="f9539-176">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f9539-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9539-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9539-177">-WhatIf</span></span>
<span data-ttu-id="f9539-178">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f9539-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9539-179">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f9539-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9539-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9539-180">CommonParameters</span></span>
<span data-ttu-id="f9539-181">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f9539-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9539-182">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9539-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9539-183">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9539-183">INPUTS</span></span>

### <span data-ttu-id="f9539-184">Nincs</span><span class="sxs-lookup"><span data-stu-id="f9539-184">None</span></span>

## <span data-ttu-id="f9539-185">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9539-185">OUTPUTS</span></span>

### <span data-ttu-id="f9539-186">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f9539-186">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f9539-187">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f9539-187">NOTES</span></span>

## <span data-ttu-id="f9539-188">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f9539-188">RELATED LINKS</span></span>

[<span data-ttu-id="f9539-189">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="f9539-189">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="f9539-190">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="f9539-190">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
