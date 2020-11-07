---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: BA79EDC8-BE89-4836-92EF-748D6F518886
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/enable-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Enable-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Enable-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 832b7659da0b71d804ddc1a8f19703b85fc8500b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679707"
---
# <span data-ttu-id="7930c-101">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7930c-101">Enable-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="7930c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7930c-102">SYNOPSIS</span></span>
<span data-ttu-id="7930c-103">Begyűjtheti a beosztást.</span><span class="sxs-lookup"><span data-stu-id="7930c-103">Enables a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7930c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7930c-104">SYNTAX</span></span>

```
Enable-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7930c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7930c-105">DESCRIPTION</span></span>
<span data-ttu-id="7930c-106">Az **enable-AzureRmSchedulerJobCollection** parancsmag lehetővé teszi a begyűjtést az Azure schedulerben.</span><span class="sxs-lookup"><span data-stu-id="7930c-106">The **Enable-AzureRmSchedulerJobCollection** cmdlet enables a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="7930c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7930c-107">EXAMPLES</span></span>

## <span data-ttu-id="7930c-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7930c-108">PARAMETERS</span></span>

### <span data-ttu-id="7930c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7930c-109">-DefaultProfile</span></span>
<span data-ttu-id="7930c-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7930c-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7930c-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="7930c-111">-JobCollectionName</span></span>
<span data-ttu-id="7930c-112">A begyűjtő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7930c-112">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="7930c-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7930c-113">-PassThru</span></span>
<span data-ttu-id="7930c-114">Jelzi, hogy ez a parancsmag a siker sikerének értékét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="7930c-114">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="7930c-115">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="7930c-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7930c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7930c-116">-ResourceGroupName</span></span>
<span data-ttu-id="7930c-117">A begyűjtő erőforrás csoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7930c-117">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="7930c-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7930c-118">-Confirm</span></span>
<span data-ttu-id="7930c-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7930c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7930c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7930c-120">-WhatIf</span></span>
<span data-ttu-id="7930c-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7930c-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7930c-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7930c-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7930c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7930c-123">CommonParameters</span></span>
<span data-ttu-id="7930c-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7930c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7930c-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7930c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7930c-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7930c-126">INPUTS</span></span>

### <span data-ttu-id="7930c-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="7930c-127">None</span></span>
<span data-ttu-id="7930c-128">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="7930c-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7930c-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7930c-129">OUTPUTS</span></span>

## <span data-ttu-id="7930c-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7930c-130">NOTES</span></span>

## <span data-ttu-id="7930c-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7930c-131">RELATED LINKS</span></span>

[<span data-ttu-id="7930c-132">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7930c-132">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="7930c-133">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7930c-133">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="7930c-134">Új – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7930c-134">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="7930c-135">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7930c-135">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="7930c-136">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7930c-136">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


