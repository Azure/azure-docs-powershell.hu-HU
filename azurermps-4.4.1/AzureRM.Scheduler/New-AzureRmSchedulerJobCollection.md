---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: D82270AD-50C2-4980-ABE2-58049C187875
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: d3577b906134a940a9339441f305d98c32b8fe74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501624"
---
# <span data-ttu-id="57678-101">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="57678-101">New-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="57678-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="57678-102">SYNOPSIS</span></span>
<span data-ttu-id="57678-103">Begyűjtőt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="57678-103">Creates a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57678-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="57678-104">SYNTAX</span></span>

```
New-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> -Location <String>
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57678-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="57678-105">DESCRIPTION</span></span>
<span data-ttu-id="57678-106">A **New-AzureRmSchedulerJobCollection** parancsmag létrehoz egy munkagyűjteményt az Azure schedulerben.</span><span class="sxs-lookup"><span data-stu-id="57678-106">The **New-AzureRmSchedulerJobCollection** cmdlet creates a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="57678-107">Példák</span><span class="sxs-lookup"><span data-stu-id="57678-107">EXAMPLES</span></span>

## <span data-ttu-id="57678-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="57678-108">PARAMETERS</span></span>

### <span data-ttu-id="57678-109">-Gyakoriság</span><span class="sxs-lookup"><span data-stu-id="57678-109">-Frequency</span></span>
<span data-ttu-id="57678-110">Itt adhatja meg, hogy a feladatban milyen maximális gyakoriságot adhat meg a program a webhelycsoportban.</span><span class="sxs-lookup"><span data-stu-id="57678-110">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="57678-111">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="57678-111">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="57678-112">Perces</span><span class="sxs-lookup"><span data-stu-id="57678-112">Minute</span></span> 
- <span data-ttu-id="57678-113">Óra</span><span class="sxs-lookup"><span data-stu-id="57678-113">Hour</span></span> 
- <span data-ttu-id="57678-114">Nap</span><span class="sxs-lookup"><span data-stu-id="57678-114">Day</span></span> 
- <span data-ttu-id="57678-115">Héten</span><span class="sxs-lookup"><span data-stu-id="57678-115">Week</span></span> 
- <span data-ttu-id="57678-116">Hónap</span><span class="sxs-lookup"><span data-stu-id="57678-116">Month</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57678-117">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="57678-117">-Interval</span></span>
<span data-ttu-id="57678-118">Az ismétlődés intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="57678-118">Specifies an interval of recurrence.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57678-119">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="57678-119">-JobCollectionName</span></span>
<span data-ttu-id="57678-120">A begyűjtő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="57678-120">Specifies a name for the job collection.</span></span>

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

### <span data-ttu-id="57678-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="57678-121">-Location</span></span>
<span data-ttu-id="57678-122">Azt az Azure-területet adja meg, amelyben ez a parancsmag létrehozta a begyűjtési feladatot.</span><span class="sxs-lookup"><span data-stu-id="57678-122">Specifies the Azure region in which this cmdlet creates the job collection.</span></span>

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

### <span data-ttu-id="57678-123">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="57678-123">-MaxJobCount</span></span>
<span data-ttu-id="57678-124">A begyűjtő által létrehozható feladatok maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="57678-124">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="57678-125">A maximális érték attól függ, hogy melyik csomagot adja meg a *terv* paraméter.</span><span class="sxs-lookup"><span data-stu-id="57678-125">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57678-126">-Terv</span><span class="sxs-lookup"><span data-stu-id="57678-126">-Plan</span></span>
<span data-ttu-id="57678-127">A begyűjtési terv megadása</span><span class="sxs-lookup"><span data-stu-id="57678-127">Specifies the job collection plan.</span></span>
<span data-ttu-id="57678-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="57678-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="57678-129">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="57678-129">Free</span></span> 
- <span data-ttu-id="57678-130">Standard</span><span class="sxs-lookup"><span data-stu-id="57678-130">Standard</span></span> 
- <span data-ttu-id="57678-131">P10Premium</span><span class="sxs-lookup"><span data-stu-id="57678-131">P10Premium</span></span> 
- <span data-ttu-id="57678-132">P20Premium</span><span class="sxs-lookup"><span data-stu-id="57678-132">P20Premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Standard, P10Premium, P20Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57678-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57678-133">-ResourceGroupName</span></span>
<span data-ttu-id="57678-134">A begyűjtő erőforrás csoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="57678-134">Specifies the resource group for the job collection.</span></span>

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

### <span data-ttu-id="57678-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="57678-135">-Confirm</span></span>
<span data-ttu-id="57678-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="57678-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57678-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57678-137">-WhatIf</span></span>
<span data-ttu-id="57678-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="57678-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57678-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="57678-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57678-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57678-140">-DefaultProfile</span></span>
<span data-ttu-id="57678-141">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="57678-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57678-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57678-142">CommonParameters</span></span>
<span data-ttu-id="57678-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="57678-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57678-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57678-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57678-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="57678-145">INPUTS</span></span>

## <span data-ttu-id="57678-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="57678-146">OUTPUTS</span></span>

### <span data-ttu-id="57678-147">Microsoft. Azure. Command. Scheduler. models. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="57678-147">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="57678-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="57678-148">NOTES</span></span>

## <span data-ttu-id="57678-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="57678-149">RELATED LINKS</span></span>

[<span data-ttu-id="57678-150">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="57678-150">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="57678-151">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="57678-151">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="57678-152">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="57678-152">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="57678-153">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="57678-153">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="57678-154">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="57678-154">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


