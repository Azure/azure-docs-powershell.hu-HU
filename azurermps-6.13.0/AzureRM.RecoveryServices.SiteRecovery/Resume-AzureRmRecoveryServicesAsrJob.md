---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/resume-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: c5efb6b9aa7d78ef5f8d50ef80c5155c7e731f11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502915"
---
# <span data-ttu-id="41d2f-101">Resume-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="41d2f-101">Resume-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="41d2f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="41d2f-102">SYNOPSIS</span></span>
<span data-ttu-id="41d2f-103">Felfüggesztett Azure webhely-helyreállítási feladatot folytat.</span><span class="sxs-lookup"><span data-stu-id="41d2f-103">Resumes a suspended Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41d2f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="41d2f-104">SYNTAX</span></span>

### <span data-ttu-id="41d2f-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="41d2f-105">ByObject (Default)</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41d2f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="41d2f-106">ByName</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -Name <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41d2f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="41d2f-107">DESCRIPTION</span></span>
<span data-ttu-id="41d2f-108">A **resume-AzureRmRecoveryServicesAsrJob** parancsmag folytatja a felfüggesztett Azure webhely-helyreállítási feladatot.</span><span class="sxs-lookup"><span data-stu-id="41d2f-108">The **Resume-AzureRmRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="41d2f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="41d2f-109">EXAMPLES</span></span>

### <span data-ttu-id="41d2f-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="41d2f-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="41d2f-111">A megadott feladat folytatása, ha várakozó vagy felfüggesztett állapotban van, és visszaadja az ASR feladatnak megfelelő frissített ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="41d2f-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="41d2f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="41d2f-112">PARAMETERS</span></span>

### <span data-ttu-id="41d2f-113">-Megjegyzés</span><span class="sxs-lookup"><span data-stu-id="41d2f-113">-Comment</span></span>
<span data-ttu-id="41d2f-114">A Projektnapló megjegyzései.</span><span class="sxs-lookup"><span data-stu-id="41d2f-114">Comments for the job log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Comments

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41d2f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41d2f-115">-DefaultProfile</span></span>
<span data-ttu-id="41d2f-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="41d2f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41d2f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41d2f-117">-InputObject</span></span>
<span data-ttu-id="41d2f-118">A bemeneti objektum az a parancsmag: az ASR-feladat objektuma, amely a projektnek megfelelően folytatódik.</span><span class="sxs-lookup"><span data-stu-id="41d2f-118">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41d2f-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="41d2f-119">-Name</span></span>
<span data-ttu-id="41d2f-120">Adja meg az ASR-feladatot név szerint.</span><span class="sxs-lookup"><span data-stu-id="41d2f-120">Specify the ASR job by name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41d2f-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="41d2f-121">-Confirm</span></span>
<span data-ttu-id="41d2f-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="41d2f-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41d2f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41d2f-123">-WhatIf</span></span>
<span data-ttu-id="41d2f-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="41d2f-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41d2f-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="41d2f-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41d2f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41d2f-126">CommonParameters</span></span>
<span data-ttu-id="41d2f-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="41d2f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41d2f-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41d2f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41d2f-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="41d2f-129">INPUTS</span></span>

### <span data-ttu-id="41d2f-130">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="41d2f-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="41d2f-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41d2f-131">OUTPUTS</span></span>

### <span data-ttu-id="41d2f-132">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="41d2f-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="41d2f-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="41d2f-133">NOTES</span></span>

## <span data-ttu-id="41d2f-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41d2f-134">RELATED LINKS</span></span>

[<span data-ttu-id="41d2f-135">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="41d2f-135">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="41d2f-136">Újraindítás – AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="41d2f-136">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="41d2f-137">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="41d2f-137">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
