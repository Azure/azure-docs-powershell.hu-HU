---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 3edbee06d2e4079d8c2283cc1b3af166d81450de
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920986"
---
# <span data-ttu-id="75cef-101">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="75cef-101">New-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="75cef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75cef-102">SYNOPSIS</span></span>
<span data-ttu-id="75cef-103">Létrehoz egy Azure-webhely-helyreállítási replikációs házirendet.</span><span class="sxs-lookup"><span data-stu-id="75cef-103">Creates an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="75cef-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="75cef-104">SYNTAX</span></span>

### <span data-ttu-id="75cef-105">HyperVToAzure (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="75cef-105">HyperVToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrPolicy [-HyperVToAzure] -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75cef-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="75cef-106">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrPolicy [-VMwareToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75cef-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="75cef-107">AzureToVMware</span></span>
```
New-AzRecoveryServicesAsrPolicy [-AzureToVMware] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75cef-108">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="75cef-108">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrPolicy [-AzureToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75cef-109">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="75cef-109">EnterpriseToEnterprise</span></span>
```
New-AzRecoveryServicesAsrPolicy [-VmmToVmm] -Name <String> -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String>
 [-NumberOfRecoveryPointsToRetain <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-Compression <String>] -ReplicationPort <UInt16> [-Authentication <String>]
 [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75cef-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="75cef-110">DESCRIPTION</span></span>
<span data-ttu-id="75cef-111">A **New-AzRecoveryServicesAsrPolicy** parancsmag létrehoz egy Azure-webhely-helyreállítási replikációs házirendet.</span><span class="sxs-lookup"><span data-stu-id="75cef-111">The **New-AzRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="75cef-112">A replikációs házirend olyan replikációs beállítások megadására használható, mint például a replikáció gyakorisága és a helyreállítási pontok száma.</span><span class="sxs-lookup"><span data-stu-id="75cef-112">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="75cef-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="75cef-113">EXAMPLES</span></span>

### <span data-ttu-id="75cef-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="75cef-114">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name "abc" -ReplicationProvider HyperVReplicaAzure -ReplicationFrequencyInSeconds 30 -NumberOfRecoveryPointsToRetain 10
```

<span data-ttu-id="75cef-115">A megadott paraméterekkel elindítja a replikációs házirend-létrehozási műveletet, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="75cef-115">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="75cef-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="75cef-116">Example 2</span></span>
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

<span data-ttu-id="75cef-117">A megadott paraméterekkel elindítja a replikációs házirend-létrehozási műveletet, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="75cef-117">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="75cef-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="75cef-118">Example 3</span></span>
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

### <span data-ttu-id="75cef-119">4. példa</span><span class="sxs-lookup"><span data-stu-id="75cef-119">Example 4</span></span>
```
PS C:\>  $Job = New-AzRecoveryServicesAsrPolicy -Name $TestPolicy1 -AzureToAzure -RecoveryPointRetentionInHours 10  -ApplicationConsistentSnapshotFrequencyInHours 5 
PS C:\>  Get-AsrJob -name $Job.id
```

<span data-ttu-id="75cef-120">A megadott paraméterekkel elindítja a replikációs házirend-létrehozási műveletet, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="75cef-120">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="75cef-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75cef-121">PARAMETERS</span></span>

### <span data-ttu-id="75cef-122">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="75cef-122">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="75cef-123">Az alkalmazás konzisztens helyreállítási pontjainak létrehozására használt gyakoriság (óra) megadása.</span><span class="sxs-lookup"><span data-stu-id="75cef-123">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="75cef-124">-Hitelesítés</span><span class="sxs-lookup"><span data-stu-id="75cef-124">-Authentication</span></span>
<span data-ttu-id="75cef-125">A használt hitelesítés típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="75cef-125">Specifies the type of authentication used.</span></span>
<span data-ttu-id="75cef-126">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="75cef-126">Valid values are:</span></span>

- <span data-ttu-id="75cef-127">Tanúsítvány</span><span class="sxs-lookup"><span data-stu-id="75cef-127">Certificate</span></span>
-  <span data-ttu-id="75cef-128">Kerberos</span><span class="sxs-lookup"><span data-stu-id="75cef-128">Kerberos</span></span>

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

### <span data-ttu-id="75cef-129">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="75cef-129">-AzureToAzure</span></span>
<span data-ttu-id="75cef-130">A Kapcsoló paraméter az Azure–Azure-házirendek létrehozásának forgatókönyvét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="75cef-130">Switch parameter specifies the scenario for azure to azure policy creation.</span></span>

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

### <span data-ttu-id="75cef-131">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="75cef-131">-AzureToVMware</span></span>
<span data-ttu-id="75cef-132">A Kapcsoló paraméter az Azure-nak a vMWare-házirendek létrehozásának forgatókönyvét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="75cef-132">Switch parameter specifies the scenario for azure to vMWare policy creation.</span></span>

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

### <span data-ttu-id="75cef-133">-Compression</span><span class="sxs-lookup"><span data-stu-id="75cef-133">-Compression</span></span>
<span data-ttu-id="75cef-134">Azt adja meg, hogy engedélyezve kell-e lennie a tömörítésnek.</span><span class="sxs-lookup"><span data-stu-id="75cef-134">Specifies if compression should be enabled.</span></span>

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

### <span data-ttu-id="75cef-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75cef-135">-DefaultProfile</span></span>
<span data-ttu-id="75cef-136">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="75cef-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="75cef-137">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="75cef-137">-HyperVToAzure</span></span>
<span data-ttu-id="75cef-138">A paraméter váltása a házirend megadásához a Hyper-V virtuális gépek Azure-ba való replikálása érdekében használható</span><span class="sxs-lookup"><span data-stu-id="75cef-138">Switch parameter to specify policy is to be used to replicate Hyper-V virtual machines to Azure</span></span>

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

### <span data-ttu-id="75cef-139">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="75cef-139">-MultiVmSyncStatus</span></span>
<span data-ttu-id="75cef-140">TöbbVm-szinkronizálási állapotot ad meg a házirendhez.</span><span class="sxs-lookup"><span data-stu-id="75cef-140">Specifies multiVm sync status for the policy.</span></span>

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

### <span data-ttu-id="75cef-141">-Name</span><span class="sxs-lookup"><span data-stu-id="75cef-141">-Name</span></span>
<span data-ttu-id="75cef-142">Az ASR replikációs házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="75cef-142">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="75cef-143">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="75cef-143">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="75cef-144">Megadja a megőrizni szükséges helyreállítási pontokat.</span><span class="sxs-lookup"><span data-stu-id="75cef-144">Specifies the number recovery points to retain.</span></span>

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

### <span data-ttu-id="75cef-145">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="75cef-145">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="75cef-146">Annak az Azure-tárfióknak az azonosítója, amelybe replikálni kell.</span><span class="sxs-lookup"><span data-stu-id="75cef-146">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="75cef-147">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="75cef-147">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="75cef-148">Őrizze meg a helyreállítási pontokat adott ideig órában.</span><span class="sxs-lookup"><span data-stu-id="75cef-148">Retain the recovery points for given time in hours.</span></span>

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

### <span data-ttu-id="75cef-149">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="75cef-149">-ReplicaDeletion</span></span>
<span data-ttu-id="75cef-150">Azt adja meg, hogy a virtuális replika-gépet törölni kell-e, amikor letiltja a VMM által felügyelt webhelyről egy másikra történő replikációt.</span><span class="sxs-lookup"><span data-stu-id="75cef-150">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

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

### <span data-ttu-id="75cef-151">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="75cef-151">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="75cef-152">Másodpercben megadja a replikációs gyakorisági intervallumot.</span><span class="sxs-lookup"><span data-stu-id="75cef-152">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="75cef-153">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="75cef-153">Valid values are:</span></span>

- <span data-ttu-id="75cef-154">30</span><span class="sxs-lookup"><span data-stu-id="75cef-154">30</span></span>
- <span data-ttu-id="75cef-155">300</span><span class="sxs-lookup"><span data-stu-id="75cef-155">300</span></span>
- <span data-ttu-id="75cef-156">900</span><span class="sxs-lookup"><span data-stu-id="75cef-156">900</span></span>

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

### <span data-ttu-id="75cef-157">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="75cef-157">-ReplicationMethod</span></span>
<span data-ttu-id="75cef-158">A replikációs módszert adja meg.</span><span class="sxs-lookup"><span data-stu-id="75cef-158">Specifies the replication method.</span></span>
<span data-ttu-id="75cef-159">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="75cef-159">Valid values are:</span></span>

- <span data-ttu-id="75cef-160">Online</span><span class="sxs-lookup"><span data-stu-id="75cef-160">Online</span></span>
- <span data-ttu-id="75cef-161">Offline</span><span class="sxs-lookup"><span data-stu-id="75cef-161">Offline</span></span>

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

### <span data-ttu-id="75cef-162">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="75cef-162">-ReplicationPort</span></span>
<span data-ttu-id="75cef-163">A replikációhoz használt portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="75cef-163">Specifies the port used for replication.</span></span>

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

### <span data-ttu-id="75cef-164">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="75cef-164">-ReplicationProvider</span></span>
<span data-ttu-id="75cef-165">A házirend replikációs szolgáltatóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="75cef-165">Specifies the replication provider for the policy.</span></span>

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

### <span data-ttu-id="75cef-166">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="75cef-166">-ReplicationStartTime</span></span>
<span data-ttu-id="75cef-167">A replikáció kezdési idejét adja meg.</span><span class="sxs-lookup"><span data-stu-id="75cef-167">Specifies the replication start time.</span></span>
<span data-ttu-id="75cef-168">A feladat kezdése után legalább 24 óranek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="75cef-168">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="75cef-169">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="75cef-169">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="75cef-170">Az RPO küszöbértéke percek alatt, amelyeknél figyelmeztetést kell alkalmazni.</span><span class="sxs-lookup"><span data-stu-id="75cef-170">The RPO threshold value in minutes to warn on.</span></span>

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

### <span data-ttu-id="75cef-171">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="75cef-171">-VmmToVmm</span></span>
<span data-ttu-id="75cef-172">A paraméter váltása a házirend megadásához a VMM-kiszolgáló által kezelt Hyper-V webhelyek közötti replikáláshoz használatos.</span><span class="sxs-lookup"><span data-stu-id="75cef-172">Switch parameter to specify policy is to be used to replicate between Hyper-V sites managed by a VMM server.</span></span>

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

### <span data-ttu-id="75cef-173">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="75cef-173">-VMwareToAzure</span></span>
<span data-ttu-id="75cef-174">Switch parameter specify that the replication policy being used to replikálása VMware virtual machines and/or Physical servers to Azure.</span><span class="sxs-lookup"><span data-stu-id="75cef-174">Switch parameter specifying that the replication policy being created will be used to replicate VMware virtual machines and/or Physical servers to Azure.</span></span>

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

### <span data-ttu-id="75cef-175">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75cef-175">-Confirm</span></span>
<span data-ttu-id="75cef-176">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="75cef-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75cef-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75cef-177">-WhatIf</span></span>
<span data-ttu-id="75cef-178">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="75cef-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75cef-179">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="75cef-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75cef-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75cef-180">CommonParameters</span></span>
<span data-ttu-id="75cef-181">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75cef-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75cef-182">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75cef-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75cef-183">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75cef-183">INPUTS</span></span>

### <span data-ttu-id="75cef-184">Nincs</span><span class="sxs-lookup"><span data-stu-id="75cef-184">None</span></span>

## <span data-ttu-id="75cef-185">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="75cef-185">OUTPUTS</span></span>

### <span data-ttu-id="75cef-186">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="75cef-186">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="75cef-187">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="75cef-187">NOTES</span></span>

## <span data-ttu-id="75cef-188">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="75cef-188">RELATED LINKS</span></span>

[<span data-ttu-id="75cef-189">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="75cef-189">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="75cef-190">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="75cef-190">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
