---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: DC151161-72C0-40F7-B2F0-45FA01142AE1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
ms.openlocfilehash: 89c4a6bd9d009456c97aa246f608c1920c27c823
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503376"
---
# <span data-ttu-id="170ca-101">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="170ca-101">Get-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="170ca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="170ca-102">SYNOPSIS</span></span>
<span data-ttu-id="170ca-103">A Feladatütemező munkalapjait kapja.</span><span class="sxs-lookup"><span data-stu-id="170ca-103">Gets Scheduler jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="170ca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="170ca-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> [-JobName <String>]
 [-JobState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="170ca-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="170ca-105">DESCRIPTION</span></span>
<span data-ttu-id="170ca-106">A **Get-AzureRmSchedulerJob** parancsmag Azure Scheduler-feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="170ca-106">The **Get-AzureRmSchedulerJob** cmdlet gets Azure Scheduler jobs.</span></span>

## <span data-ttu-id="170ca-107">Példák</span><span class="sxs-lookup"><span data-stu-id="170ca-107">EXAMPLES</span></span>

## <span data-ttu-id="170ca-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="170ca-108">PARAMETERS</span></span>

### <span data-ttu-id="170ca-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="170ca-109">-DefaultProfile</span></span>
<span data-ttu-id="170ca-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="170ca-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="170ca-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="170ca-111">-JobCollectionName</span></span>
<span data-ttu-id="170ca-112">Annak a webhelycsoporthoz a nevét adja meg, amely a beszerzéshez feladatokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="170ca-112">Specifies the name of a job collection that contains jobs to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170ca-113">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="170ca-113">-JobName</span></span>
<span data-ttu-id="170ca-114">A beolvasott feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="170ca-114">Specifies the name of a job to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170ca-115">-JobState</span><span class="sxs-lookup"><span data-stu-id="170ca-115">-JobState</span></span>
<span data-ttu-id="170ca-116">A beolvasott feladatok állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="170ca-116">Specifies a job state of jobs to get.</span></span>
<span data-ttu-id="170ca-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="170ca-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="170ca-118">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="170ca-118">Enabled</span></span> 
- <span data-ttu-id="170ca-119">Tiltva</span><span class="sxs-lookup"><span data-stu-id="170ca-119">Disabled</span></span> 
- <span data-ttu-id="170ca-120">Hibázott</span><span class="sxs-lookup"><span data-stu-id="170ca-120">Faulted</span></span> 
- <span data-ttu-id="170ca-121">Kész</span><span class="sxs-lookup"><span data-stu-id="170ca-121">Completed</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Faulted, Completed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170ca-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="170ca-122">-ResourceGroupName</span></span>
<span data-ttu-id="170ca-123">A beolvasott feladatok erőforráscsoport részét adja meg.</span><span class="sxs-lookup"><span data-stu-id="170ca-123">Specifies the resource group of the jobs to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170ca-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="170ca-124">CommonParameters</span></span>
<span data-ttu-id="170ca-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="170ca-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="170ca-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="170ca-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="170ca-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="170ca-127">INPUTS</span></span>

### <span data-ttu-id="170ca-128">System. String</span><span class="sxs-lookup"><span data-stu-id="170ca-128">System.String</span></span>

## <span data-ttu-id="170ca-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="170ca-129">OUTPUTS</span></span>

### <span data-ttu-id="170ca-130">Microsoft. Azure. Command. Scheduler. models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="170ca-130">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="170ca-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="170ca-131">NOTES</span></span>

## <span data-ttu-id="170ca-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="170ca-132">RELATED LINKS</span></span>

[<span data-ttu-id="170ca-133">Új – AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="170ca-133">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="170ca-134">Új – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="170ca-134">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="170ca-135">Új – AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="170ca-135">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="170ca-136">Új – AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="170ca-136">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="170ca-137">Új – AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="170ca-137">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="170ca-138">Remove-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="170ca-138">Remove-AzureRmSchedulerJob</span></span>](./Remove-AzureRmSchedulerJob.md)

[<span data-ttu-id="170ca-139">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="170ca-139">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="170ca-140">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="170ca-140">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="170ca-141">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="170ca-141">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="170ca-142">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="170ca-142">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


