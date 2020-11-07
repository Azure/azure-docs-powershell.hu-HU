---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 2d172c440163d70ef388c7de190371492767b2e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680500"
---
# <span data-ttu-id="676d8-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="676d8-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="676d8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="676d8-102">SYNOPSIS</span></span>
<span data-ttu-id="676d8-103">Visszaadja a megadott ASR-helyreállítási csomagot a helyreállítási szolgáltatások pincéjében.</span><span class="sxs-lookup"><span data-stu-id="676d8-103">Delets the specified ASR recovery plan from Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="676d8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="676d8-104">SYNTAX</span></span>

### <span data-ttu-id="676d8-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="676d8-105">ByObject (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="676d8-106">ByName</span><span class="sxs-lookup"><span data-stu-id="676d8-106">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="676d8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="676d8-107">DESCRIPTION</span></span>
<span data-ttu-id="676d8-108">A **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** parancsmag törli a megadott helyreállítási csomagot a helyreállítási szolgáltatások boltozatból.</span><span class="sxs-lookup"><span data-stu-id="676d8-108">The **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="676d8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="676d8-109">EXAMPLES</span></span>

### <span data-ttu-id="676d8-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="676d8-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="676d8-111">Elindítja a megadott helyreállítási terv törlését, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="676d8-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="676d8-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="676d8-112">PARAMETERS</span></span>

### <span data-ttu-id="676d8-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="676d8-113">-InputObject</span></span>
<span data-ttu-id="676d8-114">A bemeneti objektum a parancsmag: az ASR-helyreállítási terv objektuma, amely megfelel a törlendő helyreállítási tervnek.</span><span class="sxs-lookup"><span data-stu-id="676d8-114">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="676d8-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="676d8-115">-Name</span></span>
<span data-ttu-id="676d8-116">A törlendő helyreállítási terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="676d8-116">Specifies the name of the recovery plan to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="676d8-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="676d8-117">-Confirm</span></span>
<span data-ttu-id="676d8-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="676d8-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="676d8-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="676d8-119">-WhatIf</span></span>
<span data-ttu-id="676d8-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="676d8-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="676d8-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="676d8-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="676d8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="676d8-122">CommonParameters</span></span>
<span data-ttu-id="676d8-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="676d8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="676d8-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="676d8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="676d8-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="676d8-125">INPUTS</span></span>

### <span data-ttu-id="676d8-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="676d8-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="676d8-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="676d8-127">OUTPUTS</span></span>

### <span data-ttu-id="676d8-128">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="676d8-128">System.Object</span></span>

## <span data-ttu-id="676d8-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="676d8-129">NOTES</span></span>

## <span data-ttu-id="676d8-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="676d8-130">RELATED LINKS</span></span>

[<span data-ttu-id="676d8-131">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="676d8-131">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="676d8-132">Új – AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="676d8-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="676d8-133">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="676d8-133">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


