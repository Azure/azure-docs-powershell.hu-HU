---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 691c1d822df332bb9a3e89b218ed2c7ba1166f38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493045"
---
# <span data-ttu-id="cf325-101">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="cf325-101">New-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="cf325-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cf325-102">SYNOPSIS</span></span>
<span data-ttu-id="cf325-103">Azure-webhely-helyreállítási replikációs házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="cf325-103">Creates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf325-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cf325-104">SYNTAX</span></span>

### <span data-ttu-id="cf325-105">HyperVToAzure (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cf325-105">HyperVToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-HyperVToAzure] -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf325-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="cf325-106">VMwareToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-VMwareToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf325-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="cf325-107">AzureToVMware</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-AzureToVMware] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf325-108">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="cf325-108">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-AzureToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf325-109">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="cf325-109">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-VmmToVmm] -Name <String> -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String>
 [-NumberOfRecoveryPointsToRetain <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-Compression <String>] -ReplicationPort <UInt16> [-Authentication <String>]
 [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf325-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="cf325-110">DESCRIPTION</span></span>
<span data-ttu-id="cf325-111">A **New-AzureRmRecoveryServicesAsrPolicy** parancsmag létrehoz egy Azure-webhely-helyreállítási replikációs házirendet.</span><span class="sxs-lookup"><span data-stu-id="cf325-111">The **New-AzureRmRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="cf325-112">A replikációs házirend segítségével megadhatja a replikációs beállításokat, például a replikációs gyakoriságot és a helyreállítási pontok számát.</span><span class="sxs-lookup"><span data-stu-id="cf325-112">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="cf325-113">Példák</span><span class="sxs-lookup"><span data-stu-id="cf325-113">EXAMPLES</span></span>

### <span data-ttu-id="cf325-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cf325-114">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrPolicy -Name "abc" -ReplicationProvider HyperVReplicaAzure -ReplicationFrequencyInSeconds 30 -NumberOfRecoveryPointsToRetain 10
```

<span data-ttu-id="cf325-115">A megadott paraméterekkel elindítja a replikációs házirend-létrehozási műveletet, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="cf325-115">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="cf325-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="cf325-116">Example 2</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrPolicy -Name "abc122" -ReplicationProvider HyperVReplica2012R2 -ReplicationFrequencyInSeconds 300 -ReplicationPort 211

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

<span data-ttu-id="cf325-117">A megadott paraméterekkel elindítja a replikációs házirend-létrehozási műveletet, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="cf325-117">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="cf325-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="cf325-118">Example 3</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrPolicy -Name $policyName1 -ReplicationProvider InMageAzureV2 -RecoveryPoints 40  -RPOWarningThresholdInMinutes 5 -ApplicationConsistentSnapshotFrequencyInMinutes 15
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

### <span data-ttu-id="cf325-119">4. példa</span><span class="sxs-lookup"><span data-stu-id="cf325-119">Example 4</span></span>
```
PS C:\>  $Job = New-AzureRmRecoveryServicesAsrPolicy -Name $TestPolicy1 -AzureToAzure -RecoveryPointRetentionInHours 10  -ApplicationConsistentSnapshotFrequencyInHours 5 
PS C:\>  Get-AsrJob -name $Job.id
```

<span data-ttu-id="cf325-120">A megadott paraméterekkel elindítja a replikációs házirend-létrehozási műveletet, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="cf325-120">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="cf325-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cf325-121">PARAMETERS</span></span>

### <span data-ttu-id="cf325-122">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="cf325-122">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="cf325-123">Annak a gyakoriságnak a gyakorisága (óra), amelyben az alkalmazások konzisztens helyreállítási pontja hozható létre.</span><span class="sxs-lookup"><span data-stu-id="cf325-123">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="cf325-124">-Hitelesítés</span><span class="sxs-lookup"><span data-stu-id="cf325-124">-Authentication</span></span>
<span data-ttu-id="cf325-125">A használt hitelesítés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf325-125">Specifies the type of authentication used.</span></span>
<span data-ttu-id="cf325-126">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="cf325-126">Valid values are:</span></span>

- <span data-ttu-id="cf325-127">Tanúsítvány</span><span class="sxs-lookup"><span data-stu-id="cf325-127">Certificate</span></span>
-  <span data-ttu-id="cf325-128">Kerberos</span><span class="sxs-lookup"><span data-stu-id="cf325-128">Kerberos</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf325-129">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="cf325-129">-AzureToAzure</span></span>
<span data-ttu-id="cf325-130">Switch paraméter, amely azt adja meg, hogy a létrehozott replikációs házirendet a rendszer két Azure-régió között a replikált Azure Virtual Machines rendszerhez használja.</span><span class="sxs-lookup"><span data-stu-id="cf325-130">Switch parameter specifying that the replication policy being created will be used to replicated Azure virtual machines between two Azure regions.</span></span>

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

### <span data-ttu-id="cf325-131">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="cf325-131">-AzureToVMware</span></span>
<span data-ttu-id="cf325-132">Kapcsoló paraméter, amely azt adja meg, hogy a létrehozott replikációs házirendet a rendszer a replikálás visszavonására használja a VMware virtuális gépek és az Azure-alapú fizikai kiszolgálók esetén a helyszíni VMware-webhelyre való visszalépéshez.</span><span class="sxs-lookup"><span data-stu-id="cf325-132">Switch parameter specifying that the replication policy being created will be used to reverse replicate failed over VMware virtual machines and Physical servers running in Azure back to an on-premises VMware site.</span></span>

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

### <span data-ttu-id="cf325-133">-Tömörítés</span><span class="sxs-lookup"><span data-stu-id="cf325-133">-Compression</span></span>
<span data-ttu-id="cf325-134">Megadja, hogy engedélyezve kell-e a tömörítést.</span><span class="sxs-lookup"><span data-stu-id="cf325-134">Specifies if compression should be enabled.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf325-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cf325-135">-Confirm</span></span>
<span data-ttu-id="cf325-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cf325-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf325-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf325-137">-DefaultProfile</span></span>
<span data-ttu-id="cf325-138">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf325-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="cf325-139">-Titkosítás</span><span class="sxs-lookup"><span data-stu-id="cf325-139">-Encryption</span></span>
<span data-ttu-id="cf325-140">Megadja, hogy engedélyezve vagy le kell-e kapcsolni a titkosítást.</span><span class="sxs-lookup"><span data-stu-id="cf325-140">Specifies if encryption should be enabled or disabled.</span></span>

```yaml
Type: String
Parameter Sets: HyperVToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf325-141">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="cf325-141">-HyperVToAzure</span></span>
<span data-ttu-id="cf325-142">Kapcsoló paraméter megadása: a házirendet a Hyper-V virtuális gépek az Azure-ra való replikálásához használja.</span><span class="sxs-lookup"><span data-stu-id="cf325-142">Switch parameter to specify policy is to be used to replicate Hyper-V virtual machines to Azure</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf325-143">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="cf325-143">-MultiVmSyncStatus</span></span>
<span data-ttu-id="cf325-144">A házirend multiVm szinkronizálási állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf325-144">Specifies multiVm sync status for the policy.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, AzureToVMware, AzureToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf325-145">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cf325-145">-Name</span></span>
<span data-ttu-id="cf325-146">Az ASR-replikációs házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf325-146">Specifies the name of the ASR replication policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf325-147">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="cf325-147">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="cf325-148">A megőrzendő szám-helyreállítási pontok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf325-148">Specifies the number recovery points to retain.</span></span>

```yaml
Type: Int32
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf325-149">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="cf325-149">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="cf325-150">A RPO küszöbértéke percben, ahol a figyelmeztetés be van kapcsolva.</span><span class="sxs-lookup"><span data-stu-id="cf325-150">The RPO threshold value in minutes to warn on.</span></span>

```yaml
Type: Int32
Parameter Sets: VMwareToAzure, AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf325-151">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="cf325-151">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="cf325-152">A replikálni kívánt Azure Storage-fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf325-152">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: String
Parameter Sets: HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf325-153">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="cf325-153">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="cf325-154">Megtartja a helyreállítási pontokat órákban megadott idő alatt.</span><span class="sxs-lookup"><span data-stu-id="cf325-154">Retain the recovery points for given time in hours.</span></span>

```yaml
Type: Int32
Parameter Sets: VMwareToAzure, AzureToVMware, AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf325-155">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="cf325-155">-ReplicaDeletion</span></span>
<span data-ttu-id="cf325-156">Annak megadása, hogy a virtuális kópiát törölni kell-e a VMM felügyelt webhelyről a másikra történő replikáció letiltásával.</span><span class="sxs-lookup"><span data-stu-id="cf325-156">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf325-157">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="cf325-157">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="cf325-158">A replikációs gyakoriság másodpercben megadott intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf325-158">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="cf325-159">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="cf325-159">Valid values are:</span></span>

- <span data-ttu-id="cf325-160">30</span><span class="sxs-lookup"><span data-stu-id="cf325-160">30</span></span>
- <span data-ttu-id="cf325-161">300</span><span class="sxs-lookup"><span data-stu-id="cf325-161">300</span></span>
- <span data-ttu-id="cf325-162">900</span><span class="sxs-lookup"><span data-stu-id="cf325-162">900</span></span>

```yaml
Type: String
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf325-163">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="cf325-163">-ReplicationMethod</span></span>
<span data-ttu-id="cf325-164">A replikációs módszert adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf325-164">Specifies the replication method.</span></span>
<span data-ttu-id="cf325-165">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="cf325-165">Valid values are:</span></span>

- <span data-ttu-id="cf325-166">Online</span><span class="sxs-lookup"><span data-stu-id="cf325-166">Online</span></span>
- <span data-ttu-id="cf325-167">Offline</span><span class="sxs-lookup"><span data-stu-id="cf325-167">Offline</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf325-168">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="cf325-168">-ReplicationPort</span></span>
<span data-ttu-id="cf325-169">A replikációhoz használt portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf325-169">Specifies the port used for replication.</span></span>

```yaml
Type: UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf325-170">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="cf325-170">-ReplicationProvider</span></span>
<span data-ttu-id="cf325-171">A házirend replikációs szolgáltatóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf325-171">Specifies the replication provider for the policy.</span></span>

```yaml
Type: String
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf325-172">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="cf325-172">-ReplicationStartTime</span></span>
<span data-ttu-id="cf325-173">A replikációs kezdési időpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf325-173">Specifies the replication start time.</span></span>
<span data-ttu-id="cf325-174">A feladat elejétől legkésőbb 24 óráig kell szerepelnie.</span><span class="sxs-lookup"><span data-stu-id="cf325-174">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf325-175">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="cf325-175">-VMwareToAzure</span></span>
<span data-ttu-id="cf325-176">Kapcsoló paraméter, amely azt adja meg, hogy a létrehozott replikációs házirendet a rendszer a VMware virtuális gépek és/vagy fizikai kiszolgálók Azure-ra való replikálására használja.</span><span class="sxs-lookup"><span data-stu-id="cf325-176">Switch parameter specifying that the replication policy being created will be used to replicate VMware virtual machines and/or Physical servers to Azure.</span></span>

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

### <span data-ttu-id="cf325-177">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="cf325-177">-VmmToVmm</span></span>
<span data-ttu-id="cf325-178">A paramétert választva megadhatja, hogy milyen házirendet szeretne használni a VMM-kiszolgáló által felügyelt Hyper-V-webhelyek közötti replikáláshoz.</span><span class="sxs-lookup"><span data-stu-id="cf325-178">Switch parameter to specify policy is to be used to replicate between Hyper-V sites managed by a VMM server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf325-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf325-179">-WhatIf</span></span>
<span data-ttu-id="cf325-180">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cf325-180">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf325-181">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cf325-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf325-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf325-182">CommonParameters</span></span>
<span data-ttu-id="cf325-183">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cf325-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf325-184">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf325-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf325-185">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf325-185">INPUTS</span></span>

### <span data-ttu-id="cf325-186">Nincs</span><span class="sxs-lookup"><span data-stu-id="cf325-186">None</span></span>

## <span data-ttu-id="cf325-187">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf325-187">OUTPUTS</span></span>

### <span data-ttu-id="cf325-188">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="cf325-188">System.Object</span></span>

## <span data-ttu-id="cf325-189">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cf325-189">NOTES</span></span>

## <span data-ttu-id="cf325-190">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf325-190">RELATED LINKS</span></span>

[<span data-ttu-id="cf325-191">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="cf325-191">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="cf325-192">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="cf325-192">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
