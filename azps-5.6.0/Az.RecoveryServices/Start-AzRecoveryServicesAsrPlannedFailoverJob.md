---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/start-azrecoveryservicesasrplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: 78aa310d6fd3cdb7a27de066e234744b3e450520
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000965"
---
# <span data-ttu-id="6eb63-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="6eb63-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span></span>

## <span data-ttu-id="6eb63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6eb63-102">SYNOPSIS</span></span>
<span data-ttu-id="6eb63-103">Tervezett feladatátvételi műveletet kezd.</span><span class="sxs-lookup"><span data-stu-id="6eb63-103">Starts a planned failover operation.</span></span>

## <span data-ttu-id="6eb63-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6eb63-104">SYNTAX</span></span>

### <span data-ttu-id="6eb63-105">ByRPIObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6eb63-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6eb63-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="6eb63-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6eb63-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6eb63-107">DESCRIPTION</span></span>
<span data-ttu-id="6eb63-108">A **Start-AzRecoveryServicesAsrPlannedFailoverService parancsmag** elindítja az Azure-webhely-helyreállítási replikációval védett elem vagy helyreállítási terv tervezett feladatátvételét.</span><span class="sxs-lookup"><span data-stu-id="6eb63-108">The **Start-AzRecoveryServicesAsrPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="6eb63-109">A feladat sikeres voltának ellenőrzéséhez használja a Get-AzRecoveryServicesAsrJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6eb63-109">You can check whether the job succeeds by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="6eb63-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6eb63-110">EXAMPLES</span></span>

### <span data-ttu-id="6eb63-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="6eb63-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="6eb63-112">Elindítja a megadott ASR helyreállítási terv tervezett feladatátvételét, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="6eb63-112">Starts the planned failover for the specified ASR recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="6eb63-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6eb63-113">PARAMETERS</span></span>

### <span data-ttu-id="6eb63-114">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="6eb63-114">-CreateVmIfNotFound</span></span>
<span data-ttu-id="6eb63-115">Hozza létre a virtuális gépet, ha nem található meg, miközben nem áll vissza az elsődleges régióba (alternatív hely-helyreállításban használva).) A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="6eb63-115">Create the virtual machine if not found while failing back to the primary region (used in alternate location recovery.) The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6eb63-116">igen</span><span class="sxs-lookup"><span data-stu-id="6eb63-116">Yes</span></span>
- <span data-ttu-id="6eb63-117">nem</span><span class="sxs-lookup"><span data-stu-id="6eb63-117">No</span></span>

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

### <span data-ttu-id="6eb63-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="6eb63-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="6eb63-119">Az elsődleges tanúsítványfájlt adja meg.</span><span class="sxs-lookup"><span data-stu-id="6eb63-119">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="6eb63-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="6eb63-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="6eb63-121">A másodlagos tanúsítványfájlt adja meg.</span><span class="sxs-lookup"><span data-stu-id="6eb63-121">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="6eb63-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eb63-122">-DefaultProfile</span></span>
<span data-ttu-id="6eb63-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6eb63-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6eb63-124">-Irány</span><span class="sxs-lookup"><span data-stu-id="6eb63-124">-Direction</span></span>
<span data-ttu-id="6eb63-125">A feladatátvétel irányát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="6eb63-125">Specifies the direction of the failover.</span></span>
<span data-ttu-id="6eb63-126">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="6eb63-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6eb63-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="6eb63-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="6eb63-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="6eb63-128">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="6eb63-129">- Optimalizálás</span><span class="sxs-lookup"><span data-stu-id="6eb63-129">-Optimize</span></span>
<span data-ttu-id="6eb63-130">Meghatározza, hogy mire optimalizálható.</span><span class="sxs-lookup"><span data-stu-id="6eb63-130">Specifies what to optimize for.</span></span>
<span data-ttu-id="6eb63-131">Ez a paraméter akkor érvényes, ha egy Azure-webhelyről egy helyszíni webhelyre történik feladatátvétel, amely jelentős adatszinkronizálást igényel.</span><span class="sxs-lookup"><span data-stu-id="6eb63-131">This parameter applies when failover is done from an Azure site to an on-premise site which requires substantial data synchronization.</span></span>
<span data-ttu-id="6eb63-132">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="6eb63-132">Valid values are:</span></span>

