---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 7263601a3f719ce48a43e26ad76f9ba388a058ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494731"
---
# <span data-ttu-id="af068-101">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="af068-101">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="af068-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="af068-102">SYNOPSIS</span></span>
<span data-ttu-id="af068-103">Törli a megadott ASR-replikációs házirendet a helyreállítási szolgáltatások boltozatról.</span><span class="sxs-lookup"><span data-stu-id="af068-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af068-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="af068-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af068-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="af068-105">DESCRIPTION</span></span>
<span data-ttu-id="af068-106">A **Remove-AzureRmRecoveryServicesAsrPolicy** parancsmag törölte a megadott replikációs házirendet a helyreállítási szolgáltatások pincéjében.</span><span class="sxs-lookup"><span data-stu-id="af068-106">The **Remove-AzureRmRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="af068-107">Példák</span><span class="sxs-lookup"><span data-stu-id="af068-107">EXAMPLES</span></span>

### <span data-ttu-id="af068-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="af068-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="af068-109">Elindítja a megadott replikációs házirend törlését, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="af068-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="af068-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="af068-110">PARAMETERS</span></span>

### <span data-ttu-id="af068-111">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af068-111">-InputObject</span></span>
<span data-ttu-id="af068-112">A bemeneti objektum a parancsmag: az ASR replikációs házirend-objektuma, amely a törlendő replikációs házirendnek megfelelő.</span><span class="sxs-lookup"><span data-stu-id="af068-112">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

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

### <span data-ttu-id="af068-113">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="af068-113">-Confirm</span></span>
<span data-ttu-id="af068-114">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="af068-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af068-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af068-115">-WhatIf</span></span>
<span data-ttu-id="af068-116">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="af068-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af068-117">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="af068-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af068-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af068-118">CommonParameters</span></span>
<span data-ttu-id="af068-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="af068-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af068-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af068-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af068-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="af068-121">INPUTS</span></span>

### <span data-ttu-id="af068-122">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="af068-122">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="af068-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af068-123">OUTPUTS</span></span>

### <span data-ttu-id="af068-124">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="af068-124">System.Object</span></span>

## <span data-ttu-id="af068-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="af068-125">NOTES</span></span>

## <span data-ttu-id="af068-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af068-126">RELATED LINKS</span></span>

[<span data-ttu-id="af068-127">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="af068-127">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="af068-128">Új – AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="af068-128">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)
