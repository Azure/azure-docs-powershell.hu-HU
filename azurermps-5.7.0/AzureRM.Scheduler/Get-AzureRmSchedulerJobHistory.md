---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: F6D8710D-1D42-493C-B7F1-EDA35FCCDC23
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjobhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
ms.openlocfilehash: 6c1582c8e82bf344685f9e1feb002625bddd6748
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672513"
---
# <span data-ttu-id="e4237-101">Get-AzureRmSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="e4237-101">Get-AzureRmSchedulerJobHistory</span></span>

## <span data-ttu-id="e4237-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e4237-102">SYNOPSIS</span></span>
<span data-ttu-id="e4237-103">A projekt előzményeit kapja.</span><span class="sxs-lookup"><span data-stu-id="e4237-103">Gets job history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4237-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e4237-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobHistory -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-JobExecutionStatus <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4237-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e4237-105">DESCRIPTION</span></span>
<span data-ttu-id="e4237-106">A **Get-AzureRmSchedulerJobHistory** parancsmag az Azure Scheduler-feladatok előzményeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e4237-106">The **Get-AzureRmSchedulerJobHistory** cmdlet gets history for an Azure Scheduler job.</span></span>

## <span data-ttu-id="e4237-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e4237-107">EXAMPLES</span></span>

## <span data-ttu-id="e4237-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e4237-108">PARAMETERS</span></span>

### <span data-ttu-id="e4237-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4237-109">-DefaultProfile</span></span>
<span data-ttu-id="e4237-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e4237-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4237-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="e4237-111">-JobCollectionName</span></span>
<span data-ttu-id="e4237-112">A begyűjtő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4237-112">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="e4237-113">-JobExecutionStatus</span><span class="sxs-lookup"><span data-stu-id="e4237-113">-JobExecutionStatus</span></span>
<span data-ttu-id="e4237-114">Egy feladat állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4237-114">Specifies the status of a job.</span></span>
<span data-ttu-id="e4237-115">Ez a parancsmag olyan előzményeket kap, amelyek megfelelnek a megadott állapotnak.</span><span class="sxs-lookup"><span data-stu-id="e4237-115">This cmdlet gets history that matches the status that you specify.</span></span>
<span data-ttu-id="e4237-116">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e4237-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e4237-117">Kész</span><span class="sxs-lookup"><span data-stu-id="e4237-117">Completed</span></span> 
- <span data-ttu-id="e4237-118">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="e4237-118">Failed</span></span> 
- <span data-ttu-id="e4237-119">Elhalasztották</span><span class="sxs-lookup"><span data-stu-id="e4237-119">Postponed</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Completed, Failed, Postponed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4237-120">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="e4237-120">-JobName</span></span>
<span data-ttu-id="e4237-121">Annak a feladatnak a nevét adja meg, amelyhez ez a parancsmag az előzményeket kapja.</span><span class="sxs-lookup"><span data-stu-id="e4237-121">Specifies the name of a job for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="e4237-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4237-122">-ResourceGroupName</span></span>
<span data-ttu-id="e4237-123">Azt az erőforráscsoport-csoportot adja meg, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="e4237-123">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="e4237-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4237-124">CommonParameters</span></span>
<span data-ttu-id="e4237-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e4237-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4237-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4237-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4237-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4237-127">INPUTS</span></span>

### <span data-ttu-id="e4237-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="e4237-128">None</span></span>
<span data-ttu-id="e4237-129">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="e4237-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e4237-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4237-130">OUTPUTS</span></span>

### <span data-ttu-id="e4237-131">Microsoft. Azure. Command. Scheduler. models. PSJobHistory</span><span class="sxs-lookup"><span data-stu-id="e4237-131">Microsoft.Azure.Commands.Scheduler.Models.PSJobHistory</span></span>

## <span data-ttu-id="e4237-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e4237-132">NOTES</span></span>

## <span data-ttu-id="e4237-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4237-133">RELATED LINKS</span></span>

[<span data-ttu-id="e4237-134">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="e4237-134">Get-AzureRmSchedulerJob</span></span>](./Get-AzureRmSchedulerJob.md)


