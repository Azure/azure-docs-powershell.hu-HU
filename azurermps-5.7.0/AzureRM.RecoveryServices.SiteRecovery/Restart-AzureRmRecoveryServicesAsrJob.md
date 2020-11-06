---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/restart-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 0ac09a527aff78648d3af14413baa33da137d59e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495305"
---
# <span data-ttu-id="90afc-101">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="90afc-101">Restart-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="90afc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="90afc-102">SYNOPSIS</span></span>
<span data-ttu-id="90afc-103">Az Azure webhely-helyreállítási feladat újraindítása.</span><span class="sxs-lookup"><span data-stu-id="90afc-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90afc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="90afc-104">SYNTAX</span></span>

### <span data-ttu-id="90afc-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="90afc-105">ByObject (Default)</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90afc-106">ByName</span><span class="sxs-lookup"><span data-stu-id="90afc-106">ByName</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90afc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="90afc-107">DESCRIPTION</span></span>
<span data-ttu-id="90afc-108">Az **Újraindítás – AzureRmRecoveryServicesAsrJob** parancsmag újraindítja az Azure webhely-helyreállítási feladatot.</span><span class="sxs-lookup"><span data-stu-id="90afc-108">The **Restart-AzureRmRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="90afc-109">Példák</span><span class="sxs-lookup"><span data-stu-id="90afc-109">EXAMPLES</span></span>

### <span data-ttu-id="90afc-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="90afc-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="90afc-111">A megadott ASR-feladat újraindítása, és az ASR-feladat frissített automatikus helyreállítási feladatát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="90afc-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="90afc-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="90afc-112">PARAMETERS</span></span>

### <span data-ttu-id="90afc-113">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="90afc-113">-Confirm</span></span>
<span data-ttu-id="90afc-114">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="90afc-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90afc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90afc-115">-DefaultProfile</span></span>
<span data-ttu-id="90afc-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="90afc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="90afc-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90afc-117">-InputObject</span></span>
<span data-ttu-id="90afc-118">A bemeneti objektum az a parancsmag: az ASR-feladat objektuma, amelyet az ASR-feladatnak megfelelően kell elindítani.</span><span class="sxs-lookup"><span data-stu-id="90afc-118">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>
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

### <span data-ttu-id="90afc-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="90afc-119">-Name</span></span>
<span data-ttu-id="90afc-120">Adja meg a feladatot név szerint.</span><span class="sxs-lookup"><span data-stu-id="90afc-120">Specify the job by name.</span></span>

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

### <span data-ttu-id="90afc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90afc-121">-WhatIf</span></span>
<span data-ttu-id="90afc-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="90afc-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90afc-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="90afc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90afc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90afc-124">CommonParameters</span></span>
<span data-ttu-id="90afc-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="90afc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90afc-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90afc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90afc-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="90afc-127">INPUTS</span></span>

### <span data-ttu-id="90afc-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="90afc-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="90afc-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="90afc-129">OUTPUTS</span></span>

### <span data-ttu-id="90afc-130">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="90afc-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="90afc-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="90afc-131">NOTES</span></span>

## <span data-ttu-id="90afc-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="90afc-132">RELATED LINKS</span></span>

[<span data-ttu-id="90afc-133">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="90afc-133">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="90afc-134">Önéletrajz – AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="90afc-134">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="90afc-135">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="90afc-135">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
