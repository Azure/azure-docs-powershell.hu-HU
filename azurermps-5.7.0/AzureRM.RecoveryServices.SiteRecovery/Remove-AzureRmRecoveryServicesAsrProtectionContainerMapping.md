---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 7a2508669c0beba7fc9edd92ac645ce149633e05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672846"
---
# <span data-ttu-id="48f30-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="48f30-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="48f30-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="48f30-102">SYNOPSIS</span></span>
<span data-ttu-id="48f30-103">A megadott Azure webhely-helyreállítási védelmi tároló megfeleltetésének törlése.</span><span class="sxs-lookup"><span data-stu-id="48f30-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48f30-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="48f30-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48f30-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="48f30-105">DESCRIPTION</span></span>
<span data-ttu-id="48f30-106">A **Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping** parancsmag törli a megadott Azure site Recovery Protection Container-megfeleltetést.</span><span class="sxs-lookup"><span data-stu-id="48f30-106">The **Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="48f30-107">Példák</span><span class="sxs-lookup"><span data-stu-id="48f30-107">EXAMPLES</span></span>

### <span data-ttu-id="48f30-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="48f30-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="48f30-109">Elindítja a kijelölt védelmi tároló megfeleltetésének törlését, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="48f30-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="48f30-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="48f30-110">PARAMETERS</span></span>

### <span data-ttu-id="48f30-111">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="48f30-111">-Confirm</span></span>
<span data-ttu-id="48f30-112">Adja meg, hogy szükség van-e megerősítésre.</span><span class="sxs-lookup"><span data-stu-id="48f30-112">Specify if confirmation is required.</span></span> <span data-ttu-id="48f30-113">A megerősítési paraméter értékének beállítása $falsera a megerősítés kihagyása érdekében</span><span class="sxs-lookup"><span data-stu-id="48f30-113">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="48f30-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48f30-114">-DefaultProfile</span></span>
<span data-ttu-id="48f30-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48f30-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48f30-116">-Force</span><span class="sxs-lookup"><span data-stu-id="48f30-116">-Force</span></span>
<span data-ttu-id="48f30-117">Kényszerítse a parancsot, hogy ne adjon meg további figyelmeztetést.</span><span class="sxs-lookup"><span data-stu-id="48f30-117">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="48f30-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48f30-118">-InputObject</span></span>
<span data-ttu-id="48f30-119">A bemeneti objektum a parancsmag: az ASR-védelmi tároló társítása, amely a törlendő védelmi tárolóhoz tartozó objektum.</span><span class="sxs-lookup"><span data-stu-id="48f30-119">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48f30-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48f30-120">-WhatIf</span></span>
<span data-ttu-id="48f30-121">Annak megjelenítése, hogy mi történik, ha a parancsmagot ténylegesen végrehajtják a parancsmag végrehajtása nélkül.</span><span class="sxs-lookup"><span data-stu-id="48f30-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="48f30-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48f30-122">CommonParameters</span></span>
<span data-ttu-id="48f30-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="48f30-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48f30-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48f30-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48f30-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="48f30-125">INPUTS</span></span>

### <span data-ttu-id="48f30-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="48f30-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="48f30-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48f30-127">OUTPUTS</span></span>

### <span data-ttu-id="48f30-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="48f30-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="48f30-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="48f30-129">NOTES</span></span>

## <span data-ttu-id="48f30-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48f30-130">RELATED LINKS</span></span>

[<span data-ttu-id="48f30-131">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="48f30-131">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="48f30-132">Új – AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="48f30-132">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
