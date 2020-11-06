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
# <span data-ttu-id="deea3-101">Update-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="deea3-101">Update-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="deea3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="deea3-102">SYNOPSIS</span></span>
<span data-ttu-id="deea3-103">Az Azure-webhely helyreállítási replikációs házirendjének frissítése</span><span class="sxs-lookup"><span data-stu-id="deea3-103">Updates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="deea3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="deea3-104">SYNTAX</span></span>

### <span data-ttu-id="deea3-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="deea3-105">Default (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="deea3-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="deea3-106">VMwareToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-VMwareToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="deea3-107">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="deea3-107">AzureToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-AzureToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="deea3-108">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="deea3-108">AzureToVMware</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-AzureToVMware] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="deea3-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="deea3-109">HyperVToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-HyperVToAzure] -InputObject <ASRPolicy>
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="deea3-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="deea3-110">EnterpriseToEnterprise</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-VmmToVmm] -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="deea3-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="deea3-111">DESCRIPTION</span></span>
<span data-ttu-id="deea3-112">Az **Update-AzureRmRecoveryServicesAsrPolicy** parancsmag frissíti a megadott Azure-webhely-helyreállítási replikációs házirendet.</span><span class="sxs-lookup"><span data-stu-id="deea3-112">The **Update-AzureRmRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="deea3-113">Példák</span><span class="sxs-lookup"><span data-stu-id="deea3-113">EXAMPLES</span></span>

### <span data-ttu-id="deea3-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="deea3-114">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="deea3-115">Elindítja az Update replikációs házirend-műveletet a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="deea3-115">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="deea3-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="deea3-116">Example 2</span></span>
```
PS C:\> Update-AzureRmRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="deea3-117">Elindítja az Azure-től az Azure Replication Policy műveletet a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="deea3-117">Starts the update azure to azure replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="deea3-118">3. példa</span><span class="sxs-lookup"><span data-stu-id="deea3-118">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -RecoveryPointRetentionInHours 20
```

<span data-ttu-id="deea3-119">Elindítja az Azure-től az Azure replikációs házirendet a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="deea3-119">Starts the update azure to azure replication policy using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="deea3-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="deea3-120">PARAMETERS</span></span>

### <span data-ttu-id="deea3-121">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="deea3-121">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="deea3-122">Annak a gyakoriságnak a gyakorisága (óra), amelyben az alkalmazások konzisztens helyreállítási pontja hozható létre.</span><span class="sxs-lookup"><span data-stu-id="deea3-122">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="deea3-123">-Hitelesítés</span><span class="sxs-lookup"><span data-stu-id="deea3-123">-Authentication</span></span>
<span data-ttu-id="deea3-124">A használt hitelesítés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="deea3-124">Specifies the type of authentication used.</span></span>

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

### <span data-ttu-id="deea3-125">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="deea3-125">-AzureToAzure</span></span>
<span data-ttu-id="deea3-126">A Switch paraméter azt adja meg, hogy az Azure Virtual Machines rendszer két Azure-régió közötti replikálásához használt replikációs házirendet frissíti a rendszer.</span><span class="sxs-lookup"><span data-stu-id="deea3-126">Switch parameter specifying that the replication policy used to replicate Azure virtual machines between two Azure regions will be updated.</span></span>

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

### <span data-ttu-id="deea3-127">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="deea3-127">-AzureToVMware</span></span>
<span data-ttu-id="deea3-128">Kapcsoló paraméter, amely azt jelzi, hogy a specfied házirendet az Azure-ban futó virtuális gépeken nem sikerült áthelyezni egy helyszíni VMware-webhelyre.</span><span class="sxs-lookup"><span data-stu-id="deea3-128">Switch parameter indicating that the specfied policy is used to replicate failed over virtual machines running in Azure back to an on-premises VMware site.</span></span>

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

### <span data-ttu-id="deea3-129">-Tömörítés</span><span class="sxs-lookup"><span data-stu-id="deea3-129">-Compression</span></span>
<span data-ttu-id="deea3-130">Megadja, hogy engedélyezve kell-e a tömörítést.</span><span class="sxs-lookup"><span data-stu-id="deea3-130">Specifies if compression should be enabled.</span></span>

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

### <span data-ttu-id="deea3-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="deea3-131">-Confirm</span></span>
<span data-ttu-id="deea3-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="deea3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="deea3-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deea3-133">-DefaultProfile</span></span>
<span data-ttu-id="deea3-134">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="deea3-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="deea3-135">-Titkosítás</span><span class="sxs-lookup"><span data-stu-id="deea3-135">-Encryption</span></span>
<span data-ttu-id="deea3-136">Megadja, hogy engedélyezve vagy le kell-e kapcsolni a titkosítást.</span><span class="sxs-lookup"><span data-stu-id="deea3-136">Specifies if encryption should be enabled or disabled.</span></span>

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

### <span data-ttu-id="deea3-137">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="deea3-137">-HyperVToAzure</span></span>
<span data-ttu-id="deea3-138">Kapcsoló paraméter, amely azt jelzi, hogy a specfied házirend a Hyper-V virtuális gépeket az Azure-ra replikálja.</span><span class="sxs-lookup"><span data-stu-id="deea3-138">Switch parameter indicating that the specfied policy is used to replicate Hyper-V virtual machines to Azure.</span></span>

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

