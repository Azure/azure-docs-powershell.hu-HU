---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F6D8710D-1D42-493C-B7F1-EDA35FCCDC23
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
ms.openlocfilehash: 7eec69a441efbf1a4d9f73e85a0385c24a012e34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501628"
---
# <span data-ttu-id="3bed0-101">Get-AzureRmSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="3bed0-101">Get-AzureRmSchedulerJobHistory</span></span>

## <span data-ttu-id="3bed0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3bed0-102">SYNOPSIS</span></span>
<span data-ttu-id="3bed0-103">A projekt előzményeit kapja.</span><span class="sxs-lookup"><span data-stu-id="3bed0-103">Gets job history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3bed0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3bed0-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobHistory -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-JobExecutionStatus <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bed0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3bed0-105">DESCRIPTION</span></span>
<span data-ttu-id="3bed0-106">A **Get-AzureRmSchedulerJobHistory** parancsmag az Azure Scheduler-feladatok előzményeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3bed0-106">The **Get-AzureRmSchedulerJobHistory** cmdlet gets history for an Azure Scheduler job.</span></span>

## <span data-ttu-id="3bed0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3bed0-107">EXAMPLES</span></span>

## <span data-ttu-id="3bed0-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3bed0-108">PARAMETERS</span></span>

### <span data-ttu-id="3bed0-109">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="3bed0-109">-JobCollectionName</span></span>
<span data-ttu-id="3bed0-110">A begyűjtő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3bed0-110">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="3bed0-111">-JobExecutionStatus</span><span class="sxs-lookup"><span data-stu-id="3bed0-111">-JobExecutionStatus</span></span>
<span data-ttu-id="3bed0-112">Egy feladat állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3bed0-112">Specifies the status of a job.</span></span>
<span data-ttu-id="3bed0-113">Ez a parancsmag olyan előzményeket kap, amelyek megfelelnek a megadott állapotnak.</span><span class="sxs-lookup"><span data-stu-id="3bed0-113">This cmdlet gets history that matches the status that you specify.</span></span>
<span data-ttu-id="3bed0-114">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="3bed0-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3bed0-115">Kész</span><span class="sxs-lookup"><span data-stu-id="3bed0-115">Completed</span></span> 
- <span data-ttu-id="3bed0-116">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="3bed0-116">Failed</span></span> 
- <span data-ttu-id="3bed0-117">Elhalasztották</span><span class="sxs-lookup"><span data-stu-id="3bed0-117">Postponed</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Completed, Failed, Postponed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bed0-118">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="3bed0-118">-JobName</span></span>
<span data-ttu-id="3bed0-119">Annak a feladatnak a nevét adja meg, amelyhez ez a parancsmag az előzményeket kapja.</span><span class="sxs-lookup"><span data-stu-id="3bed0-119">Specifies the name of a job for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="3bed0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bed0-120">-ResourceGroupName</span></span>
<span data-ttu-id="3bed0-121">Azt az erőforráscsoport-csoportot adja meg, amelyhez a projekt tartozik.</span><span class="sxs-lookup"><span data-stu-id="3bed0-121">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="3bed0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bed0-122">-DefaultProfile</span></span>
<span data-ttu-id="3bed0-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3bed0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3bed0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bed0-124">CommonParameters</span></span>
<span data-ttu-id="3bed0-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3bed0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bed0-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bed0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bed0-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3bed0-127">INPUTS</span></span>

## <span data-ttu-id="3bed0-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3bed0-128">OUTPUTS</span></span>

### <span data-ttu-id="3bed0-129">Microsoft. Azure. Command. Scheduler. models. PSJobHistory</span><span class="sxs-lookup"><span data-stu-id="3bed0-129">Microsoft.Azure.Commands.Scheduler.Models.PSJobHistory</span></span>

## <span data-ttu-id="3bed0-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3bed0-130">NOTES</span></span>

## <span data-ttu-id="3bed0-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3bed0-131">RELATED LINKS</span></span>

[<span data-ttu-id="3bed0-132">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="3bed0-132">Get-AzureRmSchedulerJob</span></span>](./Get-AzureRmSchedulerJob.md)


