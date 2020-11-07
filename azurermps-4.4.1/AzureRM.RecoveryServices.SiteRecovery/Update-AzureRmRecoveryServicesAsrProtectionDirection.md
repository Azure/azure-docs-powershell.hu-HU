---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: afa5da5a34954c1e1a610ce9153172934069c2a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679356"
---
# <span data-ttu-id="07a15-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="07a15-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="07a15-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="07a15-102">SYNOPSIS</span></span>
<span data-ttu-id="07a15-103">Frissíti a megadott replikációs védett elem vagy helyreállítási terv replikációs irányát.</span><span class="sxs-lookup"><span data-stu-id="07a15-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="07a15-104">A replikált elem vagy helyreállítási terv ismételt védelméhez/visszavonásához használható.</span><span class="sxs-lookup"><span data-stu-id="07a15-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07a15-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="07a15-105">SYNTAX</span></span>

### <span data-ttu-id="07a15-106">ByRPIObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="07a15-106">ByRPIObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07a15-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="07a15-107">ByRPObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07a15-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="07a15-108">ByPEObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -Direction <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="07a15-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="07a15-109">DESCRIPTION</span></span>
<span data-ttu-id="07a15-110">Az **Update-AzureRmRecoveryServicesAsrProtectionDirection** parancsmag a megadott Azure-webhely helyreállítási objektumának replikációs irányát frissíti a véglegesítést követő feladatátvételi művelet befejezése után.</span><span class="sxs-lookup"><span data-stu-id="07a15-110">The **Update-AzureRmRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="07a15-111">Példák</span><span class="sxs-lookup"><span data-stu-id="07a15-111">EXAMPLES</span></span>

### <span data-ttu-id="07a15-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="07a15-112">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="07a15-113">Indítsa el a megadott recoveyr-csomag frissítési irányát, és adja meg a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="07a15-113">Start the update direction operation for the specified recoveyr plan and returns the ASR job object used to track the operation.</span></span>

## <span data-ttu-id="07a15-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="07a15-114">PARAMETERS</span></span>

### <span data-ttu-id="07a15-115">-Irány</span><span class="sxs-lookup"><span data-stu-id="07a15-115">-Direction</span></span>
<span data-ttu-id="07a15-116">Megadja, hogy milyen irányt kell használni a frissítési művelethez a feladatátvétel után.</span><span class="sxs-lookup"><span data-stu-id="07a15-116">Specifies the direction to be used for the update operation post a failover.</span></span>  
<span data-ttu-id="07a15-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="07a15-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="07a15-118">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="07a15-118">PrimaryToRecovery</span></span>
- <span data-ttu-id="07a15-119">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="07a15-119">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="07a15-120">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="07a15-120">-RecoveryPlan</span></span>
<span data-ttu-id="07a15-121">Az ASR-helyreállítási terv objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="07a15-121">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="07a15-122">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="07a15-122">-ReplicationProtectedItem</span></span>
<span data-ttu-id="07a15-123">Egy ASR-replikációs védelemmel ellátott elemet ad meg</span><span class="sxs-lookup"><span data-stu-id="07a15-123">Specifies an ASR replication protected item</span></span>

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

### <span data-ttu-id="07a15-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="07a15-124">-Confirm</span></span>
<span data-ttu-id="07a15-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="07a15-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07a15-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07a15-126">-WhatIf</span></span>
<span data-ttu-id="07a15-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="07a15-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07a15-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="07a15-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07a15-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07a15-129">CommonParameters</span></span>
<span data-ttu-id="07a15-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="07a15-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07a15-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07a15-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07a15-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="07a15-132">INPUTS</span></span>

### <span data-ttu-id="07a15-133">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="07a15-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="07a15-134">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="07a15-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="07a15-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07a15-135">OUTPUTS</span></span>

### <span data-ttu-id="07a15-136">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="07a15-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="07a15-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="07a15-137">NOTES</span></span>

## <span data-ttu-id="07a15-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07a15-138">RELATED LINKS</span></span>

