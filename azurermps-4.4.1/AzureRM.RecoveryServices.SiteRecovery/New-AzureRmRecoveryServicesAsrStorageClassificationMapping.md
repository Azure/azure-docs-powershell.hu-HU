---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 14cd1606bc4c8d1709b0ddd64e845a2e84b26df0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494734"
---
# <span data-ttu-id="17216-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="17216-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="17216-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="17216-102">SYNOPSIS</span></span>
<span data-ttu-id="17216-103">Az ASR-tárolók osztályozási megfeleltetését hozza létre a helyreállítási szolgáltatások pincéjében.</span><span class="sxs-lookup"><span data-stu-id="17216-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17216-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="17216-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17216-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="17216-105">DESCRIPTION</span></span>
<span data-ttu-id="17216-106">A **New-AzureRmRecoveryServicesAsrStorageClassificationMapping** parancsmag létrehoz egy tárterület-osztályozási társítást a helyreállítási szolgáltatások boltozatához.</span><span class="sxs-lookup"><span data-stu-id="17216-106">The **New-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="17216-107">Példák</span><span class="sxs-lookup"><span data-stu-id="17216-107">EXAMPLES</span></span>

### <span data-ttu-id="17216-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="17216-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name $StrorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="17216-109">A megadott paraméterekkel elindítja a tárolási osztályozási hozzárendelés-készítési műveletet, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="17216-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="17216-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="17216-110">PARAMETERS</span></span>

### <span data-ttu-id="17216-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="17216-111">-Name</span></span>
<span data-ttu-id="17216-112">Az ASR-tárolók besorolási megfeleltetésének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="17216-112">Specifies a name for the ASR storage classification mapping.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17216-113">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="17216-113">-PrimaryStorageClassification</span></span>
<span data-ttu-id="17216-114">A megfeleltetés elsődleges ASR-tárterület-osztályozási objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="17216-114">Specifies the primary ASR storage classification object for the mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17216-115">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="17216-115">-RecoveryStorageClassification</span></span>
<span data-ttu-id="17216-116">Megadja a megfeleltetés helyreállítási ASR-tárolási osztályozási objektumát.</span><span class="sxs-lookup"><span data-stu-id="17216-116">Specifies the recovery ASR storage classification object for the mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17216-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="17216-117">-Confirm</span></span>
<span data-ttu-id="17216-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="17216-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17216-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17216-119">-WhatIf</span></span>
<span data-ttu-id="17216-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="17216-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="17216-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="17216-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17216-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17216-122">CommonParameters</span></span>
<span data-ttu-id="17216-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="17216-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17216-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17216-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17216-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="17216-125">INPUTS</span></span>

### <span data-ttu-id="17216-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="17216-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="17216-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="17216-127">OUTPUTS</span></span>

### <span data-ttu-id="17216-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="17216-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="17216-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="17216-129">NOTES</span></span>

## <span data-ttu-id="17216-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="17216-130">RELATED LINKS</span></span>

[<span data-ttu-id="17216-131">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="17216-131">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="17216-132">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="17216-132">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
