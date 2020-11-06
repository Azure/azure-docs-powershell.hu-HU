---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 13c2f20f6d8ef7823244c62cfbe97e4b3a25eb73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494730"
---
# <span data-ttu-id="fece6-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="fece6-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="fece6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fece6-102">SYNOPSIS</span></span>
<span data-ttu-id="fece6-103">Törli a megadott ASR-hálózati megfeleltetést a helyreállítási szolgáltatások pincéjében.</span><span class="sxs-lookup"><span data-stu-id="fece6-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fece6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fece6-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fece6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fece6-105">DESCRIPTION</span></span>
<span data-ttu-id="fece6-106">A **Remove-AzureRmRecoveryServicesAsrNetworkMapping** parancsmag törli a megadott ASR-hálózati megfeleltetést.</span><span class="sxs-lookup"><span data-stu-id="fece6-106">The **Remove-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="fece6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fece6-107">EXAMPLES</span></span>

### <span data-ttu-id="fece6-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fece6-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="fece6-109">Elindítja a megadott ASR-hálózati megfeleltetés törlését, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="fece6-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="fece6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fece6-110">PARAMETERS</span></span>

### <span data-ttu-id="fece6-111">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fece6-111">-InputObject</span></span>
<span data-ttu-id="fece6-112">A bemeneti objektum a parancsmag: az ASR hálózati megfeleltetési objektum, amely megfelel a törölni kívánt ASR-hálózati megfeleltetésnek.</span><span class="sxs-lookup"><span data-stu-id="fece6-112">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fece6-113">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fece6-113">-Confirm</span></span>
<span data-ttu-id="fece6-114">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fece6-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fece6-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fece6-115">-WhatIf</span></span>
<span data-ttu-id="fece6-116">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fece6-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fece6-117">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fece6-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fece6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fece6-118">CommonParameters</span></span>
<span data-ttu-id="fece6-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fece6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fece6-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fece6-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fece6-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fece6-121">INPUTS</span></span>

### <span data-ttu-id="fece6-122">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="fece6-122">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="fece6-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fece6-123">OUTPUTS</span></span>

### <span data-ttu-id="fece6-124">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="fece6-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fece6-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fece6-125">NOTES</span></span>

## <span data-ttu-id="fece6-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fece6-126">RELATED LINKS</span></span>

[<span data-ttu-id="fece6-127">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="fece6-127">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="fece6-128">Új – AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="fece6-128">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)
