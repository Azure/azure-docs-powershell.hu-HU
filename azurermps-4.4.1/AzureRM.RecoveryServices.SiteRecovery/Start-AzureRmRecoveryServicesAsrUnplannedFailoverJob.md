---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: 0d619084f62f4cad9b5bd7a9295987681994e53e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679362"
---
# <span data-ttu-id="6a7f9-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="6a7f9-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="6a7f9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6a7f9-102">SYNOPSIS</span></span>
<span data-ttu-id="6a7f9-103">Nem tervezett feladatátvételi műveletet indít el.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-103">Starts an unplanned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a7f9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6a7f9-104">SYNTAX</span></span>

### <span data-ttu-id="6a7f9-105">ByRPIObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6a7f9-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a7f9-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="6a7f9-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a7f9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6a7f9-107">DESCRIPTION</span></span>
<span data-ttu-id="6a7f9-108">A **Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob** parancsmag az Azure webhely-helyreállítási replikációs szolgáltatással védett elemek vagy helyreállítási terv nem tervezett feladatátvételét indítja el.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-108">The **Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="6a7f9-109">Ellenőrizheti, hogy a feladat sikeres volt-e az Get-AzureRmRecoveryServicesAsrJob parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-109">You can check whether the job succeeds by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="6a7f9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6a7f9-110">EXAMPLES</span></span>

### <span data-ttu-id="6a7f9-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6a7f9-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="6a7f9-112">Elindítja a meghatározott helyreállítási terv nem tervezett feladatátvételi műveletét a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-112">Starts the unplanned failover operation for the specified recovery plan using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="6a7f9-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6a7f9-113">PARAMETERS</span></span>

### <span data-ttu-id="6a7f9-114">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="6a7f9-114">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="6a7f9-115">Az elsődleges tanúsítvány fájlját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-115">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="6a7f9-116">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="6a7f9-116">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="6a7f9-117">A másodlagos tanúsítvány fájlját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-117">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="6a7f9-118">-Irány</span><span class="sxs-lookup"><span data-stu-id="6a7f9-118">-Direction</span></span>
<span data-ttu-id="6a7f9-119">A feladatátvétel irányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-119">Specifies the direction of the failover.</span></span>
<span data-ttu-id="6a7f9-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="6a7f9-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6a7f9-121">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="6a7f9-121">PrimaryToRecovery</span></span>
- <span data-ttu-id="6a7f9-122">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="6a7f9-122">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="6a7f9-123">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="6a7f9-123">-PerformSourceSideAction</span></span>
<span data-ttu-id="6a7f9-124">Azt jelzi, hogy a helyreállítási tervben megadott bármely forrású webhelyet meg kell ismételni a feladatátvétel részeként.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-124">Indicates that any source site operations specified in the recovery plan must be attempted to be performed as part of the fail over.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: PerformSourceSideActions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a7f9-125">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6a7f9-125">-RecoveryPlan</span></span>
<span data-ttu-id="6a7f9-126">Egy olyan ASR-helyreállítási terv objektumot ad meg, amely megfelel annak a helyreállítási tervnek, amelyen a feladatátvételi műveletet végre kell hajtani.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-126">Specifies an ASR recovery plan object corresponding to the recovery plan on which the failover operation is to be performed.</span></span>

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

### <span data-ttu-id="6a7f9-127">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6a7f9-127">-ReplicationProtectedItem</span></span>
<span data-ttu-id="6a7f9-128">Az ASR replikációs szolgáltatással védett elem objektuma, amely megfelel annak a replikációs védelemmel ellátott elemnek, amelyen a feladatátvételi műveletet végre kell hajtani.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-128">Specifies the ASR replication protected item object corresponding to the replication protected item on which the failover operation is to be performed.</span></span>

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

### <span data-ttu-id="6a7f9-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6a7f9-129">-Confirm</span></span>
<span data-ttu-id="6a7f9-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a7f9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a7f9-131">-WhatIf</span></span>
<span data-ttu-id="6a7f9-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6a7f9-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6a7f9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a7f9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a7f9-134">CommonParameters</span></span>
<span data-ttu-id="6a7f9-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6a7f9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a7f9-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a7f9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a7f9-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a7f9-137">INPUTS</span></span>

### <span data-ttu-id="6a7f9-138">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6a7f9-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="6a7f9-139">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6a7f9-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="6a7f9-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a7f9-140">OUTPUTS</span></span>

### <span data-ttu-id="6a7f9-141">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="6a7f9-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6a7f9-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6a7f9-142">NOTES</span></span>

## <span data-ttu-id="6a7f9-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a7f9-143">RELATED LINKS</span></span>

[<span data-ttu-id="6a7f9-144">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="6a7f9-144">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)


