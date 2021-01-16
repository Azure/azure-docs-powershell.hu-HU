---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/stop-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: a86e58fe3c933ffaa9a382dc1e5140d3b42a34cb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358118"
---
# <span data-ttu-id="2eab4-101">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="2eab4-101">Stop-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="2eab4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2eab4-102">SYNOPSIS</span></span>
<span data-ttu-id="2eab4-103">Leállít egy Azure-webhely-helyreállítási feladatot.</span><span class="sxs-lookup"><span data-stu-id="2eab4-103">Stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="2eab4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2eab4-104">SYNTAX</span></span>

### <span data-ttu-id="2eab4-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2eab4-105">ByObject (Default)</span></span>
```
Stop-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2eab4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2eab4-106">ByName</span></span>
```
Stop-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2eab4-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2eab4-107">DESCRIPTION</span></span>
<span data-ttu-id="2eab4-108">A **Stop-AzRecoveryServicesAsr Job parancsmag** leállítja a megadott Azure-webhely-helyreállítási feladatot.</span><span class="sxs-lookup"><span data-stu-id="2eab4-108">The **Stop-AzRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="2eab4-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2eab4-109">EXAMPLES</span></span>

### <span data-ttu-id="2eab4-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="2eab4-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="2eab4-111">Megkísérli leállítani a megadott feladatot, és egy frissített ASR-feladatobjektumot ad vissza.</span><span class="sxs-lookup"><span data-stu-id="2eab4-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="2eab4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2eab4-112">PARAMETERS</span></span>

### <span data-ttu-id="2eab4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eab4-113">-DefaultProfile</span></span>
<span data-ttu-id="2eab4-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2eab4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2eab4-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2eab4-115">-InputObject</span></span>
<span data-ttu-id="2eab4-116">Bemeneti objektum: A leállítani kívánt ASR-feladatnak megfelelő ASR-feladatobjektum megadása</span><span class="sxs-lookup"><span data-stu-id="2eab4-116">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

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

### <span data-ttu-id="2eab4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2eab4-117">-Name</span></span>
<span data-ttu-id="2eab4-118">Adja meg azt az ASR-feladatot, amelyet le kell állítani az ASR-feladat neve alapján.</span><span class="sxs-lookup"><span data-stu-id="2eab4-118">Specify the ASR Job to be stopped by the ASR job name.</span></span>

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

### <span data-ttu-id="2eab4-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2eab4-119">-Confirm</span></span>
<span data-ttu-id="2eab4-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2eab4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2eab4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2eab4-121">-WhatIf</span></span>
<span data-ttu-id="2eab4-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2eab4-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2eab4-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2eab4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2eab4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eab4-124">CommonParameters</span></span>
<span data-ttu-id="2eab4-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eab4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eab4-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2eab4-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eab4-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2eab4-127">INPUTS</span></span>

### <span data-ttu-id="2eab4-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="2eab4-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2eab4-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2eab4-129">OUTPUTS</span></span>

### <span data-ttu-id="2eab4-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="2eab4-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2eab4-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2eab4-131">NOTES</span></span>

## <span data-ttu-id="2eab4-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2eab4-132">RELATED LINKS</span></span>

[<span data-ttu-id="2eab4-133">Get-AzRecoveryServicesAsrService</span><span class="sxs-lookup"><span data-stu-id="2eab4-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="2eab4-134">Restart-AzRecoveryServicesAsrService</span><span class="sxs-lookup"><span data-stu-id="2eab4-134">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="2eab4-135">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="2eab4-135">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)
