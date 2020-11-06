---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
ms.openlocfilehash: 590512c822bd55b992c8cc58eab4091863792e21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500779"
---
# <span data-ttu-id="03e8a-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="03e8a-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span></span>

## <span data-ttu-id="03e8a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="03e8a-102">SYNOPSIS</span></span>
<span data-ttu-id="03e8a-103">Egy webhely-helyreállítási objektum véglegesítési feladatátvételi tevékenységének indítása.</span><span class="sxs-lookup"><span data-stu-id="03e8a-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03e8a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="03e8a-104">SYNTAX</span></span>

### <span data-ttu-id="03e8a-105">ByRPIObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="03e8a-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03e8a-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="03e8a-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03e8a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="03e8a-107">DESCRIPTION</span></span>
<span data-ttu-id="03e8a-108">A **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** parancsmag a feladatátvételi művelet után egy Azure-webhely helyreállítási objektum véglegesítésének véglegesítését indítja el.</span><span class="sxs-lookup"><span data-stu-id="03e8a-108">The **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="03e8a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="03e8a-109">EXAMPLES</span></span>

### <span data-ttu-id="03e8a-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="03e8a-110">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan $RP
```

<span data-ttu-id="03e8a-111">Elindítja a megadott helyreállítási csomag véglegesítési feladatátvételét, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="03e8a-111">Starts the commit failover for the specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="03e8a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="03e8a-112">PARAMETERS</span></span>

### <span data-ttu-id="03e8a-113">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="03e8a-113">-RecoveryPlan</span></span>
<span data-ttu-id="03e8a-114">Az ASR-helyreállítási terv objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="03e8a-114">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="03e8a-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="03e8a-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="03e8a-116">Egy ASR-replikációs védett elem objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="03e8a-116">Specifies an ASR replication protected item object.</span></span>

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

### <span data-ttu-id="03e8a-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="03e8a-117">-Confirm</span></span>
<span data-ttu-id="03e8a-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="03e8a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03e8a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03e8a-119">-WhatIf</span></span>
<span data-ttu-id="03e8a-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="03e8a-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03e8a-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="03e8a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03e8a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03e8a-122">CommonParameters</span></span>
<span data-ttu-id="03e8a-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="03e8a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03e8a-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03e8a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03e8a-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="03e8a-125">INPUTS</span></span>

### <span data-ttu-id="03e8a-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="03e8a-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="03e8a-127">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="03e8a-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="03e8a-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03e8a-128">OUTPUTS</span></span>

### <span data-ttu-id="03e8a-129">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="03e8a-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="03e8a-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="03e8a-130">NOTES</span></span>

## <span data-ttu-id="03e8a-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03e8a-131">RELATED LINKS</span></span>

