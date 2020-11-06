---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: b209c706a8da88cfc5188b11302166469749c33f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503992"
---
# <span data-ttu-id="695a8-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="695a8-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="695a8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="695a8-102">SYNOPSIS</span></span>
<span data-ttu-id="695a8-103">A védelemmel ellátott elemek beolvasása az ASR-védelmi tárolóban</span><span class="sxs-lookup"><span data-stu-id="695a8-103">Get the protectable items in an ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="695a8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="695a8-104">SYNTAX</span></span>

### <span data-ttu-id="695a8-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="695a8-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="695a8-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="695a8-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="695a8-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="695a8-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

## <span data-ttu-id="695a8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="695a8-108">DESCRIPTION</span></span>
<span data-ttu-id="695a8-109">A **Get-AzureRmRecoveryServicesAsrProtectableItem** parancsmag az Azure webhely-helyreállítási védelmi tárolóban található védelemmel ellátott elemeket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="695a8-109">The **Get-AzureRmRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="695a8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="695a8-110">EXAMPLES</span></span>

### <span data-ttu-id="695a8-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="695a8-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="695a8-112">A megadott ASR-védelmi tároló minden védett elemének beolvasása</span><span class="sxs-lookup"><span data-stu-id="695a8-112">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="695a8-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="695a8-113">PARAMETERS</span></span>

### <span data-ttu-id="695a8-114">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="695a8-114">-FriendlyName</span></span>
<span data-ttu-id="695a8-115">Az ASR-védelemmel ellátott elem rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="695a8-115">Specifies the friendly name of the ASR protectable item.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="695a8-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="695a8-116">-Name</span></span>
<span data-ttu-id="695a8-117">Az ASR-védelemmel ellátott elem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="695a8-117">Specifies the name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="695a8-118">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="695a8-118">-ProtectionContainer</span></span>
<span data-ttu-id="695a8-119">Az Azure site Recovery Protection Container objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="695a8-119">Specifies the Azure Site Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="695a8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="695a8-120">CommonParameters</span></span>
<span data-ttu-id="695a8-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="695a8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="695a8-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="695a8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="695a8-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="695a8-123">INPUTS</span></span>

### <span data-ttu-id="695a8-124">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="695a8-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="695a8-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="695a8-125">OUTPUTS</span></span>

### <span data-ttu-id="695a8-126">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRProtectableItem, Microsoft. Azure. commands. RecoveryServices. SiteRecovery; Version = 4.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="695a8-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="695a8-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="695a8-127">NOTES</span></span>

## <span data-ttu-id="695a8-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="695a8-128">RELATED LINKS</span></span>

[<span data-ttu-id="695a8-129">Get-AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="695a8-129">Get-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionEntity.md)

[<span data-ttu-id="695a8-130">Set-AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="695a8-130">Set-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Set-AzureRmRecoveryServicesAsrProtectionEntity.md)
