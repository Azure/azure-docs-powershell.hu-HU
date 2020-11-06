---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: ac3f3c843f13fd500156cf148b5c80436e2e2649
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501675"
---
# <span data-ttu-id="71902-101">Resume-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="71902-101">Resume-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="71902-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="71902-102">SYNOPSIS</span></span>
<span data-ttu-id="71902-103">Felfüggesztett Azure webhely-helyreállítási feladatot folytat.</span><span class="sxs-lookup"><span data-stu-id="71902-103">Resumes a suspended Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71902-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="71902-104">SYNTAX</span></span>

### <span data-ttu-id="71902-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="71902-105">ByObject (Default)</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71902-106">ByName</span><span class="sxs-lookup"><span data-stu-id="71902-106">ByName</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -Name <String> [-Comment <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="71902-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="71902-107">DESCRIPTION</span></span>
<span data-ttu-id="71902-108">A **resume-AzureRmRecoveryServicesAsrJob** parancsmag folytatja a felfüggesztett Azure webhely-helyreállítási feladatot.</span><span class="sxs-lookup"><span data-stu-id="71902-108">The **Resume-AzureRmRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="71902-109">Példák</span><span class="sxs-lookup"><span data-stu-id="71902-109">EXAMPLES</span></span>

### <span data-ttu-id="71902-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="71902-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="71902-111">A megadott feladat folytatása, ha várakozó vagy felfüggesztett állapotban van, és visszaadja az ASR feladatnak megfelelő frissített ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="71902-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="71902-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="71902-112">PARAMETERS</span></span>

### <span data-ttu-id="71902-113">-Megjegyzés</span><span class="sxs-lookup"><span data-stu-id="71902-113">-Comment</span></span>
<span data-ttu-id="71902-114">A Projektnapló megjegyzései.</span><span class="sxs-lookup"><span data-stu-id="71902-114">Comments for the job log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Comments

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71902-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71902-115">-InputObject</span></span>
<span data-ttu-id="71902-116">A bemeneti objektum az a parancsmag: az ASR-feladat objektuma, amely a projektnek megfelelően folytatódik.</span><span class="sxs-lookup"><span data-stu-id="71902-116">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

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

### <span data-ttu-id="71902-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="71902-117">-Name</span></span>
<span data-ttu-id="71902-118">Adja meg az ASR-feladatot név szerint.</span><span class="sxs-lookup"><span data-stu-id="71902-118">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="71902-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="71902-119">-Confirm</span></span>
<span data-ttu-id="71902-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="71902-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71902-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71902-121">-WhatIf</span></span>
<span data-ttu-id="71902-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="71902-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71902-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="71902-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71902-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71902-124">CommonParameters</span></span>
<span data-ttu-id="71902-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="71902-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71902-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71902-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71902-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="71902-127">INPUTS</span></span>

### <span data-ttu-id="71902-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="71902-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="71902-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71902-129">OUTPUTS</span></span>

### <span data-ttu-id="71902-130">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="71902-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="71902-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="71902-131">NOTES</span></span>

## <span data-ttu-id="71902-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71902-132">RELATED LINKS</span></span>

[<span data-ttu-id="71902-133">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="71902-133">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="71902-134">Újraindítás – AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="71902-134">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="71902-135">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="71902-135">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
