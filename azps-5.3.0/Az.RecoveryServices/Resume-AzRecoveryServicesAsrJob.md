---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/resume-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 6af467e5fd90a7d3028d67297b62f517f512b1b1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467242"
---
# <span data-ttu-id="b1ab0-101">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="b1ab0-101">Resume-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="b1ab0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1ab0-102">SYNOPSIS</span></span>
<span data-ttu-id="b1ab0-103">Egy felfüggesztett Azure-webhely-helyreállítási feladat folytatása.</span><span class="sxs-lookup"><span data-stu-id="b1ab0-103">Resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="b1ab0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b1ab0-104">SYNTAX</span></span>

### <span data-ttu-id="b1ab0-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b1ab0-105">ByObject (Default)</span></span>
```
Resume-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1ab0-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b1ab0-106">ByName</span></span>
```
Resume-AzRecoveryServicesAsrJob -Name <String> [-Comment <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1ab0-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b1ab0-107">DESCRIPTION</span></span>
<span data-ttu-id="b1ab0-108">A **Resume-AzRecoveryServicesAsr Job parancsmag** egy felfüggesztett Azure-webhely-helyreállítási feladatot folytat.</span><span class="sxs-lookup"><span data-stu-id="b1ab0-108">The **Resume-AzRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="b1ab0-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b1ab0-109">EXAMPLES</span></span>

### <span data-ttu-id="b1ab0-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="b1ab0-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="b1ab0-111">Folytassa a megadott feladatot, ha az várakozási vagy felfüggesztett állapotban van, és visszaadja az ASR-feladatnak megfelelő frissített ASR-feladatobjektumot.</span><span class="sxs-lookup"><span data-stu-id="b1ab0-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="b1ab0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1ab0-112">PARAMETERS</span></span>

### <span data-ttu-id="b1ab0-113">-Comment</span><span class="sxs-lookup"><span data-stu-id="b1ab0-113">-Comment</span></span>
<span data-ttu-id="b1ab0-114">A feladatnapló megjegyzései.</span><span class="sxs-lookup"><span data-stu-id="b1ab0-114">Comments for the job log.</span></span>

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

### <span data-ttu-id="b1ab0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1ab0-115">-DefaultProfile</span></span>
<span data-ttu-id="b1ab0-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b1ab0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b1ab0-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1ab0-117">-InputObject</span></span>
<span data-ttu-id="b1ab0-118">A parancsmag bemeneti objektuma: A feladatnak megfelelő ASR-feladat objektum.</span><span class="sxs-lookup"><span data-stu-id="b1ab0-118">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

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

### <span data-ttu-id="b1ab0-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b1ab0-119">-Name</span></span>
<span data-ttu-id="b1ab0-120">Adja meg az ASR-feladatot név szerint.</span><span class="sxs-lookup"><span data-stu-id="b1ab0-120">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="b1ab0-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1ab0-121">-Confirm</span></span>
<span data-ttu-id="b1ab0-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b1ab0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1ab0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1ab0-123">-WhatIf</span></span>
<span data-ttu-id="b1ab0-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b1ab0-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1ab0-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b1ab0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1ab0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1ab0-126">CommonParameters</span></span>
<span data-ttu-id="b1ab0-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1ab0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1ab0-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1ab0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1ab0-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b1ab0-129">INPUTS</span></span>

### <span data-ttu-id="b1ab0-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="b1ab0-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b1ab0-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1ab0-131">OUTPUTS</span></span>

### <span data-ttu-id="b1ab0-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="b1ab0-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b1ab0-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b1ab0-133">NOTES</span></span>

## <span data-ttu-id="b1ab0-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1ab0-134">RELATED LINKS</span></span>

[<span data-ttu-id="b1ab0-135">Get-AzRecoveryServicesAsrService</span><span class="sxs-lookup"><span data-stu-id="b1ab0-135">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="b1ab0-136">Restart-AzRecoveryServicesAsrService</span><span class="sxs-lookup"><span data-stu-id="b1ab0-136">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="b1ab0-137">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="b1ab0-137">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
