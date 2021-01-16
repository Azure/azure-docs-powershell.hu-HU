---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 31b43930737627a3013f60a82c2ec30626b8518c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349122"
---
# <span data-ttu-id="59e36-101">Update-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="59e36-101">Update-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="59e36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59e36-102">SYNOPSIS</span></span>
<span data-ttu-id="59e36-103">Frissíti az Azure-webhely-helyreállítási replikációs házirendet.</span><span class="sxs-lookup"><span data-stu-id="59e36-103">Updates an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="59e36-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="59e36-104">SYNTAX</span></span>

### <span data-ttu-id="59e36-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="59e36-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59e36-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="59e36-106">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VMwareToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59e36-107">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="59e36-107">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59e36-108">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="59e36-108">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToVMware] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59e36-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="59e36-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-HyperVToAzure] -InputObject <ASRPolicy>
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59e36-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="59e36-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VmmToVmm] -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59e36-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="59e36-111">DESCRIPTION</span></span>
<span data-ttu-id="59e36-112">Az **Update-AzRecoveryServicesAsrPolicy** parancsmag frissíti a megadott Azure-webhely-helyreállítási replikációs házirendet.</span><span class="sxs-lookup"><span data-stu-id="59e36-112">The **Update-AzRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="59e36-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="59e36-113">EXAMPLES</span></span>

