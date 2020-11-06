---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: df52a9b690060903affa666d66bfbd2a3afb7aea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493038"
---
# <span data-ttu-id="1ade8-101">Start-AzureRmRecoveryServicesAsrPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="1ade8-101">Start-AzureRmRecoveryServicesAsrPlannedFailoverJob</span></span>

## <span data-ttu-id="1ade8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1ade8-102">SYNOPSIS</span></span>
<span data-ttu-id="1ade8-103">Elindítja a tervezett feladatátvételi műveletet.</span><span class="sxs-lookup"><span data-stu-id="1ade8-103">Starts a planned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ade8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1ade8-104">SYNTAX</span></span>

### <span data-ttu-id="1ade8-105">ByRPIObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1ade8-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1ade8-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="1ade8-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ade8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1ade8-107">DESCRIPTION</span></span>
<span data-ttu-id="1ade8-108">A **Start-AzureRmRecoveryServicesAsrPlannedFailoverJob** parancsmag tervezett feladatátvételt indít az Azure webhely-helyreállítási replikációs szolgáltatással védett elemekkel vagy helyreállítási tervekkel.</span><span class="sxs-lookup"><span data-stu-id="1ade8-108">The **Start-AzureRmRecoveryServicesAsrPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="1ade8-109">Ellenőrizheti, hogy a feladat sikeres volt-e az Get-AzureRmRecoveryServicesAsrJob parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="1ade8-109">You can check whether the job succeeds by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="1ade8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1ade8-110">EXAMPLES</span></span>

### <span data-ttu-id="1ade8-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1ade8-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="1ade8-112">Elindítja a megadott ASR-helyreállítási csomag tervezett feladatátvételét, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="1ade8-112">Starts the planned failover for the specified ASR recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="1ade8-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1ade8-113">PARAMETERS</span></span>

### <span data-ttu-id="1ade8-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1ade8-114">-Confirm</span></span>
<span data-ttu-id="1ade8-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1ade8-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ade8-116">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="1ade8-116">-CreateVmIfNotFound</span></span>
<span data-ttu-id="1ade8-117">A virtuális gépet akkor hozza létre, ha az nem található, miközben nem sikerült visszatérnie az elsődleges területre (a másodlagos helyre való helyreállításban használják). A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="1ade8-117">Create the virtual machine if not found while failing back to the primary region (used in alternate location recovery.) The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1ade8-118">igen</span><span class="sxs-lookup"><span data-stu-id="1ade8-118">Yes</span></span>
- <span data-ttu-id="1ade8-119">nem</span><span class="sxs-lookup"><span data-stu-id="1ade8-119">No</span></span>

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

### <span data-ttu-id="1ade8-120">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="1ade8-120">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="1ade8-121">Az elsődleges tanúsítvány fájlját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ade8-121">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="1ade8-122">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="1ade8-122">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="1ade8-123">A másodlagos tanúsítvány fájlját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ade8-123">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="1ade8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ade8-124">-DefaultProfile</span></span>
<span data-ttu-id="1ade8-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1ade8-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="1ade8-126">-Irány</span><span class="sxs-lookup"><span data-stu-id="1ade8-126">-Direction</span></span>
<span data-ttu-id="1ade8-127">A feladatátvétel irányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ade8-127">Specifies the direction of the failover.</span></span>
<span data-ttu-id="1ade8-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="1ade8-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1ade8-129">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="1ade8-129">PrimaryToRecovery</span></span>
- <span data-ttu-id="1ade8-130">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="1ade8-130">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="1ade8-131">-Optimalizálás</span><span class="sxs-lookup"><span data-stu-id="1ade8-131">-Optimize</span></span>
<span data-ttu-id="1ade8-132">Itt adhatja meg, hogy mit szeretne optimalizálni.</span><span class="sxs-lookup"><span data-stu-id="1ade8-132">Specifies what to optimize for.</span></span>
<span data-ttu-id="1ade8-133">Ez a paraméter akkor érvényes, ha egy Azure-webhelyről egy olyan helyszíni webhelyre végez feladatátvételt, amely jelentős adatszinkronizálást követel meg.</span><span class="sxs-lookup"><span data-stu-id="1ade8-133">This parameter applies when failover is done from an Azure site to an on-premise site which requires substantial data synchronization.</span></span>
<span data-ttu-id="1ade8-134">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="1ade8-134">Valid values are:</span></span>

