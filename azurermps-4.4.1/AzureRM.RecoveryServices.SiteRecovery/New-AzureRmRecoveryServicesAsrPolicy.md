---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: a0a55ad071a21f7924eb5a4115a7699fc6690060
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494744"
---
# <span data-ttu-id="64db7-101">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="64db7-101">New-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="64db7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="64db7-102">SYNOPSIS</span></span>
<span data-ttu-id="64db7-103">Azure-webhely-helyreállítási replikációs házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="64db7-103">Creates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64db7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="64db7-104">SYNTAX</span></span>

### <span data-ttu-id="64db7-105">EnterpriseToAzure (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="64db7-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64db7-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="64db7-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy -Name <String> -ReplicationProvider <String> [-ReplicationMethod <String>]
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="64db7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="64db7-107">DESCRIPTION</span></span>
<span data-ttu-id="64db7-108">A **New-AzureRmRecoveryServicesAsrPolicy** parancsmag létrehoz egy Azure-webhely-helyreállítási replikációs házirendet.</span><span class="sxs-lookup"><span data-stu-id="64db7-108">The **New-AzureRmRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="64db7-109">A replikációs házirend segítségével megadhatja a replikációs beállításokat, például a replikációs gyakoriságot és a helyreállítási pontok számát.</span><span class="sxs-lookup"><span data-stu-id="64db7-109">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="64db7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="64db7-110">EXAMPLES</span></span>

