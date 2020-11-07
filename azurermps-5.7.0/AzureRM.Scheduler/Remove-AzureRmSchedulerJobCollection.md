---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: F315B193-C17B-41A9-B61D-0A0212B6B643
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/remove-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: b4ff486bac10c79a544761c1946fd3e34dce69a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679256"
---
# <span data-ttu-id="c824b-101">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c824b-101">Remove-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="c824b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c824b-102">SYNOPSIS</span></span>
<span data-ttu-id="c824b-103">Begyűjtő eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c824b-103">Removes a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c824b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c824b-104">SYNTAX</span></span>

```
Remove-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c824b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c824b-105">DESCRIPTION</span></span>
<span data-ttu-id="c824b-106">A **Remove-AzureRmSchedulerJobCollection** parancsmag eltávolítja a beosztást az Azure schedulerben.</span><span class="sxs-lookup"><span data-stu-id="c824b-106">The **Remove-AzureRmSchedulerJobCollection** cmdlet removes a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="c824b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c824b-107">EXAMPLES</span></span>

## <span data-ttu-id="c824b-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c824b-108">PARAMETERS</span></span>

### <span data-ttu-id="c824b-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c824b-109">-DefaultProfile</span></span>
<span data-ttu-id="c824b-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c824b-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c824b-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="c824b-111">-JobCollectionName</span></span>
<span data-ttu-id="c824b-112">A begyűjtő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c824b-112">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="c824b-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c824b-113">-PassThru</span></span>
<span data-ttu-id="c824b-114">Jelzi, hogy ez a parancsmag a siker sikerének értékét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="c824b-114">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="c824b-115">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="c824b-115">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c824b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c824b-116">-ResourceGroupName</span></span>
<span data-ttu-id="c824b-117">A begyűjtő erőforrás csoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c824b-117">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="c824b-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c824b-118">-Confirm</span></span>
<span data-ttu-id="c824b-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c824b-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c824b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c824b-120">-WhatIf</span></span>
<span data-ttu-id="c824b-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c824b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c824b-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c824b-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c824b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c824b-123">CommonParameters</span></span>
<span data-ttu-id="c824b-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c824b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c824b-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c824b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c824b-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c824b-126">INPUTS</span></span>

### <span data-ttu-id="c824b-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="c824b-127">None</span></span>
<span data-ttu-id="c824b-128">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="c824b-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c824b-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c824b-129">OUTPUTS</span></span>

## <span data-ttu-id="c824b-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c824b-130">NOTES</span></span>

## <span data-ttu-id="c824b-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c824b-131">RELATED LINKS</span></span>

[<span data-ttu-id="c824b-132">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c824b-132">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="c824b-133">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c824b-133">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="c824b-134">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c824b-134">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="c824b-135">Új – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c824b-135">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="c824b-136">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c824b-136">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