### <span data-ttu-id="deea3-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="deea3-139">-InputObject</span></span>
<span data-ttu-id="deea3-140">A parancsmag bemeneti objektuma: Itt adhatja meg az ASR replikációs házirend-objektumát, amely megfelel a frissítendő replikációs házirendnek.</span><span class="sxs-lookup"><span data-stu-id="deea3-140">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

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

### <span data-ttu-id="deea3-141">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="deea3-141">-MultiVmSyncStatus</span></span>
<span data-ttu-id="deea3-142">A házirend multiVm szinkronizálási állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="deea3-142">Specifies multiVm sync status for the policy.</span></span>

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

### <span data-ttu-id="deea3-143">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="deea3-143">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="deea3-144">A megőrzendő szám-helyreállítási pontok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="deea3-144">Specifies the number recovery points to retain.</span></span>

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

### <span data-ttu-id="deea3-145">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="deea3-145">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="deea3-146">A RPO küszöbértéke percben, ahol a figyelmeztetés be van kapcsolva.</span><span class="sxs-lookup"><span data-stu-id="deea3-146">The RPO threshold value in minutes to warn on.</span></span>

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

### <span data-ttu-id="deea3-147">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="deea3-147">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="deea3-148">A replikációs cél Azure Storage Account ID azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="deea3-148">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="deea3-149">Akkor használható, ha a cél tárolási fiókja a replikáció, ha az New-AzureRmRecoveryServicesASRReplicationProtectedItem parancsmaggal való engedélyezéskor a rendszer nem ad meg alternatív szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="deea3-149">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>


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

### <span data-ttu-id="deea3-150">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="deea3-150">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="deea3-151">Órák száma órákban a létrehozás után a helyreállítási pontok megőrzéséhez.</span><span class="sxs-lookup"><span data-stu-id="deea3-151">Time in hours to retain recovery points after creation.</span></span>

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

### <span data-ttu-id="deea3-152">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="deea3-152">-ReplicaDeletion</span></span>
<span data-ttu-id="deea3-153">Annak megadása, hogy a virtuális kópiát törölni kell-e a VMM felügyelt webhelyről a másikra történő replikáció letiltásával.</span><span class="sxs-lookup"><span data-stu-id="deea3-153">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

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

### <span data-ttu-id="deea3-154">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="deea3-154">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="deea3-155">A replikációs gyakoriság másodpercben megadott intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="deea3-155">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="deea3-156">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="deea3-156">Valid values are:</span></span>

- <span data-ttu-id="deea3-157">30</span><span class="sxs-lookup"><span data-stu-id="deea3-157">30</span></span>
- <span data-ttu-id="deea3-158">300</span><span class="sxs-lookup"><span data-stu-id="deea3-158">300</span></span>
- <span data-ttu-id="deea3-159">900</span><span class="sxs-lookup"><span data-stu-id="deea3-159">900</span></span>

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

### <span data-ttu-id="deea3-160">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="deea3-160">-ReplicationMethod</span></span>
<span data-ttu-id="deea3-161">A replikációs módszert adja meg.</span><span class="sxs-lookup"><span data-stu-id="deea3-161">Specifies the replication method.</span></span>

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

### <span data-ttu-id="deea3-162">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="deea3-162">-ReplicationPort</span></span>
<span data-ttu-id="deea3-163">A replikációhoz használt portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="deea3-163">Specifies the port used for replication.</span></span>

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

### <span data-ttu-id="deea3-164">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="deea3-164">-ReplicationStartTime</span></span>
<span data-ttu-id="deea3-165">A replikációs kezdési időpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="deea3-165">Specifies the replication start time.</span></span>
<span data-ttu-id="deea3-166">A feladat elejétől legkésőbb 24 óráig kell szerepelnie.</span><span class="sxs-lookup"><span data-stu-id="deea3-166">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="deea3-167">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="deea3-167">-VMwareToAzure</span></span>
<span data-ttu-id="deea3-168">Kapcsoló paraméter, amely azt jelzi, hogy a specfied-házirend a VMware Virtual Machines Azure rendszerre való replikálásához használatos.</span><span class="sxs-lookup"><span data-stu-id="deea3-168">Switch parameter indicating that the specfied policy is used to replicate VMware virtual machines to Azure.</span></span>

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

### <span data-ttu-id="deea3-169">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="deea3-169">-VmmToVmm</span></span>
<span data-ttu-id="deea3-170">Kapcsoló paraméter, amely azt jelzi, hogy a specfied házirend a VMM felügyelt Hyper-V virtuális gépek két Hyper-V-webhelyre való replikálásához használatos.</span><span class="sxs-lookup"><span data-stu-id="deea3-170">Switch parameter indicating that the specfied policy is used to replicate VMM managed Hyper-V virtual machines between two Hyper-V sites.</span></span>

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

### <span data-ttu-id="deea3-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="deea3-171">-WhatIf</span></span>
<span data-ttu-id="deea3-172">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="deea3-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="deea3-173">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="deea3-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="deea3-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deea3-174">CommonParameters</span></span>
<span data-ttu-id="deea3-175">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="deea3-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deea3-176">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="deea3-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deea3-177">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="deea3-177">INPUTS</span></span>

### <span data-ttu-id="deea3-178">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="deea3-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="deea3-179">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="deea3-179">OUTPUTS</span></span>

### <span data-ttu-id="deea3-180">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="deea3-180">System.Object</span></span>

## <span data-ttu-id="deea3-181">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="deea3-181">NOTES</span></span>

## <span data-ttu-id="deea3-182">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="deea3-182">RELATED LINKS</span></span>
