---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: D82270AD-50C2-4980-ABE2-58049C187875
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 479b91f222852ebfc356d320cf880eb2ae99db6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493938"
---
# <span data-ttu-id="d7333-101">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d7333-101">New-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="d7333-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7333-102">SYNOPSIS</span></span>
<span data-ttu-id="d7333-103">Begyűjtőt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d7333-103">Creates a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7333-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7333-104">SYNTAX</span></span>

```
New-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> -Location <String>
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7333-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7333-105">DESCRIPTION</span></span>
<span data-ttu-id="d7333-106">A **New-AzureRmSchedulerJobCollection** parancsmag létrehoz egy munkagyűjteményt az Azure schedulerben.</span><span class="sxs-lookup"><span data-stu-id="d7333-106">The **New-AzureRmSchedulerJobCollection** cmdlet creates a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="d7333-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d7333-107">EXAMPLES</span></span>

## <span data-ttu-id="d7333-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7333-108">PARAMETERS</span></span>

### <span data-ttu-id="d7333-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7333-109">-DefaultProfile</span></span>
<span data-ttu-id="d7333-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d7333-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7333-111">-Gyakoriság</span><span class="sxs-lookup"><span data-stu-id="d7333-111">-Frequency</span></span>
<span data-ttu-id="d7333-112">Itt adhatja meg, hogy a feladatban milyen maximális gyakoriságot adhat meg a program a webhelycsoportban.</span><span class="sxs-lookup"><span data-stu-id="d7333-112">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="d7333-113">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d7333-113">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d7333-114">Perces</span><span class="sxs-lookup"><span data-stu-id="d7333-114">Minute</span></span> 
- <span data-ttu-id="d7333-115">Óra</span><span class="sxs-lookup"><span data-stu-id="d7333-115">Hour</span></span> 
- <span data-ttu-id="d7333-116">Nap</span><span class="sxs-lookup"><span data-stu-id="d7333-116">Day</span></span> 
- <span data-ttu-id="d7333-117">Héten</span><span class="sxs-lookup"><span data-stu-id="d7333-117">Week</span></span> 
- <span data-ttu-id="d7333-118">Hónap</span><span class="sxs-lookup"><span data-stu-id="d7333-118">Month</span></span>

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

### <span data-ttu-id="d7333-119">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="d7333-119">-Interval</span></span>
<span data-ttu-id="d7333-120">Az ismétlődés intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7333-120">Specifies an interval of recurrence.</span></span>

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

### <span data-ttu-id="d7333-121">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="d7333-121">-JobCollectionName</span></span>
<span data-ttu-id="d7333-122">A begyűjtő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7333-122">Specifies a name for the job collection.</span></span>

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

### <span data-ttu-id="d7333-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="d7333-123">-Location</span></span>
<span data-ttu-id="d7333-124">Azt az Azure-területet adja meg, amelyben ez a parancsmag létrehozta a begyűjtési feladatot.</span><span class="sxs-lookup"><span data-stu-id="d7333-124">Specifies the Azure region in which this cmdlet creates the job collection.</span></span>

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

### <span data-ttu-id="d7333-125">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="d7333-125">-MaxJobCount</span></span>
<span data-ttu-id="d7333-126">A begyűjtő által létrehozható feladatok maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7333-126">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="d7333-127">A maximális érték attól függ, hogy melyik csomagot adja meg a *terv* paraméter.</span><span class="sxs-lookup"><span data-stu-id="d7333-127">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

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

### <span data-ttu-id="d7333-128">-Terv</span><span class="sxs-lookup"><span data-stu-id="d7333-128">-Plan</span></span>
<span data-ttu-id="d7333-129">A begyűjtési terv megadása</span><span class="sxs-lookup"><span data-stu-id="d7333-129">Specifies the job collection plan.</span></span>
<span data-ttu-id="d7333-130">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d7333-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d7333-131">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="d7333-131">Free</span></span> 
- <span data-ttu-id="d7333-132">Standard</span><span class="sxs-lookup"><span data-stu-id="d7333-132">Standard</span></span> 
- <span data-ttu-id="d7333-133">P10Premium</span><span class="sxs-lookup"><span data-stu-id="d7333-133">P10Premium</span></span> 
- <span data-ttu-id="d7333-134">P20Premium</span><span class="sxs-lookup"><span data-stu-id="d7333-134">P20Premium</span></span>

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

### <span data-ttu-id="d7333-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7333-135">-ResourceGroupName</span></span>
<span data-ttu-id="d7333-136">A begyűjtő erőforrás csoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7333-136">Specifies the resource group for the job collection.</span></span>

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

### <span data-ttu-id="d7333-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d7333-137">-Confirm</span></span>
<span data-ttu-id="d7333-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d7333-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7333-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7333-139">-WhatIf</span></span>
<span data-ttu-id="d7333-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d7333-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7333-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d7333-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7333-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7333-142">CommonParameters</span></span>
<span data-ttu-id="d7333-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7333-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7333-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7333-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7333-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7333-145">INPUTS</span></span>

### <span data-ttu-id="d7333-146">System. String</span><span class="sxs-lookup"><span data-stu-id="d7333-146">System.String</span></span>

## <span data-ttu-id="d7333-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7333-147">OUTPUTS</span></span>

### <span data-ttu-id="d7333-148">Microsoft. Azure. Command. Scheduler. models. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="d7333-148">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="d7333-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7333-149">NOTES</span></span>

## <span data-ttu-id="d7333-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7333-150">RELATED LINKS</span></span>

[<span data-ttu-id="d7333-151">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d7333-151">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d7333-152">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d7333-152">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d7333-153">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d7333-153">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d7333-154">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d7333-154">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d7333-155">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d7333-155">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


