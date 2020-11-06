---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 68e06f8a4d9c88b57fa88ee8044ca2e5d04d9ce9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503220"
---
# <span data-ttu-id="f09a1-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f09a1-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="f09a1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f09a1-102">SYNOPSIS</span></span>
<span data-ttu-id="f09a1-103">Webhely-helyreállítási csomag szerkesztése</span><span class="sxs-lookup"><span data-stu-id="f09a1-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f09a1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f09a1-104">SYNTAX</span></span>

### <span data-ttu-id="f09a1-105">AppendGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f09a1-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f09a1-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="f09a1-106">RemoveGroup</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f09a1-107">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="f09a1-107">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f09a1-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="f09a1-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f09a1-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="f09a1-109">DESCRIPTION</span></span>
<span data-ttu-id="f09a1-110">A **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** parancsmag az Azure-webhely helyreállítási csomagját szerkeszti.</span><span class="sxs-lookup"><span data-stu-id="f09a1-110">The **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="f09a1-111">Példák</span><span class="sxs-lookup"><span data-stu-id="f09a1-111">EXAMPLES</span></span>

### <span data-ttu-id="f09a1-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f09a1-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="f09a1-113">Hozzáfűzi a csoportot a meglévő Azure webhely-helyreállítási helyreállítási csomaghoz, és a frissített helyreállítási csomagot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="f09a1-113">Appends a group to existing Azure Site Recovery recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="f09a1-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f09a1-114">PARAMETERS</span></span>

### <span data-ttu-id="f09a1-115">-AddProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f09a1-115">-AddProtectedItem</span></span>
<span data-ttu-id="f09a1-116">A helyreállítási terv objektum helyreállítási terv csoportjához hozzáadott ASR-replikációs védelemmel ellátott elemek listája.</span><span class="sxs-lookup"><span data-stu-id="f09a1-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: AddProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f09a1-117">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="f09a1-117">-AppendGroup</span></span>
<span data-ttu-id="f09a1-118">Váltson paraméterre a helyreállítási terv csoport a helyreállítási terv objektumhoz való hozzáfűzéséhez.</span><span class="sxs-lookup"><span data-stu-id="f09a1-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AppendGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f09a1-119">-Csoport</span><span class="sxs-lookup"><span data-stu-id="f09a1-119">-Group</span></span>
<span data-ttu-id="f09a1-120">A helyreállítási terv csoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f09a1-120">Specifies a recovery plan group.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f09a1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f09a1-121">-InputObject</span></span>
<span data-ttu-id="f09a1-122">A szerkeszteni kívánt ASR-helyreállítási terv objektuma (a memória műveletben.</span><span class="sxs-lookup"><span data-stu-id="f09a1-122">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="f09a1-123">A helyreállítási terv frissítéséhez futtassa a szerkesztett helyreállítási terv objektummal Update-AzureRmASRRecoveryPlant.)</span><span class="sxs-lookup"><span data-stu-id="f09a1-123">To update the recovery plan run Update-AzureRmASRRecoveryPlan with the edited recovery plan object.)</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: (All)
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f09a1-124">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="f09a1-124">-RemoveGroup</span></span>
<span data-ttu-id="f09a1-125">Eltávolítja a megadott csoportot a helyreállítási terv objektumból.</span><span class="sxs-lookup"><span data-stu-id="f09a1-125">Removes the specified group from the recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f09a1-126">-RemoveProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f09a1-126">-RemoveProtectedItem</span></span>
<span data-ttu-id="f09a1-127">A helyreállítási terv objektum helyreállítási terv csoportjának helyreállítási terv csoportjának eltávolítása az ASR-replikációval védett elemek listájából.</span><span class="sxs-lookup"><span data-stu-id="f09a1-127">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: RemoveProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f09a1-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f09a1-128">-Confirm</span></span>
<span data-ttu-id="f09a1-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f09a1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f09a1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f09a1-130">-WhatIf</span></span>
<span data-ttu-id="f09a1-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f09a1-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f09a1-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f09a1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f09a1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f09a1-133">CommonParameters</span></span>
<span data-ttu-id="f09a1-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f09a1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f09a1-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f09a1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f09a1-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f09a1-136">INPUTS</span></span>

### <span data-ttu-id="f09a1-137">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f09a1-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="f09a1-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f09a1-138">OUTPUTS</span></span>

### <span data-ttu-id="f09a1-139">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="f09a1-139">System.Object</span></span>

## <span data-ttu-id="f09a1-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f09a1-140">NOTES</span></span>

## <span data-ttu-id="f09a1-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f09a1-141">RELATED LINKS</span></span>

[<span data-ttu-id="f09a1-142">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f09a1-142">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="f09a1-143">Új – AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f09a1-143">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)
