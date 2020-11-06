---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 302b781ee6af68cb960ab01668147edc56e04284
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501667"
---
# <span data-ttu-id="bb8f1-101">Update-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="bb8f1-101">Update-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="bb8f1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bb8f1-102">SYNOPSIS</span></span>
<span data-ttu-id="bb8f1-103">Az Azure-webhely helyreállítási replikációs házirendjének frissítése</span><span class="sxs-lookup"><span data-stu-id="bb8f1-103">Updates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb8f1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bb8f1-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb8f1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bb8f1-105">DESCRIPTION</span></span>
<span data-ttu-id="bb8f1-106">Az **Update-AzureRmRecoveryServicesAsrPolicy** parancsmag frissíti a megadott Azure-webhely-helyreállítási replikációs házirendet.</span><span class="sxs-lookup"><span data-stu-id="bb8f1-106">The **Update-AzureRmRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="bb8f1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bb8f1-107">EXAMPLES</span></span>

### <span data-ttu-id="bb8f1-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bb8f1-108">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="bb8f1-109">Elindítja az Update replikációs házirend-műveletet a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="bb8f1-109">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="bb8f1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bb8f1-110">PARAMETERS</span></span>

### <span data-ttu-id="bb8f1-111">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="bb8f1-111">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="bb8f1-112">Annak a gyakoriságnak a gyakorisága (óra), amelyben az alkalmazások konzisztens helyreállítási pontja hozható létre.</span><span class="sxs-lookup"><span data-stu-id="bb8f1-112">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="bb8f1-113">-Hitelesítés</span><span class="sxs-lookup"><span data-stu-id="bb8f1-113">-Authentication</span></span>
<span data-ttu-id="bb8f1-114">A használt hitelesítés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb8f1-114">Specifies the type of authentication used.</span></span>
<span data-ttu-id="bb8f1-115">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="bb8f1-115">Valid values are:</span></span>

- <span data-ttu-id="bb8f1-116">Tanúsítvány</span><span class="sxs-lookup"><span data-stu-id="bb8f1-116">Certificate</span></span>
-  <span data-ttu-id="bb8f1-117">Kerberos</span><span class="sxs-lookup"><span data-stu-id="bb8f1-117">Kerberos</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb8f1-118">-Tömörítés</span><span class="sxs-lookup"><span data-stu-id="bb8f1-118">-Compression</span></span>
<span data-ttu-id="bb8f1-119">Megadja, hogy engedélyezve kell-e a tömörítést.</span><span class="sxs-lookup"><span data-stu-id="bb8f1-119">Specifies if compression should be enabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb8f1-120">-Titkosítás</span><span class="sxs-lookup"><span data-stu-id="bb8f1-120">-Encryption</span></span>
<span data-ttu-id="bb8f1-121">Megadja, hogy engedélyezve vagy le kell-e kapcsolni a titkosítást.</span><span class="sxs-lookup"><span data-stu-id="bb8f1-121">Specifies if encryption should be enabled or disabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb8f1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb8f1-122">-InputObject</span></span>
<span data-ttu-id="bb8f1-123">A parancsmag bemeneti objektuma: Itt adhatja meg az ASR replikációs házirend-objektumát, amely megfelel a frissítendő replikációs házirendnek.</span><span class="sxs-lookup"><span data-stu-id="bb8f1-123">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

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

### <span data-ttu-id="bb8f1-124">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="bb8f1-124">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="bb8f1-125">A megőrzendő szám-helyreállítási pontok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb8f1-125">Specifies the number recovery points to retain.</span></span>

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

### <span data-ttu-id="bb8f1-126">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="bb8f1-126">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="bb8f1-127">A replikációs cél Azure Storage Account ID azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb8f1-127">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="bb8f1-128">Akkor használható, ha a cél tárolási fiókja a replikáció, ha az New-AzureRmRecoveryServicesASRReplicationProtectedItem parancsmaggal való engedélyezéskor a rendszer nem ad meg alternatív szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="bb8f1-128">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb8f1-129">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="bb8f1-129">-ReplicaDeletion</span></span>
<span data-ttu-id="bb8f1-130">Annak megadása, hogy a virtuális kópiát törölni kell-e a VMM felügyelt webhelyről a másikra történő replikáció letiltásával.</span><span class="sxs-lookup"><span data-stu-id="bb8f1-130">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb8f1-131">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="bb8f1-131">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="bb8f1-132">A replikációs gyakoriság másodpercben megadott intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb8f1-132">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="bb8f1-133">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="bb8f1-133">Valid values are:</span></span>

- <span data-ttu-id="bb8f1-134">30</span><span class="sxs-lookup"><span data-stu-id="bb8f1-134">30</span></span>
- <span data-ttu-id="bb8f1-135">300</span><span class="sxs-lookup"><span data-stu-id="bb8f1-135">300</span></span>
- <span data-ttu-id="bb8f1-136">900</span><span class="sxs-lookup"><span data-stu-id="bb8f1-136">900</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb8f1-137">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="bb8f1-137">-ReplicationMethod</span></span>
<span data-ttu-id="bb8f1-138">A replikációs módszert adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb8f1-138">Specifies the replication method.</span></span>
<span data-ttu-id="bb8f1-139">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="bb8f1-139">Valid values are:</span></span>

- <span data-ttu-id="bb8f1-140">Online</span><span class="sxs-lookup"><span data-stu-id="bb8f1-140">Online</span></span>
- <span data-ttu-id="bb8f1-141">Offline</span><span class="sxs-lookup"><span data-stu-id="bb8f1-141">Offline</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb8f1-142">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="bb8f1-142">-ReplicationPort</span></span>
<span data-ttu-id="bb8f1-143">A replikációhoz használt portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb8f1-143">Specifies the port used for replication.</span></span>

```yaml
Type: UInt16
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb8f1-144">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="bb8f1-144">-ReplicationStartTime</span></span>
<span data-ttu-id="bb8f1-145">A replikációs kezdési időpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb8f1-145">Specifies the replication start time.</span></span>
<span data-ttu-id="bb8f1-146">A feladat elejétől legkésőbb 24 óráig kell szerepelnie.</span><span class="sxs-lookup"><span data-stu-id="bb8f1-146">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="bb8f1-147">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bb8f1-147">-Confirm</span></span>
<span data-ttu-id="bb8f1-148">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bb8f1-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb8f1-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb8f1-149">-WhatIf</span></span>
<span data-ttu-id="bb8f1-150">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bb8f1-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb8f1-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bb8f1-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb8f1-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb8f1-152">CommonParameters</span></span>
<span data-ttu-id="bb8f1-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bb8f1-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb8f1-154">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb8f1-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb8f1-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb8f1-155">INPUTS</span></span>

### <span data-ttu-id="bb8f1-156">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="bb8f1-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="bb8f1-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb8f1-157">OUTPUTS</span></span>

### <span data-ttu-id="bb8f1-158">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="bb8f1-158">System.Object</span></span>

## <span data-ttu-id="bb8f1-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bb8f1-159">NOTES</span></span>

## <span data-ttu-id="bb8f1-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bb8f1-160">RELATED LINKS</span></span>

