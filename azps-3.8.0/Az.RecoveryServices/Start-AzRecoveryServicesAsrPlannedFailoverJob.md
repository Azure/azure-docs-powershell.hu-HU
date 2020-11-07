---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: e5864271e96add95624f857357defdea3039c7a8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846962"
---
# <span data-ttu-id="f22f9-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="f22f9-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span></span>

## <span data-ttu-id="f22f9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f22f9-102">SYNOPSIS</span></span>
<span data-ttu-id="f22f9-103">Elindítja a tervezett feladatátvételi műveletet.</span><span class="sxs-lookup"><span data-stu-id="f22f9-103">Starts a planned failover operation.</span></span>

## <span data-ttu-id="f22f9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f22f9-104">SYNTAX</span></span>

### <span data-ttu-id="f22f9-105">ByRPIObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f22f9-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f22f9-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="f22f9-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f22f9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f22f9-107">DESCRIPTION</span></span>
<span data-ttu-id="f22f9-108">A **Start-AzRecoveryServicesAsrPlannedFailoverJob** parancsmag tervezett feladatátvételt indít az Azure webhely-helyreállítási replikációs szolgáltatással védett elemekkel vagy helyreállítási tervekkel.</span><span class="sxs-lookup"><span data-stu-id="f22f9-108">The **Start-AzRecoveryServicesAsrPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="f22f9-109">Ellenőrizheti, hogy a feladat sikeres volt-e az Get-AzRecoveryServicesAsrJob parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="f22f9-109">You can check whether the job succeeds by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="f22f9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f22f9-110">EXAMPLES</span></span>

### <span data-ttu-id="f22f9-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f22f9-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="f22f9-112">Elindítja a megadott ASR-helyreállítási csomag tervezett feladatátvételét, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="f22f9-112">Starts the planned failover for the specified ASR recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f22f9-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f22f9-113">PARAMETERS</span></span>

### <span data-ttu-id="f22f9-114">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="f22f9-114">-CreateVmIfNotFound</span></span>
<span data-ttu-id="f22f9-115">A virtuális gépet akkor hozza létre, ha az nem található, miközben nem sikerült visszatérnie az elsődleges területre (a másodlagos helyre való helyreállításban használják). A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f22f9-115">Create the virtual machine if not found while failing back to the primary region (used in alternate location recovery.) The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f22f9-116">igen</span><span class="sxs-lookup"><span data-stu-id="f22f9-116">Yes</span></span>
- <span data-ttu-id="f22f9-117">nem</span><span class="sxs-lookup"><span data-stu-id="f22f9-117">No</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Yes, No

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f22f9-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="f22f9-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="f22f9-119">Az elsődleges tanúsítvány fájlját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f22f9-119">Specifies the primary certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f22f9-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="f22f9-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="f22f9-121">A másodlagos tanúsítvány fájlját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f22f9-121">Specifies the secondary certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f22f9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f22f9-122">-DefaultProfile</span></span>
<span data-ttu-id="f22f9-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f22f9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f22f9-124">-Irány</span><span class="sxs-lookup"><span data-stu-id="f22f9-124">-Direction</span></span>
<span data-ttu-id="f22f9-125">A feladatátvétel irányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f22f9-125">Specifies the direction of the failover.</span></span>
<span data-ttu-id="f22f9-126">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f22f9-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f22f9-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="f22f9-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="f22f9-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="f22f9-128">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f22f9-129">-Optimalizálás</span><span class="sxs-lookup"><span data-stu-id="f22f9-129">-Optimize</span></span>
<span data-ttu-id="f22f9-130">Itt adhatja meg, hogy mit szeretne optimalizálni.</span><span class="sxs-lookup"><span data-stu-id="f22f9-130">Specifies what to optimize for.</span></span>
<span data-ttu-id="f22f9-131">Ez a paraméter akkor érvényes, ha egy Azure-webhelyről egy olyan helyszíni webhelyre végez feladatátvételt, amely jelentős adatszinkronizálást követel meg.</span><span class="sxs-lookup"><span data-stu-id="f22f9-131">This parameter applies when failover is done from an Azure site to an on-premise site which requires substantial data synchronization.</span></span>
<span data-ttu-id="f22f9-132">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="f22f9-132">Valid values are:</span></span>

