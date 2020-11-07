---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: DC151161-72C0-40F7-B2F0-45FA01142AE1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
ms.openlocfilehash: d22f1acf8f99f15df83be95aafdc8ff0aefd2a29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679706"
---
# <span data-ttu-id="d7b98-101">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="d7b98-101">Get-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="d7b98-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7b98-102">SYNOPSIS</span></span>
<span data-ttu-id="d7b98-103">A Feladatütemező munkalapjait kapja.</span><span class="sxs-lookup"><span data-stu-id="d7b98-103">Gets Scheduler jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7b98-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7b98-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> [-JobName <String>]
 [-JobState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7b98-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7b98-105">DESCRIPTION</span></span>
<span data-ttu-id="d7b98-106">A **Get-AzureRmSchedulerJob** parancsmag Azure Scheduler-feladatokat kap.</span><span class="sxs-lookup"><span data-stu-id="d7b98-106">The **Get-AzureRmSchedulerJob** cmdlet gets Azure Scheduler jobs.</span></span>

## <span data-ttu-id="d7b98-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d7b98-107">EXAMPLES</span></span>

## <span data-ttu-id="d7b98-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7b98-108">PARAMETERS</span></span>

### <span data-ttu-id="d7b98-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7b98-109">-DefaultProfile</span></span>
<span data-ttu-id="d7b98-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d7b98-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7b98-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="d7b98-111">-JobCollectionName</span></span>
<span data-ttu-id="d7b98-112">Annak a webhelycsoporthoz a nevét adja meg, amely a beszerzéshez feladatokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="d7b98-112">Specifies the name of a job collection that contains jobs to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7b98-113">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="d7b98-113">-JobName</span></span>
<span data-ttu-id="d7b98-114">A beolvasott feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7b98-114">Specifies the name of a job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7b98-115">-JobState</span><span class="sxs-lookup"><span data-stu-id="d7b98-115">-JobState</span></span>
<span data-ttu-id="d7b98-116">A beolvasott feladatok állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7b98-116">Specifies a job state of jobs to get.</span></span>
<span data-ttu-id="d7b98-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d7b98-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d7b98-118">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="d7b98-118">Enabled</span></span> 
- <span data-ttu-id="d7b98-119">Tiltva</span><span class="sxs-lookup"><span data-stu-id="d7b98-119">Disabled</span></span> 
- <span data-ttu-id="d7b98-120">Hibázott</span><span class="sxs-lookup"><span data-stu-id="d7b98-120">Faulted</span></span> 
- <span data-ttu-id="d7b98-121">Kész</span><span class="sxs-lookup"><span data-stu-id="d7b98-121">Completed</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled, Faulted, Completed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7b98-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7b98-122">-ResourceGroupName</span></span>
<span data-ttu-id="d7b98-123">A beolvasott feladatok erőforráscsoport részét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7b98-123">Specifies the resource group of the jobs to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7b98-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7b98-124">CommonParameters</span></span>
<span data-ttu-id="d7b98-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7b98-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7b98-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7b98-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7b98-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7b98-127">INPUTS</span></span>

### <span data-ttu-id="d7b98-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="d7b98-128">None</span></span>
<span data-ttu-id="d7b98-129">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="d7b98-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d7b98-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7b98-130">OUTPUTS</span></span>

### <span data-ttu-id="d7b98-131">Microsoft. Azure. Command. Scheduler. models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="d7b98-131">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="d7b98-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7b98-132">NOTES</span></span>

## <span data-ttu-id="d7b98-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7b98-133">RELATED LINKS</span></span>

[<span data-ttu-id="d7b98-134">Új – AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="d7b98-134">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="d7b98-135">Új – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d7b98-135">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d7b98-136">Új – AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="d7b98-136">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="d7b98-137">Új – AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="d7b98-137">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="d7b98-138">Új – AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="d7b98-138">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="d7b98-139">Remove-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="d7b98-139">Remove-AzureRmSchedulerJob</span></span>](./Remove-AzureRmSchedulerJob.md)

[<span data-ttu-id="d7b98-140">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="d7b98-140">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="d7b98-141">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="d7b98-141">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="d7b98-142">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="d7b98-142">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="d7b98-143">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="d7b98-143">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


