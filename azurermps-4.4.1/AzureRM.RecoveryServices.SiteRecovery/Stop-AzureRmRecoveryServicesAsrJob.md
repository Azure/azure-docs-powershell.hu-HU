---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: e639e6fc42e440b5088a34ee29e21d324ed7d235
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679360"
---
# <span data-ttu-id="eac07-101">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="eac07-101">Stop-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="eac07-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eac07-102">SYNOPSIS</span></span>
<span data-ttu-id="eac07-103">Az Azure webhely-helyreállítási feladat leállítása.</span><span class="sxs-lookup"><span data-stu-id="eac07-103">Stops an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eac07-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eac07-104">SYNTAX</span></span>

### <span data-ttu-id="eac07-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eac07-105">ByObject (Default)</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eac07-106">ByName</span><span class="sxs-lookup"><span data-stu-id="eac07-106">ByName</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -Name <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eac07-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="eac07-107">DESCRIPTION</span></span>
<span data-ttu-id="eac07-108">A **stop-AzureRmRecoveryServicesAsrJob** parancsmag leállítja a megadott Azure-webhely helyreállítási feladatát.</span><span class="sxs-lookup"><span data-stu-id="eac07-108">The **Stop-AzureRmRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="eac07-109">Példák</span><span class="sxs-lookup"><span data-stu-id="eac07-109">EXAMPLES</span></span>

### <span data-ttu-id="eac07-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="eac07-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="eac07-111">Megkísérli leállítani a megadott feladatot, és egy frissített ASR-objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="eac07-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="eac07-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eac07-112">PARAMETERS</span></span>

### <span data-ttu-id="eac07-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eac07-113">-InputObject</span></span>
<span data-ttu-id="eac07-114">Beviteli objektum: Itt adhatja meg az ASR-feladat leállításának megfelelő ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="eac07-114">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eac07-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eac07-115">-Name</span></span>
<span data-ttu-id="eac07-116">Adja meg azt az ASR-feladatot, amelyet az ASR-feladat nevében le kell állítani.</span><span class="sxs-lookup"><span data-stu-id="eac07-116">Specify the ASR Job to be stopped by the ASR job name.</span></span>

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

### <span data-ttu-id="eac07-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="eac07-117">-Confirm</span></span>
<span data-ttu-id="eac07-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eac07-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eac07-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eac07-119">-WhatIf</span></span>
<span data-ttu-id="eac07-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="eac07-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eac07-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eac07-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eac07-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eac07-122">CommonParameters</span></span>
<span data-ttu-id="eac07-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eac07-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eac07-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eac07-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eac07-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eac07-125">INPUTS</span></span>

### <span data-ttu-id="eac07-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="eac07-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="eac07-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eac07-127">OUTPUTS</span></span>

### <span data-ttu-id="eac07-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="eac07-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="eac07-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eac07-129">NOTES</span></span>

## <span data-ttu-id="eac07-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eac07-130">RELATED LINKS</span></span>

[<span data-ttu-id="eac07-131">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="eac07-131">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="eac07-132">Újraindítás – AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="eac07-132">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="eac07-133">Önéletrajz – AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="eac07-133">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)
