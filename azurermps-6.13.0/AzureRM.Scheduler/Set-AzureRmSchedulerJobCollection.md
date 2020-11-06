---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F9CF1EEB-6EFF-4C24-AC79-1328034D22A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 535455f73795d85acf05da191694f35dbeee9ba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494930"
---
# <span data-ttu-id="d53c6-101">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d53c6-101">Set-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="d53c6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d53c6-102">SYNOPSIS</span></span>
<span data-ttu-id="d53c6-103">Begyűjti a feladatot.</span><span class="sxs-lookup"><span data-stu-id="d53c6-103">Modifies a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d53c6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d53c6-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-Location <String>]
 [-Plan <String>] [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d53c6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d53c6-105">DESCRIPTION</span></span>
<span data-ttu-id="d53c6-106">A **set-AzureRmSchedulerJobCollection** parancsmag az Azure Scheduler programban módosítja a beosztást.</span><span class="sxs-lookup"><span data-stu-id="d53c6-106">The **Set-AzureRmSchedulerJobCollection** cmdlet modifies a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="d53c6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d53c6-107">EXAMPLES</span></span>

## <span data-ttu-id="d53c6-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d53c6-108">PARAMETERS</span></span>

### <span data-ttu-id="d53c6-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d53c6-109">-DefaultProfile</span></span>
<span data-ttu-id="d53c6-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d53c6-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d53c6-111">-Gyakoriság</span><span class="sxs-lookup"><span data-stu-id="d53c6-111">-Frequency</span></span>
<span data-ttu-id="d53c6-112">Itt adhatja meg, hogy a feladatban milyen maximális gyakoriságot adhat meg a program a webhelycsoportban.</span><span class="sxs-lookup"><span data-stu-id="d53c6-112">Specifies the maximum frequency that you can specify on any job in the job collection.</span></span>
<span data-ttu-id="d53c6-113">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d53c6-113">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d53c6-114">Perces</span><span class="sxs-lookup"><span data-stu-id="d53c6-114">Minute</span></span> 
- <span data-ttu-id="d53c6-115">Óra</span><span class="sxs-lookup"><span data-stu-id="d53c6-115">Hour</span></span> 
- <span data-ttu-id="d53c6-116">Nap</span><span class="sxs-lookup"><span data-stu-id="d53c6-116">Day</span></span> 
- <span data-ttu-id="d53c6-117">Héten</span><span class="sxs-lookup"><span data-stu-id="d53c6-117">Week</span></span> 
- <span data-ttu-id="d53c6-118">Hónap</span><span class="sxs-lookup"><span data-stu-id="d53c6-118">Month</span></span>

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

### <span data-ttu-id="d53c6-119">-Intervallum</span><span class="sxs-lookup"><span data-stu-id="d53c6-119">-Interval</span></span>
<span data-ttu-id="d53c6-120">Az ismétlődés intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d53c6-120">Specifies an interval of recurrence.</span></span>

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

### <span data-ttu-id="d53c6-121">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="d53c6-121">-JobCollectionName</span></span>
<span data-ttu-id="d53c6-122">A begyűjtő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d53c6-122">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="d53c6-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="d53c6-123">-Location</span></span>
<span data-ttu-id="d53c6-124">Azt az Azure-területet adja meg, amelyben a webhelycsoport létezik.</span><span class="sxs-lookup"><span data-stu-id="d53c6-124">Specifies the Azure region in which the job collection exists.</span></span>

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

### <span data-ttu-id="d53c6-125">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="d53c6-125">-MaxJobCount</span></span>
<span data-ttu-id="d53c6-126">A begyűjtő által létrehozható feladatok maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d53c6-126">Specifies the maximum number of jobs that you can create in the job collection.</span></span>
<span data-ttu-id="d53c6-127">A maximális érték attól függ, hogy melyik csomagot adja meg a *terv* paraméter.</span><span class="sxs-lookup"><span data-stu-id="d53c6-127">The maximum depends on the plan that the *Plan* parameter specifies.</span></span>

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

### <span data-ttu-id="d53c6-128">-Terv</span><span class="sxs-lookup"><span data-stu-id="d53c6-128">-Plan</span></span>
<span data-ttu-id="d53c6-129">A begyűjtési terv megadása</span><span class="sxs-lookup"><span data-stu-id="d53c6-129">Specifies the job collection plan.</span></span>
<span data-ttu-id="d53c6-130">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d53c6-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d53c6-131">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="d53c6-131">Free</span></span> 
- <span data-ttu-id="d53c6-132">Standard</span><span class="sxs-lookup"><span data-stu-id="d53c6-132">Standard</span></span> 
- <span data-ttu-id="d53c6-133">P10Premium</span><span class="sxs-lookup"><span data-stu-id="d53c6-133">P10Premium</span></span> 
- <span data-ttu-id="d53c6-134">P20Premium</span><span class="sxs-lookup"><span data-stu-id="d53c6-134">P20Premium</span></span>

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

### <span data-ttu-id="d53c6-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d53c6-135">-ResourceGroupName</span></span>
<span data-ttu-id="d53c6-136">A begyűjtő erőforrás csoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d53c6-136">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="d53c6-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d53c6-137">-Confirm</span></span>
<span data-ttu-id="d53c6-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d53c6-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d53c6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d53c6-139">-WhatIf</span></span>
<span data-ttu-id="d53c6-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d53c6-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d53c6-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d53c6-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d53c6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d53c6-142">CommonParameters</span></span>
<span data-ttu-id="d53c6-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d53c6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d53c6-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d53c6-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d53c6-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d53c6-145">INPUTS</span></span>

### <span data-ttu-id="d53c6-146">System. String</span><span class="sxs-lookup"><span data-stu-id="d53c6-146">System.String</span></span>

## <span data-ttu-id="d53c6-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d53c6-147">OUTPUTS</span></span>

### <span data-ttu-id="d53c6-148">Microsoft. Azure. Command. Scheduler. models. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="d53c6-148">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="d53c6-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d53c6-149">NOTES</span></span>

## <span data-ttu-id="d53c6-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d53c6-150">RELATED LINKS</span></span>

[<span data-ttu-id="d53c6-151">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d53c6-151">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d53c6-152">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d53c6-152">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d53c6-153">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d53c6-153">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d53c6-154">Új – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d53c6-154">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d53c6-155">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d53c6-155">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)


