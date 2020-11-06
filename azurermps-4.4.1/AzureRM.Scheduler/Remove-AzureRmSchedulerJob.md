---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 774699A8-8916-4F2A-973E-97E5E487D42E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJob.md
ms.openlocfilehash: 582953886b8ea39e04dee122c85d70884dabcf11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496904"
---
# <span data-ttu-id="4ce1d-101">Remove-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="4ce1d-101">Remove-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="4ce1d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4ce1d-102">SYNOPSIS</span></span>
<span data-ttu-id="4ce1d-103">A Feladatütemező feladatát távolítja el.</span><span class="sxs-lookup"><span data-stu-id="4ce1d-103">Removes a Scheduler job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ce1d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4ce1d-104">SYNTAX</span></span>

```
Remove-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ce1d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4ce1d-105">DESCRIPTION</span></span>
<span data-ttu-id="4ce1d-106">A **Remove-AzureRmSchedulerJob** parancsmag eltávolítja az Azure Scheduler-feladatot.</span><span class="sxs-lookup"><span data-stu-id="4ce1d-106">The **Remove-AzureRmSchedulerJob** cmdlet removes an Azure Scheduler job.</span></span>

## <span data-ttu-id="4ce1d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4ce1d-107">EXAMPLES</span></span>

## <span data-ttu-id="4ce1d-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4ce1d-108">PARAMETERS</span></span>

### <span data-ttu-id="4ce1d-109">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="4ce1d-109">-JobCollectionName</span></span>
<span data-ttu-id="4ce1d-110">Az eltávolítandó feladatot tartalmazó webhelycsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ce1d-110">Specifies the name of a job collection that contains the job to remove.</span></span>

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

### <span data-ttu-id="4ce1d-111">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="4ce1d-111">-JobName</span></span>
<span data-ttu-id="4ce1d-112">Itt adhatja meg az eltávolítandó feladat nevét.</span><span class="sxs-lookup"><span data-stu-id="4ce1d-112">Specifies the name of a job to remove.</span></span>

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

### <span data-ttu-id="4ce1d-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ce1d-113">-PassThru</span></span>
<span data-ttu-id="4ce1d-114">Jelzi, hogy ez a parancsmag a siker sikerének értékét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="4ce1d-114">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="4ce1d-115">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="4ce1d-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4ce1d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ce1d-116">-ResourceGroupName</span></span>
<span data-ttu-id="4ce1d-117">Annak az erőforrásnak a csoportját adja meg, amelyből el szeretné távolítani a feladatot.</span><span class="sxs-lookup"><span data-stu-id="4ce1d-117">Specifies the resource group of the job to remove.</span></span>

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

### <span data-ttu-id="4ce1d-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4ce1d-118">-Confirm</span></span>
<span data-ttu-id="4ce1d-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4ce1d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ce1d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ce1d-120">-WhatIf</span></span>
<span data-ttu-id="4ce1d-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4ce1d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ce1d-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4ce1d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ce1d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ce1d-123">-DefaultProfile</span></span>
<span data-ttu-id="4ce1d-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4ce1d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ce1d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ce1d-125">CommonParameters</span></span>
<span data-ttu-id="4ce1d-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4ce1d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ce1d-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ce1d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ce1d-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ce1d-128">INPUTS</span></span>

## <span data-ttu-id="4ce1d-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ce1d-129">OUTPUTS</span></span>

## <span data-ttu-id="4ce1d-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4ce1d-130">NOTES</span></span>

## <span data-ttu-id="4ce1d-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ce1d-131">RELATED LINKS</span></span>

[<span data-ttu-id="4ce1d-132">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="4ce1d-132">Get-AzureRmSchedulerJob</span></span>](./Get-AzureRmSchedulerJob.md)