### <span data-ttu-id="59e36-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="59e36-114">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="59e36-115">Elindítja a frissítési replikációs házirendműveletet a megadott paraméterekkel, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="59e36-115">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="59e36-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="59e36-116">Example 2</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="59e36-117">A megadott paraméterekkel elindítja az Azure–Azure replikációs házirendműveletet, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="59e36-117">Starts the update azure to azure replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="59e36-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="59e36-118">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -RecoveryPointRetentionInHours 20
```

<span data-ttu-id="59e36-119">A megadott paraméterekkel elindítja az Azure–Azure replikációs házirend frissítési házirendet, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="59e36-119">Starts the update azure to azure replication policy using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="59e36-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59e36-120">PARAMETERS</span></span>

### <span data-ttu-id="59e36-121">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="59e36-121">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="59e36-122">Az alkalmazás konzisztens helyreállítási pontjainak létrehozására használt gyakoriság (óra) megadása.</span><span class="sxs-lookup"><span data-stu-id="59e36-122">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="59e36-123">-Hitelesítés</span><span class="sxs-lookup"><span data-stu-id="59e36-123">-Authentication</span></span>
<span data-ttu-id="59e36-124">A használt hitelesítés típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="59e36-124">Specifies the type of authentication used.</span></span>

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

### <span data-ttu-id="59e36-125">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="59e36-125">-AzureToAzure</span></span>
<span data-ttu-id="59e36-126">Az Azure–Azure katasztrófa-helyreállítást határozza meg.</span><span class="sxs-lookup"><span data-stu-id="59e36-126">Specifies the Azure to Azure disaster recovery.</span></span>

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

### <span data-ttu-id="59e36-127">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="59e36-127">-AzureToVMware</span></span>
<span data-ttu-id="59e36-128">Az Azure–vMWare katasztrófa-helyreállítást adja meg.</span><span class="sxs-lookup"><span data-stu-id="59e36-128">Specifies the Azure to vMWare disaster recovery.</span></span>

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

### <span data-ttu-id="59e36-129">-Compression</span><span class="sxs-lookup"><span data-stu-id="59e36-129">-Compression</span></span>
<span data-ttu-id="59e36-130">Azt adja meg, hogy engedélyezve kell-e lennie a tömörítésnek.</span><span class="sxs-lookup"><span data-stu-id="59e36-130">Specifies if compression should be enabled.</span></span>

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

### <span data-ttu-id="59e36-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59e36-131">-DefaultProfile</span></span>
<span data-ttu-id="59e36-132">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59e36-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="59e36-133">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="59e36-133">-HyperVToAzure</span></span>
<span data-ttu-id="59e36-134">Switch parameter indicating that the specified policy is used to replicate Hyper-V virtual machines to Azure.</span><span class="sxs-lookup"><span data-stu-id="59e36-134">Switch parameter indicating that the specified policy is used to replicate Hyper-V virtual machines to Azure.</span></span>

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

### <span data-ttu-id="59e36-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59e36-135">-InputObject</span></span>
<span data-ttu-id="59e36-136">Bemeneti objektum a parancsmaghoz: A frissíthető replikációs házirendnek megfelelő ASR replikációs házirendobjektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="59e36-136">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

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

### <span data-ttu-id="59e36-137">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="59e36-137">-MultiVmSyncStatus</span></span>
<span data-ttu-id="59e36-138">TöbbVm-szinkronizálási állapotot ad meg a házirendhez.</span><span class="sxs-lookup"><span data-stu-id="59e36-138">Specifies multiVm sync status for the policy.</span></span>

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

### <span data-ttu-id="59e36-139">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="59e36-139">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="59e36-140">Megadja a megőrizni szükséges helyreállítási pontokat.</span><span class="sxs-lookup"><span data-stu-id="59e36-140">Specifies the number recovery points to retain.</span></span>

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

### <span data-ttu-id="59e36-141">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="59e36-141">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="59e36-142">A replikációs cél Azure-tárfiók-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="59e36-142">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="59e36-143">A replikáció céltároló fiókjaként használható, ha nem áll rendelkezésre alternatív megoldás, miközben engedélyezi a replikációt a New-AzRecoveryServicesASRReplicationProtectedItem parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="59e36-143">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>


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

### <span data-ttu-id="59e36-144">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="59e36-144">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="59e36-145">A létrehozás után a helyreállítási pontok megőrzésének ideje órákban.</span><span class="sxs-lookup"><span data-stu-id="59e36-145">Time in hours to retain recovery points after creation.</span></span>

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

### <span data-ttu-id="59e36-146">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="59e36-146">-ReplicaDeletion</span></span>
<span data-ttu-id="59e36-147">Azt adja meg, hogy a virtuális replika-gépet törölni kell-e, amikor letiltja a VMM által felügyelt webhelyről egy másikra történő replikációt.</span><span class="sxs-lookup"><span data-stu-id="59e36-147">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

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

### <span data-ttu-id="59e36-148">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="59e36-148">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="59e36-149">Másodpercben megadja a replikációs gyakorisági intervallumot.</span><span class="sxs-lookup"><span data-stu-id="59e36-149">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="59e36-150">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="59e36-150">Valid values are:</span></span>

- <span data-ttu-id="59e36-151">30</span><span class="sxs-lookup"><span data-stu-id="59e36-151">30</span></span>
- <span data-ttu-id="59e36-152">300</span><span class="sxs-lookup"><span data-stu-id="59e36-152">300</span></span>
- <span data-ttu-id="59e36-153">900</span><span class="sxs-lookup"><span data-stu-id="59e36-153">900</span></span>

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

### <span data-ttu-id="59e36-154">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="59e36-154">-ReplicationMethod</span></span>
<span data-ttu-id="59e36-155">A replikációs módszert adja meg.</span><span class="sxs-lookup"><span data-stu-id="59e36-155">Specifies the replication method.</span></span>

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

### <span data-ttu-id="59e36-156">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="59e36-156">-ReplicationPort</span></span>
<span data-ttu-id="59e36-157">A replikációhoz használt portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="59e36-157">Specifies the port used for replication.</span></span>

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

### <span data-ttu-id="59e36-158">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="59e36-158">-ReplicationStartTime</span></span>
<span data-ttu-id="59e36-159">A replikáció kezdési idejét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59e36-159">Specifies the replication start time.</span></span>
<span data-ttu-id="59e36-160">A feladat kezdése után legalább 24 óranek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="59e36-160">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="59e36-161">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="59e36-161">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="59e36-162">Az RPO küszöbértéke percek alatt, amelyeknél figyelmeztetést kell alkalmazni.</span><span class="sxs-lookup"><span data-stu-id="59e36-162">The RPO threshold value in minutes to warn on.</span></span>

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

### <span data-ttu-id="59e36-163">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="59e36-163">-VmmToVmm</span></span>
<span data-ttu-id="59e36-164">Switch parameter indicating that the specified policy is used to replicate VMM managed Hyper-V virtual machines between two Hyper-V sites.</span><span class="sxs-lookup"><span data-stu-id="59e36-164">Switch parameter indicating that the specified policy is used to replicate VMM managed Hyper-V virtual machines between two Hyper-V sites.</span></span>

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

### <span data-ttu-id="59e36-165">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="59e36-165">-VMwareToAzure</span></span>
<span data-ttu-id="59e36-166">Switch parameter indicating that the specified policy is used to replicate VMware virtual machines to Azure.</span><span class="sxs-lookup"><span data-stu-id="59e36-166">Switch parameter indicating that the specified policy is used to replicate VMware virtual machines to Azure.</span></span>

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

### <span data-ttu-id="59e36-167">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59e36-167">-Confirm</span></span>
<span data-ttu-id="59e36-168">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="59e36-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59e36-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59e36-169">-WhatIf</span></span>
<span data-ttu-id="59e36-170">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="59e36-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59e36-171">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="59e36-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59e36-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59e36-172">CommonParameters</span></span>
<span data-ttu-id="59e36-173">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59e36-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59e36-174">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59e36-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59e36-175">INPUTS</span><span class="sxs-lookup"><span data-stu-id="59e36-175">INPUTS</span></span>

### <span data-ttu-id="59e36-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="59e36-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="59e36-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59e36-177">OUTPUTS</span></span>

### <span data-ttu-id="59e36-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="59e36-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="59e36-179">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="59e36-179">NOTES</span></span>

## <span data-ttu-id="59e36-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59e36-180">RELATED LINKS</span></span>
