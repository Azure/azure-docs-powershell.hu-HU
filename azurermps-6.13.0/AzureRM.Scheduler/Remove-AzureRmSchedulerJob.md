---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 774699A8-8916-4F2A-973E-97E5E487D42E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/remove-azurermschedulerjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJob.md
ms.openlocfilehash: 6a15f51290efec856494737881693c3d1fae0620
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493934"
---
# <span data-ttu-id="030b4-101">Remove-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="030b4-101">Remove-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="030b4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="030b4-102">SYNOPSIS</span></span>
<span data-ttu-id="030b4-103">A Feladatütemező feladatát távolítja el.</span><span class="sxs-lookup"><span data-stu-id="030b4-103">Removes a Scheduler job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="030b4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="030b4-104">SYNTAX</span></span>

```
Remove-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="030b4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="030b4-105">DESCRIPTION</span></span>
<span data-ttu-id="030b4-106">A **Remove-AzureRmSchedulerJob** parancsmag eltávolítja az Azure Scheduler-feladatot.</span><span class="sxs-lookup"><span data-stu-id="030b4-106">The **Remove-AzureRmSchedulerJob** cmdlet removes an Azure Scheduler job.</span></span>

## <span data-ttu-id="030b4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="030b4-107">EXAMPLES</span></span>

## <span data-ttu-id="030b4-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="030b4-108">PARAMETERS</span></span>

### <span data-ttu-id="030b4-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="030b4-109">-DefaultProfile</span></span>
<span data-ttu-id="030b4-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="030b4-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="030b4-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="030b4-111">-JobCollectionName</span></span>
<span data-ttu-id="030b4-112">Az eltávolítandó feladatot tartalmazó webhelycsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="030b4-112">Specifies the name of a job collection that contains the job to remove.</span></span>

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

### <span data-ttu-id="030b4-113">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="030b4-113">-JobName</span></span>
<span data-ttu-id="030b4-114">Itt adhatja meg az eltávolítandó feladat nevét.</span><span class="sxs-lookup"><span data-stu-id="030b4-114">Specifies the name of a job to remove.</span></span>

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

### <span data-ttu-id="030b4-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="030b4-115">-PassThru</span></span>
<span data-ttu-id="030b4-116">Jelzi, hogy ez a parancsmag a siker sikerének értékét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="030b4-116">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="030b4-117">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="030b4-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="030b4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="030b4-118">-ResourceGroupName</span></span>
<span data-ttu-id="030b4-119">Annak az erőforrásnak a csoportját adja meg, amelyből el szeretné távolítani a feladatot.</span><span class="sxs-lookup"><span data-stu-id="030b4-119">Specifies the resource group of the job to remove.</span></span>

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

### <span data-ttu-id="030b4-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="030b4-120">-Confirm</span></span>
<span data-ttu-id="030b4-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="030b4-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="030b4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="030b4-122">-WhatIf</span></span>
<span data-ttu-id="030b4-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="030b4-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="030b4-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="030b4-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="030b4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="030b4-125">CommonParameters</span></span>
<span data-ttu-id="030b4-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="030b4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="030b4-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="030b4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="030b4-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="030b4-128">INPUTS</span></span>

### <span data-ttu-id="030b4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="030b4-129">System.String</span></span>

## <span data-ttu-id="030b4-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="030b4-130">OUTPUTS</span></span>

### <span data-ttu-id="030b4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="030b4-131">System.String</span></span>

## <span data-ttu-id="030b4-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="030b4-132">NOTES</span></span>

## <span data-ttu-id="030b4-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="030b4-133">RELATED LINKS</span></span>

[<span data-ttu-id="030b4-134">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="030b4-134">Get-AzureRmSchedulerJob</span></span>](./Get-AzureRmSchedulerJob.md)


