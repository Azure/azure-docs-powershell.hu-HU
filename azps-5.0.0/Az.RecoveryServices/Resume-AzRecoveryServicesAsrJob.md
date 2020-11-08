---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/resume-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 6af467e5fd90a7d3028d67297b62f517f512b1b1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187211"
---
# <span data-ttu-id="631c8-101">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="631c8-101">Resume-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="631c8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="631c8-102">SYNOPSIS</span></span>
<span data-ttu-id="631c8-103">Felfüggesztett Azure webhely-helyreállítási feladatot folytat.</span><span class="sxs-lookup"><span data-stu-id="631c8-103">Resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="631c8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="631c8-104">SYNTAX</span></span>

### <span data-ttu-id="631c8-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="631c8-105">ByObject (Default)</span></span>
```
Resume-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="631c8-106">ByName</span><span class="sxs-lookup"><span data-stu-id="631c8-106">ByName</span></span>
```
Resume-AzRecoveryServicesAsrJob -Name <String> [-Comment <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="631c8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="631c8-107">DESCRIPTION</span></span>
<span data-ttu-id="631c8-108">A **resume-AzRecoveryServicesAsrJob** parancsmag folytatja a felfüggesztett Azure webhely-helyreállítási feladatot.</span><span class="sxs-lookup"><span data-stu-id="631c8-108">The **Resume-AzRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="631c8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="631c8-109">EXAMPLES</span></span>

### <span data-ttu-id="631c8-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="631c8-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="631c8-111">A megadott feladat folytatása, ha várakozó vagy felfüggesztett állapotban van, és visszaadja az ASR feladatnak megfelelő frissített ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="631c8-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="631c8-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="631c8-112">PARAMETERS</span></span>

### <span data-ttu-id="631c8-113">-Megjegyzés</span><span class="sxs-lookup"><span data-stu-id="631c8-113">-Comment</span></span>
<span data-ttu-id="631c8-114">A Projektnapló megjegyzései.</span><span class="sxs-lookup"><span data-stu-id="631c8-114">Comments for the job log.</span></span>

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

### <span data-ttu-id="631c8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="631c8-115">-DefaultProfile</span></span>
<span data-ttu-id="631c8-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="631c8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="631c8-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="631c8-117">-InputObject</span></span>
<span data-ttu-id="631c8-118">A bemeneti objektum az a parancsmag: az ASR-feladat objektuma, amely a projektnek megfelelően folytatódik.</span><span class="sxs-lookup"><span data-stu-id="631c8-118">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

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

### <span data-ttu-id="631c8-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="631c8-119">-Name</span></span>
<span data-ttu-id="631c8-120">Adja meg az ASR-feladatot név szerint.</span><span class="sxs-lookup"><span data-stu-id="631c8-120">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="631c8-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="631c8-121">-Confirm</span></span>
<span data-ttu-id="631c8-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="631c8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="631c8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="631c8-123">-WhatIf</span></span>
<span data-ttu-id="631c8-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="631c8-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="631c8-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="631c8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="631c8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="631c8-126">CommonParameters</span></span>
<span data-ttu-id="631c8-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="631c8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="631c8-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="631c8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="631c8-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="631c8-129">INPUTS</span></span>

### <span data-ttu-id="631c8-130">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="631c8-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="631c8-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="631c8-131">OUTPUTS</span></span>

### <span data-ttu-id="631c8-132">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="631c8-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="631c8-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="631c8-133">NOTES</span></span>

## <span data-ttu-id="631c8-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="631c8-134">RELATED LINKS</span></span>

[<span data-ttu-id="631c8-135">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="631c8-135">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="631c8-136">Újraindítás – AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="631c8-136">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="631c8-137">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="631c8-137">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
