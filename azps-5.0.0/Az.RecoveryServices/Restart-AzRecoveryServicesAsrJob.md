---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restart-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: cf8b2617e01e472de32f128d4907d68edaebb2e6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188021"
---
# <span data-ttu-id="0d056-101">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0d056-101">Restart-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="0d056-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0d056-102">SYNOPSIS</span></span>
<span data-ttu-id="0d056-103">Az Azure webhely-helyreállítási feladat újraindítása.</span><span class="sxs-lookup"><span data-stu-id="0d056-103">Restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="0d056-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0d056-104">SYNTAX</span></span>

### <span data-ttu-id="0d056-105">ByObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0d056-105">ByObject (Default)</span></span>
```
Restart-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d056-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0d056-106">ByName</span></span>
```
Restart-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0d056-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0d056-107">DESCRIPTION</span></span>
<span data-ttu-id="0d056-108">Az **Újraindítás – AzRecoveryServicesAsrJob** parancsmag újraindítja az Azure webhely-helyreállítási feladatot.</span><span class="sxs-lookup"><span data-stu-id="0d056-108">The **Restart-AzRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="0d056-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0d056-109">EXAMPLES</span></span>

### <span data-ttu-id="0d056-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0d056-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="0d056-111">A megadott ASR-feladat újraindítása, és az ASR-feladat frissített automatikus helyreállítási feladatát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="0d056-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="0d056-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0d056-112">PARAMETERS</span></span>

### <span data-ttu-id="0d056-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d056-113">-DefaultProfile</span></span>
<span data-ttu-id="0d056-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0d056-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="0d056-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d056-115">-InputObject</span></span>
<span data-ttu-id="0d056-116">A bemeneti objektum az a parancsmag: az ASR-feladat objektuma, amelyet az ASR-feladatnak megfelelően kell elindítani.</span><span class="sxs-lookup"><span data-stu-id="0d056-116">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>


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

### <span data-ttu-id="0d056-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0d056-117">-Name</span></span>
<span data-ttu-id="0d056-118">Adja meg a feladatot név szerint.</span><span class="sxs-lookup"><span data-stu-id="0d056-118">Specify the job by name.</span></span>

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

### <span data-ttu-id="0d056-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0d056-119">-Confirm</span></span>
<span data-ttu-id="0d056-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0d056-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d056-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d056-121">-WhatIf</span></span>
<span data-ttu-id="0d056-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0d056-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d056-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0d056-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d056-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d056-124">CommonParameters</span></span>
<span data-ttu-id="0d056-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0d056-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d056-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0d056-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d056-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d056-127">INPUTS</span></span>

### <span data-ttu-id="0d056-128">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0d056-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0d056-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d056-129">OUTPUTS</span></span>

### <span data-ttu-id="0d056-130">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0d056-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0d056-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0d056-131">NOTES</span></span>

## <span data-ttu-id="0d056-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0d056-132">RELATED LINKS</span></span>

[<span data-ttu-id="0d056-133">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0d056-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="0d056-134">Önéletrajz – AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0d056-134">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="0d056-135">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0d056-135">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
