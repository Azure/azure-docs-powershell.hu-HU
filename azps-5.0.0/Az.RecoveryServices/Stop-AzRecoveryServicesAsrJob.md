---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/stop-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: a86e58fe3c933ffaa9a382dc1e5140d3b42a34cb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186849"
---
# <span data-ttu-id="51ffd-101">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="51ffd-101">Stop-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="51ffd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="51ffd-102">SYNOPSIS</span></span>
<span data-ttu-id="51ffd-103">Az Azure webhely-helyreállítási feladat leállítása.</span><span class="sxs-lookup"><span data-stu-id="51ffd-103">Stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="51ffd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="51ffd-104">SYNTAX</span></span>

### <span data-ttu-id="51ffd-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="51ffd-105">ByObject (Default)</span></span>
```
Stop-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51ffd-106">ByName</span><span class="sxs-lookup"><span data-stu-id="51ffd-106">ByName</span></span>
```
Stop-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="51ffd-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="51ffd-107">DESCRIPTION</span></span>
<span data-ttu-id="51ffd-108">A **stop-AzRecoveryServicesAsrJob** parancsmag leállítja a megadott Azure-webhely helyreállítási feladatát.</span><span class="sxs-lookup"><span data-stu-id="51ffd-108">The **Stop-AzRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="51ffd-109">Példák</span><span class="sxs-lookup"><span data-stu-id="51ffd-109">EXAMPLES</span></span>

### <span data-ttu-id="51ffd-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="51ffd-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="51ffd-111">Megkísérli leállítani a megadott feladatot, és egy frissített ASR-objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="51ffd-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="51ffd-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="51ffd-112">PARAMETERS</span></span>

### <span data-ttu-id="51ffd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51ffd-113">-DefaultProfile</span></span>
<span data-ttu-id="51ffd-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="51ffd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="51ffd-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51ffd-115">-InputObject</span></span>
<span data-ttu-id="51ffd-116">Beviteli objektum: Itt adhatja meg az ASR-feladat leállításának megfelelő ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="51ffd-116">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

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

### <span data-ttu-id="51ffd-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="51ffd-117">-Name</span></span>
<span data-ttu-id="51ffd-118">Adja meg azt az ASR-feladatot, amelyet az ASR-feladat nevében le kell állítani.</span><span class="sxs-lookup"><span data-stu-id="51ffd-118">Specify the ASR Job to be stopped by the ASR job name.</span></span>

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

### <span data-ttu-id="51ffd-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="51ffd-119">-Confirm</span></span>
<span data-ttu-id="51ffd-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="51ffd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51ffd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51ffd-121">-WhatIf</span></span>
<span data-ttu-id="51ffd-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="51ffd-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51ffd-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="51ffd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51ffd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51ffd-124">CommonParameters</span></span>
<span data-ttu-id="51ffd-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="51ffd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51ffd-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="51ffd-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51ffd-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="51ffd-127">INPUTS</span></span>

### <span data-ttu-id="51ffd-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="51ffd-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="51ffd-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51ffd-129">OUTPUTS</span></span>

### <span data-ttu-id="51ffd-130">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="51ffd-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="51ffd-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="51ffd-131">NOTES</span></span>

## <span data-ttu-id="51ffd-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51ffd-132">RELATED LINKS</span></span>

[<span data-ttu-id="51ffd-133">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="51ffd-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="51ffd-134">Újraindítás – AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="51ffd-134">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="51ffd-135">Önéletrajz – AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="51ffd-135">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)