- <span data-ttu-id="1ade8-135">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="1ade8-135">ForDowntime</span></span>
- <span data-ttu-id="1ade8-136">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="1ade8-136">ForSynchronization</span></span>

<span data-ttu-id="1ade8-137">Ha a **ForDowntime** meg van adva, ez azt jelzi, hogy az adatokat a program szinkronizálja a feladatátvétel minimalizálása előtt.</span><span class="sxs-lookup"><span data-stu-id="1ade8-137">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="1ade8-138">A szinkronizálás a virtuális gép leállítása nélkül végezhető el.</span><span class="sxs-lookup"><span data-stu-id="1ade8-138">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="1ade8-139">Miután befejeződött a szinkronizálás, a program felfüggeszti a feladatot.</span><span class="sxs-lookup"><span data-stu-id="1ade8-139">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="1ade8-140">Folytassa a feladatot, és végezze el a szinkronizálási műveletet, amely leállítja a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="1ade8-140">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="1ade8-141">Ha a **ForSynchronization** meg van adva, ez azt jelzi, hogy az adatok szinkronizálása a feladatátvétel során történik, így az adatok szinkronizálása kisméretű.</span><span class="sxs-lookup"><span data-stu-id="1ade8-141">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="1ade8-142">Ha engedélyezve van ez a beállítás, a virtuális gép azonnal leállt.</span><span class="sxs-lookup"><span data-stu-id="1ade8-142">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="1ade8-143">A szinkronizálás a leállítást követően kezdődik a feladatátvételi művelet befejezéséhez.</span><span class="sxs-lookup"><span data-stu-id="1ade8-143">Synchronization starts after shutdown to complete the failover operation.</span></span>

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

### <span data-ttu-id="1ade8-144">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1ade8-144">-RecoveryPlan</span></span>
<span data-ttu-id="1ade8-145">A helyreállítási tervnek megfelelő ASR helyreállítási terv objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ade8-145">Specifies the ASR Recovery plan object corresponding to the recovery plan to be failed over.</span></span>

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

### <span data-ttu-id="1ade8-146">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1ade8-146">-ReplicationProtectedItem</span></span>
<span data-ttu-id="1ade8-147">Az ASR replikációs szolgáltatással védett elem objektuma, amely a replikációs védelemmel ellátott elemnek felel meg</span><span class="sxs-lookup"><span data-stu-id="1ade8-147">Specifies the ASR replication protected item object corresponding to the replication protected item to be failed over.</span></span>

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

### <span data-ttu-id="1ade8-148">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="1ade8-148">-ServicesProvider</span></span>
<span data-ttu-id="1ade8-149">Annak az állomásnak a neve, amelybe a virtuális gépet létre szeretné hozni, miközben az nem az állomáson futó ASR-szolgáltató objektumnak felel meg.</span><span class="sxs-lookup"><span data-stu-id="1ade8-149">Identifies the host to on which to create the virtual machine while failing over to an alternate location by specifying the ASR services provider object corresponding to the ASR services provider running on the host.</span></span>

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

### <span data-ttu-id="1ade8-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ade8-150">-WhatIf</span></span>
<span data-ttu-id="1ade8-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1ade8-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1ade8-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1ade8-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ade8-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ade8-153">CommonParameters</span></span>
<span data-ttu-id="1ade8-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1ade8-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ade8-155">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ade8-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ade8-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ade8-156">INPUTS</span></span>

### <span data-ttu-id="1ade8-157">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1ade8-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="1ade8-158">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1ade8-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="1ade8-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ade8-159">OUTPUTS</span></span>

### <span data-ttu-id="1ade8-160">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1ade8-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1ade8-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1ade8-161">NOTES</span></span>

## <span data-ttu-id="1ade8-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ade8-162">RELATED LINKS</span></span>
