---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 2f219882199010b2765ebd4386691451d74a182d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679364"
---
# <span data-ttu-id="7b97c-101">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="7b97c-101">Restart-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="7b97c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7b97c-102">SYNOPSIS</span></span>
<span data-ttu-id="7b97c-103">Az Azure webhely-helyreállítási feladat újraindítása.</span><span class="sxs-lookup"><span data-stu-id="7b97c-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b97c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7b97c-104">SYNTAX</span></span>

### <span data-ttu-id="7b97c-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7b97c-105">ByObject (Default)</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b97c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7b97c-106">ByName</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -Name <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b97c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7b97c-107">DESCRIPTION</span></span>
<span data-ttu-id="7b97c-108">Az **Újraindítás – AzureRmRecoveryServicesAsrJob** parancsmag újraindítja az Azure webhely-helyreállítási feladatot.</span><span class="sxs-lookup"><span data-stu-id="7b97c-108">The **Restart-AzureRmRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="7b97c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7b97c-109">EXAMPLES</span></span>

### <span data-ttu-id="7b97c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7b97c-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="7b97c-111">A megadott ASR-feladat újraindítása, és az ASR-feladat frissített automatikus helyreállítási feladatát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="7b97c-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="7b97c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7b97c-112">PARAMETERS</span></span>

### <span data-ttu-id="7b97c-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b97c-113">-InputObject</span></span>
<span data-ttu-id="7b97c-114">A bemeneti objektum az a parancsmag: az ASR-feladat objektuma, amelyet az ASR-feladatnak megfelelően kell elindítani.</span><span class="sxs-lookup"><span data-stu-id="7b97c-114">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>
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

### <span data-ttu-id="7b97c-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7b97c-115">-Name</span></span>
<span data-ttu-id="7b97c-116">Adja meg a feladatot név szerint.</span><span class="sxs-lookup"><span data-stu-id="7b97c-116">Specify the job by name.</span></span>

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

### <span data-ttu-id="7b97c-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7b97c-117">-Confirm</span></span>
<span data-ttu-id="7b97c-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7b97c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b97c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b97c-119">-WhatIf</span></span>
<span data-ttu-id="7b97c-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7b97c-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b97c-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7b97c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b97c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b97c-122">CommonParameters</span></span>
<span data-ttu-id="7b97c-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7b97c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b97c-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b97c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b97c-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b97c-125">INPUTS</span></span>

### <span data-ttu-id="7b97c-126">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7b97c-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7b97c-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7b97c-127">OUTPUTS</span></span>

### <span data-ttu-id="7b97c-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7b97c-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7b97c-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7b97c-129">NOTES</span></span>

## <span data-ttu-id="7b97c-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7b97c-130">RELATED LINKS</span></span>

[<span data-ttu-id="7b97c-131">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="7b97c-131">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="7b97c-132">Önéletrajz – AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="7b97c-132">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="7b97c-133">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="7b97c-133">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
