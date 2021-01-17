---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restart-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: cf8b2617e01e472de32f128d4907d68edaebb2e6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468633"
---
# <span data-ttu-id="97d4f-101">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="97d4f-101">Restart-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="97d4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97d4f-102">SYNOPSIS</span></span>
<span data-ttu-id="97d4f-103">Újraindít egy Azure-webhely-helyreállítási feladatot.</span><span class="sxs-lookup"><span data-stu-id="97d4f-103">Restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="97d4f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="97d4f-104">SYNTAX</span></span>

### <span data-ttu-id="97d4f-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="97d4f-105">ByObject (Default)</span></span>
```
Restart-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97d4f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="97d4f-106">ByName</span></span>
```
Restart-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="97d4f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="97d4f-107">DESCRIPTION</span></span>
<span data-ttu-id="97d4f-108">Az **Restart-AzRecoveryServicesAsr Job parancsmag** újraindít egy Azure-webhely-helyreállítási feladatot.</span><span class="sxs-lookup"><span data-stu-id="97d4f-108">The **Restart-AzRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="97d4f-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="97d4f-109">EXAMPLES</span></span>

### <span data-ttu-id="97d4f-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="97d4f-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="97d4f-111">Újraindítja a megadott ASR-feladatot, és visszaadja az ASR-feladat frissített ASR-feladatobjektumát.</span><span class="sxs-lookup"><span data-stu-id="97d4f-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="97d4f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97d4f-112">PARAMETERS</span></span>

### <span data-ttu-id="97d4f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97d4f-113">-DefaultProfile</span></span>
<span data-ttu-id="97d4f-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="97d4f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="97d4f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97d4f-115">-InputObject</span></span>
<span data-ttu-id="97d4f-116">A parancsmag bemeneti objektuma: Az újraindítani szükséges ASR-feladatnak megfelelő ASR-feladatobjektum</span><span class="sxs-lookup"><span data-stu-id="97d4f-116">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>


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

### <span data-ttu-id="97d4f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="97d4f-117">-Name</span></span>
<span data-ttu-id="97d4f-118">Adja meg a feladatot név szerint.</span><span class="sxs-lookup"><span data-stu-id="97d4f-118">Specify the job by name.</span></span>

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

### <span data-ttu-id="97d4f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="97d4f-119">-Confirm</span></span>
<span data-ttu-id="97d4f-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="97d4f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97d4f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97d4f-121">-WhatIf</span></span>
<span data-ttu-id="97d4f-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="97d4f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97d4f-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="97d4f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97d4f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97d4f-124">CommonParameters</span></span>
<span data-ttu-id="97d4f-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97d4f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97d4f-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97d4f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97d4f-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="97d4f-127">INPUTS</span></span>

### <span data-ttu-id="97d4f-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="97d4f-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="97d4f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97d4f-129">OUTPUTS</span></span>

### <span data-ttu-id="97d4f-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="97d4f-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="97d4f-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="97d4f-131">NOTES</span></span>

## <span data-ttu-id="97d4f-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97d4f-132">RELATED LINKS</span></span>

[<span data-ttu-id="97d4f-133">Get-AzRecoveryServicesAsrService</span><span class="sxs-lookup"><span data-stu-id="97d4f-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="97d4f-134">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="97d4f-134">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="97d4f-135">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="97d4f-135">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