### <span data-ttu-id="64db7-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="64db7-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $PolicyName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer
```

<span data-ttu-id="64db7-112">A megadott paraméterekkel elindítja a replikációs házirend-létrehozási műveletet, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="64db7-112">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="64db7-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="64db7-113">PARAMETERS</span></span>

### <span data-ttu-id="64db7-114">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="64db7-114">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="64db7-115">Annak a gyakoriságnak a gyakorisága (óra), amelyben az alkalmazások konzisztens helyreállítási pontja hozható létre.</span><span class="sxs-lookup"><span data-stu-id="64db7-115">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="64db7-116">-Hitelesítés</span><span class="sxs-lookup"><span data-stu-id="64db7-116">-Authentication</span></span>
<span data-ttu-id="64db7-117">A használt hitelesítés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="64db7-117">Specifies the type of authentication used.</span></span>
<span data-ttu-id="64db7-118">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="64db7-118">Valid values are:</span></span>

- <span data-ttu-id="64db7-119">Tanúsítvány</span><span class="sxs-lookup"><span data-stu-id="64db7-119">Certificate</span></span>
-  <span data-ttu-id="64db7-120">Kerberos</span><span class="sxs-lookup"><span data-stu-id="64db7-120">Kerberos</span></span>

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

### <span data-ttu-id="64db7-121">-Tömörítés</span><span class="sxs-lookup"><span data-stu-id="64db7-121">-Compression</span></span>
<span data-ttu-id="64db7-122">Megadja, hogy engedélyezve kell-e a tömörítést.</span><span class="sxs-lookup"><span data-stu-id="64db7-122">Specifies if compression should be enabled.</span></span>

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

### <span data-ttu-id="64db7-123">-Titkosítás</span><span class="sxs-lookup"><span data-stu-id="64db7-123">-Encryption</span></span>
<span data-ttu-id="64db7-124">Megadja, hogy engedélyezve vagy le kell-e kapcsolni a titkosítást.</span><span class="sxs-lookup"><span data-stu-id="64db7-124">Specifies if encryption should be enabled or disabled.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64db7-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="64db7-125">-Name</span></span>
<span data-ttu-id="64db7-126">Az ASR-replikációs házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="64db7-126">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="64db7-127">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="64db7-127">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="64db7-128">A megőrzendő szám-helyreállítási pontok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="64db7-128">Specifies the number recovery points to retain.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64db7-129">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="64db7-129">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="64db7-130">A replikációs cél Azure Storage Account ID azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="64db7-130">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="64db7-131">Akkor használható, ha a cél tárolási fiókja a replikáció, ha az New-AzureRmRecoveryServicesASRReplicationProtectedItem parancsmaggal való engedélyezéskor a rendszer nem ad meg alternatív szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="64db7-131">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64db7-132">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="64db7-132">-ReplicaDeletion</span></span>
<span data-ttu-id="64db7-133">Annak megadása, hogy a virtuális kópiát törölni kell-e a VMM felügyelt webhelyről a másikra történő replikáció letiltásával.</span><span class="sxs-lookup"><span data-stu-id="64db7-133">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

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

### <span data-ttu-id="64db7-134">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="64db7-134">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="64db7-135">A replikációs gyakoriság másodpercben megadott intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="64db7-135">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="64db7-136">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="64db7-136">Valid values are:</span></span>

- <span data-ttu-id="64db7-137">30</span><span class="sxs-lookup"><span data-stu-id="64db7-137">30</span></span>
- <span data-ttu-id="64db7-138">300</span><span class="sxs-lookup"><span data-stu-id="64db7-138">300</span></span>
- <span data-ttu-id="64db7-139">900</span><span class="sxs-lookup"><span data-stu-id="64db7-139">900</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64db7-140">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="64db7-140">-ReplicationMethod</span></span>
<span data-ttu-id="64db7-141">A replikációs módszert adja meg.</span><span class="sxs-lookup"><span data-stu-id="64db7-141">Specifies the replication method.</span></span>
<span data-ttu-id="64db7-142">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="64db7-142">Valid values are:</span></span>

- <span data-ttu-id="64db7-143">Online</span><span class="sxs-lookup"><span data-stu-id="64db7-143">Online</span></span>
- <span data-ttu-id="64db7-144">Offline</span><span class="sxs-lookup"><span data-stu-id="64db7-144">Offline</span></span>

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

### <span data-ttu-id="64db7-145">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="64db7-145">-ReplicationPort</span></span>
<span data-ttu-id="64db7-146">A replikációhoz használt portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="64db7-146">Specifies the port used for replication.</span></span>

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

### <span data-ttu-id="64db7-147">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="64db7-147">-ReplicationProvider</span></span>
<span data-ttu-id="64db7-148">A replikációs szolgáltatót adja meg.</span><span class="sxs-lookup"><span data-stu-id="64db7-148">Specifies the replication provider.</span></span>
<span data-ttu-id="64db7-149">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="64db7-149">Valid values are:</span></span>

- <span data-ttu-id="64db7-150">HyperVReplica2012R2</span><span class="sxs-lookup"><span data-stu-id="64db7-150">HyperVReplica2012R2</span></span>
- <span data-ttu-id="64db7-151">HyperVReplica2012</span><span class="sxs-lookup"><span data-stu-id="64db7-151">HyperVReplica2012</span></span>
- <span data-ttu-id="64db7-152">HyperVReplicaAzure</span><span class="sxs-lookup"><span data-stu-id="64db7-152">HyperVReplicaAzure</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64db7-153">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="64db7-153">-ReplicationStartTime</span></span>
<span data-ttu-id="64db7-154">A replikációs kezdési időpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="64db7-154">Specifies the replication start time.</span></span>
<span data-ttu-id="64db7-155">A feladat elejétől legkésőbb 24 óráig kell szerepelnie.</span><span class="sxs-lookup"><span data-stu-id="64db7-155">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64db7-156">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="64db7-156">-Confirm</span></span>
<span data-ttu-id="64db7-157">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="64db7-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64db7-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64db7-158">-WhatIf</span></span>
<span data-ttu-id="64db7-159">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="64db7-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64db7-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="64db7-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64db7-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64db7-161">CommonParameters</span></span>
<span data-ttu-id="64db7-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="64db7-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64db7-163">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64db7-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64db7-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="64db7-164">INPUTS</span></span>

### <span data-ttu-id="64db7-165">Nincs</span><span class="sxs-lookup"><span data-stu-id="64db7-165">None</span></span>

## <span data-ttu-id="64db7-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64db7-166">OUTPUTS</span></span>

### <span data-ttu-id="64db7-167">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="64db7-167">System.Object</span></span>

## <span data-ttu-id="64db7-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="64db7-168">NOTES</span></span>

## <span data-ttu-id="64db7-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64db7-169">RELATED LINKS</span></span>

[<span data-ttu-id="64db7-170">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="64db7-170">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="64db7-171">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="64db7-171">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
