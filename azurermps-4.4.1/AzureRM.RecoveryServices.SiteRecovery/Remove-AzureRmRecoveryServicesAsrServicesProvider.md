---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 5220271538903206876dd8d5c476824e1ac10874
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504775"
---
# <span data-ttu-id="fc5c8-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="fc5c8-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="fc5c8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fc5c8-102">SYNOPSIS</span></span>
<span data-ttu-id="fc5c8-103">Törli a kijelölt Azure-webhely helyreállítási szolgáltatás-szolgáltatóját a helyreállítási szolgáltatások boltozatáról.</span><span class="sxs-lookup"><span data-stu-id="fc5c8-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc5c8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fc5c8-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc5c8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fc5c8-105">DESCRIPTION</span></span>
<span data-ttu-id="fc5c8-106">A **Remove-AzureRmRecoveryServicesAsrServicesProvider** parancsmag eltávolítja a megadott Azure webhely-helyreállítási helyreállítási szolgáltatót a boltozatról.</span><span class="sxs-lookup"><span data-stu-id="fc5c8-106">The **Remove-AzureRmRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="fc5c8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fc5c8-107">EXAMPLES</span></span>

### <span data-ttu-id="fc5c8-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fc5c8-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="fc5c8-109">Elindítja a megadott Azure webhely-helyreállítási szolgáltató törlését/regisztrációját, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="fc5c8-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="fc5c8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fc5c8-110">PARAMETERS</span></span>

### <span data-ttu-id="fc5c8-111">-Force</span><span class="sxs-lookup"><span data-stu-id="fc5c8-111">-Force</span></span>
<span data-ttu-id="fc5c8-112">Kényszerítse a parancsot, hogy ne adjon meg további figyelmeztetést.</span><span class="sxs-lookup"><span data-stu-id="fc5c8-112">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc5c8-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc5c8-113">-InputObject</span></span>
<span data-ttu-id="fc5c8-114">A bemeneti objektum a parancsmaghoz: az ASR helyreállítási szolgáltatója objektum, amely megfelel az ASR-helyreállítási szolgáltatás által törlendő helyreállítási szolgáltatásnak.</span><span class="sxs-lookup"><span data-stu-id="fc5c8-114">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc5c8-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fc5c8-115">-Confirm</span></span>
<span data-ttu-id="fc5c8-116">Adja meg, hogy szükség van-e megerősítésre.</span><span class="sxs-lookup"><span data-stu-id="fc5c8-116">Specify if confirmation is required.</span></span> <span data-ttu-id="fc5c8-117">Adja meg a megerősítési paraméter értékét $false a megerősítés kihagyása érdekében.</span><span class="sxs-lookup"><span data-stu-id="fc5c8-117">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="fc5c8-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc5c8-118">-WhatIf</span></span>
<span data-ttu-id="fc5c8-119">Annak megjelenítése, hogy mi történik, ha a parancsmagot ténylegesen végrehajtják a parancsmag végrehajtása nélkül.</span><span class="sxs-lookup"><span data-stu-id="fc5c8-119">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="fc5c8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc5c8-120">CommonParameters</span></span>
<span data-ttu-id="fc5c8-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fc5c8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc5c8-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc5c8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc5c8-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc5c8-123">INPUTS</span></span>

### <span data-ttu-id="fc5c8-124">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="fc5c8-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="fc5c8-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc5c8-125">OUTPUTS</span></span>

### <span data-ttu-id="fc5c8-126">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fc5c8-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="fc5c8-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fc5c8-127">NOTES</span></span>

## <span data-ttu-id="fc5c8-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc5c8-128">RELATED LINKS</span></span>

[<span data-ttu-id="fc5c8-129">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="fc5c8-129">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="fc5c8-130">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="fc5c8-130">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)