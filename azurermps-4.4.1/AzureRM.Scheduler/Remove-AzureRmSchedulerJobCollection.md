---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F315B193-C17B-41A9-B61D-0A0212B6B643
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: b1caa041f92312d3d122e758a9e63bc7299887b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496903"
---
# <span data-ttu-id="dedb0-101">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="dedb0-101">Remove-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="dedb0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dedb0-102">SYNOPSIS</span></span>
<span data-ttu-id="dedb0-103">Begyűjtő eltávolítása</span><span class="sxs-lookup"><span data-stu-id="dedb0-103">Removes a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dedb0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dedb0-104">SYNTAX</span></span>

```
Remove-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dedb0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dedb0-105">DESCRIPTION</span></span>
<span data-ttu-id="dedb0-106">A **Remove-AzureRmSchedulerJobCollection** parancsmag eltávolítja a beosztást az Azure schedulerben.</span><span class="sxs-lookup"><span data-stu-id="dedb0-106">The **Remove-AzureRmSchedulerJobCollection** cmdlet removes a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="dedb0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dedb0-107">EXAMPLES</span></span>

## <span data-ttu-id="dedb0-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dedb0-108">PARAMETERS</span></span>

### <span data-ttu-id="dedb0-109">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="dedb0-109">-JobCollectionName</span></span>
<span data-ttu-id="dedb0-110">A begyűjtő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dedb0-110">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="dedb0-111">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dedb0-111">-PassThru</span></span>
<span data-ttu-id="dedb0-112">Jelzi, hogy ez a parancsmag a siker sikerének értékét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="dedb0-112">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="dedb0-113">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="dedb0-113">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dedb0-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dedb0-114">-ResourceGroupName</span></span>
<span data-ttu-id="dedb0-115">A begyűjtő erőforrás csoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="dedb0-115">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="dedb0-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dedb0-116">-Confirm</span></span>
<span data-ttu-id="dedb0-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dedb0-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dedb0-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dedb0-118">-WhatIf</span></span>
<span data-ttu-id="dedb0-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dedb0-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dedb0-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dedb0-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dedb0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dedb0-121">-DefaultProfile</span></span>
<span data-ttu-id="dedb0-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dedb0-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dedb0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dedb0-123">CommonParameters</span></span>
<span data-ttu-id="dedb0-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dedb0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dedb0-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dedb0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dedb0-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dedb0-126">INPUTS</span></span>

## <span data-ttu-id="dedb0-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dedb0-127">OUTPUTS</span></span>

## <span data-ttu-id="dedb0-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dedb0-128">NOTES</span></span>

## <span data-ttu-id="dedb0-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dedb0-129">RELATED LINKS</span></span>

[<span data-ttu-id="dedb0-130">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="dedb0-130">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="dedb0-131">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="dedb0-131">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="dedb0-132">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="dedb0-132">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="dedb0-133">Új – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="dedb0-133">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="dedb0-134">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="dedb0-134">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


