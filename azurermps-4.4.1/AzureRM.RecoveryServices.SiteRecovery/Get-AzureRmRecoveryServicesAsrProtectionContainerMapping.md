---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 06dca346610af2f5ba54eef1c509d18a3465f34f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503987"
---
# <span data-ttu-id="4a014-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="4a014-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="4a014-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4a014-102">SYNOPSIS</span></span>
<span data-ttu-id="4a014-103">Megkapja az Azure site Recovery Protection Container-megfeleltetéseket.</span><span class="sxs-lookup"><span data-stu-id="4a014-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a014-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4a014-104">SYNTAX</span></span>

### <span data-ttu-id="4a014-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4a014-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="4a014-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="4a014-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

## <span data-ttu-id="4a014-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4a014-107">DESCRIPTION</span></span>
<span data-ttu-id="4a014-108">A **Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** parancsmag információkat kap a védelmi tárolóról a megadott ASR-védelmi tárolóhoz tartozó replikációs házirend-megfeleltetések (társítás) esetén.</span><span class="sxs-lookup"><span data-stu-id="4a014-108">The **Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet gets information about the protection container to replication policy mappings(association) in the vault for the specified ASR protection container.</span></span>

## <span data-ttu-id="4a014-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4a014-109">EXAMPLES</span></span>

### <span data-ttu-id="4a014-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4a014-110">Example 1</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container
```

<span data-ttu-id="4a014-111">A megadott védelmi tároló minden védelmi tárolójának megfeleltetése.</span><span class="sxs-lookup"><span data-stu-id="4a014-111">Gets all protection container mappings for the specified protection container.</span></span>

## <span data-ttu-id="4a014-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4a014-112">PARAMETERS</span></span>

### <span data-ttu-id="4a014-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4a014-113">-Name</span></span>
<span data-ttu-id="4a014-114">Megadja a beszerzéshez tartozó védelmi tároló megfeleltetésének nevét.</span><span class="sxs-lookup"><span data-stu-id="4a014-114">Specifies the name of the protection container mapping to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a014-115">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4a014-115">-ProtectionContainer</span></span>
<span data-ttu-id="4a014-116">A megadott ASR-védelmi tároló objektumnak megfelelő védelmi tároló megfeleltetések beszerzése.</span><span class="sxs-lookup"><span data-stu-id="4a014-116">Get protection container mappings corresponding to the specified ASR protection container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a014-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a014-117">CommonParameters</span></span>
<span data-ttu-id="4a014-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4a014-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a014-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a014-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a014-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a014-120">INPUTS</span></span>

### <span data-ttu-id="4a014-121">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4a014-121">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="4a014-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a014-122">OUTPUTS</span></span>

### <span data-ttu-id="4a014-123">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4a014-123">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4a014-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4a014-124">NOTES</span></span>

## <span data-ttu-id="4a014-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4a014-125">RELATED LINKS</span></span>

[<span data-ttu-id="4a014-126">Új – AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="4a014-126">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="4a014-127">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="4a014-127">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
