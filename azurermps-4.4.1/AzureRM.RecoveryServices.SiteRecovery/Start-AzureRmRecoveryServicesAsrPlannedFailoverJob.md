---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: e96a57a00d6314015d1d13f4f540d3f763c96c23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494728"
---
# <span data-ttu-id="94b0e-101">Start-AzureRmRecoveryServicesAsrPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="94b0e-101">Start-AzureRmRecoveryServicesAsrPlannedFailoverJob</span></span>

## <span data-ttu-id="94b0e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="94b0e-102">SYNOPSIS</span></span>
<span data-ttu-id="94b0e-103">Elindítja a tervezett feladatátvételi műveletet.</span><span class="sxs-lookup"><span data-stu-id="94b0e-103">Starts a planned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94b0e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="94b0e-104">SYNTAX</span></span>

### <span data-ttu-id="94b0e-105">ByRPIObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="94b0e-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94b0e-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="94b0e-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94b0e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="94b0e-107">DESCRIPTION</span></span>
<span data-ttu-id="94b0e-108">A **Start-AzureRmRecoveryServicesAsrPlannedFailoverJob** parancsmag tervezett feladatátvételt indít az Azure webhely-helyreállítási replikációs szolgáltatással védett elemekkel vagy helyreállítási tervekkel.</span><span class="sxs-lookup"><span data-stu-id="94b0e-108">The **Start-AzureRmRecoveryServicesAsrPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="94b0e-109">Ellenőrizheti, hogy a feladat sikeres volt-e az Get-AzureRmRecoveryServicesAsrJob parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="94b0e-109">You can check whether the job succeeds by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="94b0e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="94b0e-110">EXAMPLES</span></span>

### <span data-ttu-id="94b0e-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="94b0e-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="94b0e-112">Elindítja a megadott ASR-helyreállítási csomag tervezett feladatátvételét, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="94b0e-112">Starts the planned failover for the specified ASR recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="94b0e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="94b0e-113">PARAMETERS</span></span>

### <span data-ttu-id="94b0e-114">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="94b0e-114">-CreateVmIfNotFound</span></span>
<span data-ttu-id="94b0e-115">A virtuális gépet akkor hozza létre, ha az nem található, miközben nem sikerült visszatérnie az elsődleges területre (a másodlagos helyre való helyreállításban használják). A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="94b0e-115">Create the virtual machine if not found while failing back to the primary region (used in alternate location recovery.) The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="94b0e-116">igen</span><span class="sxs-lookup"><span data-stu-id="94b0e-116">Yes</span></span>
- <span data-ttu-id="94b0e-117">nem</span><span class="sxs-lookup"><span data-stu-id="94b0e-117">No</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Yes, No

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94b0e-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="94b0e-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="94b0e-119">Az elsődleges tanúsítvány fájlját adja meg.</span><span class="sxs-lookup"><span data-stu-id="94b0e-119">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="94b0e-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="94b0e-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="94b0e-121">A másodlagos tanúsítvány fájlját adja meg.</span><span class="sxs-lookup"><span data-stu-id="94b0e-121">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="94b0e-122">-Irány</span><span class="sxs-lookup"><span data-stu-id="94b0e-122">-Direction</span></span>
<span data-ttu-id="94b0e-123">A feladatátvétel irányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="94b0e-123">Specifies the direction of the failover.</span></span>
<span data-ttu-id="94b0e-124">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="94b0e-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="94b0e-125">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="94b0e-125">PrimaryToRecovery</span></span>
- <span data-ttu-id="94b0e-126">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="94b0e-126">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94b0e-127">-Optimalizálás</span><span class="sxs-lookup"><span data-stu-id="94b0e-127">-Optimize</span></span>
<span data-ttu-id="94b0e-128">Itt adhatja meg, hogy mit szeretne optimalizálni.</span><span class="sxs-lookup"><span data-stu-id="94b0e-128">Specifies what to optimize for.</span></span>
<span data-ttu-id="94b0e-129">Ez a paraméter akkor érvényes, ha egy Azure-webhelyről olyan helyszíni webhelyre végez feladatátvételt, amely jelentős adatszinkronizálást követel meg.</span><span class="sxs-lookup"><span data-stu-id="94b0e-129">This parameter applies when failover is done from an Azure site to an on-premise site which requires a substantial data synchronization.</span></span>
<span data-ttu-id="94b0e-130">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="94b0e-130">Valid values are:</span></span>