- <span data-ttu-id="6eb63-133">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="6eb63-133">ForDowntime</span></span>
- <span data-ttu-id="6eb63-134">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="6eb63-134">ForSynchronization</span></span>

<span data-ttu-id="6eb63-135">Ha **a ForDowntime** meg van adva, az azt jelenti, hogy a rendszer a feladatátvétel előtt szinkronizálja az adatokat, hogy minimalizálja a leállást.</span><span class="sxs-lookup"><span data-stu-id="6eb63-135">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="6eb63-136">A szinkronizálás a virtuális gép leállítása nélkül történik.</span><span class="sxs-lookup"><span data-stu-id="6eb63-136">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="6eb63-137">A szinkronizálás befejezése után a feladat fel van függesztve.</span><span class="sxs-lookup"><span data-stu-id="6eb63-137">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="6eb63-138">Folytassa a feladatot egy további szinkronizálási művelettel, amely leállíthatja a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="6eb63-138">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="6eb63-139">Ha meg van adva a **ForSynchronization** tulajdonság, az azt jelenti, hogy az adatok szinkronizálása csak feladatátvételkor történik meg, így az adatszinkronizálás kis méretűre van adva.</span><span class="sxs-lookup"><span data-stu-id="6eb63-139">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="6eb63-140">Ha ez a beállítás engedélyezve van, a virtuális gép azonnal leáll.</span><span class="sxs-lookup"><span data-stu-id="6eb63-140">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="6eb63-141">A szinkronizálás a leállítás után elindul a feladatátvételi művelet befejezéséhez.</span><span class="sxs-lookup"><span data-stu-id="6eb63-141">Synchronization starts after shutdown to complete the failover operation.</span></span>

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

### <span data-ttu-id="6eb63-142">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6eb63-142">-RecoveryPlan</span></span>
<span data-ttu-id="6eb63-143">Azt az ASR helyreállítási tervobjektumot adja meg, amely megfelel a helyreállítási terv meghiúsulási tervének.</span><span class="sxs-lookup"><span data-stu-id="6eb63-143">Specifies the ASR Recovery plan object corresponding to the recovery plan to be failed over.</span></span>

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

### <span data-ttu-id="6eb63-144">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6eb63-144">-ReplicationProtectedItem</span></span>
<span data-ttu-id="6eb63-145">A replikálás által védett elem asR-rel védett objektumának megadása, amely megfelel annak a replikációval védett elemnek, amelyről sikertelenül kell leírni a elemet.</span><span class="sxs-lookup"><span data-stu-id="6eb63-145">Specifies the ASR replication protected item object corresponding to the replication protected item to be failed over.</span></span>

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

### <span data-ttu-id="6eb63-146">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="6eb63-146">-ServicesProvider</span></span>
<span data-ttu-id="6eb63-147">Azonosítja azt az állomást, amelyen létre kell hoznia a virtuális gépet, miközben másik helyre kell átesni, az adott állomáson futó ASR-szolgáltatóhoz tartozó ASR-szolgáltató objektum megadásával.</span><span class="sxs-lookup"><span data-stu-id="6eb63-147">Identifies the host to on which to create the virtual machine while failing over to an alternate location by specifying the ASR services provider object corresponding to the ASR services provider running on the host.</span></span>

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

### <span data-ttu-id="6eb63-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6eb63-148">-Confirm</span></span>
<span data-ttu-id="6eb63-149">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6eb63-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6eb63-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6eb63-150">-WhatIf</span></span>
<span data-ttu-id="6eb63-151">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6eb63-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6eb63-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6eb63-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6eb63-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eb63-153">CommonParameters</span></span>
<span data-ttu-id="6eb63-154">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6eb63-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eb63-155">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6eb63-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eb63-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6eb63-156">INPUTS</span></span>

### <span data-ttu-id="6eb63-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6eb63-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="6eb63-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6eb63-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="6eb63-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6eb63-159">OUTPUTS</span></span>

### <span data-ttu-id="6eb63-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="6eb63-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6eb63-161">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6eb63-161">NOTES</span></span>

## <span data-ttu-id="6eb63-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6eb63-162">RELATED LINKS</span></span>