- <span data-ttu-id="f22f9-133">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="f22f9-133">ForDowntime</span></span>
- <span data-ttu-id="f22f9-134">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="f22f9-134">ForSynchronization</span></span>

<span data-ttu-id="f22f9-135">Ha a **ForDowntime** meg van adva, ez azt jelzi, hogy az adatokat a program szinkronizálja a feladatátvétel minimalizálása előtt.</span><span class="sxs-lookup"><span data-stu-id="f22f9-135">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="f22f9-136">A szinkronizálás a virtuális gép leállítása nélkül végezhető el.</span><span class="sxs-lookup"><span data-stu-id="f22f9-136">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="f22f9-137">Miután befejeződött a szinkronizálás, a program felfüggeszti a feladatot.</span><span class="sxs-lookup"><span data-stu-id="f22f9-137">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="f22f9-138">Folytassa a feladatot, és végezze el a szinkronizálási műveletet, amely leállítja a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="f22f9-138">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="f22f9-139">Ha a **ForSynchronization** meg van adva, ez azt jelzi, hogy az adatok szinkronizálása a feladatátvétel során történik, így az adatok szinkronizálása kisméretű.</span><span class="sxs-lookup"><span data-stu-id="f22f9-139">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="f22f9-140">Ha engedélyezve van ez a beállítás, a virtuális gép azonnal leállt.</span><span class="sxs-lookup"><span data-stu-id="f22f9-140">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="f22f9-141">A szinkronizálás a leállítást követően kezdődik a feladatátvételi művelet befejezéséhez.</span><span class="sxs-lookup"><span data-stu-id="f22f9-141">Synchronization starts after shutdown to complete the failover operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ForDownTime, ForSynchronization

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f22f9-142">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f22f9-142">-RecoveryPlan</span></span>
<span data-ttu-id="f22f9-143">A helyreállítási tervnek megfelelő ASR helyreállítási terv objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f22f9-143">Specifies the ASR Recovery plan object corresponding to the recovery plan to be failed over.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f22f9-144">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f22f9-144">-ReplicationProtectedItem</span></span>
<span data-ttu-id="f22f9-145">Az ASR replikációs szolgáltatással védett elem objektuma, amely a replikációs védelemmel ellátott elemnek felel meg</span><span class="sxs-lookup"><span data-stu-id="f22f9-145">Specifies the ASR replication protected item object corresponding to the replication protected item to be failed over.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f22f9-146">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="f22f9-146">-ServicesProvider</span></span>
<span data-ttu-id="f22f9-147">Annak az állomásnak a neve, amelybe a virtuális gépet létre szeretné hozni, miközben az nem az állomáson futó ASR-szolgáltató objektumnak felel meg.</span><span class="sxs-lookup"><span data-stu-id="f22f9-147">Identifies the host to on which to create the virtual machine while failing over to an alternate location by specifying the ASR services provider object corresponding to the ASR services provider running on the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f22f9-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f22f9-148">-Confirm</span></span>
<span data-ttu-id="f22f9-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f22f9-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f22f9-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f22f9-150">-WhatIf</span></span>
<span data-ttu-id="f22f9-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f22f9-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f22f9-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f22f9-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f22f9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f22f9-153">CommonParameters</span></span>
<span data-ttu-id="f22f9-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f22f9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f22f9-155">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f22f9-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f22f9-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f22f9-156">INPUTS</span></span>

### <span data-ttu-id="f22f9-157">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f22f9-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="f22f9-158">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f22f9-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="f22f9-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f22f9-159">OUTPUTS</span></span>

### <span data-ttu-id="f22f9-160">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f22f9-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f22f9-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f22f9-161">NOTES</span></span>

## <span data-ttu-id="f22f9-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f22f9-162">RELATED LINKS</span></span>