- <span data-ttu-id="94b0e-131">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="94b0e-131">ForDowntime</span></span>
- <span data-ttu-id="94b0e-132">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="94b0e-132">ForSynchronization</span></span>

<span data-ttu-id="94b0e-133">Ha a **ForDowntime** meg van adva, ez azt jelzi, hogy az adatokat a program szinkronizálja a feladatátvétel minimalizálása előtt.</span><span class="sxs-lookup"><span data-stu-id="94b0e-133">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="94b0e-134">A szinkronizálás a virtuális gép leállítása nélkül végezhető el.</span><span class="sxs-lookup"><span data-stu-id="94b0e-134">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="94b0e-135">Miután befejeződött a szinkronizálás, a program felfüggeszti a feladatot.</span><span class="sxs-lookup"><span data-stu-id="94b0e-135">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="94b0e-136">Folytassa a feladatot, és végezze el a szinkronizálási műveletet, amely leállítja a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="94b0e-136">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="94b0e-137">Ha a **ForSynchronization** meg van adva, ez azt jelzi, hogy az adatok szinkronizálása a feladatátvétel során történik, így az adatok szinkronizálása kisméretű.</span><span class="sxs-lookup"><span data-stu-id="94b0e-137">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="94b0e-138">Ha engedélyezve van ez a beállítás, a virtuális gép azonnal leállt.</span><span class="sxs-lookup"><span data-stu-id="94b0e-138">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="94b0e-139">A szinkronizálás a leállítást követően kezdődik a feladatátvételi művelet befejezéséhez.</span><span class="sxs-lookup"><span data-stu-id="94b0e-139">Synchronization starts after shutdown to complete the failover operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: ForDownTime, ForSynchronization

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94b0e-140">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="94b0e-140">-RecoveryPlan</span></span>
<span data-ttu-id="94b0e-141">A helyreállítási tervnek megfelelő ASR helyreállítási terv objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="94b0e-141">Specifies the ASR Recovery plan object corresponding to the recovery plan to be failed over.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94b0e-142">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="94b0e-142">-ReplicationProtectedItem</span></span>
<span data-ttu-id="94b0e-143">Az ASR replikációs szolgáltatással védett elem objektuma, amely a replikációs védelemmel ellátott elemnek felel meg</span><span class="sxs-lookup"><span data-stu-id="94b0e-143">Specifies the ASR replication protected item object corresponding to the replication protected item to be failed over.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94b0e-144">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="94b0e-144">-ServicesProvider</span></span>
<span data-ttu-id="94b0e-145">Annak az állomásnak a neve, amelybe a virtuális gépet létre szeretné hozni, miközben az nem az állomáson futó ASR-szolgáltató objektumnak felel meg.</span><span class="sxs-lookup"><span data-stu-id="94b0e-145">Identifies the host to on which to create the virtual machine while failing over to an alternate location by specifying the ASR services provider object corresponding to the ASR services provider running on the host.</span></span> 

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94b0e-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="94b0e-146">-Confirm</span></span>
<span data-ttu-id="94b0e-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="94b0e-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94b0e-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94b0e-148">-WhatIf</span></span>
<span data-ttu-id="94b0e-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="94b0e-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94b0e-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="94b0e-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94b0e-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94b0e-151">CommonParameters</span></span>
<span data-ttu-id="94b0e-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="94b0e-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94b0e-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94b0e-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94b0e-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="94b0e-154">INPUTS</span></span>

### <span data-ttu-id="94b0e-155">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="94b0e-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="94b0e-156">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="94b0e-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="94b0e-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94b0e-157">OUTPUTS</span></span>

### <span data-ttu-id="94b0e-158">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="94b0e-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="94b0e-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="94b0e-159">NOTES</span></span>

## <span data-ttu-id="94b0e-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94b0e-160">RELATED LINKS</span></span>

