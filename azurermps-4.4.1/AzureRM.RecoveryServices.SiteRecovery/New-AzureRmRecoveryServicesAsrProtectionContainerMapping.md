---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: aa2cd93d21ba22405fff0f3c5fcf336d00f2f6b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494741"
---
# <span data-ttu-id="1295b-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="1295b-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="1295b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1295b-102">SYNOPSIS</span></span>
<span data-ttu-id="1295b-103">Az Azure webhely-helyreállítási védelmi tárolók megfeleltetését a megadott replikációs házirendnek a megadott ASR-védelmi tárolóhoz társításával hozza létre.</span><span class="sxs-lookup"><span data-stu-id="1295b-103">Creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1295b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1295b-104">SYNTAX</span></span>

### <span data-ttu-id="1295b-105">EnterpriseToAzure (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1295b-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1295b-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="1295b-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1295b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1295b-107">DESCRIPTION</span></span>
<span data-ttu-id="1295b-108">A **New-AzureRmRecoveryServicesAsrProtectionContainerMapping** parancsmag létrehoz egy Azure site Recovery Protection Container-megfeleltetést úgy, hogy társítja a megadott replikációs házirendet a megadott védelmi tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="1295b-108">The **New-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified protection container.</span></span>

## <span data-ttu-id="1295b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1295b-109">EXAMPLES</span></span>

### <span data-ttu-id="1295b-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1295b-110">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $ContainerMappingName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer
```

<span data-ttu-id="1295b-111">Elindítja a védett tároló megfeleltetésének létrehozását a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="1295b-111">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="1295b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1295b-112">PARAMETERS</span></span>

### <span data-ttu-id="1295b-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1295b-113">-Name</span></span>
<span data-ttu-id="1295b-114">A védelmi tároló megfeleltetésének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1295b-114">Specifies the name of the Protection Container mapping.</span></span>

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

### <span data-ttu-id="1295b-115">-Házirend</span><span class="sxs-lookup"><span data-stu-id="1295b-115">-Policy</span></span>
<span data-ttu-id="1295b-116">Megadja a megfeleltetéshez használni kívánt replikációs házirendhez tartozó ASR-replikációs házirend-objektumot.</span><span class="sxs-lookup"><span data-stu-id="1295b-116">Specifies the ASR replication policy object for the replication policy to be used in the mapping.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1295b-117">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="1295b-117">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="1295b-118">Megadja a megfeleltetéshez használni kívánt elsődleges védelmi tárolóhoz tartozó ASR-védelmi tároló objektumot.</span><span class="sxs-lookup"><span data-stu-id="1295b-118">Specifies the ASR protection container object for the  primary protection container to be used in the mapping.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1295b-119">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="1295b-119">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="1295b-120">Az ASR-védelem tároló objektum a megfeleltetéshez használt helyreállítási védelmi tároló objektumhoz (ez akkor használatos, ha az nem Azure-helyreállítási helyre replikálódik).</span><span class="sxs-lookup"><span data-stu-id="1295b-120">Specifies the ASR protection container object for the  recovery protection container to be used in the mapping (used if replicating to a recovery location that is not Azure.)</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1295b-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1295b-121">-Confirm</span></span>
<span data-ttu-id="1295b-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1295b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1295b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1295b-123">-WhatIf</span></span>
<span data-ttu-id="1295b-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1295b-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1295b-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1295b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1295b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1295b-126">CommonParameters</span></span>
<span data-ttu-id="1295b-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1295b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1295b-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1295b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1295b-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1295b-129">INPUTS</span></span>

### <span data-ttu-id="1295b-130">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="1295b-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="1295b-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1295b-131">OUTPUTS</span></span>

### <span data-ttu-id="1295b-132">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1295b-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1295b-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1295b-133">NOTES</span></span>

## <span data-ttu-id="1295b-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1295b-134">RELATED LINKS</span></span>

[<span data-ttu-id="1295b-135">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="1295b-135">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="1295b-136">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="1295b-136">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
